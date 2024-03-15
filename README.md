# project1
#include<bits/stdc++.h>
using namespace std;
int main(){
    //heading
    cout<<"Let me think of a number between 1 to 50"<<endl;
    string level;
    cout<<"Choose the level of difficulty.....Type 'Easy' or 'Hard'."<<endl;
    cin>>level;
    //generate random number
    random_device rd;
    mt19937 gen(rd());
    uniform_int_distribution<> dis(1, 50);
    int com_choice = dis(gen);

    //code for level
    if(level == "Easy"){
        int attempts = 10;
        cout<<"You have 10 attempts remaining for guess the number!"<<endl;
        //cout<<com_choice<<endl;
        int ur_choice;
        for(int i=0; i<10; i++){
            cout<<"Make your choice --> ";
            cin>>ur_choice;
            if(com_choice > ur_choice){
                cout<<"Guess Is Too Low"<<endl;
                cout<<"Guess Again"<<endl;
                attempts -= 1;
                cout<<"You have "<<attempts<<" attempts remaining to Guess the number!"<<endl;
            }
            else if(com_choice < ur_choice){
                cout<<"Guess Is Too High"<<endl;
                cout<<"Guess Again"<<endl;
                attempts -= 1;
                cout<<"You have "<<attempts<<" attempts remaining to Guess the number!"<<endl;
            }
            else{
                break;
            }
        }
        if(ur_choice == com_choice){
            cout<<"Congratulations......Your guess is right!!!"<<endl;
        }
        else{
            cout<<"You are out of guesses.....You Lose"<<endl;
        }
    }
    if(level == "Hard"){
        int attempts = 5;
        cout<<"You have 5 attempts remaining for guess the number!"<<endl;
        cout<<com_choice<<endl;
        int ur_choice;
        for(int i=0; i<5; i++){
            cout<<"Make your choice --> ";
            cin>>ur_choice;
            if(com_choice > ur_choice){
                cout<<"Guess Is Too Low"<<endl;
                cout<<"Guess Again"<<endl;
                attempts -= 1;
                cout<<"You have "<<attempts<<" attempts remaining to Guess the number!"<<endl;
            }
            else if(com_choice < ur_choice){
                cout<<"Guess Is Too High"<<endl;
                cout<<"Guess Again"<<endl;
                attempts -= 1;
                cout<<"You have "<<attempts<<" attempts remaining to Guess the number!"<<endl;
            }
            else{
                break;
            }
        }
        if(ur_choice == com_choice){
            cout<<"Congratulations......Your guess is right!!!"<<endl;
        }
        else{
            cout<<"You are out of guesses.....You Lose"<<endl;
        }
    }
    return 0;
}
