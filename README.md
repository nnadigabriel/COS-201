# COS-201
COS 201 Computer Programming Assignments 
<!-- COVER PAGE -->

<div class="cover">
  <h1>COS 201 – Computer Programming I</h1>
  <p style="font-size:14pt; font-weight:bold; color:#0b3d6b;">Practical Assignments (Weeks 1–3)</p>
  <br>
  <p><strong>Student Name:</strong> Nnadi Gabriel Ugochukwu</p>
  <p><strong>Matriculation Number:</strong> 25/18103</p>
  <p><strong>Programme:</strong> Software Engineering (SEN)</p>
  <p><strong>Course:</strong> COS 201 – Computer Programming I</p>
</div>

<!-- WEEK 1 -->

<h2>Week 1 Practical: Introduction to Programming &amp; Problem Solving</h2>

<h3>Problem Statement</h3>

<p>Write a Java program that introduces the student, their programme of study, and explains why programming matters to a Software Engineering student.</p>

<h3>Algorithm</h3>

<ol>
  <li>Start the program.</li>
  <li>Print the course code and title.</li>
  <li>Print the programme of study.</li>
  <li>Print three reasons programming is relevant.</li>
  <li>Print one personal learning goal.</li>
  <li>End the program.</li>
</ol>

<h3>Pseudocode</h3>

<pre>BEGIN
  DISPLAY "Course: COS 201 - Computer Programming I"
  DISPLAY "Programme: Software Engineering"
  DISPLAY "1. Programming builds logical problem-solving skills."
  DISPLAY "2. Programming turns ideas into usable software."
  DISPLAY "3. Programming is the foundation of software engineering."
  DISPLAY "Goal: Build a small working application by end of semester."
END</pre>

<h3>Java Source: week01/FirstProgram.java</h3>

<pre>/*
 * COS 201 - Computer Programming I
 * Week 1 Practical: Introduction to Programming
 * Nnadi Gabriel Ugochokwu | 25/18103 | Software Engineering
 */
public class FirstProgram {
    public static void main(String[] args) {
        System.out.println("Course: COS 201 - Computer Programming I");
        System.out.println("Programme: Software Engineering");
        System.out.println();
        System.out.println("Why programming matters:");
        System.out.println("1. Programming builds logical problem-solving skills.");
        System.out.println("2. Programming turns ideas into usable software.");
        System.out.println("3. Programming is the foundation of software engineering.");
        System.out.println();
        System.out.println("Goal: Build a small working application by end of semester.");
    }
}</pre>

<h3>Expected Output</h3>

<pre>&gt; javac FirstProgram.java
&gt; java FirstProgram

Course: COS 201 - Computer Programming I
Programme: Software Engineering

Why programming matters:
1. Programming builds logical problem-solving skills.
2. Programming turns ideas into usable software.
3. Programming is the foundation of software engineering.

Goal: Build a small working application by end of semester.</pre>

<h3>README.md (Week 1 extract)</h3>

<pre># COS 201 – Computer Programming I

**Student:** Nnadi Gabriel Ugochukwu
**Matric:** 25/18103
**Programme:** Software Engineering

## Week 1 – Introduction to Programming
- Wrote and ran a Java program that prints introductory details.
- Practised the class/main method structure, print statements, and compiling with `javac`.

**File:** `week01/FirstProgram.java`</pre>

<!-- WEEK 2 -->

<div class="page-break"></div>
<h2>Week 2 Practical: Setting Up the Development Environment</h2>

<h3>Objective</h3>

<p>Configure a working Java environment, then write and run a first "Hello World" program to confirm the setup is correct.</p>

<h3>Environment Setup</h3>

<table>
  <tr><th>Tool</th><th>Purpose</th></tr>
  <tr><td>JDK (Java Development Kit)</td><td>Compiles and runs Java code</td></tr>
  <tr><td>VS Code</td><td>Code editor for writing Java source files</td></tr>
  <tr><td>Git &amp; GitHub</td><td>Version control and submission</td></tr>
</table>

<h3>Java Source: week02/HelloWorld.java</h3>

<pre>/*
 * COS 201 - Computer Programming I
 * Week 2 Practical: Hello World
 * Nnadi Gabriel Ugochukwu | 25/18103 | Software Engineering
 */
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
        System.out.println("This is my first program in COS 201.");

        String course = "COS 201";
        String title  = "Computer Programming I";
        String prog   = "Software Engineering";

        System.out.println("Course: " + course + " - " + title);
        System.out.println("Programme: " + prog);
    }
}</pre>

<h3>Expected Output</h3>

<pre>&gt; javac HelloWorld.java
&gt; java HelloWorld

Hello, World!
This is my first program in COS 201.
Course: COS 201 - Computer Programming I
Programme: Software Engineering</pre>

<h3>README.md (Week 2 extract)</h3>

<pre>## Week 2 – Development Environment
**Tools:** JDK, VS Code, Git, GitHub

**Steps taken**
1. Installed the JDK and confirmed with `java -version`.
2. Wrote `HelloWorld.java` in VS Code.
3. Compiled with `javac HelloWorld.java`.
4. Ran with `java HelloWorld`.

**File:** `week02/HelloWorld.java`

**Outcome:** Environment is working correctly; program compiled and ran without errors.</pre>

<!-- WEEK 3 -->

<div class="page-break"></div>
<h2>Week 3 Practical: Variables, Data Types, Expressions &amp; Input/Output</h2>

<h3>Overview</h3>

<p>Three short programs applying variables, arithmetic expressions, the <code>Scanner</code> class, and formatted output.</p>

<h3>Program 1 — Simple Calculator</h3>

<pre>/*
 * COS 201 - Computer Programming I
 * Week 3 Practical 1: Simple Calculator
 * Nnadi Gabriel Ugochukwu | 25/18103 | Software Engineering
 */
import java.util.Scanner;

public class SimpleCalculator {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);

        System.out.print("First number: ");
        double a = in.nextDouble();
        System.out.print("Second number: ");
        double b = in.nextDouble();

        double sum  = a + b;
        double diff = a - b;
        double prod = a * b;

        System.out.println("\nResults");
        System.out.printf("  Sum        = %.2f%n", sum);
        System.out.printf("  Difference = %.2f%n", diff);
        System.out.printf("  Product    = %.2f%n", prod);

        if (b == 0) {
            System.out.println("  Quotient   = cannot divide by zero");
        } else {
            System.out.printf("  Quotient   = %.2f%n", a / b);
        }

        in.close();
    }
}</pre>

<h3>Sample Run</h3>

<pre>First number: 20
Second number: 4

Results
  Sum        = 24.00
  Difference = 16.00
  Product    = 80.00
  Quotient   = 5.00</pre>

<h3>Program 2 — Student Average Calculator</h3>

<pre>/*
 * COS 201 - Computer Programming I
 * Week 3 Practical 2: Student Average Calculator
 * Nnadi Gabriel Ugochukwu | 25/18103 | Software Engineering
 */
import java.util.Scanner;

public class AverageCalculator {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);

        System.out.print("Student name: ");
        String name = in.nextLine();

        System.out.print("Course 1 score: ");
        double c1 = in.nextDouble();
        System.out.print("Course 2 score: ");
        double c2 = in.nextDouble();
        System.out.print("Course 3 score: ");
        double c3 = in.nextDouble();

        if (c1 < 0 || c1 > 100 || c2 < 0 || c2 > 100 || c3 < 0 || c3 > 100) {
            System.out.println("Invalid input: scores must be between 0 and 100.");
            in.close();
            return;
        }

        double total = c1 + c2 + c3;
        double avg   = total / 3;

        System.out.println("\nResult for " + name);
        System.out.printf("  Total   = %.2f%n", total);
        System.out.printf("  Average = %.2f%n", avg);

        in.close();
    }
}</pre>

<h3>Sample Run</h3>

<pre>Student name: Nnadi Gabriel
Course 1 score: 70
Course 2 score: 80
Course 3 score: 90

Result for Nnadi Gabriel
  Total   = 240.00
  Average = 80.00</pre>

<h3>Program 3 — Item Cost Calculator</h3>

<pre>/*
 * COS 201 - Computer Programming I
 * Week 3 Practical 3: Item Cost Calculator
 * Nnadi Gabriel Ugochukwu | 25/18103 | Software Engineering
 */
import java.util.Scanner;

public class ItemCost {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);

        System.out.print("Item name: ");
        String item = in.nextLine();
        System.out.print("Quantity: ");
        int qty = in.nextInt();
        System.out.print("Unit price: ");
        double price = in.nextDouble();

        double total = qty * price;

        System.out.println("\nPurchase Summary");
        System.out.println("  Item       : " + item);
        System.out.println("  Quantity   : " + qty);
        System.out.printf("  Unit price : %.2f%n", price);
        System.out.printf("  Total cost : %.2f%n", total);

        in.close();
    }
}</pre>

<h3>Sample Run</h3>

<pre>Item name: Exercise Book
Quantity: 3
Unit price: 1500

Purchase Summary
  Item       : Exercise Book
  Quantity   : 3
  Unit price : 1500.00
  Total cost : 4500.00</pre>

<!-- REPO STRUCTURE + SUBMISSION -->

<div class="page-break"></div>
<h2>Repository Structure</h2>
<pre>COS201-Programming-I/
├── README.md
├── week01/
│   └── FirstProgram.java
├── week02/
│   └── HelloWorld.java
└── week03/
    ├── SimpleCalculator.java
    ├── AverageCalculator.java
    └── ItemCost.java</pre>

<h2>Submission Note</h2>

<div class="note">
<strong>COS 201 – Practical Submission (Weeks 1–3)</strong>
</div>
<p>Dear Lecturer,</p>
<p>Please find my practical work for COS 201 – Computer Programming I below.</p>
<table>
  <tr><th>Field</th><th>Details</th></tr>
  <tr><td>Student Name</td><td>Nnadi Gabriel Ugochukwu</td></tr>
  <tr><td>Matriculation Number</td><td>25/18103</td></tr>
  <tr><td>Programme</td><td>Software Engineering</td></tr>
  <tr><td>Assignments Covered</td><td>Week 1 (Introduction to Programming), Week 2 (Development Environment &amp; Hello World), Week 3 (Variables, Data Types, Expressions and I/O)</td></tr>
  <tr><td>GitHub Repository URL</td><td>[Insert actual repository URL here]</td></tr>
</table>
<p>The repository contains all source files for the three weeks along with a README detailing objectives, setup steps, and how to compile/run each program. All programs have been compiled and tested successfully.</p>
<p>Thank you.</p>

<footer>
  COS 201 – Computer Programming I &nbsp;|&nbsp; Nnadi Gabriel Ugochukwu &nbsp;|&nbsp; 25/18103
</footer>

</body>
</html>
