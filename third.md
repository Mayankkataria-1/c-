Program-3 With Output

#include <iostream>
#include <string>
#include <map>
using namespace std;

void countOccurrences(string str) {
    map<char, int> freq;
    
    for (char c : str) {
        if (isalpha(c)) {
            freq[tolower(c)]++;
        }
    }

    cout << "Character Frequency Table:\n";
    for (auto pair : freq) {
        cout << pair.first << " -> " << pair.second << endl;  // Fixed syntax error
    }
}

int main() {
    string input;
    cout << "Enter a string: ";
    getline(cin, input);
    
    countOccurrences(input);
    
    return 0;
}
