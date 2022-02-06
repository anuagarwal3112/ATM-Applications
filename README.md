# ATM-Applications
#include <iostream>
using namespace std;

void showMenu()
{
    cout << "*****MENU*****" << endl;
    cout << "1. Cheak Balance" << endl;
    cout << "2. Deposit" << endl;
    cout << "3. Withdraw" << endl;
    cout << "4. Exit" << endl;
}

int main()
{
    int option;
    double balance = 500;

    do
    {
        showMenu();
        cout << "Option: ";
        cin>> option;

        switch (option)
        {
            case 1:cout << "Balnce is: " <<balance << " Rs." << endl;
            break;
            case 2:cout << "Deposit Amount: ";
                double depositAmount;
                cin >> depositAmount;
                balance += depositAmount;
                break;
            case 3:cout << "Withdraw amount:";
                double withdrawAmount;
                cin >> withdrawAmount;
                if(withdrawAmount <= balance)
                    balance -= withdrawAmount;
                else 
                    cout << "Not enough money" << endl;
                break; 
        }
    }
    while (option != 4);
    {
        system("pause>0");
    }
        
}
