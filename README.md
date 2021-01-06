# Laboratory-Work-2-BSM

#include<stdio.h>
#include<math.h>

float root_fun(float a1, float b1,float c1){
    int n,s;
    float r;
    printf("n\tx\tf(x)\n");
    while (b1<=a1){
    printf("%d%10.2f%10.2f\n",n,b1,exp(-b1)-c1);
        b1+=0.1;n++;
        if (exp(-b1)-c1>0) // Checking for sign change
        s=1;
        if (exp(-b1)-c1>0 && exp(-b1)-c1<0.009){
        r=b1;
        return r;}}
    printf("%d%10.2f%10.2f\n",n,b1,exp(-b1)-c1);
        b1+=0.1;n++;
        if (s!=1)
        return a1+1;
        return r;
}
int main(){
    float a,b,c,root;
    printf("Function e^(-x) = c \n(Please note c must be greater than 0)Enter a value for c = ");
    scanf("%f",&c);
    if (c>0){
        printf("Enter the range (a,b) to calculate the root of e^(-x) = c\n(Please note a and b must have opposite signs in order for there to be a root)\n a = ");
        scanf("%f",&a);
        printf(" b = ");
        scanf("%f",&b);}
        else
        printf("Please check critera for c and try again\n");
        
        if(a*b>0)
        printf("Please check critera for range(a,b) and try again\n");
        
        if (a<0 && b>=0)
        root=root_fun(b,a,c);
        if (b<0 && a>=0)
        root=root_fun(a,b,c);
        if (root==0 && c!=1 )
        printf("ex^(x) = %10.1f at range(%10.1f,%10.1f)\nThere is no specific root for this range with 0.1 precision\n",c,a,b);
        else
        printf("Approximate root of ex^(x) = %10.1f at range(%10.1f,%10.1f) is - %10.2f\n",c,a,b,root);
        if (root==a+1 | root==b+1)
        printf("There is no root for function e^(-x) in given range\n");
 return 0;   
}
