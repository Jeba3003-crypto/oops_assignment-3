#include <iostream>
using namespace std;

class Student {
protected:
    string name;
    int roll;

public:
    void getStudent() {
        cout << "Enter Name: ";
        cin >> name;
        cout << "Enter Roll No: ";
        cin >> roll;
    }

    void displayStudent() {
        cout << "\nName: " << name << endl;
        cout << "Roll No: " << roll << endl;
    }
};

class Marks : public Student {
protected:
    int m1, m2;

public:
    void getMarks() {
        cout << "Enter 2 Marks: ";
        cin >> m1 >> m2;
    }

    void displayMarks() {
        displayStudent();
        cout << "Marks: " << m1 << " " << m2 << endl;
    }
};

int main() {
    Marks s;
    s.getStudent();
    s.getMarks();
    s.displayMarks();
}
