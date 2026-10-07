# part2-subtask1
#include <iostream>
#include <string>
#include <cctype> // For toupper()

using namespace std;

// Function to convert a single character to Morse code
string charToMorse(char c) {
    c = toupper(c); // Convert to uppercase to simplify matching
    
    // You will need to fill in the rest of the alphabet here
    if (c == 'A') return ".-";
    if (c == 'B') return "-...";
    if (c == 'C') return "-.-.";
    if (c == 'D') return "-..";
    if (c == 'E') return ".";
    if (c == 'F') return "..-.";
    if (c == 'G') return "--.";
    if (c == 'H') return "....";
    if (c == 'I') return "..";
    if (c == 'J') return ".---";
    if (c == 'K') return "-.-";
    if (c == 'L') return ".-..";
    if (c == 'M') return "--";
    if (c == 'N') return "-.";
    if (c == 'O') return "---";
    if (c == 'P') return ".--.";
    if (c == 'Q') return "--.-";
    if (c == 'R') return ".-.";
    if (c == 'S') return "...";
    if (c == 'T') return "-";
    if (c == 'U') return "..-";
    if (c == 'V') return "...-";
    if (c == 'W') return ".--";
    if (c == 'X') return "-..-";
    if (c == 'Y') return "-.--";
    if (c == 'Z') return "--..";
    if (c == ' ') return "/"; // Use / to separate words
    
    return ""; // Return empty for unknown characters
}

int main() {
    string input;
    
    cout << "Enter a short English message: ";
    getline(cin, input); // Use getline to capture spaces
    
    cout << "\nIndividual Letters:\n";
    // Loop through each letter and print it with its Morse code
    for (char c : input) {
        if (c != ' ') {
            cout << c << " : " << charToMorse(c) << endl;
        }
    }
    
    cout << "\nFull Translated Message:\n";
    // Loop through again to print the full message
    for (char c : input) {
        cout << charToMorse(c) << " ";
    }
    cout << endl;
    
    return 0;
}
