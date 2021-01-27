# sc-wrangle
## Introduction:

sc-wrangle repo says about data wrangling commands. By these commands, I wrangled the data of shakeshpeare under tragedy. The play name is "THE LIFE AND DEATH OF JULIUS CAESAR"

Note: I used the speakers of Antony and Octavius to count how many times they spoke.

## Files and Commands(Bash)
* entireplay.txt - Input file
Copied and pasted entire text in this file.
* nopunct.txt - entireplay file without punctuation 

```bash
tr -d [:punct:] <entireplay.txt> nopunct.txt
```
* antony.txt - File with count of how many times antony speaks
```bash
grep -i 'ANTONY' nopunct.txt -c > antony.txt
```
Note: i is the case sensitive. So it takes only capital letters.

* octavius.txt - File with count of how many times octavius speaks
```bash
grep -i 'OCTAVIUS' nopunct.txt -c > octavius.txt
```
* ao.txt - Both antony and octavius count in file
```bash
$ paste antony.txt octavius.txt >ao.txt
```
Note: This command directly be used as below command,but if you want to look how they paste in a file,then use it as. sample.
* output.txt - summation of antony and octavius count
```bash
$ paste antony.txt octavius.txt | awk '{print $1+$2;}' >output.txt
```

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
```bash 
$ paste antony.txt octavius.txt | awk '{print $1+$2;}' >output.txt
```
