#include<stdio.h>
int isprime(int x[])
{
	//int x[101]={0,};
	int i;
	int a;
	int c;
	int ret;
	for(i=0;i<101;i++){
		printf("请输入多项式:");
        scanf("%d %d",&a,&c);
		x[a]+=c;
		if(i==0) ret=a;
		if(a==0) break;	
	}
		return ret;
}
int main(){
	int i;
	int a;
	int b;
	int x[101]={0,};
	a=isprime(x);
	b=isprime(x);
	if(a<b){
		a=b;
	}
	for(i=a;i>1;i--){
		if(x[i]>0){
		printf("%dx%d+",x[i],i);
		}
	}if(x[1]>0) printf("%dx+",x[1]);
	 if(x[0]>=0) printf("%d",x[0]);
	
	
		
	return 0;
} 
