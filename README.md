# Lab06: Regular Expressions

The goal of this laboratory exercise is to learn more about Regular Expressions, both from a theoritical and practical stand point. Understanding the theory behind regular expressions helps you to understand when regular expression will not be able solve a particular problem. The goal of this lab is to understand their power as well as their limitations

> Some people, when confronted with a problem, think 
> “I know, I'll use regular expressions.”   Now they have two problems.

Said someone who did not fully understand regular expressions.

## Step 1. Cloning this laboratory

First, we need to get this project onto your computer. We do this using the `git clone` command. In the Terminal app type the following command

```bash
git clone https://github.com/groovy-training-logicmonitor/lab06
```

This command creates a copy of all the files in this project onto your computer. Once this operation is complete, we can then move onto opening the project in IntelliJ. First, go to IntelliJ and go to the Welcome screen by either launching the app or closing all project windows. Next, select *Checkout from Version Control*. In the dropdown, select *GitHub* and select *Password* in the *Auth Type* drop down menu. Enter your login and password credentials using the GitHub user account you gave me at the beginning of this training. Once you have logged in, copy the above URL into the *Git Repository URL* field. Then click *Clone*. You should now have the project cloned to your computer and opened in IntelliJ. You can skip to **Step 3** if you used this alternative method.

**Alternative** If you wish, you can also clone this project using IntelliJ.

## Step 2. I *Really* Like repeating jokes

Let's see who's paying attention. Dustin?

## Step 3. Opening the project in IntelliJ

Opening the project is simple. Select *Open* from the Welcome screen. Next, navigate to the location of the project on your computer and select the directory *lab05*. This should open the project in IntelliJ and you should be ready to run it.

## Step 4. Write Regular Expressions to recognize the following languages

In the project write some code that creates and tests regular expressions to recognize the following languages.

### Language 1. Recognizes all words over the alphabet {a, b} with an even number of a's

This regular expression is write out of my slides regarding Finite State Automata (FSA).

### Language 2. Recognizes all words over the alphabet {a, b} with an odd number of a's

This language results in a very small change in the state machine, but a more complex regular expression. *Hint:* you may need to use the '|' operator to handle the words with only one 'a'.

### Language 3. Recognizes all words over the alphabet (1, 2} where all 1's are followed by at least two 2's.

This one might be pretty easy. You may not even need to draw up a state machine. However, if it's not obvious at first try writing a state machine.

### Language 4. Tokenizes the following traceroute output for Mac OS X

The following traceroute is taken from my home to www.cs.ucsb.edu (It goes through LA?!?!?!?!!!!)on my Mac laptop. What I have in mind is two separate regular expressions. The first to tokenize the lines. The second to tokenize each line into their individual columns. Both will need to handle the special case where ICMP packets are not returned by the router (i.e. `* * *`).  It's OK to drop the first line that starts `traceroute to www.cs.ucsb.edu` for processing the columns.

```bash
traceroute to www.cs.ucsb.edu (128.111.27.13), 64 hops max, 52 byte packets
 1  192.168.127.1 (192.168.127.1)  3.194 ms  1.787 ms  1.852 ms
 2  10.6.144.1 (10.6.144.1)  29.277 ms  14.622 ms  14.468 ms
 3  ip68-4-12-38.oc.oc.cox.net (68.4.12.38)  17.034 ms  14.002 ms  16.251 ms
 4  ip68-4-11-98.oc.oc.cox.net (68.4.11.98)  23.861 ms  25.166 ms  22.373 ms
 5  68.1.1.61 (68.1.1.61)  33.633 ms  34.606 ms  34.931 ms
 6  xe-5-0-1.edge2.losangeles9.level3.net (4.53.230.85)  34.023 ms
    xe-9-0-2.edge2.losangeles9.level3.net (4.53.230.225)  33.962 ms
    xe-7-3-3.edge2.losangeles9.level3.net (4.53.230.73)  16.751 ms
 7  * * *
 8  cenic.ear1.losangeles1.level3.net (4.35.156.66)  29.238 ms  128.859 ms  17.238 ms
 9  ucsb--lax-agg6-10g.cenic.net (137.164.23.91)  17.861 ms  168.860 ms  17.481 ms
10  r2--r1--1.commserv.ucsb.edu (128.111.252.169)  153.407 ms  21.137 ms  151.096 ms
11  574-c--r1.commserv.ucsb.edu (128.111.252.145)  24.069 ms  23.491 ms  20.303 ms
12  556-c-v1071.noc.ucsb.edu (128.111.4.53)  147.382 ms  143.398 ms  27.808 ms
13  drupal2.engr.ucsb.edu (128.111.27.13)  27.904 ms  23.773 ms  20.479 ms
```
