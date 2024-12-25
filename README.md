# Calculator-using-java
Simple Java Calculator: A basic program to perform addition, subtraction, multiplication, and division ,modules . Easy to understand and modify for beginners.

import java.util.Scanner;
public class calculator {

    Scanner obj = new Scanner(System.in);

    int num1,num2;

    public void getdata(){

        System.out.println("Enter the First number\n");
        num1 = obj.nextInt();

        System.out.println("Enter he Second number\n");
        num2 = obj.nextInt();
    }

    public void add(){
        System.out.println("The Addition of two numbers are:\n"+ (num1 + num2));
    }

    public void sub(){
        System.out.println("The Substration of two numbers are:\n"+ (num1 - num2));
    }

    public void multi(){
        System.out.println("The Multiplication of two numbers are:\n"+ (num1 * num2));
    }

    public void div(){
        System.out.println("The division of two numbers are:\n"+ (num1 / num2));
    }

    public void modul(){
        System.out.println("The modules of two numbers are:\n"+ (num1 % num2));
    }

    public static void main(String args[]){
        Scanner obj1 = new Scanner(System.in);
        int input,choice;
        calculator obj2 = new calculator();
        do{
            System.out.println("***********List of Operation***********\n");
            System.out.println("Press-1:To Enter the numbers\n");
            System.out.println("Press-2:For Addition the numbers\n");
            System.out.println("Press-3:For Substraction the numbers\n");
            System.out.println("Press-4:For Mutliplication the numbers\n");
            System.out.println("Press-5:For division the numbers\n");
            System.out.println("Press-6:For modules the numbers\n");
            System.out.println("Press-7:To exit from the application\n");

            System.out.println("Enter the input\n");
            input = obj1.nextInt();

            switch(input){

                case 1:
                    obj2.getdata();
                    break;
                case 2:
                    obj2.add();
                    break;
                case 3:
                    obj2.sub();
                    break;
                case 4:
                    obj2.multi();
                    break;
                case 5:
                    obj2.div();
                    break;
                case 6:
                    obj2.modul();
                    break;
                case 7:
                    System.out.println("Exit from the application\n");
                    System.exit(0);
                default:
                    System.out.println("*******INVAILD INPUT*******\n");
            }
            System.out.println("Do you want to perform another operation----1-yess/0-No\n");
            choice = obj1.nextInt();
        }while(choice == 1);
    }
}
