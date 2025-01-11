# Uncommon CSS `calc()` Errors in Flexbox Layout

This repository demonstrates a subtle bug related to the use of the `calc()` function in CSS within a flexbox context.  The problem stems from a misunderstanding of how `calc()` interacts with flexbox properties and the necessity of consistent unit usage.

The `bug.css` file contains the problematic code, while `bugSolution.css` shows the corrected version.

## Bug Description
The original code uses `calc(100% - 10px)` within a flexbox item to adjust its width. However, this calculation can fail to produce the expected result if the flex container's size isn't explicitly defined or is affected by other factors like `min-width` and `max-width`.  Furthermore, missing spaces or inconsistent units within the `calc()` expression can further complicate the issue. 

## How to Reproduce
Clone this repo and open `bug.html` in your browser. You'll observe unexpected spacing or dimensions.

## Solution
The solution involves ensuring that the flex container has a defined width, or by using a different approach to sizing the flex item that does not rely on `calc()` with percentage widths, if necessary. Consistent unit usage within `calc()` is also crucial. The corrected code is provided in `bugSolution.css`.