#include <iostream>
#include <string>
using namespace std;

int main() {
    int choice;
    int voteCount1 = 0, voteCount2 = 0, voteCount3 = 0;
    int totalVoters;
    string voterName;

    cout << "=============================\n";
    cout << "     SIMPLE VOTING SYSTEM     \n";
    cout << "=============================\n\n";

    cout << "Enter total number of voters: ";
    cin >> totalVoters;

    for (int i = 1; i <= totalVoters; i++) {
        cout << "\nVoter " << i << ", please enter your name: ";
        cin >> voterName;

        cout << "\nHello " << voterName << ", please cast your vote:\n";
        cout << "1. Candidate A\n";
        cout << "2. Candidate B\n";
        cout << "3. Candidate C\n";
        cout << "Enter your choice (1-3): ";
        cin >> choice;

        switch (choice) {
            case 1:
                voteCount1++;
                cout << "You voted for Candidate A.\n";
                break;
            case 2:
                voteCount2++;
                cout << "You voted for Candidate B.\n";
                break;
            case 3:
                voteCount3++;
                cout << "You voted for Candidate C.\n";
                break;
            default:
                cout << "Invalid choice! Vote not counted.\n";
        }
    }

    cout << "\n=============================\n";
    cout << "         VOTING RESULT        \n";
    cout << "=============================\n";
    cout << "Candidate A: " << voteCount1 << " votes\n";
    cout << "Candidate B: " << voteCount2 << " votes\n";
    cout << "Candidate C: " << voteCount3 << " votes\n";

    // Find winner
    if (voteCount1 > voteCount2 && voteCount1 > voteCount3)
        cout << "\nWinner: Candidate A \n";
    else if (voteCount2 > voteCount1 && voteCount2 > voteCount3)
        cout << "\nWinner: Candidate B \n";
    else if (voteCount3 > voteCount1 && voteCount3 > voteCount2)
        cout << "\nWinner: Candidate C \n";
    else
        cout << "\nIt's a tie!\n";

    cout << "=============================\n";
    cout << "     THANK YOU FOR VOTING     \n";
    cout << "=============================\n";

    return 0;
}
