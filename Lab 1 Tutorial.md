# Remote Connection tutorial (Windows)
Steps:
1. Finding account information needed for remote log in
  * Look up account "CSE15L" [here](https://sdacs.ucsd.edu/~icc/index.php)
  * Log in using normal school username and Student ID
  * Make sure to follow [tutorial](https://drive.google.com/file/d/17IDZn8Qq7Q0RkYMxdiIR0o6HJ3B5YqSW/view) to reset your password for the "CSE15L" account
  * Remember "CSE15L" user name and password you set
2. Download [Visual Studio Code](https://code.visualstudio.com/)
  * Follow the link above and click on download
  * Wait until download finishes dowloading and click on it once it is finished downloading
  * Follow the directionos to set it up
  * Should look like as below when set up properly and opened
  ![Once set up should look like](https://ucsd-cse15l-s23.github.io/images/vscode.png)
3. Dowload Git 
  * follow this [link](https://gitforwindows.org/)
  * Click download (for Windows)
  * Properly set up with your prefrences
5. Logging in to the remote connection
  * Open up Visual Studio Code
  * Click the terminal button on the top left of cornere of the screen and open a new terminal (Example below)
    ![example](https://user-images.githubusercontent.com/130005453/231017651-83bb093b-ae0d-402f-9051-df2c71ed9dab.png)
  * Click the drop down icon in between the plus icon and the two rectangles icon
  * Once the open click the Git Bash option on the list (if git isn't properly installed the option will not show up)
    ![image](https://user-images.githubusercontent.com/130005453/231017936-f386ae59-f350-4272-857b-773ecc4339e2.png)
  * In the command line put in "ssh " + the username you looked up earlier + "@ieng6.ucsd.edu" (Example below)
  ![image](https://user-images.githubusercontent.com/130005453/231018880-f84d8917-e4e5-4a14-9c4d-b70d0b25bd6a.png)
  * You don't need to type the "$" because that just means the command line
  * (If first time using remote connect) Something like below will pop up and all you simply need to do is type in yes
  ![image](https://user-images.githubusercontent.com/130005453/231019266-51ffacb4-2a79-4ef0-8e89-754aea4fa6d5.png)
  * After accepting, type in the password to the "CS15l" account (note: even if you do type in the password it will not visually appear so make sure to get spelling and capitilization correct without needing to see it)
  * If correct password inputed will look similar to the following terminal
  ![image](https://user-images.githubusercontent.com/130005453/231020145-750dda06-2185-43b8-b2a9-3c50f20ff889.png)
6. Try some commands
  * Some useful commands for starting are: 
    `cd ~` 
    `cd` 
    `ls -lat` 
    `ls -a` 
    `ls`
  * Some code examples that were tried showed as follows:
  ![image](https://user-images.githubusercontent.com/130005453/231022238-fbac159e-7762-4b33-9210-2f7e0bcb41bd.png)
7. When done exit the remote servers
  * Can be done by pressing `Ctrl and D`
  * An alternative is typing `exit` into the command line
