# C-Programs

## Any Type of C Programs ##

### C Program to Find ASCII Value of a Character ###

#include <stdio.h>
int main() {  
    char c;
    printf("Enter a character: ");
    scanf("%c", &c);  
    
    // %d displays the integer value of a character
    // %c displays the actual character
    printf("ASCII value of %c = %d", c, c);
    
    return 0;
}

### C Program to Multiply Two Floating-Point Numbers ###

#include <stdio.h>
int main() {
    double a, b, product;
    printf("Enter two numbers: ");
    scanf("%lf %lf", &a, &b);  
 
    // Calculating product
    product = a * b;

    // %.2lf displays number up to 2 decimal point
    printf("Product = %.2lf", product);
    
    return 0;
}


### C Program to Swap Two Numbers ###

    #include<stdio.h>
    int main() {
    double first, second, temp;
    printf("Enter first number: ");
    scanf("%lf", &first);
    printf("Enter second number: ");
    scanf("%lf", &second);

    // value of first is assigned to temp
    temp = first;

    // value of second is assigned to first
    first = second;

    // value of temp (initial value of first) is assigned to second
    second = temp;

    // %.2lf displays number up to 2 decimal points
    printf("\nAfter swapping, first number = %.2lf\n", first);
    printf("After swapping, second number = %.2lf", second);
    return 0;
    }

### C Program to Check Whether a Number is Even or Odd ###

#include <stdio.h>
int main() {
    int num;
    printf("Enter an integer: ");
    scanf("%d", &num);

    // true if num is perfectly divisible by 2
    if(num % 2 == 0)
        printf("%d is even.", num);
    else
        printf("%d is odd.", num);
    
    return 0;
}

### C Program to Check Whether a Number is Prime or not ###

    #include<stdio.h>  
    int main(){    
        int n,i,m=0,flag=0;    
        printf("Enter the number to check prime:");    
        scanf("%d",&n);    
        m=n/2;    
        for(i=2;i<=m;i++)    
        {    
            if(n%i==0)    
            {    
                printf("Number is not prime");    
                flag=1;    
                break;    
            }    
        }    
        if(flag==0)    
        printf("Number is prime");     
        return 0;  
    }    
 
 ### c program to check Armstrong Number in C ###
 
    #include<stdio.h>  
    int main()    
    {    
        int n,r,sum=0,temp;    
        printf("enter the number=");    
        scanf("%d",&n);    
        temp=n;    
        while(n>0)    
        {    
            r=n%10;    
            sum=sum+(r*r*r);    
            n=n/10;    
        }    
        if(temp==sum)    
            printf("armstrong  number ");    
        else    
            printf("not armstrong number");    
        return 0;  
    }   

### c program to check whether number is palindrome or not ###
 
    #include<stdio.h>  
    int main()    
    {    
        int n,r,sum=0,temp;    
        printf("enter the number=");    
        scanf("%d",&n);    
        temp=n;    
        while(n>0)    
        {    
            r=n%10;    
            sum=(sum*10)+r;    
            n=n/10;    
        }    
        if(temp==sum)    
            printf("palindrome number ");    
        else    
            printf("not palindrome");   
        return 0;  
    }

### c program for Strings and Pointers ###

    #include <stdio.h>
    int main(void) {
    char name[] = "Harry Potter";

    printf("%c", *name);     // Output: H
    printf("%c", *(name+1));   // Output: a
    printf("%c", *(name+7));   // Output: o

    char *namePtr;

    namePtr = name;
    printf("%c", *namePtr);     // Output: H
    printf("%c", *(namePtr+1));   // Output: a
    printf("%c", *(namePtr+7));   // Output: o
    }

### c program for fibonacci series without recursion.
    #include<stdio.h>    
    int main()    
    {    
        int n1=0,n2=1,n3,i,number;    
        printf("Enter the number of elements:");    
        scanf("%d",&number);    
        printf("\n%d %d",n1,n2);//printing 0 and 1    
        for(i=2;i<number;++i)
        {    
            n3=n1+n2;    
            printf(" %d",n3);    
            n1=n2;    
            n2=n3;    
        }  
        return 0;  
    }   

### c program for fibonacci series with recursion.

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

### c program for Sum of digits.
    #include<stdio.h>  
    int main()    
    {    
        int n,sum=0,m;    
        printf("Enter a number:");    
        scanf("%d",&n);    
        while(n>0)    
        {    
            m=n%10;    
            sum=sum+m;    
            n=n/10;    
        }    
        printf("Sum is=%d",sum);    
        return 0;  
    }   
### c program for reverse number.

    #include<stdio.h>  
    int main()    
    {    
    int n, reverse=0, rem;    
    printf("Enter a number: ");    
    scanf("%d", &n);    
    while(n!=0)    
    {    
        rem=n%10;    
        reverse=reverse*10+rem;    
        n/=10;    
    }    
    printf("Reversed Number: %d",reverse);    
    return 0;  
    }   

### C Program to print Number Triangle.
       1
      121
     12321
    1234321

    #include<stdio.h>    
    #include<stdlib.h>  
    int main(){  
        int i,j,k,l,n;    
        system("cls");  
        printf("enter the range=");    
        scanf("%d",&n);    
        
        for(i=1;i<=n;i++)    
        {    
            for(j=1;j<=n-i;j++)    
            {    
                 printf(" ");    
            }    
            for(k=1;k<=i;k++)    
            {    
                printf("%d",k);    
            }    
            for(l=i-1;l>=1;l--)    
            {    
                printf("%d",l);    
            }    
            printf("\n");    
        }    
        return 0;  
    }  
    
### C Program to print Alphabet Triangle.
        A
       ABA
      ABCBA
     ABCDCBA
    ABCDEDCBA

    #include<stdio.h>    
    #include<stdlib.h>  
    int main(){  
    int ch=65;    
        int i,j,k,m;    
    system("cls");  
        for(i=1;i<=5;i++)    
        {    
            for(j=5;j>=i;j--)    
                printf(" ");    
            for(k=1;k<=i;k++)    
                printf("%c",ch++);    
                ch--;    
            for(m=1;m<i;m++)    
                printf("%c",--ch);    
            printf("\n");    
            ch=65;    
        }    
    return 0;  
    }  
### C Program to print Prime Numbers Between Two Integers

    #include <stdio.h>
    int checkPrimeNumber(int n);
    int main() {
        int n1, n2, i, flag;
        printf("Enter two positive integers: ");
        scanf("%d %d", &n1, &n2);
        printf("Prime numbers between %d and %d are: ", n1, n2);
        for (i = n1 + 1; i < n2; ++i) {

            // flag will be equal to 1 if i is prime
            flag = checkPrimeNumber(i);

            if (flag == 1)
                printf("%d ", i);
        }
        return 0;
    }
 
    int checkPrimeNumber(int n) {
        int j, flag = 1;
        for (j = 2; j <= n / 2; ++j) {
            if (n % j == 0) {
                flag = 0;
                break;
            }
        }
        return flag;
    }
### C Program to calculate power using recursion
    #include <stdio.h>
    int power(int n1, int n2);
    int main() {
        int base, a, result;
        printf("Enter base number: ");
        scanf("%d", &base);
        printf("Enter power number(positive integer): ");
        scanf("%d", &a);
        result = power(base, a);
        printf("%d^%d = %d", base, a, result);
        return 0;
    }

    int power(int base, int a) {
        if (a != 0)
            return (base * power(base, a - 1));
        else
            return 1;
    }
### C Program to Concatenate two string
    #include <stdio.h>
    int main() {
      char s1[100] = "programming ", s2[] = "is awesome";
      int length, j;

      // store length of s1 in the length variable
      length = 0;
      while (s1[length] != '\0') {
        ++length;
      }

      // concatenate s2 to s1
      for (j = 0; s2[j] != '\0'; ++j, ++length) {
        s1[length] = s2[j];
      }

      // terminating the s1 string
      s1[length] = '\0';

      printf("After concatenation: ");
      puts(s1);

      return 0;
    }
### C Program to Find Largest Element in an Array
    #include <stdio.h>
    int main() {
      int n;
      double arr[100];
      printf("Enter the number of elements (1 to 100): ");
      scanf("%d", &n);

      for (int i = 0; i < n; ++i) {
        printf("Enter number%d: ", i + 1);
        scanf("%lf", &arr[i]);
      }

      // storing the largest number to arr[0]
      for (int i = 1; i < n; ++i) {
        if (arr[0] < arr[i]) {
          arr[0] = arr[i];
        }
      }

      printf("Largest element = %.2lf", arr[0]);

      return 0;
    }
