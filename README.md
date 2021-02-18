# MissingNumber
Find single missing number in an sub array starting from any index point within the array

import java.util.Arrays;   //import the arrays package

public class find_missing_number {
    
    //main function
    public static void main(String[] args) {
        int n = 6;                                        //the number of elements supposed to be there in an array or subarray 
        int[] arr = new int[]{1,2,3,5,6};                 //the number of elements present in the array or subarray    (one number is missing in the substring) 
        System.out.println(Arrays.toString(arr));         // displaying the array 
        System.out.println(findMissingNumber(arr, n));    //calling and displaying the missing number from the findMissingNumber function
    }

    //missing number function
    private static int findMissingNumber(int[] array, int len) {
        int expectedTotal = array[0],actualTotal = 0;         
        for (int k = 0,i = array[0] + 1; k < len-1; k++) {
            expectedTotal += i++;
            actualTotal += array[k];
        }
        return expectedTotal - actualTotal;
    }

}
