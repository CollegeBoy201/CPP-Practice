//this program tests maps and vectors together. The user is asked to guess the state's capital and if user guesses right, they earn a point. If user guesses wrong they earn an incorrect point. The map is copied into the vector using push_back in order for this to work.
#include <iostream>
#include <map>
#include <random>
#include <vector>
using std::string;

int main(){
    //a map with all 50 states in their capital
    std::map<string, string>stateToCapitals = {
        /*1*/{"Alabama", "Montgomery"},
        /*2*/{"Alaska", "Juneau"},
        /*3*/{"Arizona", "Phoenix"},
        /*4*/{"Arkansas", "Little Rock"},
        /*5*/{"California", "Sacramento"},
        /*6*/{"Colorado", "Denver"},
        /*7*/{"Connecticut", "Hartford"},
        /*8*/{"Delaware", "Dover"},
        /*9*/{"Florida", "Tallahassee"},
        /*10*/{"Georgia", "Atlanta"},
        /*11*/{"Hawaii", "Honolulu"},
        /*12*/{"Idaho", "Boise"},
        /*13*/{"Illinois", "Springfield"},
        /*14*/{"Indiana", "Indianapolis"},
        /*15*/{"Iowa", "Des Moines"},
        /*16*/{"Kansas", "Topeka"},
        /*17*/{"Kentucky", "Frankfort"},
        /*18*/{"Louisiana", "Baton Rouge"},
        /*19*/{"Maine", "Augusta"},
        /*20*/{"Maryland", "Annapolis"},
        /*21*/{"Massachusetts", "Boston"},
        /*22*/{"Michigan", "Lansing"},
        /*23*/{"Minnesota", "Saint Paul"},
        /*24*/{"Mississippi", "Jackson"},
        /*25*/{"Missouri", "Jefferson City"},
        /*26*/{"Montana", "Helena"},
        /*27*/{"Nebraska", "Lincoln"},
        /*28*/{"Nevada", "Carson City"},
        /*29*/{"New Hampshire", "Concord"},
        /*30*/{"New Jersey", "Trenton"},
        /*31*/{"New Mexico", "Santa Fe"},
        /*32*/{"New York", "Albany"},
        /*33*/{"North Carolina", "Raleigh"},
        /*34*/{"North Dakota", "Bismarck"},
        /*35*/{"Ohio", "Columbus"},
        /*36*/{"Oklahoma", "Oklahoma City"},
        /*37*/{"Oregon", "Salem"},
        /*38*/{"Pennsylvania", "Harrisburg"},
        /*39*/{"Rhode Island", "Providence"},
        /*40*/{"South Carolina", "Columbia"},
        /*41*/{"South Dakota", "Pierre"},
        /*42*/{"Tennessee", "Nashville"},
        /*43*/{"Texas", "Austin"},
        /*44*/{"Utah", "Salt Lake City"},
        /*45*/{"Vermont", "Montpelier"},
        /*46*/{"Virginia", "Richmond"},
        /*47*/{"Washington", "Olympia"},
        /*48*/{"West Virginia", "Charleston"},
        /*49*/{"Wisconsin", "Madison"},
        /*50*/{"Wyoming", "Cheyenne"},

    };
    
    string capital; //for user input
    int correct = 0, incorrect = 0; //for tracking points

    do{
        std::vector<string> USkeys; //create a vector named 'USkeys'
        
        //put the map keys into the vector using for range loop(all 50 states and their capitals
        for(const auto &us_keys : stateToCapitals){
            USkeys.push_back(us_keys.first);
        }
        
        //create RNG syntax
        std::random_device engine;  //gets random seed from generator
        std::mt19937 gen(engine()); //creates the RNG
        std::uniform_int_distribution<> dist(0, (USkeys.size()) - 1);   //RNG is from 0 to size of vector(50 - 1) 0-49
        int randomIndex = dist(gen);    //store the RNG index into variable
        //display random index value that it got when it compiled
        //std::cout << "Random index: " << randomIndex << "\n";
        
        
        //get the 'randomIndex' value from the vector and store that value into 'testing'
        string randomState = USkeys.at(randomIndex);
        
        //using find(), pass 'testing' in the parameter to find the string that was initialized with the random index and store it into an iterator pointer named 'it2'
        auto it2 = stateToCapitals.find(randomState);
        //it2->first is the key which is the state displays as a string
        std::cout << "What's " << it2->first << "'s " << "capital? ";
        std::getline(std::cin, capital);
        
        //if user types "quit" dont show this condition
        if(capital != "quit"){
            if(capital == it2->second){ //if they guess right show this
                std::cout << "Correct!\n";
                std::cout << it2->first << "'s " << "capital is " << it2->second << "\n";
                correct++;
            }
            else{
                std::cout << "Incorrect!\n";//if they guess wrong show this
                std::cout << it2->first << "'s " << "capital is actually " << it2->second << "\n";
                incorrect++;
                
            }
        }
    }while(capital != "quit");  //break loop if they type "quit"
        
    //after loop breaks. show their correct and incorrect score
    std::cout << "Correct: " << correct << "\n";
    std::cout << "Incorrect: " << incorrect << "\n\n";


    return 0;
}
