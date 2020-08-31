# simple-chatty-bot
package Bot;

import java.util.Scanner;

public class SimpleBot {
    final static Scanner scanner = new Scanner(System.in);

    public static void main(String[] args) {
        botIntroduction("Zeem", "2020");
        userIntroduction();
        countBot();
        quiz();
        end();
    }
        static void botIntroduction(String botName, String botYear) {
            System.out.println("Hello! My name is " + botName + ".");
            System.out.println("I was created in " + botYear + ".");
            System.out.println("Please remind me your name.");
        }

        static void userIntroduction() {
            String userName = scanner.next(); // reads the user name

            System.out.println("What a great name you have, " + userName + "!");
            System.out.println("Let me guess your age.");
            System.out.println("Enter remainders of dividing your age by 3, 5 and 7");

            int remainder3 = scanner.nextInt(); // reads the remainder of the age divided by 3
            int remainder5 = scanner.nextInt(); // reads the remainder of the age divided by 5
            int remainder7 = scanner.nextInt(); // reads the remainder of the age divided by 7

            int age = (remainder3 * 70 + remainder5 * 21 + remainder7 * 15) % 105;

            System.out.println("Your age is " + age + "; that's a good time to start programming!");
            System.out.println("Now I will prove to you that I can count to any number you want.");
        }

        static void countBot() {
            int countingNumber = scanner.nextInt(); //reads the number that the bot want to count

            for (int i = 0; i <= countingNumber; i++) {
                System.out.println(i + "!");     // prints the number
            }
            //System.out.println("Completed, have a nice day!");
        }

        static void quiz() {
            System.out.println("Let's test your programming knowledge");
            System.out.println("Why do we use methods in Java?");
            System.out.println("1. To repeat a statement multiple times.");
            System.out.println("2. To decompose a program into several small subroutines.");
            System.out.println("3. To determine the execution time of a program.");
            System.out.println("4. To interrupt the execution of a program.");

            int answer = scanner.nextInt();

            if (answer == 2) {
                end();
            } else {
                System.out.println("Please, try again.");
                answer = scanner.nextInt();
            }
        }

        static void end() {
            System.out.println("Congratulations, have a nice day!");
        }

}
