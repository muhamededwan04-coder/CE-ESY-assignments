#include <stdio.h>
#include <stdlib.h>
#define size 5

//تعريف وتهيئة المخزون الدائري
char array[size];
int front=0;
int rear=0;
int count=0;


//حالة الامتلاء
int isFull()
{
return (count==size);
}

//حالة الفراغ
int isEmpty()
{
    return(count==0);
}

//اضافة عنصر
void write_value(char value)
{

    if(isFull()){printf("OVERFLOW\n");return;}
    array[rear]=value;

    rear++;
    if(rear == size)rear=0;//الاعادة من البداية بحال امتلئ المخزون
    count++;

}

// حذف عنص ر وقرائته
char delete_value()
{
if(isEmpty()){printf("UNDERFLOW\n");return '\0' ;}
char value=array[front]; //يكون الحذف من البداية لكي نستفيد من المخزون الدائري
front++;
if(front==size)front=0;// الاعادة من البداية بحال قد تم حذف كل العناصر
count--;
return value;
}

//طباعة المخزون
void print()
{
 if(isEmpty()){printf("EMPTY\n");return;}
   int i=front;
   int c=0;
   while(c < count)
    {
    printf("%c ",array[i]);
    i++;
   if(i==size)i=0;//الاعادة من البداية بحال  كان هناك عناصر في بداية المصفوفة
    c++;
    }
   printf("\n");
}

int main()
{
char name[100];
scanf("%s",name);
//تخزين الاسم
int i=0;
while(name[i]!='\0')
{
    write_value(name[i]);
    i++;
}
//اضافة سلسلة نصية الى الاسم
char extra[] = " CE-ESY";

int j = 0;
while(extra[j] != '\0')
{
    write_value(extra[j]);
    j++;
}
//قراءة الاسم
printf("the name is: ");
while(!isEmpty())
    printf("%c",delete_value());
    printf("\n");

    //التاكد من انه فارغ
    print();
    return 0;

}
