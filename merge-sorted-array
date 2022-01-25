#Merge Sorted Array - Problem No 88
https://leetcode.com/problems/merge-sorted-array/

* Create two variables and assign last index of arrays to both of it and also create another vaiable and assign it the last index of final array after merging.
* Now run the loop till both variable comes to first index and compare elements of both the array using these variables and find out the biiger value and put it to
  the last index of final array.
* Again run the loop for second array is any element left in second array then put that to last indices of final array.

#Code :-

void mergeArray( vector<int> &a, vector<int> &b, int m, int n){
    int i = m-1, j = n-1, k = m+n-1; 
    int t = k;
    while(i >= 0 && j >= 0){
        if(a[i] > b[j]){
            a[k] = a[i];
            i--;
        }
        else{
            a[k] = b[j];
            j--;
        }
        k--;
    }
    
    //Check this condition if any element left in array b
    while(j >= 0){
        a[k] = b[j];
        j--;
        k--;
        
    }
} 
