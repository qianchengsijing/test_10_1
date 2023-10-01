# test_10_1
#include <stdio.h>

//设"tag"判断队列是否空或满
#define MaxSize 50
typedef struct{
	int data[MaxSize];
	int top;
}SqStack;
#define MaxSize 50
typedef struct{
	int data[MaxSize];
	int front,rear;
	int tag;
}SqQueue;
int EnQueue(SqQueue Q,int x){
	if(Q.front == Q.rear && tag = 1)
		return 0;
	Q.data[Q.rear] = x;
	Q.rear = (Q.rear+1)%MaxSize;
	Q.tag = 1;
	return 1;
}
int DeQueue(SqQueue Q,int x){
	if(Q.front == Q.rear && tag = 0)
		return 0;
	x = Q.data[Q.front];
	Q.front = (Q.front+1)% MaxSize;
	return 1;
}
//一个队列和一个栈实现元素的逆置
int Inserver(SqStack S,SqQueue Q){
	while(!QueueEmpty(Q)){
		x = DeQueue(Q);
		Push(S,x);
	}
	while(!StackEmpty(S)){
		Pop(S,x);
		EnQueue(Q,x);
	}
}
//用两个栈实现一个队列的入队和出队
//入队
int EnQueue(SqStack &S1,SqStack &S2,ElemType x){
	if(!StackOverflow(S1)){
		Push(S1,x)
		return 1;
     }
	if(StackOverflow(S1) && !StackEmpty(S2)){
		printf("队列满");
		return 0;
	}
	if(StackOverflow(S1) && StackEmpty(S2)){
		Pop(S1,x);
		Push(S2,x);
	}
	Push(S1,x);
	return 1;
}
//出队
void DeQueue(SqStack &S1,SqStack &S2,ElemType x){
	if(!StackEmpty(S2)){
		Pop(S2,x);
	}
	else if(StackEmpty(S1)){
		printf("队列空");
	}
	else{
		while(!StackEmpty(S1)){
			Pop(S1,x);
			Push(S2,x);
		}
		Pop(S2,x);
	}
}
int QueueEmpty(SqStack S1,SqSatck S2){
	if(StackEmpty(S1) && StackEmpty(S2))
		return 1;
	else
		return 0;
}
void testQueue(){
	SqQueue Q;

}
