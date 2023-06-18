# Weekly-contest-150
2739. Total Distance Traveled
java code ->
class Solution {
    public int distanceTraveled(int mainTank, int additionalTank) {
        int ans = 0;
        while(true){
             if(mainTank >=5){
                 mainTank -= 5;
                 int multiply = 5*10;
                 ans = ans+multiply;
                 if(additionalTank>0){
                         mainTank++;
                     additionalTank--;
                 }
                      
             }
             else break; 
        }
           int multiply = mainTank*10;
            return ans+multiply;
    }
}

2740. Find the Value of the Partition
 java code ->
class Solution {
    public int findValueOfPartition(int[] nums) {
        Arrays.sort(nums);
        int  ans = -1;
        int n = nums.length;
        for(int i=0; i<n-1; i++){
         int diff = nums[i+1] - nums[i];
            if(ans ==-1){
              ans = diff;
            }else{
               if(diff < ans)
                   ans = diff;
            }
        }
        return ans;
    }
}
