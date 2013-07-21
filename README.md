Search-in-Sorted-Array
======================


public class Solution {
    public int searchInsert(int[] A, int target) {
        // Start typing your Java solution below
        // DO NOT write main() function
           
        if(A[0] > target) return 0;
        if(A[A.length-1] < target) return A.length;
        
        return helper(A,target,0,A.length-1);
        
    }
    
    public int helper(int[] A, int target, int start, int end){
        
        
       
        
        //if(start>end) return start;
        //return -1;
        
      
        while(start <= end){
            int mid = (start+end)/2;
            
       
        
            if(A[mid] == target) return mid;
            
            if(target > A[mid]) start = mid +1;
            
            else end = mid-1;
        }
        
    return start;
        
    }
}
       
     
        

        
        
    
       
