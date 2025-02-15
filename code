package cs3090block2;

import java.util.Scanner;
import java.util.regex.Matcher;
import java.util.regex.Pattern;

/**
 * Password strength checker based on typical criteria
 * @author Breanna Giang
 * @version February 15, 2025
 */
public class Blockproject2 {

    public static boolean isStrongPassword(String password) {
        // Length check
        if (password.length() < 8) {
            return false;
        }

        // Uppercase letter check
        Pattern uppercase = Pattern.compile("[A-Z]");
        Matcher matcher1 = uppercase.matcher(password);
        if (!matcher1.find()) {
            return false;
        }

        // Lower case letter check
        Pattern lowercase = Pattern.compile("[a-z]");
        Matcher matcher2 = lowercase.matcher(password);
        if (!matcher2.find()) {
            return false;
        }

        // Digit check
        Pattern digit = Pattern.compile("[0-9]");
        Matcher matcher3 = digit.matcher(password);
        if (!matcher3.find()) {
            return false;
        }

        // Special character check
        Pattern special = Pattern.compile("[^a-zA-Z0-9]");
        Matcher matcher4 = special.matcher(password);
        if (!matcher4.find()) {
            return false;
        }

        // If the password meets all of the above criteria, then it is a strong password.
        return true;
    }

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.print("Write your password: ");
        String password = input.nextLine(); 
        
        if (isStrongPassword(password)) {
            System.out.println(password + " is a strong password.");
        } else {
            System.out.println(password + " is not a strong password.");
        }
       input.close();
    }
}
