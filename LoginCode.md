# Login-module
Simple log-in module

package javaapplication1;
import java.util.Scanner;
import javaapplication1.Account;

public class JavaApplication1 {




    public static void main(String[] args) {
        
        
        
        String login = loginSet();
        String password = passwordSet();
        String firstName = firstNameSet();
        String familyName = familyNameSet();
        
        Account account1 = new Account(login,password, firstName,familyName);
         
        Scanner userInput = new Scanner(System.in);
        System.out.println("Log in:");
        System.out.print("Type you login: ");
        String typedLogin = userInput.next();
        System.out.print("Type you password: ");
        String typedPassword = userInput.next();

        if (stringCompare(typedLogin,account1.login) && stringCompare(typedPassword,account1.password))
        {
            System.out.println("You are now logged in as " + firstName + " " + familyName);        
        }
        else
        {
            System.out.println("Typed login or password does not match.");
        }
        
       };
    
    public static String loginSet()
    {
        Scanner userInput = new Scanner(System.in);
        System.out.print("Set your login: ");
        String login = userInput.next();
        return login;
    }
    
    public static String passwordSet()
    {
        Scanner userInput = new Scanner(System.in);
        System.out.print("Set your password: ");
        String password = userInput.next();
        return password;
    }
    
    public static String firstNameSet()
    {
        Scanner userInput = new Scanner(System.in);
        System.out.print("Type your name: ");
        String firstName = userInput.next();
        return firstName;
    }
    
    public static String familyNameSet()
    {
        Scanner userInput = new Scanner(System.in);
        System.out.print("Type your family name: ");
        String familyName = userInput.next();
        return familyName;
    }
    
    static public boolean stringCompare(String a,String b)
    {
       return a.equals(b);
    }
    
};
