# 5A STACK ADT

## PROGRAM STATEMENT:
Write a CPP Program to insert five double elements in to Stack ADT (use STL for Stack)

## ALGORITHM:
1. Push five fixed double values into the stack using push().
2. Push five doubles from an array into the stack using a loop.
3. Read five user-input doubles and push each into the stack.
4. Push five doubles from a vector into the stack using iteration.
5. Generate five random doubles and push them into the stack.

## PROGRAM:
```
#include<iostream>
#include<stack>
using namespace std;
int main(){
   stack<double> stk;
   int i,n;
   float x;
   cin>>n; 
   for(i=0;i<n;i++)
    {
     cin>>x;    
     stk.push(x);
    }
   cout << "Size of the stack: " << stk.size() << endl;
   while(! stk.empty() )
   {
     cout << stk.top() << " ";
     stk.pop();
   } 
}
```

## OUTPUT:
![Screenshot 2025-05-02 154111](https://github.com/user-attachments/assets/e997c460-d124-4680-90ce-4f3c1141cb3d)

## RESULT:
Thus,the CPP Program to insert five double elements in to Stack ADT (use STL for Stack) has been successfully created.


# 5B STACK APPLICATIONS

## PROGRAM STATEMENT:
Write a CPP program for Postfix to Prefix Conversion using Stack STL

## ALGORITHM:
1. Define a function priority to assign precedence to operators. 
2. Create a prefix string and a stack to hold operators. 
3. Loop through each character in the Postfix expression, processing operands and operators. 
4. Handle parentheses by pushing and popping from the stack. 
5. After processing the expression, pop any remaining operators from the stack to prefix. 
6. Print the resulting prefix expression. 
7. End the program

## PROGRAM:
```
#include<bits/stdc++.h>
using namespace std;

bool isOperator(char c)
{
    switch(c)
    {
        case '+':
        case '-':
        case '*':
        case '/':
            return true;
    }
    
    return false;
}

string postToPre(string post)
{
    stack<string> s;
    
    int l = post.size();
    
    for(int i=0;i<l;i++)
    {
        if(isOperator(post[i]))
        {
            string op1 = s.top();
            s.pop();
            string op2 = s.top();
            s.pop();
            
            string temp = post[i]+op2+op1;
            s.push(temp);
        }
        else
        {
            s.push(string(1,post[i]));
        }
    }
    
    string ans="";
    while(!s.empty())
    {
        ans += s.top();
        s.pop();
    }
    return ans;
}

int main()
{
    string s;
    cin>>s;
    cout << "Postfix to Prefix expression:" << endl;
    cout<<postToPre(s);
    return 0;

}
```

## OUTPUT:
![image](https://github.com/user-attachments/assets/77220d79-6d6c-47fe-8ea3-d47ced78d973)

## RESULT:
Thus,the CPP program for Postfix to Prefix Conversion using Stack STL has been successfully created.


# 5C QUEUE ADT

## PROGRAM STATEMENT:
Write a CPP Program to insert five character elements in to Queue ADT (use STL for Queue)

## ALGORITHM:
1. Create a queue of characters using queue<char>. 
2. Input 5 characters using a loop and push each character into the queue. 
3. Print the message "Queue Elements are:". 
4. Use a while loop to traverse the queue until it is empty. 
5. For each iteration, print the front element of the queue using que.front(). 
6. Remove the front element from the queue using que.pop() 
7. End the program

## PROGRAM:
```
#include <iostream>
#include <queue>
using namespace std;
int main(){
char val;
queue<char> q;
for(int i=0;i<5;i++){
cin>>val;
q.push(val);
}
cout<<"Queue Elements are:";
for(int i=0;i<5;i++){
cout<<q.front()<<" ";
q.pop();
}
}
```

## OUTPUT:
![image](https://github.com/user-attachments/assets/b4a5bafd-3e44-4f77-b1fb-71b51f642fe9)

## RESULT:
Thus, the C++ program to insert 5 operator elements in to Queue ADT is created successfully.


# 5D QUEUE APPLICATIONS

## PROGRAM STATEMENT:
write a C++ program to implement FCFS algorithm(to read no of.process p1,p2,p3 and p4 and its burst time from the user) & find out waiting time ,Turn Around time  & Average turn around time of the the process.

## ALGORITHM:
1. Take the number of processes and their burst times from the user and push them into an array.

2. Set the first process’s waiting time to 0, then calculate each next process's waiting time as the sum of the previous burst times.

3. Calculate each process’s turnaround time as the sum of its burst time and waiting time.

4. Use a loop to accumulate all turnaround times and calculate the average by dividing by the number of processes.

5. Display each process with its burst time, waiting time, turnaround time, and the average turnaround time at the end.

## PROGRAM:
```
#include<iostream>
using namespace std;
int main()
{
    int i,n=4,bt[4],wt[4],tat[4];
    float tot_wt=0,tot_tat=0;
    
    for(i=0;i<n;i++)
    {
        cin>>bt[i];
    }
    wt[0]=0;
    for(i=1;i<n;i++){
        wt[i]=wt[i-1]+bt[i-1];
        tot_wt+=wt[i];
    }
    for(i=0;i<n;i++){
        tat[i]=wt[i]+bt[i];
        tot_tat=tot_tat+tat[i];
    }
    cout<<"Processes   BT time   WT time   TA time"<<endl;
    for(i=0;i<n;i++)
    {
    
        cout<<"       "<<i+1<<"       " <<bt[i]<<"       "<<wt[i]<<"       "<<tat[i]<<endl;
    
    }
    cout<<"Average turn around time = "<<tot_tat/n;
    
}
```

## OUTPUT:
![image](https://github.com/user-attachments/assets/518547c0-c32c-4e8a-acf5-8d6adf21a96f)

## RESULT:
Thus,the C++ program to implement FCFS algorithm(to read no of.process p1,p2,p3 and p4 and its burst time from the user) & find out waiting time ,Turn Around time  & Average turn around time of the the process has been successfully created.





