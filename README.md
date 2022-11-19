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
 
 _________________________________________________________________________________________________________________________________________________________
 
 
 QUESTION 9
 
 //number of alphabets

#include<stdio.h>
#include<string.h>
void main(){
    int i,n,length;
    char string[50];
    n=0;
    printf("Enter the string: ");
    scanf("%s",string);
    length = strlen(string);
    for(i=0;i<length;i++){
        if((string[i]>='a' && string[i]<='z') || (string[i]>='A' && string[i]<='Z'))
            n = n+1;
        }
    printf("The length of the string is: %d",n);
    
}

__________________________________________________________________________________________________________________________________________________________

QUESTION 10

// Anagrams

#include <stdio.h>
#include <string.h>
void main(){
    int len1,len2,i,j,flag;
    char str1[50],str2[50];
    flag = 0;
    printf("Enter the string 1: ");
    scanf("%s",str1);
    printf("Enter the string 2: ");
    scanf("%s",str2);
    len1 = strlen(str1);
    len2 = strlen(str2);
    for(i=0;i<len1;i++){
        for(j=0;j<len2;j++){
            if(str1[i]==str2[j]){
               
                flag = 1;
                
            }
            
            
        }
    }
    if(flag==1){
        printf("They are anagrams");
    }
    else{
        printf("Not anagrams");
    }
}

__________________________________________________________________________________________________________________________________________________

QUESTION 11

// Reverse a string

#include<stdio.h>
#include<string.h>
void main(){
    int i,len;
    char str[50];
    printf("Enter the string: ");
    scanf("%s",str);
    len = strlen(str);
    for (i=len-1;i>=0;i--){
        printf("%c",str[i]);
    }
}

___________________________________________________________________________________________________________________________________________________________

QUESTION 12

// Second largest number

#include<stdio.h>
void main(){
    int i,max,arr[50],n,sec,diff;
    printf("Enter the value for n: ");
    scanf("%d",&n);
    for(i=0;i<n;i++){
        scanf("%d",&arr[i]);
    }
    max = arr[0];
    for(i=0;i<n;i++){
        if(max<arr[i]){
            max=arr[i];
        }
    }
    sec = arr[0];
    diff = 90;
    for(i=0;i<n;i++){
        if((max-sec)<=diff){
            diff=max-sec;
            sec=arr[i];
        }
    }
printf("Second largest number is:%d",sec);
}

_______________________________________________________________________________________________________________________________________________

QUESTION 13

________________________________________________________________________________________________________________________________________________

QUESTION 14

//Maximum money

#include<stdio.h>
void main(){
    int money=0;
    int amount,house,i;
    printf("Enter number of houses: ");
    scanf("%d",&house);
    printf("Enter the amount: ");
    scanf("%d",&amount);
    for(i=1;i<=house;i++){
        if(i%2!=0){
        money+=amount;}
    }
    printf("Total amount is: %d",money);
}
___________________________________________________________________________________________________________________________________________________________

QUESTION 15

//Range sum

#include<stdio.h>

void main(){
    int n,a,b,arr[50],arr1[50],j,flag,i;
    flag=0;
    printf("Enter the value for n: ");
    scanf("%d",&n);
    printf("Enter the value for a: ");
    scanf("%d",&a);
    printf("Enter the value for b: ");
    scanf("%d",&b);
    for(i=0;i<n;i++){
        scanf("%d",&arr[i]);
    }
    for(j=0;j<n;j++){
        arr1[j]=a;
        ++a;
        if(a==b){
            break;
        }
    }
    arr1[j+1]=b;
    for(i=0;i<n;i++){
        for(j=0;j<n;j++){
        if(arr[i]==arr1[j]){
            flag=1;
        }
    }
        
    }
    if(flag==1){
        printf("They are in range");
    }
    else{
        printf("Not in range");
    }
}

_______________________________________________________________________________________________________________________________________________________

QUESTION 16

//Fine for the car

#include<stdio.h>
void main(){
    int car[50],fine[50],n,date,i,j,finesum;
    finesum=0;
    printf("Enter the value for n: ");
    scanf("%d",&n);
    printf("Enter the value for date: ");
    scanf("%d",&date);
    for(i=0;i<n;i++){
        printf("Enter the car number: ");
        scanf("%d",&car[i]);
        printf("Enter the fine: ");
        scanf("%d",&fine[i]);
    }
    if(n%2==0){
        for (i=0;i<n;i++){
            if(car[i]%2!=0){
                finesum+=fine[i];
            }
        }
    }
    else{
        for (i=0;i<n;i++){
            if(car[i]%2==0){
                finesum+=fine[i];
            }
        }
        
    }
    printf("The total fine amount is:%d",finesum);
}

_____________________________________________________________________________________________________________________________________________________

QUESTION 17


//Sum of numbers using positions

#include<stdio.h>
void main(){
    int arr[50],n,i,j,seven,sodd;
    seven=sodd=0;
    printf("Enter the value for n: ");
    scanf("%d",&n);
    for(i=0;i<n;i++){
        printf("Enter the element: ");
        scanf("%d",&arr[i]);
    }
    for(i=0;i<n;i++){
        if(i%2==0){
            seven+=arr[i];
        }
        else{
            sodd+=arr[i];
        }
    }
    printf("%d\t",seven);
    printf("%d",sodd);
}

******************************************************************* END OF PROGRAMS ********************************************************************
