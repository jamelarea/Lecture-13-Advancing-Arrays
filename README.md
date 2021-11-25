# Lecture-13-Advancing-Arrays

SLIDE 3, Range Based for Loop

    #include <iostream>
    using namespace std;

    int main()
    {
        string courses[] = { "BSU CC", "BSU BA", "HNC CC", "HND" };

        for (int i = 0; i < 4; i++) {
            cout << courses[i] << endl;
        }

        for (auto course: courses){ //range based for loop
            cout << course << endl;

        }
    }
    
SLIDE 4, Auto Keyword

    #include <iostream>
    using namespace std;

    int main()
    {
        char letters[] = { 'C', 'o', 'd', 'e', 'L', 'a', 'b' };
        for (auto letter : letters) {
            cout << letter;
        }
    }

SLIDE 5, Input/Output Array

    #include <iostream>
    using namespace std;

    int main()
    {
        cout << "Input 5 integer values:" << endl;

        int num[5];
        for (int i = 0; i < 5; i++) {
            cin >> num[i];
            while (cin.fail()) { //error handling
                cout << "\nInvalid command. Enter the integer again.\n";
                cin.clear(); //clears the error flag on cin
                cin.ignore(1000, '\n'); //used to ignore or clear one or more characters from the input
                cin >> num[i];
            }
        }

        cout << "\nThese are the integer values that you have inputted:" << endl;
        for (int j = 0; j < 5; j++) {
            cout << num[j] << endl;
        }
        return 0;
    }

MULTIDIMENSIONAL ARRAYS

SLIDE 8-9, 2D Array Initialisation

    #include <iostream>
    using namespace std;

    int main()
    {
        string snacks[3][4] = {
            {"Galaxy silk", "Marks Bar", "Snickers", "Bounty"}, //first row
            {"Flavoured Youghurt", "Oman chips", "Oreo", "Lays"}, //second row
            {"Apple", "Banana", "Orange", "Pear"} //third row
        };

        cout << snacks[1][2] << endl; //access Oreo
    }

SLIDE 10, Iterating through a 2D array

    #include <iostream>
    using namespace std;

    int main()
    {
        string snacks[3][4] = {
            {"Galaxy silk", "Marks Bar", "Snickers", "Bounty"}, //first row
            {"Flavoured Youghurt", "Oman chips", "Oreo", "Lays"}, //second row
            {"Apple", "Banana", "Orange", "Pear"} //third row (no comma)
        };

        for (int i = 0; i < 3; i++) {
            for (int j = 0; j < 4; j++) {
                cout << snacks[i][j] << " "; //displays all the snacks from rows to columns
            }
            cout << endl;
        }
    }
    
SLIDE 11, Array Art

    #include <iostream>
    using namespace std;

    int main()
    {
        string patterns[5][5] = {
            {"-----"}, //first row
            {"-0-0-"}, //second row
            {"-@@@-"}, //third row
            {"-^^^-"}, //fourth row
            {"-vvv-"} //fifth row row (no comma)
        };

        for (int i = 0; i < 5; i++) {
            for (int j = 0; j < 5; j++) {
                cout << patterns[i][j] << " "; //displays all the snacks from rows to columns
            }
            cout << endl;
        }
    }
    
    
