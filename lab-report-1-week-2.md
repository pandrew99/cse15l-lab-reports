# Lab Report 1 Week 2
`Mac Edition`
### By: Andrew Pan

## 1. Installing VScode
- Download VS Code [here](https://code.visualstudio.com/download).
- Open the downloaded link and follow the instructions on screen to successfully install VS Code.
- Open VS Code to get started! ![VSCode](VSCode.png)
## 2. Remotely Connecting
- Lookup your UCSD account info [here](https://sdacs.ucsd.edu/~icc/index.php). 
- Enter your credentials, and then find your cse15l account info under `Additional Accounts` which looks like with `cs15lwi22amm` with `wi22` replaced by the term you're taking the course, and `amm` with your specific username. ![Account lookup](AccountLookup.png)
- Then, you have to reset your password by going to the `Change Your Password` hyperlink. Enter your current password, and a new, complicated password following the guidelines on the website. When you're at the last field to `confirm password` press enter on your keyboard. If you get to a screen that says success! or a blank screen, your password was successfully changed. You will use that usernmae and password in the following steps. 
- Next, go back to VS Code and open a new terminal by the menu bar - terminal - new terminal. Run the command ```ssh cs15lwi22amm@ieng6.ucsd.edu``` with your term and username. Say yes that you agree, enter your password, and now you're connected to a computer in the CSE basement! 
## 3. Trying Some Commands
- Now, you're able to run some commands from the terminal that run on the computer in the basement! 
- Here are some to try: `cd`, `ls -a`, `cp /home/linux/ieng6/cs15lwi22/public/hello.txt ~/`
- When you are done, you can logout of the server by typing exit in the terminal, or using `Control D` on your keyboard.
- `ls` lists current elements of directory![](ls.png)
## 4. Moving Files with scp
- In VSCode, logged into your computer, make a new file called `WhereAmI.java` with the following content:
    ```
    class WhereAmI {
        public static void main(String[] args) {
            System.out.println(System.getProperty("os.name"));
            System.out.println(System.getProperty("user.name"));
            System.out.println(System.getProperty("user.home"));
            System.out.println(System.getProperty("user.dir"));
            }
    }
    ```
- Then, from the terminal run the command `scp WhereAmI.java cs15lwi22amm@ieng6.ucsd.edu:~/` with your term and username. Enter your password, and now you successfully copied a file to the server! 
- You can run the command using `javac WhereAmI.java` and then `java WhereAmI` and it should print the details of the Linux computer that's in the CSE basement, which is the server you're connected to. ![scp](scp.png)
## 5. Setting an SSH Key
- Exit the server, and then on your computer type `ssh-keygen` into the terminal. 
- Press enter when it says what file to save the key, as well as the passphrase and passphrase again to make it as easy as possible. 
- Then `ssh cs15lwi22zz@ieng6.ucsd.edu` again, enter your password, and type in the command `mkdir .ssh`. Afterwards, you can logout by typing `exit` or `Control D`.
- Then, type in the command `scp /Users/andrewpan/.ssh/id_rsa.pub cs15lwi22amm@ieng6.ucsd.edu:~/.ssh/authorized_keys` with andrewpan replaced with your username on your computer, as well as the username for your account. Enter your password. 
- Then try ssh'ing again, `ssh cs15lwizzamm@ieng6.ucsd.edu`
- Now you're good! You don't have to enter your password every time :)![keys](keys.png)
## 6. Optimizing Remote Running
- To make remote running faster on the server, there are several tips and tricks to optimize your workflow and efficiency.
- You can ssh onto the remote computer, and put commands after the ssh in "" to run the command, and then immediately exit the server. ![quotes](quotes.png)
- You can run multiple commands at the same time by using ;
- Finally, here's a pic of Joe! 
![Joe](a.png)
- Thanks for following along and hope this tutorial was helpful! Have a nice day :)