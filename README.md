# README
Please make a note of which project option you have chosen in this `README.md` file.

For each option, you must enter answers to questions in this `README.md` file,
as well as add any configuration files or scripts you wrote for the assignment to this repository. 

#### Good Luck

I will be completing Option B: Shell Scripting.

2: Command substitution allows you to execute a command that has the output of that command replace the text of the command. for example:
- echo "The file <hello.txt> contains: $(cat hello.txt)"
- echo "The directory you are currently in is: $(pwd)"

3:
a. Paused and background jobs will recieve a SIGHUP signal which will terminate all processes that dont have a "nohup"(dont recieve SIGHUP signals) configuration.

b. disown is used if you forgot to run a process with the "nohup" command. Running "disown" will configure the file to be a "nohup" file and continue to run on log out.

c. The wait command will wait for the process to be finished before finishing the rest of the script. some examples are:
    1.  ./my_file &
        PID=$!
        echo "my_file is running in the background. PID:
        $PID"
        wait $PID
        echo "process finished for my_file moving along"
    2.  echo "now we will wait for 10 seconds"
        sleep 10 &
        wait
        echo "Congratulations you just wasted 10 seconds of your precious time"
4:
    1. I can redirect the contents of standard outputs from display to a file by writing "ls > my_file.txt"
    2. I learned that I can do math straight in the terminal with "echo 2+2=$((2+2))"
    3. With a command like "mkdir {2017..2019}-{01..12}" I can make a folder for every month of the years 2017-2019.
    4. using "\a" will make the terminal beep which I thought is funny and can be useful for annoying people.
    5. running a command with the & symbol like: "command &" will put the process in the background.
    6. the ps command helps get the PID and we can use "ps x | grep my_program" to do so.
    7. With the PID we can run commands like "kill -SIGKILL PID#" which will immediately teminate the process by the linux kernel.
    8. The command "chgrp" changes the group ownership of a file for the read write and execute commands. for example like "chgrp new_group my_file"
    9. I can use "chmod 760" to change the permision on a file which will be "rwx" for the owner, "rw-" for the group and "---" for the other which all together looks like "rwx rw- ---"
    10. I can use "[[:upper:]]*" to grab all filenames that begin with an uppercase letter.
