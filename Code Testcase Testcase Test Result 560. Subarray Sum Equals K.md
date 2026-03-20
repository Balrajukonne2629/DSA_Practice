# Intuition
<!-- Describe your first thoughts on how to solve this problem. -->
It seems like here we use the previous values for getting the present value
# Approach
<!-- Describe your approach to solving the problem. -->
The approach was based on using the hashmap technique 
and the main logic was 
first we need to calculate the sum-> check the condition -> store it in the hashmap


# Complexity
- Time complexity:
<!-- Add your time complexity here, e.g. $$O(n)$$ -->

- Space complexity:
<!-- Add your space complexity here, e.g. $$O(n)$$ -->

# Code
```cpp []
class Solution {
public:
    int subarraySum(vector<int>& nums, int k) {
        unordered_map<int,int>mp;
        int sum=0,count=0;
        mp[0]=1;
        for(int i=0;i<nums.size();i++)
        {
            sum+=nums[i];
            
            if(mp.find(sum-k)!=mp.end())
            {
                
                count=count+mp[sum-k];
            }
            mp[sum]++;
        }
        return count;
        
    }
};
```
