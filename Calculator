/*
 * Click nbfs://nbhost/SystemFileSystem/Templates/Licenses/license-default.txt to change this license
 */

package virk.manpreet.airlinesystem;
 import java.util.Scanner;
/**
 *
 * @author sukhm
 */
public class AirlineSystem {
    private static boolean[] seats = new boolean[10];

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        while (true) {
            System.out.println("Enter 1 for First Class 2 for Economy");
            int section = input.nextInt();

            int seat = assignSeat(section);

            if (seat == -1) {
                
                System.out.println("Next flight leaves in 3 hours.");
                break;
            }

            printBoardingPass(section, seat);
        }
    }

    private static int assignSeat(int section) {
        int seat = -1;

        if (section == 1) {
            for (int i = 0; i < 5; i++) {
                if (!seats[i]) {
                    seats[i] = true;
                    seat = i;
                    break;
                }
            }
        } else if (section == 2) {
            for (int i = 5; i < 10; i++) {
                if (!seats[i]) {
                    seats[i] = true;
                    seat = i;
                    break;
                }
            }

            if (seat == -1) {
                System.out.println("Economy section is full. Would you like to be placed in First Class? (Type 1 for Yes or 2 for No)");
                Scanner input = new Scanner(System.in);
                int choice = input.nextInt();

                if (choice == 1) {
                    seat = assignSeat(1);
                }
            }
            
        }

        return seat;
    }

    private static void printBoardingPass(int section, int seat) {
        String sectionName = section == 1 ? "First Class" : "Economy";
        System.out.printf("Boarding Pass: Section %s, Seat %d\n", sectionName, seat + 1);
    }
}

    

