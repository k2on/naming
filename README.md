# Naming

## Word Order

The order of words should increase in specificity.

**❌ Don't do**:

```js
let Car, // <- root class
    CombustionCar,
    FordCombustionCar,
    ElectricCar,
    TeslaElectricCar;
```

**✅ Do this**:

```js
let Car, // <- root class
    CarCombustion,
    CarCombustionFord,
    CarElectric,
    CarElectricTesla;
```

## Verbs

Verbs are used in function names. Verbs with `!` have [side effects](<https://en.wikipedia.org/wiki/Side_effect_(computer_science)>).

| Intent      | Verbs                    |
| ----------- | ------------------------ |
| **C**reate  | `make`, `build!`         |
| **R**ead    | `get`, `read!`           |
| Compute     | `is`                     |
| **U**pdate  | `set!`, `add!`, `write!` |
| **D**estroy | `remove!`                |

## Examples

### Make

|     | A function that parses a string into a custom type. |
| --- | --------------------------------------------------- |
| ❌  | `parseCustomType`                                   |
| ✅  | `makeCustomTypeFromString`                          |

### Compute

> NOTE: Compute functions should be pure. If there needs to be some side effect in a computation, it should happen outside of the function and passed as an argument.

|     | A method that validates some config. |
| --- | ------------------------------------ |
| ❌  | `validateConfig`                     |
| ❌  | `isValidConfig` Config > Valid       |
| ✅  | `isConfigValid`                      |

|     | If a file exists or not.                   |
| --- | ------------------------------------------ |
| ❌  | `fileExists`                               |
| ❌  | `doesFileExist` Does is not a Compute verb |
| ✅  | `isFileExist`                              |
