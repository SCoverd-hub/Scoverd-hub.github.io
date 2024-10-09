```mermaid
flowchart TD
	Main([Main]) --> 
	A[[Integer secret]] -->
	B[[Integer guess]] -->
	C["secret = random(100)+1"] -->
    D[/Output "Please enter a guess between 1 and 100"/] -->
    E(( )) -->|True|N
    E-->F 
    F[Input guess] --> G
    G{guess > secret}
    G-->|False|H
    G-->|True|I
    H-->J
    I[/Output "Guess is too High"/]
    I-->J
    J(( ))
    J-->K
    K{guess < secret}
    K-->|False|M
    K-->|True|L
    L[/Output "Guess is too LOW"/]
    L-->M
    M(( ))
    M-->N
    N{{guess != secret}}-->|False|O
    O[/Output "Correct!"/]-->End
    End([End])	
```


FlowChart Description:<br><br>
Integer Secret: Creates the secret integer<br>
Integer Guess: Integer for guess<br>
Secret=random(100)+1: Randomizes secret integer<br>
Output "Please enter a guess between 1 and 100" : Provides the original output to prompt user to enter an integer<br>
Input Guess: What the user inputs as an integer<br>
Guess > secret: True or false depending on user input and value of the randomized secret integer<br>
Guess < Secret: True or false depending on user input and value of the randomized secret integer<br>
Output Low or High: Will notify user that guess is to low or high<br>
Guess !=secret: Will determine if guess is correct or not either looping back to Input guess or output of correct answer<br>
Output Correct: Notifies user that answer is correct.