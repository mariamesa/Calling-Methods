# Calling-Methods
//This is a simple program displaying how to call methods.

import java.util. Scanner;
public class CallingMethods {
    public static void main(String[] args) {
        //declare variables and scanner
        double faran=0;
        System.out.println("What is the degrees in Celsius today?");
        double celcius=readInTemp(0);
        System.out.println("The degrees in celsius is " + celcius);
        faran=convertToFaran(celcius, 0);
        System.out.println("The degrees in fahrenheit is " + faran);
        System.out.println(isHot(faran));

    }

    //create a method for reading in degrees in celcius
    public static double readInTemp(double celcius) {
        Scanner sc = new Scanner(System.in);
        celcius = sc.nextDouble();
        return celcius;


    }

    //convert from celcius to faranheit
   public static double convertToFaran (double celcius, double faran) {
       faran = (celcius * (9 / 5.0)) + 32;
       return faran;


   }
   //based on temperature, will return true or false for isHot
   public static boolean isHot (double faran) {
        if (faran>75) {
            return true;
        }
        else {
            return false;
        }


   }


}
