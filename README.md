# Ruby Getter Method Assignment Bug

This example demonstrates an unexpected behavior in Ruby where assigning a value through the getter method doesn't modify the instance variable if a setter method isn't explicitly defined.

The file `bug.rb` contains the buggy code. The file `bugSolution.rb` shows how to fix it using proper setter methods.

## Bug Report
When trying to assign a new value using `my_object.value = 20`, the value of the instance variable `@value` remains unchanged because a setter method wasn't defined. This is a common error for developers coming from other languages where such direct modification is allowed.

## Solution
To correctly modify the instance variable through a method, use `attr_writer`, `attr_accessor`, or define the `value=` method explicitly.