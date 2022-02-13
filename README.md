
#include <stdio.h>

int main(){
    int num1;
    int num2;
    int max;
    int min;
    int terms;
    int sum;//define all the variables
    printf("Please enter 2 numbers.\n");//Give the user instructions
    scanf("%d %d", &num1, &num2);//collect values
    while (num1>=0 && num2 >=0) //Check whether the input is positive
    {
        if (num1 > num2) {
            max = num1;
            min = num2;
        } else {
            max = num2;
            min = num1;
        }//assign corresponding value to maximum and minimum
        terms = max - min + 1;// Find how many terms there are from min to max
        sum = (min + max) * terms / 2;//Applying Gaussian quadrature formula
        printf("The result is %d.\n", sum);// show the user the result
        printf("Please enter 2 numbers.\n");//do a cycle
        scanf("%d %d", &num1, &num2);
    }// the end of the while circle. If the input is negative, nothing will be showed
}
