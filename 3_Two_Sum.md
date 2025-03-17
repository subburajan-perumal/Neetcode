# 3. Two Sum

Time Complexity: O(n)
Space Complexity: O(n)

```java
class Solution {
    public int[] twoSum(int[] nums, int target) {
        HashMap<Integer, Integer> hmap = new HashMap<Integer, Integer>();
        for(int i = 0; i < nums.length;i++ ) {
            int difference = target - nums[i];  
            if (hmap.get(difference) != null) {
                int difference_index = hmap.get(difference);
                return new int[]{difference_index, i};
            }
            hmap.put(nums[i], i);
        }
        return new int[]{};
    }
}
```
