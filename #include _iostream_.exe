#include <iostream>
#include <string>
#include <map>


using namespace std;

void bod();

map<string, string> registeredUsers;



bool validateLogin(const string& username, const string& password) {
    
    if (registeredUsers.find(username) != registeredUsers.end()) {
        
        return registeredUsers[username] == password;
    }
    return false;
}


void registerUser(const string& username, const string& password) {
    
    if (registeredUsers.find(username) != registeredUsers.end()) {
        cout << "Username already exists. Please choose a different username.\n";
    } else {
        
        registeredUsers[username] = password;
        cout << "Registration successful!\n";
    }
}

int main() {
    string username, password;
    int choice;

    cout << "                    ///Welcome////\n\n";

    while (true) {
        cout << "\n1. Login\n";
        cout << "2. Register\n";
        cout << "3. Log out\n";
        cout << "4. Quit\n";
        cout << "\nEnter your choice: \n";
        cin >> choice;

        switch(choice) {
            case 1:
                cout << "\nLogin\n";
                cout << "Username: ";
                cin >> username;
                cout << "Password: ";
                cin >> password;
                if (validateLogin(username, password)) {
                    cout << "\nLogin successful!\n";
                } else {
                    cout << "\nInvalid username or password. Please try again.\n\n";
                }
                break;
            case 2:
                cout << "\nRegister\n";
                cout << "Username: ";
                cin >> username;
                cout << "Password: ";
                cin >> password;
                registerUser(username, password);
                break;
            case 3:
                cout << "\n\See you Again!\n";
                int main();
                break;
            case 4:
                cout << "Closing Program\n";
                return 0;
                break;
            default:
                cout << "Invalid choice. Please try again.\n";
        }
    }

    return 0;
}
    