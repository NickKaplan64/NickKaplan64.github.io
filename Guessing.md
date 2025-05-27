# Random Guessing Game Flowchart

```mermaid
flowchart TD
    Start([Start]) --> Init[Initialize game: set range and generate random number]
    Init --> Prompt[Prompt user to guess a number]
    Prompt --> CheckInput{Is input valid?}
    
    CheckInput -- No --> Error[Display error message: invalid input] --> Prompt
    CheckInput -- Yes --> Compare{Is guess correct?}
    
    Compare -- Yes --> Correct[Display correct message] --> End([End])
    Compare -- No --> HighLow{Is guess too high?}
    
    HighLow -- Yes --> High[Display too high message] --> Prompt
    HighLow -- No --> Low[Display too low message] --> Prompt
```


## Description of Each Step

**Start**: The program begins execution.

**Initialize Game**: A random number is generated within a specified range. This is the target number the user must guess.

**Prompt User**: The user is asked to input a guess.

**Input Validation**:  
- If the input is not a valid number, an error message is displayed and the user is prompted again.  
- If the input is valid, the program continues.

**Compare Guess**:  
- If the guess matches the random number, the program congratulates the user and ends.  
- If the guess is incorrect, it checks whether the guess is too high or too low.

**Too High / Too Low**:  
- If the guess is too high, a message is shown and the user is prompted again.  
- If the guess is too low, a similar message is shown and the user is prompted again.

**End**: The game ends when the user guesses correctly.
