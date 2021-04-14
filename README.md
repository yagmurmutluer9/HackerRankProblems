# HackerRankProblems

   
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

