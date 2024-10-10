# CDS.EXP-14
## Aim:
**To study and implement Inheritance.**

## Software:
`Microsoft VSCode`

## Theory:
Inheritance in C++ is a fundamental concept of object-oriented programming (OOP) that allows a class (called the derived class or child class) to inherit properties and behaviors (data members and member functions) from another class (called the base class or parent class). This promotes code reusability and establishes a relationship between classes.

Key Concepts of Inheritance:
Base Class: The class whose properties and methods are inherited by another class. It is sometimes referred to as the parent or super class.

Derived Class: The class that inherits the properties and methods from the base class. It can also have additional properties and methods of its own.

Types of Inheritance:
Single Inheritance: A derived class inherits from only one base class.

Multiple Inheritance: A derived class inherits from more than one base class.

Multilevel Inheritance: A derived class is derived from another derived class.

Hierarchical Inheritance: Multiple derived classes inherit from a single base class.
## Code: 14A
```cpp
// NAME - AKALP SARKAR
// PRN- 23070123116
// EXPERIMENT - 14(A) 

// Program to show single inheritance.

# include <iostream>
# include <string>
using namespace std;

class Uni
{
    public:
    string uni= "Symbiosis";
    void discipline()
    {
        cout << "Engineering" <<endl;
    }
};
class Dep : public Uni
{
    public:
    string dept= " Electronics & Telecommunication";
};
int main()
{
    Dep u1;
    u1.discipline();
    cout<<u1.uni + " "+u1.dept ;
} 
```
## Output:
![Output14A](https://github.com/user-attachments/assets/f02f94cd-c46f-426a-a3c0-559f20afd476)


## Code: 14B
```
// NAME - AKALP SARKAR
// PRN - 23070123116
// EXPERIMENT - 14(B)

// Program to show multiple inheritance.

#include<iostream> 
#include<string> 
using namespace std; 

// Parent CLass1 
class Vehicle {
    public:
    string company=" Ford";
    void type(){
        cout << "Mustang"<< endl;
    }
};
// Parent Class 2
class Specs{
    public:
    string mileage="8 kmpl";
    void colour(){
        cout<<"Grey"<<endl;
    }
};
// Child Class-1 (derived from parent- 1&2)
class Car: public Vehicle,public Specs{
    public:
    string seater = " 4 seater";
};
int main(){
    //multiple inheritance
    Car f2;
    f2.colour();
    cout<<f2.company<<" ";
    f2.type();
    cout<<"("<<f2.seater<<")"<<endl<<"MILEAGE:"<<f2.mileage<<endl;
} 

```

## Output:
![Output14B](https://github.com/user-attachments/assets/d895cbd0-9cb6-4475-95d7-675f24c84e29)


## Code: 14C
```
// NAME - AKALP SARKAR
// PRN - 23070123116
// EXPERIMENT - 14(C)
// Program to show multilevel inheritance.

#include<iostream> 
#include<string>
using namespace std; 

// single base class
class Student {
public:
    string stud;
    void get_Student_data()
    {
        cout << "Enter the name of the student: ";
        cin >>  stud;
    }
};
 
// derived class from base class
class PRN : public Student {
public:
    int prn;
    void get_PRN_data()
    {
        cout << "Enter the PRN: ";
        cin >> prn;
    }
};
 
// derived from class derive1
class Branch : public PRN {
private:
   string branch;
 
public:
    void get_Branch_data()
    {
        cout << "Enter the branch: ";
        cin >> branch;
    }
 
    // function to print sum
    void details()
    {
        cout << "Name: "<<stud<<"  PRN: "<< prn<<"  Branch: "<<branch << endl;
    }
};
int main()
{
    // object of sub class
    Branch obj;
 
    obj.get_Student_data();
    obj.get_PRN_data();
    obj.get_Branch_data();
    obj.details();
    return 0;
}
```
## Output:
![Output14C](https://github.com/user-attachments/assets/951dee1a-994d-49e4-b2a4-615d071a08ca)


## Code: 14D
```
// NAME -AKALP SARKAR
// PRN - 23070123116
// EXPERIMENT - 14(D)

// Program to show Hiererchical Inheritance.                    

#include <iostream>
using namespace std;

// base class
class Flower {
public:
    Flower() { cout << "This is a Flower. \n"; }
};

// first sub class
class Lotus : public Flower {
public:
    Lotus() { cout << "This flower is a lotus. \n"; }
};

// second sub class
class Marigold : public Flower {
public:
    Marigold() { cout << "Thisflower is a marigold. \n"; }
};

// main function
int main()
{
    // Creating object of sub class will invoke the constructor of base class.
    Lotus obj1;
    Marigold obj2;
    return 0;
}
```                  
## Output:
![Output14D](https://github.com/user-attachments/assets/efc36acd-82c9-4a9b-88cc-d4a84a7d80fc)

### Conclusion:
I learnt about inheritance in C++, its keywords, modes, types and performed programs based on that.


