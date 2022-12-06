### shell variable expansion
**tasks 0**

##Create a script that creates an alias.
Name: ls
Value: rm *

**answer**
alias ls="rm *"

**1. Hello you**
##Create a script that prints hello user, where user is the current Linux user.

**answer**
echo "hello $USER"

**2. The path to success is to take massive, determined action**
##Add /action to the PATH. /action should be the last directory the shell looks into when looking for a program

**answer**
export PATH=$PATH:/action
