## Lab report 4

### **Numbered step starting right after the timer (steps 4-9)** 


**Step 4: Log into ieng6** 

```
ssh cs15lfa23al@ieng6.ucsd.edu
```
  
**Step 5: Clone your fork of the repository from your Github account** 

```
git clone git@github.com:ucsd-cse15l-s23/lab7.git
cd lab7
```

**Step 6: Run the tests, demonstrating that they fail** 

```
javac -cp ".;lib/hamcrest-core-1.3.jar;lib/junit-4.13.2.jar" *.java
java -cp ".;lib/junit-4.13.2.jar;lib/hamcrest-core-1.3.jar" org.junit.runner.JUnitCore ListExamplesTests
```

**Step 7: Edit the code file to fix the failing test** 

```
Vim ListExamples.java
<shift> g
<up><up><up><up><up><up>
w
i
<backspace>
2
<Esc>
:wq
```

**Step 8: Run the tests, demonstrating that they now succeed** 

```
javac -cp ".;lib/hamcrest-core-1.3.jar;lib/junit-4.13.2.jar" *.java
java -cp ".;lib/junit-4.13.2.jar;lib/hamcrest-core-1.3.jar" org.junit.runner.JUnitCore 
```

**Step 9: Commit and push the resulting change to your Github account (you can pick any commit message!)** 

```
git add ListExamples.java
git commit -m "bug fixed"
git push
```