//# C++ class
//The C++ program to implement class student having following data members functions, Accept the name of student to compute total, average to display the data.
#include<iostream>
using namespace std;

class STUDENT
{
 public :
 	int rollno,marks[10],total,i,n;
	float avg,per;
	string name,subject[20];
	
	int data()
	{
	  cout<<"Enter a roll no.";
	  cin>>rollno;
	  cout<<"Enter your name : ";
	  cin>>name;
	  cout<<"Enter a no. of subject ";
	  cin>>n;
	  cout<<"Enter a marks of subject and subject name "<<endl;
	  total=0;
	  for(int i=1;i<=n;i++)
	  {
	  	cout<<"The subject name is : ";
	  	cin>>subject[i];
	    cout<<"marks as per subject : ";
	  	cin>>marks[i];
	  	total=total+marks[i];
	  }
	  
	  
	  avg=(total/n);
	  per=avg;
	
	  
	}
	
	void display()
	{
		cout<<"\n The roll no. is : "<<rollno<<endl;
		cout<<"\n The name is : " <<name<<endl;
		
		for(int i=1;i<5;i++)
		{
			cout<<"Marks of subject : ";
			cout<<subject[i]<<"is : ";
			cout<<marks[i]<<endl;
		}
		cout<<"\n The total of "<<n<<"subject marks :"<<total<<endl;
		cout<<"\n The average marks is : "<<avg<<endl;
		cout<<"\n The percentage is :"<<per;
		
		if(per>=40)
		{
		    cout<<"__The student is **_PASS_**"<<endl;
		    
		}
		else
		{
		    cout<<"__FAIL__"<<endl;
		    cout<<"Try next year ";
		}
		
		
		
		
		
	}
};

int main()
{
	STUDENT v;
	v.data();
	v.display();
	return 0;
}
