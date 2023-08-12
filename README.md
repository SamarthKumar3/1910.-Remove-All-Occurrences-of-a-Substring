# 1910. Remove-All-Occurrences-of-a-Substring

## Intuition
A much shorter, direct and optimised approach

## Optimised Approach
- Get the positoiion of the substring to be found, using Find function.
- Use while loop to iterate through the string, until the find function returns a valid position.
- Accordingly remove the part of the string using Erase, passing in the position returned by Find.
- Update the pos variable to find new value of substring 

## Complexity
- Time complexity:
$$O(n)$$ 

- Space complexity:
$$O(1)$$

## Code
```
class Solution {
public:
    string removeOccurrences(string s, string part) {
        int pos= s.find(part);
        while(pos!=string::npos){
            s.erase(pos, part.length());
            pos=s.find(part);
        }
        return s;
    }
};
```
