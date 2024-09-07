# ITIP
Lab 1

1. JavaHelloWorldProgram.java

public class JavaHelloWorldProgram {

    public static void main(String[] args) {

        System.out.println("Hello, word!");
    }
}

2. Primes. java
   
public class Primes {

    public static void main(String[] args) {

        // Перебираем числа от 2 до 100 включительно

        for (int i = 2; i < 100; i++) {

            if (isPrime(i)) {  // Проверяем, является ли число простым

                System.out.println(i); // Выводим простое число

            }

        }

    }

    // Метод для определения, является ли число простым

    public static boolean isPrime(int n) {

        // Проверяем делимость на числа от 2 до sqrt(n)

        for (int i = 2; i < n; i++) {

            if (n % i == 0) {

                return false; // Если n делится на i, то оно не простое

            }

        }

        return true; // Если делителей не найдено, то число простое

    }

}

3. Palindrome.java
   
public class Palindrome {

    public static void main(String[] args) {
        for (int i = 0; i < args.length; i++) {
            String s = args[i];
            if(isPalindrome(s)){
                System.out.println(s + " is a palindrome");
            } else {
                System.out.println(s + " is not a palindrome");
            }
        }
    }

    public static String reverseString(String s) {
        String reversed = "";
        for (int i = s.length() - 1; i >= 0; i--) {
            reversed += s.charAt(i);
        }
        return reversed;
    }

    public static boolean isPalindrome(String s) {
        String reversed = reverseString(s);
        return s.equals(reversed);
    }
}
