class Solution {
public:
    vector<int> productExceptSelf(vector<int>& nums) {
    //first edition
        vector<int> ans(nums.size());
        vector<int> prefix(nums.size(),1);
        vector<int> suffix(nums.size(),1);

        // prefix
        for(int i =1; i<nums.size();i++){
            prefix[i] = nums[i-1]*prefix[i-1];
        
        }
    
        // suffix
        for(int j = nums.size()-2; j>=0; j-- ){
            suffix[j] =nums[j+1]*suffix[j+1];
        }

        for(int k =0; k<nums.size(); k++){
            ans[k] = prefix[k]*suffix[k];
        }
        return ans;
        
        //Sec edition

            vector<int> ans(nums.size(),1);

            for(int i =1; i< nums.size(); i++){
                ans[i] = nums[i-1]* ans[i-1];
            }
            int temp=1;

            for(int i = nums.size()-1; i>=0; i--){
                ans[i] *= temp;
                temp *= nums[i];
            }
           return ans;
        
        
    }
};
