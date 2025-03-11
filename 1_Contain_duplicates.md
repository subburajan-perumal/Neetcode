# 1. Contain Duplicates

- Time complexity: O(nlogn)
- space complexity: space complexity of sorting algorithm

```java
class Solution {
    public boolean hasDuplicate(int[] nums) {
        Arrays.sort(nums); 
        for(int i = 1;i<nums.length;i++) {
            if(nums[i] == nums[i-1]) {
                return true;
            }
        }
        return false;
    }
}

```
