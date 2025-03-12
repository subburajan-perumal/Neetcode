# 2. Valid Anagram
Time complexity: O(n)
space complexity: O(1)
```java
class Solution {
    public boolean isAnagram(String s, String t) {
        if(s.length() != t.length()) return false;
        int[] characterCount = new int[26];
        for (int i = 0; i < s.length(); i++) {
            characterCount[s.charAt(i)-'a']++;
            characterCount[t.charAt(i)-'a']--;
        }
        for(int i=0;i < characterCount.length;i++) {
            if (characterCount[i] != 0) {
                return false;
            }
        }
        return true;
        
    }
}

```
