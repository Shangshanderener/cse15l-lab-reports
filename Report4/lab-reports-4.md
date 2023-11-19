## Lab report 4

### **Numbered step starting right after the timer (steps 4-9)** 


**Step 4: Log into ieng6** 

![Image](png/s4.png)

```
ssh cs15lfa23al@ieng6.ucsd.edu <enter>
```

- ssh: a protocol used to securely access a remote server.
- cs15lfa23al@ieng6.ucsd.edu: The username and hostname of the server I'm trying to connecting to.
  
**Step 5: Clone your fork of the repository from your Github account** 

![Image](png/s5.png)

```
git clone git@github.com:Shangshanderener/lab7.git <enter>
cd lab7/ <enter>
```

- git clone: Command to copy a Git repository from a remote source (in this case, GitHub).
- git@github.com:Shangshanderener/lab7.git: The URL of the Git repository.
- cd lab7/: Change directory to the new cloned repository.

**Step 6: Run the tests, demonstrating that they fail** 

![Image](png/s6.png)

```
javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java <enter>
java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests <enter>
```

- javac: Java compiler command to compile Java source files.
- cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar: Specifies the classpath for the compilation, including required external libraries.
- *.java: Compiles all Java files in the current directory.
- java: Java interpreter command to run a Java program.
- org.junit.runner.JUnitCore ListExamplesTests: Runs JUnit tests on ListExamplesTests.

**Step 7: Edit the code file to fix the failing test** 

![Image](png/s7.png)

```
vim ListExamples.java <enter>
<shift> g
<up><up><up><up><up><up>
2w
i
<left>
<backspace>
2
<Esc>
:wq <enter>
```

- vim ListExamples.java: Opens the Vim text editor for editing the specified file.
- shift g: Jumps to the end of the file.
- up * 6: Moves the cursor up 6 lines.
- 2w: Moves the cursor two words forward.
- i: Change to insert mode to start editing.
- left: Moves the cursor one character to the left.
- backspace: Deletes the character to the left.
- 2: Inserts the number 2.
- Esc: Exits insert mode.
- :wq: Save changes to the file and quits Vim.

**Step 8: Run the tests, demonstrating that they now succeed** 

![Image](png/s8.png)

```
<up><up><up><enter>
javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java <enter>
<up><up><up><enter>
java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests <enter>
```

- up up up: Uses command history to repeat the previous commands.
- Rest are same as step 6


**Step 9: Commit and push the resulting change to your Github account (you can pick any commit message!)** 

![Image](png/s9.png)

```
git add ListExamples.java <enter>
git commit -m "bug fixed" <enter>
git push <enter>
```

- git add ListExamples.java: Adds the modified file ListExamples.java to the staging area.
- git commit -m "bug fixed": Commits the changes with a commit message.
- git push: Pushes the committed changes to the remote repository on GitHub.