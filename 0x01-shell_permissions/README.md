0. switching the current user to user betty - su betty
1. printing username of current user - whoami
2. printing group he current user is part of - groups
3. changes the owner of the file hello to the user betty - chown betty hello
4. creates an empty file hello - touch hello
5. execute permission to the owner of the file hello - chmod u+x hello
6. Write a script that adds execute permission to the owner and the group owner, and read permission to other users, to the file hello - chmod u+x,g+x,o+r hello
7. Write a script that adds execution permission to the owner, the group owner and the other users, to the file hello - chmod ugo+x hello
8. Write a script that sets the permission to the file hello - chmod 007 hello
9. Write a script that sets the mode of the file hello to this:

-rwxr-x-wx 1 julien julien 23 Sep 20 14:25 hello - chmod 753 hello
10. Write a script that sets the mode of the file hello the same as olleh’s mode.

The file hello will be in the working directory
The file olleh will be in the working directory - chmod --reference=olleh hello

11. Create a script that adds execute permission to all subdirectories of the current directory for the owner, the group owner and all other users. Regular files should not be changed. - chmod ugo+X ./* 

12. Create a script that creates a directory called my_dir with permissions 751 in the working directory. - mkdir -m 751 my_dir

13. Write a script that changes the group owner to school for the file hello

The file hello will be in the working directory - chgrp school hello

14. Write a script that changes the owner to vincent and the group owner to staff for all the files and directories in the working directory. - chown vincent:staff ./*

15. Write a script that changes the owner and the group owner of _hello to vincent and staff respectively.

The file _hello is in the working directory
The file _hello is a symbolic link - chown -h vincent:staff _hello

16. Write a script that changes the owner of the file hello to betty only if it is owned by the user guillaume.

The file hello will be in the working directory - chown --from=guillaume betty hello

17. Write a script that will play the StarWars IV episode in the terminal. - telnet towel.blinkligts.nl 
