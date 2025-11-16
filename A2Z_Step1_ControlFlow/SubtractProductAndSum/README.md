# Subtract Product and Sum of Digits of an Integer
**Platform:** LeetCode 1281  
**Difficulty:** Easy  
**Topic:** Control Flow, Loops, Digits

## 🧠 Logic  
Take the input then to take the digits of input number use % and add the digit to the sum which is initalized with zero so all the digits get summed along with this take the products of the digits as well.Later use / to move to the next digit and until reahced the last digit of the number

## ⏱ Complexity  
Time: O(log N)  
Space: O(1)

## 💻 Java Code  
import java.util.Scanner;
public class subtractProductAndSum{
    public static void  main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int sum = 0;
        int product = 1;
        while(n>0){
            int digit = n%10;
            sum = sum + digit;
            product = product*digit;
            n = n/10;
        }
        return product - sum;
    }
}
