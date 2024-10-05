# Arcade (week 1)

My team and I opened the 2 files and were presented with the source code of a website and the website itself.  The first thing that we did was look through the source code to see how one would get the flag.  The most obvious solution was to win the game, but it would take too long to actually win some.  My group mates and I decided to split look at both games (2 people looking at the brick breaker and the other half looking at the lottery).  I let the brick breaker game run, and while we were discussing what different things we could look into to win, my game started to get close to the end.  I ended up restarting the website, eventually losing my progress, but it was fun to play.  

For the lottery game, the game website actually crashed, so the flag was released.  I wanted to learn how the ctf were to be actually found, so I asked a friend to expalin:

Since the game used a network/server-client to check whether the game was won, I needed to go to the network tab, and check on the GET response.  Once I did that, I could edit the input on the URL to get all matchign numbers in order to win the lottery game.

For the brick breaker game, one of my teammates ahve found that there is a script in the HTML of the website.  Since we couldn't any of the static code, we could send requests in Java.  My teammate had found that there is a way to edit Java variables through the console.  When we sent a command to the console: ```var = 30``` we were able to trick the website to think we broke all 30 of the bricks in the game, and get our second flag.
