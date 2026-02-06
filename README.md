# sum-of-special-series
#include<stdio.h>
int main(){
	int x,n,power=1,fact=1,k=1,sum=0;
	printf("enter the vaule of x");
	scanf("%d",&x);
	printf("enter number of terms");
	scanf("%d",&n);
	for(int i=1;i<=n;i++){
		for(int j=1;j<=power;j++){
			fact=fact*j;
		}
		for(int j=1;j<=power;j++){
			k=k*x;
		}
		if(i==1) sum=sum+k;
		else{
			if(i%2==0) sum=sum-(k/x);
			else sum=sum+(k/x);
		}
		if(i==1) power=2;
		else power=power+2;
	}
	printf("sum of series=%d",sum);
        return 0;
}
