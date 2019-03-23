# GreatestCommonDevisor

import java.util.Scanner;

public class P52_GreatestCommonDevisor {
    public static void main(String[] args){
        Scanner scanner = new Scanner(System.in);

        int a = Integer.parseInt(scanner.nextLine());
        int b = Integer.parseInt(scanner.nextLine());

        int div = -1;

        while (div != 0){
            if(a > b){
                div = a % b;
                a = b;
                b = div;
            }else if(b > a){
                div = b % a;
                b = a;
                a = div;
            }else {
                System.out.println(a);
                return;
            }
        }
        if(a > b){
            System.out.println(a);
        }else {
            System.out.println(b);
        }
    }
}
