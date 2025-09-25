# Design Document: [PRoject_1: LBS to KG]

**Author:** [Anthony HArbin]
**Date:** September 24, 2025

## 1. Summary (TL;DR)

to start an EC2 instance and make it convert lbs to kg


## 2. Goals

*   [Get an EC2 instance running on AWS]
*   [SSH into the instance from a Ubuntu terminal(personal choice)]
*   [Run a program that converts lbs to kg and print the output]



## 3. Proposed Solution

Follow provided guide in order to complete project.

### 4.  Architecture

1-User would input a series of CLI in order to SSH to the instance

2-Afterwards the user will input the code required for setting up the node server and convert lbs to kg

3A-In a second terminal and give a CLI " curl "http://localhost:8080/convert?lbs=150" " so that it converts
3B-THough it was suppose to be able to work with CLI " 'http://<PUBLIC_IP>:8080/convert?lbs=150' ", but for some reason it never worked. 

4-Run it as a service using provided CLI commands.

5-Clean it up by terminatiting the instance.


## 5. Alternatives Considered
Considered using an Ubuntu VM instead of just Ubuntu terminal, as I believe that may have
  been causing an issue with with the key being used but not in its "true" memory.
  Unfortunately I came to that idea a bit too late, and I am having trouble getting the VM to work.
