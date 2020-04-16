# Insertion-sort-Java_interview_practice
Insertion is good for small elements only because it requires more time for sorting large number of elements.
package com.insertionSort;

/**
 *
 * @author Dinesh Nanda
 */

public class InsertionSort {
    
    public static void main(String[] args) {
        
        int arr[] = {5,8,1,3,9,6};
        
        int key, temp;
        
        for(int i = 1; i < arr.length; i++){
            
            key = arr[i];
            
            int j = i-1;
            
            while(j >= 0 && arr[j] > key){
                
                //swap
                temp = arr[j];
                arr[j] = arr[j+1];
                arr[j+1] = temp;
                
                j--;
            }
        }
        for(int i = 0; i < arr.length; i++){
            System.out.print(arr[i]+" ");
        }
    }
}
