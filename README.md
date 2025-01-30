# Unexpected NaN Result from Type Coercion

This repository demonstrates a common, yet subtle, bug in JavaScript related to type coercion. The function `foo` is intended to handle null values gracefully, but it fails to account for `undefined` values in the same manner.

## Bug Description
The `foo` function uses loose equality (`===`) to check if a value is `null`.  While this works for `null`, it doesn't handle the case where the input is `undefined`.  JavaScript's behavior with `undefined` in this context leads to unexpected `NaN` output.

## Solution
The provided solution explicitly checks for both `null` and `undefined` using strict equality, providing a more robust and predictable function behavior.