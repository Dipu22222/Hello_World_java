# Running HelloWorld.java Program on CMD

**Name:** Dipu Mondol  
**ID:** IT-24040

## Description

This document explains the step-by-step process to run a simple "Hello, World!" Java program using the Command Prompt (CMD) in Windows. This is the fundamental process every Java programmer needs to know to compile and execute Java programs from the command line.

## Code

```java
public class hello {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

## Steps to Run HelloWorld.java on CMD

### Step 1: Install Java JDK
- Download and install Java Development Kit (JDK) from Oracle's website
- Make sure Java is added to your system's PATH environment variable

### Step 2: Verify Java Installation
Open CMD and type:
```cmd
java -version
```
This should display your Java version. If not, you need to set up PATH correctly.

### Step 3: Create the Java File
- Open Notepad or any text editor
- Copy and paste the code above
- Save the file as `hello.java` (make sure the filename matches the class name)
- Save it in a folder (e.g., `C:\JavaPrograms\`)

### Step 4: Open Command Prompt
- Press `Windows + R`
- Type `cmd` and press Enter
- Or search "Command Prompt" in Windows search

### Step 5: Navigate to the File Location
Use the `cd` command to go to the folder where you saved the file:
```cmd
cd C:\JavaPrograms
```

Or if it's on Desktop:
```cmd
cd Desktop
```

### Step 6: Compile the Java Program
Type the following command and press Enter:
```cmd
javac hello.java
```

**What happens:**
- `javac` is the Java compiler
- It reads the `.java` file
- Creates a `.class` file (bytecode) named `hello.class`
- If there are errors, they will be displayed

### Step 7: Check if Compilation was Successful
Type:
```cmd
dir
```

You should see both:
- `hello.java` (source code)
- `hello.class` (compiled bytecode)

### Step 8: Run the Java Program
Type the following command and press Enter:
```cmd
java hello
```

**Important Notes:**
- Use `java` (not `javac`)
- Use class name without `.class` extension
- Class name is case-sensitive

### Step 9: View the Output
You should see:
```
Hello, World!
```

## Complete CMD Session Example

```cmd
C:\Users\Dipu> cd Desktop
C:\Users\Dipu\Desktop> javac hello.java
C:\Users\Dipu\Desktop> java hello
Hello, World!
C:\Users\Dipu\Desktop>
```

## Summary of Commands

| Step | Command | Purpose |
|------|---------|---------|
| 1 | `java -version` | Check Java installation |
| 2 | `cd folder_path` | Navigate to file location |
| 3 | `dir` | List files in directory |
| 4 | `javac hello.java` | Compile the Java file |
| 5 | `java hello` | Run the compiled program |

## Common Errors and Solutions

### Error 1: "javac is not recognized"
**Solution:** Java JDK is not installed or PATH is not set correctly
- Reinstall JDK
- Add Java bin folder to PATH environment variable

### Error 2: "Could not find or load main class hello"
**Solution:** 
- Make sure you're in the correct directory
- Use the exact class name (case-sensitive)
- Don't add `.class` extension when running

### Error 3: "Class names, 'hello', are only accepted if annotation processing is explicitly requested"
**Solution:**
- File name must match class name exactly
- Save as `hello.java` not `Hello.java`

### Error 4: "Error: Could not find hello.java"
**Solution:**
- Make sure you're in the right directory
- Use `dir` to check if file exists
- Check file extension (should be .java not .txt)

## Key Points to Remember

1. **File name must match class name** (hello.java for class hello)
2. **Use `javac` to compile** → creates .class file
3. **Use `java` to run** → executes the program
4. **Don't add .class when running** → `java hello` not `java hello.class`
5. **Make sure you're in the correct directory** → use `cd` command
6. **Java is case-sensitive** → Hello and hello are different

## What Happens Behind the Scenes

1. **Source Code (hello.java)**
   - Human-readable Java code
   - Written by programmer

2. **Compilation (javac)**
   - Converts .java to .class
   - Checks for syntax errors
   - Creates bytecode

3. **Bytecode (hello.class)**
   - Platform-independent code
   - Can run on any system with JVM

4. **Execution (java)**
   - Java Virtual Machine (JVM) reads bytecode
   - Converts to machine code
   - Runs the program
   - Shows output

## Flowchart

```
Write Code (hello.java)
         ↓
Save File
         ↓
Open CMD
         ↓
Navigate to folder (cd)
         ↓
Compile (javac hello.java)
         ↓
Success? → No → Fix errors
    ↓ Yes
Run (java hello)
         ↓
See Output: Hello, World!
```
