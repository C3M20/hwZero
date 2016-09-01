# hw0, Minutes of Action. Due: soon (5 days after your linux accounts are available to you).

(For example, if you are notified on class on the 10th of the month that the linux accounts are ready and given information about how to login, then the assignment is due on the 15th).

--update: Accounts information will be given Today (Thursday 9/1) during class.

You will create a C++ program that will count the total of minutes, hours, and days mentioned inside of a plain-text file.

## Input 

The input is a plain-text file, where each line is terminated with an end-of-line character.
Each line will have words or numbers.
To simplify we will assume that there will not be words containing numbers such as the word: car4sale. (Or numbers containg letters such as 22E01). A word is a string of letters (upper and lower case).
Lines in the input file that start with the symbol `#` should be considered comments and therefore skipped.

Example 1:

    A person of interest travels 20 minutes each day.
    Meredith travels 1 hour by train to visit Derek. However, Derek can visit her in one minute.
    #this line is a comment because it starts with #
    #for example, this comment line contains 1000 minutes but they do not get added anywhere
    Cristina does 4 minutes of yoga on her lunch break; she's done that in the last 3 weeks. 
    She can drink 3 minutemaid bottles a day.

Each line that is not a comment will be processed to find references of minutes, hours, or days.
Such items will be appear first as a number and then one of these words: minute, minutes, hour, hours, day, days.
There may be empty lines in the input file.
The words and numbers may be separated by spaces, commas, period, new-line character, parenthesis, etc. Words and numbers will be separated by at least one non-letter or non-digit symbol. A word is one or more consecutive letters until a non-letter is next.
You can assume that a word will be at most 30 characters long (always letters). Numbers are always digits (0,1,2,...,9). Numbers will have maximum of 10 digits. There may be things that look like a number but are not, such as: 1024K.

## Program specification

The main program should be called `uhday` and the syntax in which it will be tested is as follows:

`uhday "input=FILENAME"`

The parameter `input` specifies the name of the input file.

Example of program calls:

`uhday "input=gray.txt"`

or, `./uhday "input=gray.txt"`

The source code will be compiled as follows:

`g++ -std=c++11 -o uhday -I ./ *.cpp`

## Output

Your program will output to the console (such as via cout, or printf) with the results of counting, independently, the minutes, hours, and days metioned in the file.
Your program must follow the output format exactly to facilitate automated grading (and to avoid failing test cases due to things such as output of an empty line at the end).

Output for the input example.

    Minutes:24
    Hours:1
    Days:0

## Assumptions

* The input file can fit in main maimory (not larger than 10kb).
* The words "Minutes", "Hours", "Days" in the output will be exactly like that. They are expected to always be in plural.
* You can assume that it is safe to treat each line independently. There will not be test cases such as line 1 ending in a number, and line 2 starting with: day. 

## Requirements

* This assignment is pass/fail. If your program scores more than 60 points, then you will pass. 
* Place your codes in a folder named: `hw0` (Failure to do so will cause your program to have a zero grade due to inability for doing automated grading).
* Your program should not produce any unexpected output when it is doing intermediate calculations because doing so will interfere with automated grading and some test cases will fail.
* You can not assume a maximum number of lines in the input file.
