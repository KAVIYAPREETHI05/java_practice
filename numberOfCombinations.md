```java
import java.util.Scanner;
public class noOfCombinations {
    static int numOfCom(int[] arr,int n){
        int[]c={0,0,0};

        for(int i=0;i<n;i++){
            ++c[arr[i]%3];
           
        }

        int pair_1_2=c[1]*c[2];
        int pair_00=c[0]*(c[0]-1)/2;
        int triplet_000=c[0]*(c[0]-1)*(c[0]-2)/6;
        int triplet_111=c[1]*(c[1]-1)*(c[1]-2)/6;
        int triplet_222=c[2]*(c[2]-1)*(c[2]-2)/6;
        int triplet_012=c[0]*c[1]*c[2];

        return pair_1_2+pair_00+triplet_000+triplet_111+triplet_222+triplet_012;

    }
    public static void main(String[] args){
     
        int[] arr1 = { 1, 5, 7, 2, 9, 14 }; 
    System.out.println("Result for arr1"+numOfCom(arr1, arr1.length));

    int arr2[] = { 3, 6, 9, 12 }; 
    System.out.print("Result for arr2"+numOfCom(arr2, arr2.length));



    }
    
}


```
