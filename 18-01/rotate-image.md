# Rotate Matrix by 90 degree - Problem No 48
[Go to Question](https://leetcode.com/problems/rotate-image/)

### Approach :-
* First we will find transpose of that matrix by swaping row with columns.
* After that we will reverse all rows

### Code :-

```
void rotate(vector<vector<int>> &vect){

    for(int i=0;i<vect.size();i++){
        for(int j=i+1;j<vect.size();j++){
            swap(vect[i][j], vect[j][i]);
        }
    }

    for(int i=0;i<vect.size();i++){
        reverse(vect[i].begin(), vect[i].end());
    }
}
```
