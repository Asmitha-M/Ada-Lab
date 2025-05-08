#include<stdio.h>
#define max_items 100
double computemaxvalue(double w, double weight[], double value[], double ratio[],int nitems)
{
 double cw=0;
 double cv=0;
 printf("\n Items considered are:");
 while(cw<w)
 {
  int item=getnextitem(weight,value,ratio,nitems);
  if(item==-1)
  {
   break;
  }
  printf("%d",item+1);
  if(cw+weight[item]<=w)
  {
   cw+=weight[item];
   cv+=value[item];
   ratio[item]=0;
  }
  else
  {
   cv+=(ratio[item]*(w-cw));
   cw+=(w-cw);
   break;
  }
 }
 return cv;
}

int getnextitem(double weight[],double value[], double ratio[],int nitems)
{
 double highest=0;
 int index=-1,i;
 for(i=0;i<nitems;i++)
 {
  if(ratio[i]>highest)
  {
   highest=ratio[i];
   index=i;
  }
 }
 return index;
}

int main()
{
 int nitems,i;
 double w;
 double weight[max_items];
 double value[max_items];
 double ratio[max_items];
 printf("Enter no. of items:");
 scanf("%d",&nitems);
 printf("Enter the weights of items:\n");
 for(i=0;i<nitems;i++)
 {
  scanf("%lf",&weight[i]);
 }
 printf("Enter the value of items:\n");
 for(i=0;i<nitems;i++)
 {
  scanf("%lf",&value[i]);
 }
 for(i=0;i<nitems;i++)
 {
  ratio[i]=value[i]/weight[i];
 }
 printf("Enter the knapsack capacity:");
 scanf("%lf",&w);
 printf("\n The maximum value in knapsack of capacity %.2f is: %2f\n",w,computemaxvalue(w,weight,value,ratio,nitems));
return 0;
}











