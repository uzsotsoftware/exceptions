#include <cstdlib>
#include<iostream>
#include<string>

using namespace std;

bool EnterRegNum() {
    string regNum;

    try {
        cout << "Enter Registration Number...";
        getline(cin, regNum);
        if ((regNum.length()) != 8)
            throw 10;
        cout << "Ok! Valid Registration number" << endl;
        return 1;
    }    catch (int err) {
        cout << "Invalid Registration Number" << endl;
        return 0;

    }

}
bool Intake() {
    string intake;

    try {
        cout << "Enter Intake value..."<<endl;
        getline(cin,intake );
        if ((intake.length()) != 6)
            throw 1;
        cout << "Ok! Valid Intake value" << endl;
        return 1;
    }    catch (int err) {
        cout << "Invalid Intake value" << endl;
        return 0;

    }
}
bool AW() {
    int age;
    float weight;

    try {
        cout << "Enter age..."<<endl;
        cin>>age;
        if (age<= 0)
            throw 10;
        cout << "Ok! Valid age" << endl;
        cout<<"Enter weight.."<<endl;
        cin>>weight;
        if (weight<= 0)
            throw 'error';
        cout << "Ok! Valid weight" << endl;
        return 1;
    }    catch (int err) {
        cout << "Invalid age" << endl;
        return 0;
    }
        catch (...) {
        cout << "Invalid weight" << endl;
        return 0;

    }
    }
void CheckAddress(int houseNumber,string streetName)throw(string){

        try{
            if(houseNumber<=0)
              throw 10;

          if ((streetName.length())>10)
              throw 'error';
    }
        catch (int err) {
        cout << "Invalid house number" << endl;
        }
        catch (string) {
        cout << "Invalid street name" << endl;
        }


}

int main(int argc, char** argv) {
    string name;
    cout<<"Enter name"<<endl;
    getline(cin,name);
    bool valid;
    bool validintake;
    bool validAW;
    while (valid == 0) {
        valid=EnterRegNum();
        }
    while(validintake == 0){
          validintake=Intake();
    }
    while(validAW == 0){
        validAW=AW();
    }
    CheckAddress(-10,"a very long name");

    return 0;
}
