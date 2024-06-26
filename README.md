# Push-Swap

## Table of Contents

- [Description](#description)
- [Usage](#usage)
- [Implementation](#implementation-details)
- [Contributing](#contributing)

## Description

Push-Swap is a project that uses a Non-Comparative Sorting Algorithm to sort stacks. 

There are two programs: 
- push-swap, which calculates and displays on the standard output the smallest program using push-swap instruction language that sorts integer arguments received.

- checker, which takes integer arguments and reads instructions on the standard input. Once read, checker executes them and displays OK if integers are sorted. Otherwise, it will display KO.

## Usage

1. Clone the repository "https://learn.reboot01.com/git/araed/push-swap.git" 
2. To try the push-swap program run the following command : [ go run . "1 3 4" ] where numbers are separated by a space
3. Note : To try for 100 random elements between -100 and 100 run the following:

- ```sh
   numbers=$(seq -100 100 | shuf -n 100 | tr '\n' ' ' | sed 's/[[:space:]]*$//')
- ```sh 
  $ go run . "$numbers"

4. To try the checker program, navigate to checker directory then run "go run [1 3 4]" and enter the instruction one by one each followed by a new line 
or follow these steps:

- run the command "go build checker.go" after navigating to checker directory

- use this command format 

- ```sh 
  echo -e "rra\npb\nsa\nrra\npa" | ./checker "3 2 1 0""

## Contributing
  - Zahraa Fadhel "zfadhel"
  - Ammena Raed "araed"
  - Sara Abdulla "sabdulla"

## Implementation Details

- sa/sb: Swap the top two elements of stack A/B.
- ss: Perform sa and sb simultaneously.
- pa/pb: Push the top element of stack A/B to the top of stack B/A.
- ra/rb: Rotate the stack A/B in a clockwise direction (the top element becomes the bottom).
- rr: Perform ra and rb simultaneously.
- rra/rrb: Rotate the stack A/B in an anticlockwise direction (the bottom element becomes the top).
- rrr: Perform rra and rrb simultaneously.