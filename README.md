# permutation-call-stack-visualizer

This project is the demo project to help 
everyone to dynamically watch the call stack changing 
in the backtracking algorithm for permutation 

## Code/Algorithm used 
```
class Solution {
public:
    vector<vector<int>> permute(vector<int>& nums) {
        vector<vector<int>> res;
        getper(nums, 0, res);
        return res;
        
    }

    void getper(vector<int>& nums, int start,vector<vector<int>> &res ){
     
     if(start == nums.size()){
         res.push_back(nums);
         return;
     }

     for(int i=start; i<nums.size(); i++){
         swap(nums[i],nums[start]);
         getper(nums,start+1,res);
         swap(nums[start],nums[i]);
     }

    }
};
```
![image](https://github.com/sirparashar/permutation-call-stack-visualizer/assets/53056784/9d411a15-aea7-45a7-b630-10c811473d2a)

