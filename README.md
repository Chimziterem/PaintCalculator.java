import java.util.Scanner;
public class PaintCalculator {
    public static void main (String args[]) {
        int paint_square = 350;
        double length, width, height; 

        Scanner sc = new Scanner(System.in);
        System.out.println("Enter Length: ");
        length = sc.nextDouble();
        System.out.println("Enter width: ");
        width = sc.nextDouble();
        System.out.println("Enter height: ");
        height = sc.nextDouble();

        double area = computeArea(length, width, height);
        double price =  computeGallons(area);
        //System.out.println(area);
        //System.out.println(price);

        System.out.println("The price to paint the room is "+price);  
}

    public static double computeArea(double length, double width, double height) {
         double area = width * height;
        System.out.println("Wall of the are: "+area);
        return area;
    }
    public static double computeGallons(double area) {
        double gallons_need = area/100;
        System.out.println("You will need: "+gallons_need+" gallons");
        double  price =  gallons_need * 32;
        //System.out.println("Price: " +price);
        return price;
    }


}
