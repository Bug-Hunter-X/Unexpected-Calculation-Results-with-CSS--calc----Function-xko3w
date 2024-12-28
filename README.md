# Unexpected Calculation Results with CSS `calc()` Function

This repository demonstrates a subtle but potentially problematic error involving the CSS `calc()` function.  The issue arises from incorrectly adding a unit (such as `px`) to a percentage value within the `calc()` expression. This can lead to inconsistent rendering and unexpected results across different browsers.

## Bug Description

The primary problem is in using `calc(100% - 20px)`. Adding the `px` unit after `100%` is usually unnecessary and may not behave as expected.  The percentage should be treated as a percentage of the containing element's width or height and does not require extra unit specification.

## How to Reproduce

1. Clone this repository.
2. Open `bug.css` to see the incorrect CSS code.
3. Open `bugSolution.css` to see the corrected code.
4. Observe the difference in behavior when applied to an element in an HTML file.