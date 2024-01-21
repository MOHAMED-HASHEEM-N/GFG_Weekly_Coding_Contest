## Friend of x

<details>
<summary>Java</summary>

```java

// Given an array arr of n integers, and 2 integers x and y.
// Return "yes", if any integer in arr is a friend of x, i.e if x adds upto any integer in arr to give else "no".
// More formally, if for any 0<=i<n, if x+arr[i]=y, then return "yes", else, return "no".


//{ Driver Code Starts
import java.io.*;
import java.util.*;


class IntArray
{
    public static int[] input(BufferedReader br, int n) throws IOException
    {
        String[] s = br.readLine().trim().split(" ");
        int[] a = new int[n];
        for(int i = 0; i < n; i++)
            a[i] = Integer.parseInt(s[i]);

        return a;
    }

    public static void print(int[] a)
    {
        for(int e : a)
            System.out.print(e + " ");
        System.out.println();
    }

    public static void print(ArrayList<Integer> a)
    {
        for(int e : a)
            System.out.print(e + " ");
        System.out.println();
    }
}

class GFG {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        int t;
        t = Integer.parseInt(br.readLine());
        while(t-- > 0){
            
            int n;
            n = Integer.parseInt(br.readLine());
            
            
            int x;
            x = Integer.parseInt(br.readLine());
            
            
            int y;
            y = Integer.parseInt(br.readLine());
            
            
            int[] arr = IntArray.input(br, n);
            
            Solution obj = new Solution();
            String res = obj.isFriend(n, x, y, arr);
            
            System.out.println(res);
            
        }
    }
}

// } Driver Code Ends



class Solution {
    public static String isFriend(int n, int x, int y, int[] arr) {
        for(int i=0;i<n;i++){
            if(x+arr[i]==y){
                return "yes";
            }
        }
        return "no";
    }
}
        


```

</details>
