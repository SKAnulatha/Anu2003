# Anu2003
ISTA_Intern


QUESTION 1

// Determining triangle

#include <stdio.h>
void main(){
    int s1,s2,s3;
    printf("Enter the value for all 3 sides in cms: ");
    scanf("%d %d %d",&s1,&s2,&s3);
    if((s1==s2)&&(s1==s3)&&(s2==s3)){
        printf("Eqilateral triangle");
    }
    else if((s1*s1)==((s2*s2)+(s3*s3)) || (s2*s2)==((s1*s1)+(s3*s3)) || (s3*s3)==((s2*s2)+(s1*s1))){
        printf("Isosceles triangle");
            }
    else{
        printf("Scalene triangle");
    
    }
    
}
_______________________________________________________________________________________________________________________

QUESTION 2

//Determining month and year and number of days

#include <stdio.h>
void main(){
    int year, month,y;
    printf("Enter year: ");
    scanf("%d",&year);
    printf("Enter month: ");
    scanf("%d",&month);
    if(year%4==0 && year%100==0 && year%400==0){
                y=1;
    }
            
    else{
        y=0;
    }

if(month%2==0){
    if (month == 2){
        if(y==1){
             printf("Number of days in the month is 29");
        }
        else{
             printf("Number of days in the month is 28");
        }
    }
    else{
         printf("Number of days in the month is 30");
    }

}
else{
     printf("Number of days in the month is 31");
}
}
______________________________________________________________________________________________________________________

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
___________________________________________________________________________________________________________________________

QUESTION 4

//GP series

#include<stdio.h>
void main(){
    int i,a,n,r;
    printf("Enter the value for a,r,n: ");
    scanf("%d %d %d",&a,&r,&n);
    for(i=1;i<n;i++){
        a=a*r;
       
    } 
    printf("%dth term of the GP is: %d",n,a);
}
_______________________________________________________________________________________________________________________

QUESTION 5

//Palindrome checking

#include<stdio.h>
#include<string.h>
void main(){
    char s[50];
    int s1,j,i,n,y;
    printf("Enter the string: ");
    scanf("%s",s);
    n=strlen(s);
    s1=n-1;
    for(j=0;j<n;j++){
        if(s[s1]==s[j]){
            y=1;
        }
        else{
            y=0;
            break;
        }
        s1-=1;
    }
    if(y==1){
        printf("Yes it is a palindrome");
    }
    else{
        printf("No it is not a palindrome");
    }
    
}
__________________________________________________________________________________________________________________________________________

QUESTION 6

//Armstrong number

#include<stdio.h>
void main(){
    int c,n,temp,sum;
    printf("Enter the number to be checked:");
    scanf("%d",&n);
    sum=0;
    temp = n;
    while(n>0){
        c=n%10;
        sum+=(c*c*c);
        n=n/10;
    }
    if(temp==sum){
        printf("Armstrong number!!");
    }
    else{
        printf("not an armstrong number");
    }
}

__________________________________________________________________________________________________________________________________________________

QUESTION 7


// Search a given element

#include<stdio.h>
void main(){
    int i,n,arr[50],x,index;
    printf("Enter the value for n:");
    scanf("%d",&n);
    printf("Enter the element to be found:");
    scanf("%d",&x);
    for(i=0;i<n;i++){
        arr[i]=i+1;
    }
    for(i=0;i<n;i++){
        if(arr[i]==x){
            index = i;
            break;
        }
        else{
            index=0;
        }
    }
    if(index!=0){
        printf("%d found at %d",n,index);
    }
    else{
        printf("not found");
    }
    
}
______________________________________________________________________________________________________________________________________________________


QUESTION 8

//Fibonacci series

#include<stdio.h>    
void printFibonacci(int n){    
    static int n1=0,n2=1,n3;    
    if(n>0){    
         n3 = n1 + n2;    
         n1 = n2;    
         n2 = n3;    
         printf("%d ",n3);    
         printFibonacci(n-1);    
    }    
}    
int main(){    
    int n;    
    printf("Enter the number of elements: ");    
    scanf("%d",&n);    
    printf("Fibonacci Series: ");    
    printf("%d %d ",0,1);    
    printFibonacci(n-2); 
  return 0;  
 }    
