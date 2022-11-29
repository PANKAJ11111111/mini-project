# mini-project
#include<stdio.h>
void Dcalculater(int array[][3] , int m);
void summatrix(int array[][3], int n);
void submatrix(int array[][3], int p);
int  main() {
   
    // starting

    int array1[3][3];
    printf("----------------------------------\n");
 
 int i,j = 0;

    // storing value in array 
    printf("enter value for 1st matrix \n");
    printf("\n");

    for(i=0; i<=2; i++) {
        for(j=0; j<=2; j++) {
            printf("enter element at %d : %d = ",i,j);
            scanf("%d", &array1[i][j]);
        }
    }
printf("\n");
  // show matrix 

 printf("1st matrix  = \n");
     printf("| %d %d %d |\n", array1[0][0], array1[0][1], array1[0][2]);
     printf("| %d %d %d |\n", array1[1][0], array1[1][1], array1[1][2]);
     printf("| %d %d %d |\n", array1[2][0], array1[0][1], array1[2][2]);

printf("\n");

   // FUNCTION CALL 

    submatrix(array1, 3);
    
return 0;
}

// function for determinant calculation 


void Dcalculater(int array[][3], int m) {

int D;
    int A = array[0][0]*(array[1][1]*array[2][2]  - array[2][1]*array[1][2]);
    int B = array[0][1]*(array[2][2]*array[1][0]  - array[2][0]*array[1][2]);
    int C = array[0][2]*(array[2][1]*array[1][0]  - array[2][0]*array[1][1]);

    D = A - B + C; 

    printf("value of determinant is = %d ", D);
}


// function foe sum of two matrix 


void summatrix(int array[][3], int n) {
    int array2[3][3];
    int array3[3][3];

    printf("enter elment for 2nd matrix : \n");
    printf("\n");

int i ,j = 0 ;
for(i=0; i<=2 ; i++ ){
    for(j=0; j<=2; j++){
        printf("enter element at %d : %d =  ", i, j);
        scanf("%d", &array2[i][j]);
    }
}

 array3[0][0] = array[0][0]+array2[0][0];
 array3[0][1] = array[0][1]+array2[0][1];
array3[0][2] = array[0][2]+array2[0][2];
array3[1][0] = array[1][0]+array2[1][0];
array3[1][1] = array[1][1]+array2[1][1];
array3[1][2] = array[1][2]+array2[1][2];
array3[2][0] = array[2][0]+array2[2][0];
array3[2][1] = array[2][1]+array2[2][1];
array3[2][2] = array[2][2]+array2[2][2];

printf("\n");
// 2nd matrix
printf("seconde matrix is = \n");
       printf("|   %d  %d  %d  |\n", array2[0][0], array2[0][1], array2[0][2]);
       printf("|   %d  %d  %d  |\n", array2[1][0], array2[1][1], array2[1][2]);
       printf("|   %d  %d  %d  |\n", array2[2][0], array2[2][1], array2[2][2]);
printf("\n");
// finall matrix after sum 
printf("Finall Matrix is = \n");

       printf("|   %d  %d  %d  |\n", array3[0][0], array3[0][1], array3[0][2]);
       printf("|   %d  %d  %d  |\n", array3[1][0], array3[1][1], array3[1][2]);
       printf("|   %d  %d  %d  |\n", array3[2][0], array3[2][1], array3[2][2]);
       
       printf("\n");

  // call for determinant calculater 

       Dcalculater(array3, 3);

        printf("\n");

}
void submatrix(int array[][3], int p){
    int array4[3][3];
    int array5[3][3];
    int i ,j =0;
    for(i=0; i<=2; i++) {
        for(j=0; j<=2;j++) {
        printf("enter value at %d : %d =" ,i, j);
        scanf("%d", &array4[i][j]);
        }
}
array5[0][0] = array[0][0] - array4[0][0];
 array5[0][1] = array[0][1] - array4[0][1];
array5[0][2] = array[0][2] - array4[0][2];
array5[1][0] = array[1][0] - array4[1][0];
array5[1][1] = array[1][1] - array4[1][1];
array5[1][2] = array[1][2] - array4[1][2];
array5[2][0] = array[2][0] - array4[2][0];
array5[2][1] = array[2][1] - array4[2][1];
array5[2][2] = array[2][2] - array4[2][2];

printf("\n");
// 2nd matrix
printf("seconde matrix is = \n");
       printf("|   %d  %d  %d  |\n", array4[0][0], array4[0][1], array4[0][2]);
       printf("|   %d  %d  %d  |\n", array4[1][0], array4[1][1], array4[1][2]);
       printf("|   %d  %d  %d  |\n", array4[2][0], array4[2][1], array4[2][2]);
printf("\n");
// finall matrix after sum 
printf("Finall Matrix is = \n");

       printf("|   %d  %d  %d  |\n", array5[0][0], array5[0][1], array5[0][2]);
       printf("|   %d  %d  %d  |\n", array5[1][0], array5[1][1], array5[1][2]);
       printf("|   %d  %d  %d  |\n", array5[2][0], array5[2][1], array5[2][2]);
       
       printf("\n");

    Dcalculater(array5, 3);

        printf("\\\nnnn");

}
