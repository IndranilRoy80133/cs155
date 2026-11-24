# CS 155 — Programming in Java: Course Map

An interactive study site for **CS 155** at Southeast Missouri State University. It follows chapters 1–10 of Y. Daniel Liang, *Introduction to Java Programming and Data Structures*.

The course is drawn as a transit map: ten stops on five colour-coded lines. Each stop has:

- **A Java lab** that runs in the browser, with example programs students can edit and re-run
- **Notes** keyed to the matching Liang chapter
- **A three-question quiz** with explanations

**Live site:** https://indranilroy80133.github.io/cs155/

## The ten stops

| Stop | Topic (Liang ch.) | What the lab shows |
|---|---|---|
| 1 | Introduction to Computers, Programs, and Java | The edit → compile (`javac`) → bytecode → JVM chain. Example programs show syntax, file-name, runtime and logic errors. |
| 2 | Elementary Programming | A "What type is it?" explorer that evaluates expressions step by step with each step's type (`int`, `double`, `char`, `String`), plus programs that read input with `Scanner` |
| 3 | Selections | Which lines ran for a given input (leap year, letter grade, BMI, Chinese zodiac, missing `break`, stray semicolon) |
| 4 | Mathematical Functions, Characters, and Strings | A String explorer for `charAt`, `substring`, `indexOf`, `compareTo` and others, Unicode details for any character, plus `printf` and `Math` examples |
| 5 | Loops | A step-through debugger with a trace table that fills in one statement at a time |
| 6 | Methods | The call stack, frame by frame: pass-by-value (`swap`), overloading, modular code, recursion, scope errors |
| 7 | Single-Dimensional Arrays | Arrays drawn as boxes, with markers for `i`, `j`, `low`, `mid` and `high`: linear and binary search, selection sort, copying, off-by-one errors |
| 8 | Multidimensional Arrays | 2D arrays drawn as grids with the current `[row][col]` highlighted: column sums, grading an exam, ragged arrays |
| 9 | Objects and Classes | Objects and references in memory, `static` fields, garbage, `null`, `private` fields, plus a UML class diagram drawn from the code |
| 10 | Object-Oriented Thinking | Class abstraction (BMI), aggregation (Course), StackOfIntegers, String immutability vs StringBuilder, wrapper classes |

## Using the site

- Pick a stop on the map, or use the line of stations at the top of every page.
- In a lab, choose an example, then click **Compile & run**. Edits re-run automatically.
- In step-through labs, use **Step →**, **← Back** or the slider to move through the program one statement at a time.
- Where a program reads from the keyboard, type the input in the **Keyboard input** box, one value per line, or click one of the **Try** buttons.
- Quiz scores are saved in your own browser only. Nothing is sent anywhere.

## How it works

The whole site is a single self-contained file, `index.html`, with no build step and no server. The only thing it loads from the web is the Figtree font from Google Fonts.

The labs run a **teaching interpreter for a subset of Java**, written in JavaScript. It covers everything in chapters 1–10:

- primitive types with Java's own integer division, overflow and casting rules
- `String`, `StringBuilder`, `Math`, `Character`, `Integer`, `Double`, `Arrays`, `Scanner` and `Random`
- `if`, `switch`, all three loops, `break` and `continue`
- static and instance methods, overloading and recursion
- 1D, 2D and ragged arrays
- classes with constructors, `this(...)`, static fields and `private` access

It reports compile errors and exceptions in the same style as the JDK, for example `';' expected`, `incompatible types: possible lossy conversion from double to int` and `ArrayIndexOutOfBoundsException: Index 5 out of bounds for length 5`.

It is **not** the real JDK. It does not support inheritance, interfaces, generics, `ArrayList` or other material from chapter 11 onward. Students should compile and test their assignments with `javac`.

## Hosting on GitHub Pages

1. Put `index.html` and this `README.md` in the root of the repository.
2. Go to **Settings → Pages**. Set **Source** to *Deploy from a branch*, choose `main` and `/ (root)`, and click **Save**.
3. After a minute or two the site is live at `https://indranilroy80133.github.io/<repository-name>/`.

To update the site, replace `index.html` and commit. GitHub Pages redeploys automatically.

## Running locally

Open `index.html` in any modern browser (Chrome, Edge, Firefox, Safari). Nothing needs to be installed.

## Author

Dr. Indranil (Neel) Roy, Department of Computer Science, Southeast Missouri State University — iroy@semo.edu

## Copyright and license

© 2026 Indranil Roy.

This project uses two licenses: one for the software and one for the teaching material.

| Part | License | What it covers |
|---|---|---|
| **Code** | [MIT License](LICENSE) | The JavaScript, HTML and CSS that make up the site: the Java teaching interpreter, the step-through debugger, the memory and trace views, the course map and the quiz engine |
| **Teaching content** | [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/) | The notes, quiz questions and explanations, lab descriptions, and original example programs |

Under **CC BY-NC-SA 4.0** you may share and adapt the teaching content, for example for your own course, as long as you:

- **give credit:** "CS 155 Java Course Map by Indranil Roy, Southeast Missouri State University," with a link to this repository
- **don't use it commercially**
- **share any adaptations under the same license**

Under the **MIT License** you may reuse, modify and redistribute the code freely, provided the copyright notice and license text are kept.

**Not covered by these licenses:** example programs adapted from Liang's textbook (see below) remain the property of their copyright holder. They are not offered under either license.

**Textbook acknowledgement.** The chapter order and topic coverage follow *Introduction to Java Programming and Data Structures* by Y. Daniel Liang, published by Pearson Education. The textbook is © Pearson Education. Some short example programs (for example TestMax, LinearSearch, SelectionSort, GradeExam, TestCircle, BMI, Course and StackOfIntegers) are adapted from the book's code listings for classroom teaching. This site is not affiliated with or endorsed by the author or the publisher. Students should use the textbook as the primary reference.

"Java" is a registered trademark of Oracle and/or its affiliates.
