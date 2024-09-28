# Guessing.md
```mermaid
flowchart TD
Start([Start]) ==> CreateVariable[Create variables] ==> Output1[/Ask user to type a random number in output/] ==> Userinput{Get user input} & Secretnum[Get a random number to guess] ==> Loop[Create a loop for user input]
subgraph Guessing Game Loop
Loop --> Getnumber["if user input is not a number (non decimal)"] --> Output2[/Say "Please put a non decimal number"/] -.-> Userinput
Loop --> Bigger[if input is bigger] --> Output3[/Say "the user input is too big"/] -.-> Userinput
Loop --> Smaller[if input is smaller] --> Output4[/Say "the user input is too small"/] -.-> Userinput
end
Loop ==> Correct[if input is equal to the random number] ==> Output5[/Say "You got the answer!"/] ==> Testcode[Test code for errors] == No errors ==> End([End])
Testcode == Yes errors ==> Errors[if errors occur] ==> Fix([Check and fix the code])

```
#Steps of the process

1. First, create variables to be used in the game, one to create a random number to be guessed and the other to get the users input
2. Make sure the user knows what to do by telling them in the output
3. Second, once the user inserts an input, create a loop that will continue until the user guesses correctly
4. The loop should include <,>,=, and !=. If the users input is not = to the random number that was generated the loop should restart after the user inputs a new number
5. Third, if the user inputs the wrong number, the program must tell the user in the output that the number was either too small, too big, or not a non decimal number
6. Fourth, if the program has any errors, check where they may be located and fix them
7. Finally, if the program runs without errors and works correctly, the program is finished






















