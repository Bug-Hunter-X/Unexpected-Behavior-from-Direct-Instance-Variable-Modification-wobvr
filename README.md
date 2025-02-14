# Ruby Bug: Unexpected Behavior from Direct Instance Variable Modification

This repository demonstrates a common, yet subtle, bug in Ruby related to directly modifying instance variables using `instance_variable_set`.  While this might seem convenient at times, it circumvents the object's defined methods and can lead to unexpected behavior and maintainability problems.  Using accessors, even simple ones, promotes cleaner, more predictable code.

## Bug Description

The `bug.rb` file shows the misuse of `instance_variable_set` to modify an instance variable.  This technique skips any methods used for setting the variable, potentially neglecting input validation or other related logic.

## Solution

The `bugSolution.rb` file offers a corrected approach. Instead of direct manipulation, it uses an accessor method (`value=`) to update the instance variable, allowing for proper encapsulation and the ability to include input validation if needed.