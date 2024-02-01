de <iostream>
#include <cstdlib>
#include <ctime>

using namespace std;

int main() {
    // Seed the random number generator
    srand(time(0));

    // Generate a random number between 1 and 100
    int secretNumber = rand() % 100 + 1;

    int userGuess;
    int attempts = 0;

    cout << "Welcome to the Number Guessing Game!" << endl;

    do {
        // Prompt the user to guess the number
        cout << "Enter your guess (between 1 and 100): ";
        cin >> userGuess;

        // Provide feedback on the user's guess
        if (userGuess < secretNumber) {
            cout << "Too low! Try again." << endl;
        } else if (userGuess > secretNumber) {
            cout << "Too high! Try again." << endl;
        } else {
            cout << "Congratulations! You guessed the correct number in " << attempts << " attempts." << endl;
        }

        // Increment the number of attempts
        attempts++;

    } while (userGuess != secretNumber);

    return 0;
}
