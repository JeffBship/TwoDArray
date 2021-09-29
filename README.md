//Jeff Blankenship
//CS-151
//2d loop iteration example

//this code creates a 2d array of ints and assigns
//random values to the elements

import java.util.Random;

public class TwoDArray{

  public static void main (String[] args){
    
    //Random object for generating random numbers
    Random random = new Random();
    
    int[][] intArray = new int[5][3];
    
    //indexA through outer layer
    for (int indexA=0; indexA<intArray.length; indexA++){
      //indexB through inner layer
      for (int indexB=0; indexB<intArray[indexA].length; indexB++){
        //assign random int 1-100 inclusive
        intArray[indexA][indexB] = random.nextInt(100) + 1;
      }      
    }
    
    //print the array using do loops
    int indexA = 0;
    do{//indexA through outer layer
      int indexB = 0;
      do {//indexB through inner layer
        System.out.printf("%5d",intArray[indexA][indexB]);
        indexB++;
      } while (indexB<intArray[indexA].length);
      //new line at the end of each row
      System.out.println();
      indexA++;
    } while (indexA<intArray.length);
  }
}
