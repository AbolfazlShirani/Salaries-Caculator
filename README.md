import java.util.Scanner;
public class EmployeeSalary {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
    String[] names = new String[10];
    double[] salaries = new double[10];
    for (int i = 0; i < 10; i++) {
        System.out.print("Enter EmployeeName " + (i + 1) + " : ");
        names[i] = scanner.nextLine();
    }
    for (int i = 0; i < 10; i++) {
        System.out.print("Please enter the employee's salary " + (i + 1) + " : " );
        salaries[i] = scanner.nextDouble();
    }
    System.out.println("\n");
    System.out.println("\nEmployees with salaries above 5 million seven hundred :");
    System.out.println("Row\tName\tfinal Salaries");
    for (int i = 0; i < 10; i++) {
        if (salaries[i] > 5700000) {
            double insuranceDeduction = salaries[i] * 0.05;
            double allowanceAddition = salaries[i] * 0.07;
            double finalSalary = salaries[i] - insuranceDeduction + allowanceAddition;
            System.out.println((i + 1) + "\t" + names[i] + "\t" + finalSalary);
        }
    }
    scanner.close();
}
}
