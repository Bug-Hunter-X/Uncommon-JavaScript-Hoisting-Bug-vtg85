# Uncommon JavaScript Hoisting Bug

This repository demonstrates a subtle bug related to JavaScript's hoisting mechanism.  The code attempts to log the value of a variable before it's declared, resulting in `undefined` being printed to the console. This behavior might be unexpected for developers unfamiliar with hoisting's intricacies.

## Bug Description

The bug lies in the `myFunc` function.  Because of hoisting, the `var a` declaration is moved to the top of its scope, but the *assignment* remains in its original place.  Attempting to access `a` before the assignment results in `undefined`.

## Solution

The solution involves ensuring the variable is declared and assigned *before* it is accessed. 