# provided-is-calculating-the-area-of-a-rectangle

/*
 * Rectangle Area Calculator
 * This program reads the length and breadth of a rectangle from user input
 * and calculates the area.
 */

import java.io.*;

class Area {
    private int length;
    private int breadth;

    public Area(int length, int breadth) {
        this.length = length;
        this.breadth = breadth;
    }

    public int getArea() {
        return length * breadth;
    }
}

public class Final {

    public static void main(String[] args) {
        try {
            BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
            System.out.println("Enter the length :- ");
            int length = Integer.parseInt(br.readLine());
            System.out.println("Enter the breadth :- ");
            int breadth = Integer.parseInt(br.readLine());
            
            Area area = new Area(length, breadth);
            System.out.println("The Area of rectangle is " + area.getArea());
        } catch (IOException e) {
            System.err.println("Error reading input: " + e.getMessage());
        } catch (NumberFormatException e) {
            System.err.println("Invalid input. Please enter integers for length and breadth.");
        } catch (Exception e) {
            System.err.println("An unexpected error occurred: " + e.getMessage());
        }
    }
}
