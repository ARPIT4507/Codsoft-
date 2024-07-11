#include <iostream>
#include <cstdlib>
#include <ctime>

void guess_the_number() {
    // Initialize random seed
    std::srand(std::time(0));
    // Generate random number between 1 and 100
    int number_to_guess = std::rand() % 100 + 1;
    int user_guess = 0;
    
    std::cout << "Welcome to 'Guess the Number'!" << std::endl;
    std::cout << "I have selected a number between 1 and 100. Try to guess it!" << std::endl;
    
    // Loop until the user guesses the correct number
    while (user_guess != number_to_guess) {
        std::cout << "Enter your guess: ";
        std::cin >> user_guess;
        
        if (user_guess < number_to_guess) {
            std::cout << "Too low! Try again." << std::endl;
        } else if (user_guess > number_to_guess) {
            std::cout << "Too high! Try again." << std::endl;
        } else {
            std::cout << "Congratulations! You guessed the correct number!" << std::endl;
        }
    }
}

int main() {
    guess_the_number();
    return 0;
}
