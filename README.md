# Uncommon HTML Bug: Incorrect Element Selection

This repository demonstrates a subtle bug where an incorrect selector in JavaScript prevents an element from being manipulated, even though the element is present in the HTML.  The bug is tricky because it doesn't cause a direct error message, but results in unexpected behavior.  The solution highlights a best practice in element selection.

## Bug Description

The `bug.html` file contains a simple HTML structure with a `<div>` element. The JavaScript code attempts to select this `div` using `document.querySelector('#myDiv')`. However, this selector will fail to find the element if there are any other issues present in the HTML, such as incorrect casing or typos in the element's ID. This leads to the `else` block executing, causing an error message to be logged to the console, and the styling changes to be skipped.

## Solution

The `bugSolution.html` file presents a corrected version.  It uses more robust methods to handle the case where the element is not found. A more comprehensive error message is displayed to the user.