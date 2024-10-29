# revpaperscissors (week 5)

## Chal1
First, I put the chal1 binary into Ghidra to see what the executable was doing. Then, I logged into/ran netcat (nc) to run the actual executable from the ctf network (it won't run locally).  By looking through the main function in Ghidra, I was able to see what choices the program would make, in regards to their rock paper scissors choice.  It was very obvious as it was hard coded into the main function.

## Cha2
The second challenge requires a longer username before starting the game.  *This would be important later.* Next, the challenge requires you to win 10 games in a row (compared to the 5 wins from the previous challenge. 
Sidenote: Ghidra cannot perfectly replicate the code from a binary.
I mention that because a lot of the numbers that would be used to decipher the "algorithm" used for the rock paper scissors game is more easily understood one you decipher the hex to real numbers.  To keep the pattern of the game consistent, I kept the same username when playing the game.  This was usefule when brute forcing the win (this is where keeping the username length consistent became important).  

#### An attempt at deciphering the algorithm
After looking through the main funciton, I looked for other funciton that may be useful.  In Ghidra, I had found a "make_moves" funciton, which takes the length of the username, then generate the move that will be played.  Once this is figured out, I could predict the moves that would come about.  *I would have to convert the hex to decimal numbers first.* 

So it apparently checks only the first 10 characters of the username.  From that, it converts the characters into numbers, then does some *<silly math>*, then returns the move to be played.  


smthmg smthmg modulo...
----
**Personal Notes**
bruteforce:
- need same name
- then can record
- aaaaaa

name: asdfghjklmnbvc
2, 0, 0, 0, 0, 0, 0, 2, 0, 1

the order stays the same if ur name remains consistent
