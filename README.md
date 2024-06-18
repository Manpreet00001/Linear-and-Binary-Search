# Linear-and-Binary-Search

        int nums[] = {5,7,9,12,17};
        int target = 17;
        
        int result = linearSearch(nums, target);
        
        if(result!=-1){
            System.out.println("Element found at index"+result);
        else
            System.out.println("Element not found");
        }
      
        public static int linearSearch(int[] nums, int target){
            for(int i=0;i<nums.length;i++){
                if(nums[i] == target)
                return i;
            }
            return -1;
        }
        public static int binarySearch(int[] nums, int target, int left, int right){
        if(left<=right){
        int mid = (left+right)/2;
        if(nums [mid] == target)
        return mid;
        else if(nums[mid] < target)
        return binarySearch(nums,target,mid+1,right)
        else
        return binarySearch(nums,target,left,mid-1)
        }
