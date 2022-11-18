# Anu2003
ISTA_Intern



QUESTION 3

//Reverse a number
#include<stdio.h>
int main(){
    int n , rev;
    printf("Enter a number: ");
    scanf("%d",&n);
    while(n!=0){
        rev = n%10;
        printf("%d",rev);
        n = n/10;
    }
return 0;
}
