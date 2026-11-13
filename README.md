#include <iostream>
#include <string>
using namespace std;

int main() {
    int choice;
    int score = 0;
    char again;

    string waste[8] = {
        "Plastic Bottle",
        "Old Newspaper",
        "Banana Peel",
        "Plastic Bag",
        "Cardboard Box",
        "Vegetable Waste",
        "Water Bottle",
        "Used Paper"
    };

    int correctBin[8] = {1, 2, 3, 1, 2, 3, 1, 2};

    cout << "==============================\n";
    cout << "       ECO HERO GAME\n";
    cout << "==============================\n";

    cout << "Welcome to Eco Hero Game!\n";
    cout << "Help save the environment!\n";

    do {
        score = 0;

        cout << "\n--- GAME INSTRUCTIONS ---\n";
        cout << "1. Plastic Bin\n";
        cout << "2. Paper Bin\n";
        cout << "3. Organic Bin\n";
        cout << "Each correct answer = 10 points\n";

        cout << "\nPress 1 to start: ";
        cin >> choice;

        if (choice != 1) {
            cout << "Game not started!\n";
            return 0;
        }

        for (int i = 0; i < 8; i++) {

            cout << "\nWaste Item: " << waste[i] << endl;

            cout << "1. Plastic Bin\n";
            cout << "2. Paper Bin\n";
            cout << "3. Organic Bin\n";

            cout << "Choose your bin: ";
            cin >> choice;

            if (choice == correctBin[i]) {
                cout << "Correct! +10 Points\n";
                score += 10;
            }
            else {
                cout << "Wrong Answer! Try Again Next Time.\n";
            }
        }

        cout << "\n==============================\n";
        cout << "         GAME RESULT\n";
        cout << "==============================\n";

        cout << "Your Score: " << score << " / 80\n";

        if (score >= 70) {
            cout << "Excellent! You are an Eco Hero!\n";
        }
        else if (score >= 40) {
            cout << "Good Job! Keep saving nature!\n";
        }
        else {
            cout << "Keep Learning! Save Our Planet!\n";
        }

        cout << "\nPlay Again? (Y/N): ";
        cin >> again;

    } while (again == 'Y' || again == 'y');

    cout << "\nThank you for playing!\n";
    cout << "Keep the Earth Clean and Green!\n";

    return 0;
}
