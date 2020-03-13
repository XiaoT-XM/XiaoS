#include<stdio.h>

int main()
{
	int year1,year2,i=0;//year1:出生年份;year2:查询年份;i:闰年个数 
	int month1,month2;//month1:出生月份;month2:查询月份;
	int day1,day2;//day1:出生日;day2:查询日。 
	int sum1,sum2,sum=0;//sum1:1月1日距离出生日期的天数,sum2:1月1日距离查询日期的天数,sum:出生日期到查询日期的总天数。 
	int dif1,dif2;//便于计算sum1,sum2;
	int y1,y2;//i:闰年的个数 
	int physical,emotion,intelligence;//physical:体力节律;emotion:情绪节律;intelligence:智力节律。 

	printf("请分别输入你的出生日期及查询日期，例如2000 1 2表示的日期为2000年1月2号:\n");
	scanf("%d %d %d %d %d %d",&year1,&month1,&day1,&year2,&month2,&day2);

	y1=year1;y2=year2; 
	for(y1;y1<=y2;y1=y1+1)//计算年份之间闰年的个数。 
	{
		if((y1%400==0)||(y1%4==0&&y1%100!=0))
		i=i+1;
	}

	if((year1%400==0)||(year1%4==0&&year1%100!=0))
	{ 
	if(month1==1)dif1=0; 
	else if(month1==2)dif1=1;
	else if(3<=month1<=7)dif1=(month1-2)/2;
	else if(month1==8)dif1=3;
	else if(9<=month1<=12)dif1=(month1-1)/2;
	}
	 else 
	 {
	if(month1==1)dif1=0;
	else if(month1==2)dif1=1;
	else if(3<=month1<=7)dif1=(month1-2)/2-1;
	else if(month1==8)dif1=2;
	else if(9<=month1<=12)dif1=(month1-1)/2-1;
	}

	sum1=30*(month1-1)+dif1+day1;

	if((year2%400==0)||(year2%4==0&&year2%100!=0))
	{ 
	if(month2==1)dif2=0; 
	else if(month2==2)dif2=1;
	else if(3<=month2<=7)dif2=(month2-2)/2;
	else if(month2==8)dif2=3;
	else if(9<=month2<=12)dif2=(month2-1)/2;
	}
	 else 
	 {
	if(month2==1)dif2=0;
	else if(month2==2)dif2=1;
	else if(3<=month2<=7)dif2=(month2-2)/2-1;
	else if(month2==8)dif2=2;
	else if(9<=month2<=12)dif1=(month2-1)/2-1;
	}

	sum2=30*(month2-1)+dif2+day2;

    sum=(year2-year1)*365+i-sum1+sum2;

    physical=sum%23;
    emotion=sum%28;
    intelligence=sum%33;

	if(physical==0)
		printf("体力节律刚好处于周期日\n");  
	else if(0<physical<12)
		printf("体力节律处于高潮期第%d天\n",physical);
	else if(physical==12)
		printf("体力节律刚好处于临街日\n");
	else
		printf("体力节律处于低潮期第%d天\n",physical);

	if(emotion==0)
		printf("情绪节律刚好处于周期日\n");  
	else if(0<emotion<14)
		printf("情绪节律处于高潮期第%d天\n",emotion);
	else if(emotion==14)
		printf("情绪节律刚好处于临街日\n");
	else
		printf("情绪节律处于低潮期第%d天\n",emotion);

	if(intelligence==0)
		printf("智力节律刚好处于周期日\n");  
	else if(0<intelligence<17)
		printf("智力节律处于高潮期第%d天\n",intelligence);
	else if(intelligence==17)
		printf("智力节律刚好处于临街日\n");
	else
		printf("智力节律处于低潮期第%d天\n",intelligence);
	
	return 0;
	
} 
