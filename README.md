#include<stdio.h>
int Addition();
int Substracation();
int Multiplication();
int Division();
int Palindrom_Number();
int Sum_of_digit () ;
int Revers_the_digit ();
int  Print_the_table ();
int main()
{      
           printf("1) Addition  : \n");
           printf("2) Substracation  : \n");
           printf("3) Multiplication  : \n");
           printf("4) division  : \n");
           printf("5) Sum of digit  : \n");
           printf("6) Reverse the digit  : \n");
           printf("7) palindrom Number  : \n");
           printf("8) Print the table  : \n");

           int choice;
           printf("Choice Opration\n");

           scanf("%d",&choice);

           int addition;
           int substracation;
           int multiplication;
           int division;
           int Sum;
           int Reverse;
           int Parandom;
           int Print;
           int a,b;
          

           switch (choice)
           { 
                    case 1 :
                    addition = Addition();
                    printf("addition : %d", addition);
                    break;

                    case 2 : 
                    substracation =Substracation();
                    printf(" substracation : %d",  substracation);
                    break;

                    case 3 :
                    multiplication = Multiplication ();
                    printf("multiplication : %d",  multiplication);
                    break;

                    case 4 :
                    division = Division  ();
                    printf("division : %d",  division);
                    break;

                    case 5 :
                    Sum =  Sum_of_digit ();
                    printf("Sum of digit : %d", Sum);
                    break;

                    case 6 :
                    Revers_the_digit ();
                    break;

                    case 7 :
                    Palindrom_Number ();
                    break;

                    case 8 :
                    Print_the_table ();
                    break;
                   
           }
         
       
          return 0;
}

int Addition ()

{
         int a,b;
         printf(" Entre the value ; \n");
         scanf("%d%d",&a,&b);
          int res;

          res = a + b;
          return res;
}
int Substracation ()

{
         int a,b;
         printf(" Entre the value ; \n");
         scanf("%d%d",&a,&b);
          int res;

          res = a - b;
          return res;
}
int Multiplication ()

{         
          int a,b;
         printf(" Entre the value ; \n");
         scanf("%d%d",&a,&b);
          int res;

          res = a * b;
          return res;
}
int Division  ()

{        int a,b;
         printf(" Entre the value ; \n");
         scanf("%d%d",&a,&b);
         int res;

          res = a / b;
          return res;
}
int Sum_of_digit ()  //123

{
        int value;
        printf(" Entre the value : \n");
        scanf("%d",&value);
        int sum = 0;
        int rem;

        while (value!=0)
        {
            rem= value % 10;
            
            sum = sum + rem;

            value = value / 10;

        }

        return sum;
        
       
}
int Revers_the_digit ()  //123

{       int value;
        printf(" Entre the value : \n");
        scanf("%d",&value);
        int res;
       while (value!=0)
       {
          res = value % 10;

          printf("%d", res);

          value = value / 10;
       }

       return res;
       
}

 int Palindrom_Number ()
 {  
         int value;
        printf(" Entre the value : \n");
        scanf("%d",&value);
        int res;
        int revers=0;
        int raw = value;
       while (value!=0)
       {
          res = value % 10;
          revers  = revers*10 +res;
          value = value / 10;
          
       }
          printf("%d", revers);

       if (raw==revers)
       {
          printf(" It is palindrom Numner");
       }
       else {
          printf(" It is not palindrom");
       }

       return 0;

 }

 int  Print_the_table ()
 {
          int a;
          int i;
          printf(" Entre the value : \n");
          scanf("%d",&a);

          for ( i = 1; i<=10; i++)
          {
                    printf("%d\n", a*i);
          }
          return 0 ;
          
 }
