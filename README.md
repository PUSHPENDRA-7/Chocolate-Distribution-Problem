# Chocolate-Distribution-Problem
 public int findMinDiff(ArrayList<Integer> arr, int m) {
        // your code here
        if(arr.size() == 0){
            return 0;
        }
        Collections.sort(arr);
        int k = arr.size();
        int res = Integer.MAX_VALUE;
        for(int i=0; i<k-m+1; i++){
            int minElement = arr.get(i);
            int maxElement = arr.get(i+m-1);
            res = Math.min(res,maxElement - minElement);
        }
        return res;
    }
