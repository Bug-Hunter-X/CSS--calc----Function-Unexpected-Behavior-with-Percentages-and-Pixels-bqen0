# CSS `calc()` Function Unexpected Behavior

This repository demonstrates an uncommon issue with the CSS `calc()` function when combining percentages and fixed pixel values. The issue occurs when calculating a width using `calc(50% - 10px)`, where the parent element's width is not explicitly defined or is smaller than 20px.

The `bug.css` file contains the problematic code. The `bugSolution.css` demonstrates ways to mitigate the issue.

## Problem

The `calc(50% - 10px)` expression might result in a negative value if the parent element's width is less than 20px.  Browsers typically handle this by setting the width to `0px`, causing unexpected visual results.

## Solution

Solutions involve setting a minimum width for the parent element or using alternative approaches to sizing the element.