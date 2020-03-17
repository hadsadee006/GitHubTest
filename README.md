/***************************************************
 * Author    : CS Developers
 * Author URI: https://www.comscidev.com
 * Facebook  : https://www.facebook.com/CSDevelopers
 ***************************************************/
  
#include<stdio.h>
 
int main()
{
    int arr_size = 10;
    int number[arr_size];
    int i, tmp;
     
    for(i=0; i<arr_size; i++)
    {
        printf(" Enter number %d : ", i+1);
        scanf("%d", &number[i]);
    }
     
    i = 0;
    do
    {
        if(i < arr_size-1 && number[i] > number[i+1])
        {
            tmp = number[i+1];
            number[i+1] = number[i];
            number[i] = tmp;
            i = 0;
        }
        else
        {
            i++;
        }
         
    }while(i < arr_size);
 
     
    printf("\n Ascending order : ");
    for(i=0; i<arr_size; i++)
    {
        printf(" %d", number[i]);   
    }
     
    return 0;   
}
