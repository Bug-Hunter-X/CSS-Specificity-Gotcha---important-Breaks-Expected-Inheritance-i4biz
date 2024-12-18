# CSS Specificity Gotcha: !important Breaks Expected Inheritance

This repository demonstrates a subtle CSS issue related to specificity and the `!important` flag.  When using `!important`, it can unexpectedly break expected inheritance behavior, leading to difficult-to-debug styling problems.

The `bug.css` file shows the problematic code, and `bugSolution.css` provides a solution.

## Problem

The main issue stems from how `!important` overrides inheritance based on selector specificity. Even if a parent element sets a style, a more specific child selector with `!important` will always win, often leading to unexpected visual results and inconsistencies.

## Solution

The solution involves carefully reconsidering the use of `!important`. In many cases, a better approach is to refactor the CSS rules to achieve the desired result without relying on `!important`.  Adjusting selector specificity or using more specific rules can solve the inheritance conflict without resorting to `!important` and improving maintainability.