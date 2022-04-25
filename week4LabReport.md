# Week 4 Lab Report

> Due April 24, 2022 <br>
**Topic:** Debugging

---
# **Code Changes:**

## Code Change **#1**

* Code Diff

    ![Image](Images\codeChange1.png)

* Fixed Test Files: [test 2](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-file2.md), [test 3](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-file3.md), [test 4](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-file4.md), [test 7](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-file7.md), [test 8](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-file8.md).

* Symptom Example:

    ![Image](Images\testSymptom1.png)

* The code hadn't accounted for infinite while loops, which resulted in a bug that caused out of memory errors by looping infinitely as its symptom. The fail-inducing input of test-file2, in particular, caused an infinite loop, because whenever the index of a bracket was -1 (meaning it wasn't found), it would still continue as if a bracket was found.

&nbsp;
## Code Change **#2**

* Code Diff

    ![Image](Images\codeChange2.png)

* Fixed Test Files: [test 6](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-file6.md).

* Symptom Example:

   ![Image](Images\testSymptom2.png)

* There was a bug that resulted in the code accepting image links, hence `page.com` was returned as a symptom, even though it was formatted as an image link in test-file6.

&nbsp;
## Code Change **#3**

* Code Diff

    ![Image](Images\codeChange3.png)

* Fixed Test Files: [test 5](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-file5.md).

* Symptom Example:

   ![Image](Images\testSymptom3.png)

* There was a bug that allowed false links to be returned even though the syntax wasn't proper. This resulted in the symptom of `getLinks()` retrieving `page.com` even though the syntax for it wasn't correct (the parenthesis are supposed to be right next to square brackets: `[]`)