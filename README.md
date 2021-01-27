# sc-wrangle

## FAQ's
1. Tell us your assigned play.
Tragedy, [4, The Life and Death of Julius Caesar](http://shakespeare.mit.edu/julius_caesar/full.html)

2. Tell us your speaker 1.
Antony
3. Tell us your speaker 2.
OCTAVIUS
4. Tell us the question you were asked.
I asked count of speakers and sum of them

Antony - 123
OCTAVIUS - 43
SUM - 168 
5. List all commands used to answer the question. Final commands must be redirected to a file (or files).
Tell us the answer.
my last command 
```
$ paste antony.txt octavius.txt | awk '{print $1+$2;}' >output.txt
```
