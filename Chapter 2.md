# Variables

## Case

Although it would be nice to use `format-with-hyphens` as that is the supperior way to deal with multiple words, the next best things are `cammelCase` and `CONSTANT_NAMES`.

## Scope

An important idea is the scope of the variable.

Variables used in a **large scope** of the program should have a **very descriptive** name.

Variables with a **small scope**, such as a lambda/anonymous functions, can have **less descriptive** names, for example naming an int in a for loop: `i`.

**Important**: This is not the case for function names.

## Order

When increasing in specificity, the words should be added to the end of the name.

If you were naming constants about car types and had a parent class of `Car`.

|       ❌        |       ✅        |
| :-------------: | :-------------: |
|  `ElectricCar`  |  `CarElectric`  |
| `CombustionCar` | `CarCombustion` |

As you read to the right, the words should be increasing in specificity.

Other than being very predictable, it allows for editors to take advantage of the suggestions feature.

## Imply Units

If you have an array of color names, you would call it `colorNames` rather than `colors` because the array type is `string`.
