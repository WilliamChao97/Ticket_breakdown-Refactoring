# Refactoring

You've been asked to refactor the function `deterministicPartitionKey` in [`dpk.js`](dpk.js) to make it easier to read and understand without changing its functionality. For this task, you should:

1. Write unit tests to cover the existing functionality and ensure that your refactor doesn't break it. We typically use `jest`, but if you have another library you prefer, feel free to use it.
2. Refactor the function to be as "clean" and "readable" as possible. There are many valid ways to define those words - use your own personal definitions, but be prepared to defend them. Note that we do like to use the latest JS language features when applicable.
3. Write up a brief (~1 paragraph) explanation of why you made the choices you did and why specifically your version is more "readable" than the original.

You will be graded on the exhaustiveness and quality of your unit tests, the depth of your refactor, and the level of insight into your thought process provided by the written explanation.

## Your Explanation Here

### The changes that I made were:
1. Constant exports are now inside function
The original source code had constants such as TRIVIAL_PARTITION_KEY being exported outside the function. This may not be ideal if these constants are only used within the function itself. In the refactored code, these constants have been moved into the function ensuring better encapsulation.

2. Simplified If-Else Statements
The refactored code has simplified and removed unnecessary logic in if-else statements. By removing redundant brackets and using early returns where possible makes the code easier to read and understand.

3. Hash object created inside the function
The original code created a single global hash object which could potentially cause issues when reusing the hash object. To overcome this, the hash object is now created inside the function. Consequently, creating a new hash object each time the function is called ensures improved efficiency and avoids potential issues.

4. Changed Export Statement
Finally, the export statement was changed from the original module.exports syntax to the shorter version using exports. for consistency purposes.

All of these changes make for a cleaner and easily digestibl
