# StudentGradeCalculator
This is My First Git Repository

import java.util.Scanner;

public class StudentGradeCalculator {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        int numSub;
        System.out.print("Enter number of subjects: ");
        numSub = scanner.nextInt();
        
        double[] marks = new double[numSub];
        double total = 0;
        
        for (int i = 0; i < numSub; i++) {
        System.out.print("Enter marks for subject " + (i + 1) + ": ");
            marks[i] = scanner.nextDouble();
            total += marks[i];
        }
        
        double average = total / numSub;
        char grade;
        
        if (average >= 90) {
            grade = 'A';
        } else if (average >= 80) {
            grade = 'B';
        } else if (average >= 70) {
            grade = 'C';
        } else if (average >= 60) {
            grade = 'D';
        } else {
            grade = 'F';
        }
        
        System.out.println("\nTotal Marks: " + total);
        System.out.println("Average Percentage: " + average);
        System.out.println("Grade: " + grade);
        
        scanner.close();
}
}
