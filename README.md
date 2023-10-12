# java3

package jobexams;

import java.util.Scanner;
public class PangramCheck {
    public static void main(String[] args) {
    	
    	Scanner scan=new Scanner(System.in);
    	System.out.println("Enter the value");
    	String input = scan.nextLine(); // Replace with user input

        boolean isPangram = isPangram(input.toLowerCase());
        
        if (isPangram) {
            System.out.println("The input is a pangram.");
        } else {
            System.out.println("The input is not a pangram.");
        }
    }

    public static boolean isPangram(String input) {
        for (char c = 'a'; c <= 'z'; c++) {
            if (input.indexOf(c) == -1) {
                return false;
            }
        }
        return true;
    }
}

