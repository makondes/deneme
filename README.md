#include <iostream>
#include<stdio.h>
#include<conio.h>
#include<stdlib.h>
#include<math.h>
int main(int argc, char** argv) {
int sayi,sa,i,a,s[255],b,c,f,j,d[255],e;
b=0;
a=1;
printf("decimal sayy gir");scanf("%d",&sayi);
sa=sayi; i=0;
while(1)  
{ f=fmod(sayi,2);
switch(f)
{case 1:s[i]=1;break;
case 0:s[i]=0;break;}//case
sayi=sayi/2; i++; a=i;
if (sayi==0 || sayi==1){
switch(sayi){
case 1:s[i]=1;break;
case 0:s[i]=0;break;
}//case
break;}//if
}//while
printf("decimal say=%d",sa);printf("\nbinary=\t");
for(i=a; i>=0;i--)
printf("%d",s[i]);	
d[0]=s[0];
j=1;
for(i=0; i<a;i++)
 {
 e=s[i]+s[i+1];
 if(e%2==0)
 d[j]=0;
 else
 d[j]=1;j++;
 }
 printf("\n gray kodlar=\t");
 for(j=a; j>=0;j--)
  printf("%d\n",d[j]);
  getch();
	return 0;
}
