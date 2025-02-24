# Uncommon HTML Bug: Incorrect NodeList Handling

This repository demonstrates a common yet easily overlooked error in JavaScript when interacting with the NodeList returned by `document.querySelectorAll`. The bug arises from incorrectly treating a NodeList as a single element, rather than iterating over its items.

## Bug Description

The provided `bug.html` file includes JavaScript code that uses `document.querySelectorAll` to select all `div` elements.  The error occurs when it tries to access and modify the `style.display` property of the `divs` variable directly. Since `querySelectorAll` returns a NodeList and not a single DOM element, this results in a runtime error. 

## Bug Solution

The solution in `bugSolution.html` properly iterates over the NodeList returned by `querySelectorAll` and modifies the `style.display` property of each individual `div` element.  This ensures that all selected divs have their display property changed, resolving the error.