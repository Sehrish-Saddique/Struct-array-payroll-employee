# Struct-array-payroll-employee
# include <iostream>
# include <string>
# include <iomanip>
using namespace std;
struct Payroll
{
int empId;
string name;
float no_of_hours;
float hourlypay;
float grosspay;
};
const int SIZE=3;
Payroll p[SIZE];
void inputfunction()
{
    cout<<"Enter the "<<SIZE<<" Employees Data\n";
    for(int index=0; index<SIZE; index++)
    {
    cout<<endl<<setw(45)<<setfill('*');
    cout<<"\n Enter the Employee ID: ";
    cin>> p[index].empId;
    cin.ignore();
    cout<<"\n Enter the Employee Name: ";
    getline(cin, p[index].name);
    cout<<"\n Enter the Number of hours worked: ";
    cin>> p[index].no_of_hours;
    cout<<"\n Enter the Hourly Pay: ";
    cin>> p[index].hourlypay;
    }

    for(int index=0; index<SIZE; index++)
    {
    cout<<endl<<setw(45)<<setfill('_')<<endl;
    p[index].grosspay= (p[index].no_of_hours * p[index].hourlypay);
    cout<<"The gross pay for employee "<<(index+1)<<" is $ "<<p[index].grosspay<<endl;
    }
}
int main()
{
    cout<<"Input Fuction is calling \n";
    inputfunction();
    cout<<"\n Program is terminated . . .";
    return 0;
}
