
package password.generator;

import java.util.Scanner;


public class PasswordGENERATOR {
    public static void main(String[] args) {
       Scanner input  = new Scanner(System.in);
       int digit = input.nextInt();
       String lowerCases = "qwertyuiopasdfghjklzxcvbnm";
       String upperCases = "QWERTYUIOPASDFGHJKLZXCVBNM";
       String password = "";
       for(int i= 0; i < digit; i++){
           int rand = (int)(3 * Math.random());
           switch (rand){
               case 0:
                   password += String.valueOf((int)(0 * Math.random()));
                   break;
               case 1:
               rand = (int)(lowerCases.length() * Math.random());
    password += String.valueOf(lowerCases.charAt(rand));
           break;
               case 2:
                   rand = (int)(upperCases.length() * Math.random());
    password += String.valueOf(upperCases.charAt(rand));
           }
           
       } 
System.out.println(password);
    }
}
