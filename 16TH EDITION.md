/*CHAPTER-16/Q.[B]-K*/

/*C PROGRAM TO RECEIVE AN INTEGER NUMBER AS INPUT AND PRINTS OUT THE NUMBER IN WORDS.*/
#include<stdio.h>
#define FLAG !(arr2[i]==0 && arr2[i-1]==0)
void cycle();
void cout();
int count = -1;
int i = -1;
int arr2[10];
int main()
{
    int num;
    printf("Enter a number less than 10 digit in lenth\n");
    scanf_s("%d", &num);
    while (num != 0)
    {
        i++; count++;
        arr2[i] = num % 10;
        num = num / 10;
 
    }
    printf("\n\n");
    while (count>=0)
    {
        if (count == 8)
        {
            i = count;
            cycle();
            if (FLAG)
            printf(" Crore");
            count = count - 2;
 
        }
        if (count == 7)
        {
            i = count + 1;
            cout();
            printf(" Crore");
            count--;
 
        }
        if (count == 6)
        {
            i = count;
            cycle();
            if (FLAG)
            printf(" Lakh");
            count = count - 2;
 
        }
        if (count == 5)
        {
            i = count + 1;
            cout();
            printf(" Lakh");
            count--;
 
        }
        if (count == 4)
        {
            i = count;
            cycle();
            if (FLAG)
            printf(" Thousand");
            count = count - 2;
 
        }
        if (count == 3)
        {
            i = count + 1;
            cout();
            printf(" Thousand");
            count--;
 
        }
        if (count == 2)
        {
            i = count + 1;
            cout();
            if(arr2[i - 1] != 0)
            printf(" Hundred");
            count--;
 
        }
        if (count == 1)
        {
            i = count;
            cycle();
            printf("\n\n");
            break;
 
        }
        if (count == 0)
        {
            i = count+1;
            cout();
            printf("\n\n");
            break;
 
        }
 
 
    }
 
 
    return 0;
}
 
void cycle()
{
    if (arr2[i] == 1)
    {
        if (arr2[i - 1] == 0)
            printf(" Ten");
        if (arr2[i - 1] == 1)
            printf(" Eleven");
        if (arr2[i - 1] == 2)
            printf(" Twelve");
        if (arr2[i - 1] == 3)
            printf(" Thirteen");
        if (arr2[i - 1] == 4)
            printf(" Fourteen");
        if (arr2[i - 1] == 5)
            printf(" Fifteen");
        if (arr2[i - 1] == 6)
            printf(" Sixteen");
        if (arr2[i - 1] == 7)
            printf(" seventeen");
        if (arr2[i - 1] == 8)
            printf(" Eighteen");
        if (arr2[i - 1] == 9)
            printf(" Nineteen");
 
    }
    else if (arr2[i] == 2)
    {
        printf(" Twenty");
        cout();
    }
 
    else if (arr2[i] == 3)
    {
        printf(" Thirty");
        cout();
    }
    else if (arr2[i] == 4)
    {
        printf(" Forty");
        cout();
    }
    else if (arr2[i] == 5)
    {
        printf(" Fifty");
        cout();
    }
    else if (arr2[i] == 6)
    {
        printf(" Sixty");
        cout();
    }
    else if (arr2[i] == 7)
    {
        printf(" Seventy");
        cout();
    }
    else if (arr2[i] == 8)
    {
        printf(" Eighty");
        cout();
    }
    else if (arr2[i] == 9)
    {
        printf(" Ninety");
        cout();
    }
    else if(arr2[i] == 0)
    {
        cout();
    }
}
void cout()
{
    if (arr2[i - 1] == 1)
        printf(" One");
    else if (arr2[i - 1] == 2)
        printf(" Two");
    else if (arr2[i - 1] == 3)
        printf(" Three");
    else if (arr2[i - 1] == 4)
        printf(" Four");
    else if (arr2[i - 1] == 5)
        printf(" Five");
    else if (arr2[i - 1] == 6)
        printf(" Six");
    else if (arr2[i - 1] == 7)
        printf(" Seven");
    else if (arr2[i - 1] == 8)
        printf(" Eight");
    else if (arr2[i - 1] == 9)
        printf(" Nine");
    
 
}
