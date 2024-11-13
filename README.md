Printing Inverted Hollow Pyramid Star Pattern:
Today we will be learning, how to code a Java Program for printing inverted hollow pyramid star pattern. An inverted hollow pyramid star pattern has star only on its boundaries and the rest space is filled by blank spaces.
Go through the page, you can find the code below, along with the algorithm

Java Program for Inverted Hollow Pyramid Star Pattern
Algorithm:
Take the number of rows as input from the user and store it in any variable.(‘row‘ in this case).
Run a loop ‘row’ number of times to iterate through each of the rows. From i=row to i>0. The loop should be structured as for(int i=row;i>0;i–)
 Run a nested loop inside the main loop to print the spaces before the pyramid. From j=1 to j<=row-i. The loop should be structured as for(int j=1;j<=row-i;j++)
Inside this nested loop print white space System.out.print(” “); 
Run another nested loop inside the main loop after the previous loop to print the stars in each column of a row. From j=1 to j<i*2-1. The loop should be structured as for(int j=1;j<=row-i;j++)
Print star under the if condition (i==1 or i==row).
Under the else condition  use another if condition to print the rest of the stars.
Use if(j==1 || j==i*2-1) to print stars.
Else print white space System.out.print(” “);
In the main loop print a new line to move to the next line System.out.println();
Code in Java:
import java.util.Scanner;
public class Pattern1 {

	public static void main(String[] args) {
		Scanner sc=new Scanner(System.in);
		System.out.println("Enter Number : ");
		int row=sc.nextInt(); 
		for(int i=row;i>0;i--)
		{
		 for(int j=1;j<=row-i;j++)
		  System.out.print(" ");
		 if(i==1 || i==row)
		 for(int j=1;j<=i*2-1;j++)
		  System.out.print("*");
		else
		 for(int j=1;j<=i*2-1;j++)
		if(j==1 || j==i*2-1)
		  System.out.print("*");
		else
		  System.out.print(" ");
		System.out.println();
     }
  }
}
