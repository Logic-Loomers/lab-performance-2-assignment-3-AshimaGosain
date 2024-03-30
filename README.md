#include <iostream>
using namespace std;
class Books{
	public:
		long double isbn[20],isbnss;
		int i,n;
		string bookname[20],author[20];
		Books(){
			cout<<"Are you ready to enter the world of bizzare library";
			cout<<"\nEnter the ISBN number along with the book name and author name";
			cout<<"\nPlease enter the number of books whose data you want to enter: ";
			cin>>n;
			cout<<"\nEnter ISBN number: ";
			for(i=1;i<=n;i++){
				cin>>isbn[i];
			}
			cout<<"\nEnter author name: ";
			for(i=0;i<=n;i++){
				getline(cin,author[i]);
			}
		}
		void names(){
			cout<<"\nEnter book name: ";
			for(i=1;i<=n;i++){
				getline(cin,bookname[i]);
			}
		}
		void search(){
		    cout<<"Enter the book's ISBN number whose details you want to search: ";
		    cin>>isbnss;
		    int flag=0;
		    for(i=1;i<=n;i++){
		    	if(isbnss==isbn[i]){
		    		cout<<"\nBookname is: "<<bookname[i];
		    		cout<<"\nAuthor name is: "<<author[i];
		    		cout<<"\nISBN number is: "<<isbn[i];
		    		flag++;
				}

			}
			if(flag==0){
					cout<<"\nThe ISBN number might be wrong or the book might not be available";
			}
	}
};
int main(){
	int choice;
	Books ob;
	ob.names();
	while(choice<=1){
	      cout<<"Enter what you want to do:\n 1 for searching any book \n 2 for exit";
	    cin>>choice;
	    if(choice==1){
		   ob.search();
	    }
	else{
		cout<<"\nOk byeee";
	}
}
}(https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/Fmb6W2KK)
Design a C++ program for an employee payroll system. Create classes for Employee and Payroll. Users can add employees, enter hours worked, calculate salaries, and generate payroll reports.
