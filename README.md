package javaapplication18;

import java.util.Arrays;
import java.util.Scanner;

/**
 *
 * @author LENOVO
 */
public class JavaApplication18 {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
      
         Scanner sc = new Scanner(System.in);
         
        int y;
        System.out.println("Input size of array: ");
        int kol=sc.nextInt();
       int[]array=new int[kol];
       
        System.out.println("Input elements of array: ");
       for(int i=0; i<kol; i++)
           array[i]=sc.nextInt();
    
       int min=array[0];
       int max=array[0];
       int imin=0;
       int imax=0;
       
         for(int i=0; i<kol; i++){
             if (min>array[i]){
                 
             imin=i;
             min=array[i];}
    
             if (max<array[i]){
             max=array[i];
             imax=i;}
    }
          System.out.println("min - "+min);
          System.out.println("max - "+max);
    
        y=array[imin];
        array[imin]=array[imax];
        array[imax]=y;
    
    for(int i=0; i<kol; i++)
            System.out.print(array[i]+" ");
}
}
