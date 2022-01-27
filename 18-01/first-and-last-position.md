## Find First & Last Position of Given Number in a Sorted Array - Problem No 34
[Go to Question](https://leetcode.com/problems/find-first-and-last-position-of-element-in-sorted-array/)

---

### Approach :-
* We will use Binary Search for this problem (Sorted Array -> Binary Search).
* We will create two function one will give us first position and another will give us last position of the given number.
* Every thing will be same on both function the only change will be that we will change high to find first occurence and low to find last occurence.

### Code :-

```
//Find first occurrence using binary search
int firstOccur(vector<int> arr, int ele){
    int low = 0, high = arr.size()- 1;
    int mid, res = -1;
    
    while(low <= high){

        mid = low + ((high - low)/2);

        if(arr[mid] < ele){
            low = mid + 1;
        }
        else if(arr[mid] > ele){
            high = mid - 1;
        }
        else{
            res = mid;
            high = mid - 1;

        }
    }
    return res;

}

//Find last occurrence using binary search
int lastOccur(vector<int> arr, int ele){
    int low = 0, high = arr.size() - 1;
    int mid, res = -1;

    while(low <= high){

        mid = low + ((high - low)/2);
        
        if(arr[mid] < ele){
            low = mid + 1;
        }
        else if(arr[mid] > ele){
            high = mid - 1;
        }
        else{
            res = mid;
            low = mid + 1;

        }
    }
    return res;

}
```
