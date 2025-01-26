# Uncommon HTML Bug: innerHTML and innerText Inconsistency
This repository demonstrates an uncommon bug related to the interaction between `innerHTML` and `innerText` in HTML when modifying the content of a div element.  Certain browsers handle the sequence of clearing content with `innerHTML` and then setting new content with `innerText` inconsistently, leading to unexpected behavior.
The `bug.html` file contains the buggy code, while `bugSolution.html` provides a corrected approach that ensures consistent behavior across browsers.
## Problem
The primary issue stems from the order of operations. Clearing the div's content with `innerHTML = ""`, and then setting the new content using `innerText` does not always guarantee the expected result in all browsers.  The new content may fail to appear, or might appear only partially. 
## Solution
The solution involves using only `innerHTML` to manage the content update. This approach avoids the inconsistencies associated with the combined use of `innerHTML` and `innerText` for sequential content manipulation. 