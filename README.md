# PrimeNumber in JAVA Language
#JAVA
Checking if a number is a prime number or not and printing all the prime numbers from 2 to the number.

        import java.util.Scanner;

    public class PrimeNumbers {
         private static String isPrime(int num){
             String prime = "Yes, this is a prime number";
             for (int div = 2; div < num; div++){
                 if (num % div == 0){
                prime = "Not a prime number";
            }
        }
        return prime;
    }
    private static int printPrimeNumbers(int num){
        for (int i = 2; i < num; i++){
            boolean isPrime = true;
            for(int div = 2; div < i; div++){
                if (i % div == 0) {
                    isPrime = false;
                    break;
                }
            }
            if (isPrime){
                System.out.println(i);
            }
        }
        return num;
    }

    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        System.out.println("Enter a number: ");
        int num = scan.nextInt();
        System.out.println(isPrime(num));
        printPrimeNumbers(num);

    }
}
