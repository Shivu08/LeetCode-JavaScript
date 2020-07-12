## Two Sum

### Question

Given an array of integers, return indices of the two numbers such that they add up to a specific target.

You may assume that each input would have exactly one solution, and you may not use the same element twice.

#### Example:
```shell
Given nums = [2, 7, 11, 15], target = 9,

Because nums[0] + nums[1] = 2 + 7 = 9,
return [0, 1].
```

### Solution
```javascript
/**
 * @param {number[]} nums
 * @param {number} target
 * @return {number[]}
 */

var twoSum = function(nums, target) {
    var answer = [];
    var existObj = {};
    for (var i = 0; i < nums.length; i++){
        if (typeof(existObj[target - nums[i]]) !== "undefined"){
            return [existObj[target - nums[i]], i];
        }
        existObj[nums[i]] = i;
    }
}
```