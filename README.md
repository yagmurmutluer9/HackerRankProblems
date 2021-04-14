# HackerRankProblems

## Problem List:
### 2D Array DS 
### Repeated String

## 2D Array DS Problem

```
 static int hourglassSum(int[][] arr) {
        
        int [][] first_arr = new int [4][4];
        int [][] first_result = arrFunc(arr, first_arr);
        int maxNum = findMax(first_result);
        return maxNum;

    }
    
    static int[][] arrFunc(int [][] arr, int[][] custom_arr) {
        
        int count = 0;
            for (int row = 0; row < arr.length ; row++) {
            
            for(int column = 0; column < arr[row].length ; column++) {
                
                if ((row + 2) < arr[row].length && (column + 2) < arr[column].length) {
                    
                count += arr[row][column] + arr[row][column+1] + arr[row][column+2]  
                                     + arr[row+1][column+1] + 
                        arr[row+2][column] + arr[row+2][column+1] + arr[row+2][column+2];
                
                custom_arr[row][column] = count;
                }
            count = 0;

            }
        }
        
        return custom_arr;
        
    }
    
    static int findMax(int [][] arr) {
        
        int maxNum = Integer.MIN_VALUE;
        
        for (int i = 0; i < arr.length ; i++) {
            for(int j = 0; j < arr[i].length ; j++) {
                if(arr[i][j] > maxNum) {
                    maxNum = arr[i][j];
                }
            }
        }
        return maxNum;
    }
    
   ```
   
   
 ## Repeated String
 
 ```
    static long repeatedString(String s, long n) {
        
        long count = s.chars().filter(ch -> ch == 'a').count();
        long a_count = (n / s.length()) * count;
        long rem = ( n % s.length());
        
        for (int i = 0; i < rem ; i++) {
            
            if(s.charAt(i) == 'a') {
                a_count++;
            }
        }
    
    return a_count;

    }
 ```
