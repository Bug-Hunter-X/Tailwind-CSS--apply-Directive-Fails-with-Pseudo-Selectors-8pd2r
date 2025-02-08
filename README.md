# Tailwind CSS @apply Directive Issue with Pseudo-Selectors

This repository demonstrates a bug where Tailwind CSS's `@apply` directive doesn't correctly handle pseudo-selectors like `:hover`, `:focus`, etc.  The expected behavior is for the styles to apply based on the user interaction, but the actual result is no style change.

## Bug Description
The `@apply` directive, when used with a class containing a pseudo-selector, fails to apply the corresponding styles. This leads to a broken user experience, as the intended visual feedback is missing.

## Steps to Reproduce
1. Clone this repository.
2. Open `bug.html` in your browser.
3. Observe that the button does not change its background color on hover, even though it should based on the applied class.

## Solution
The recommended solution is to avoid using `@apply` with classes containing pseudo-selectors. Use regular class names instead, as shown in `bugSolution.html`.