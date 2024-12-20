# Incorrectly Modifying innerHTML or textContent in HTML
This repository demonstrates an uncommon bug in HTML related to incorrectly modifying the `textContent` or `innerHTML` properties of an element.  Directly replacing `textContent` can lead to data loss, while manipulating `innerHTML` requires careful attention to avoid unintended consequences.  The solution shows best practices for safely managing content.

## Bug Description
The bug showcases the issue of accidentally overwriting or losing data when modifying an HTML element's content. Specifically, replacing `textContent` replaces the entire content, while `innerHTML` can lead to issues if not handled correctly (e.g. injecting un-sanitized user input). 

## How to reproduce
1. Clone this repository.
2. Open `bug.html` in a web browser. Observe the initial content and then the console output.
3. Compare with the correct method in `bugSolution.html` which demonstrates safe content manipulation

## Solution
The `bugSolution.html` file provides the correct approach to managing element content. This involves storing the original content and using it if necessary.