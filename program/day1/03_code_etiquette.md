[Overview](./00_overview.md) |
[The Tools](./01_tools.md) |
[Project Setup](./02_project_setup.md) |
[Reproducibility](./03_reproducibility.md) |
[Code Etiquette](./04_code_etiquette.md)

# Good Code Etiquette

## Readability

> "Programs must be written for people to read, and only incidentally for machines to execute." - Harold Abelson, Structure and Interpretation of Computer Programs

As a data scientist you will spend a lot of time writing and reading code and deciphering error messages (i.e. debugging). To help with making this efficient and reproducible program language communities have style guides. These provide consistency on how to format code, naming conventions and creating readable code. For Python you should follow the PEP 8 Style Guide<sup><a id="a6">[6](#f6)</a></sup>. A good coding style will also help with optimising code.

<b id="f6">PEP 8:</b> [PEP-8 - Style Guide for Python Code](https://www.python.org/dev/peps/pep-0008/) [↩](#a6)

## Programming Rules of Thumb<sup><a id="a7">[7](#f7)</a></sup>

1. K.I.S.S. (Keep It Simple, Stupid)

  * Subprograms should do precisely ONE conceptual task and no more.
  * If a problem can be decomposed into two or more independently solvable problems, do so.

2. Rule of Three

  * When you copy/paste a piece of code 3 or more times turn it into a function.

3. 90-90 rule (failure to anticipate the hard parts)

    > "The first 90 percent of the code accounts for the first 90 percent of the development time. The remaining 10 percent of the code accounts for the other 90 percent of the development time." - Tom Cargill, Bell Labs

4. Efficiency vs clarity (chasing false efficiency)

  * Never sacrifice clarity for some perceived efficiency.

5. Naming of things

  * Naming conventions are there to make code easier to read

<b id="f7">Rules of Thumb:</b> [wou.edu/las/cs/csclasses/cs161/Lectures/rulesofthumb.html](https://wou.edu/las/cs/csclasses/cs161/Lectures/rulesofthumb.html) [↩](#a7)

##  Documentation

We’ve mentioned documentation several times throughout this summary. It does take time to document well, however, it will make future work easier as someone else should be able to follow your steps without having to ask you directly. More importantly, documenting and commenting your code will make your work easier as it acts as a reminder to what you were thinking months ago when you wrote the code. Documentation is for people using the code and describes how to run it and what the results will/should be.

Comments are for people reading the code (ie developers and future you) and help with understanding why certain decisions were (e.g. a link to a stackoverflow article describing an algorithm) and how the code works.

## Testing Code

>. "Finding your bug is a process of confirming the many things that you believe are true - until you find one which is not true."- Norm Matloff

Testing encompasses whatever you currently do to convince yourself that your code works. However, to help you with reproducibility and maintainability of your code this process should be made explicit by writing test code. Basically every time you find a bug or a corner case in your code write a test (i.e. a piece of code) that will check it.

To help you with getting in the right mindset from the beginning, consider writing both documentation and test code as part of your development process:

1. Write the function definition and basic docstring<sup><a id="a8">[8](#f8)</a></sup>.
2. Write the function contents, i.e. the actual code.
3. Write a test to ensure that the function does what the docstring claims.
4. Update code and/or docstring until (3) is true.

Testing in Python: https://docs.python-guide.org/writing/tests/

## Optimisation
Premature optimisation should be avoided. Knowing when to optimise is as important as knowing how! Consider the following:

1. Do not optimise unless you have to (your time is the most precious)
2. Optimise for readability (imagine very cranky future developers, and reduce their cognitive load)
3. Variety of optimisations
  * Readability
  * Usability
  * Performance
  * Memory
  * Lines of code (code-golf)
4. Remember, every line of code is a potential source of  bugs, and future maintenance headaches. Choose wisely!

<b id="f8">Docstrings:</b> In Python, triple quoted text immediately after a class or function definition is a docstring. Have a look at the [`numpydoc` docstring guide](https://numpydoc.readthedocs.io/en/latest/format.html). [↩](#a8)

# Where to find help

First and foremost, read the error messages, they are there to assist you. If the Python error message seems to go on forever, scroll right to the end this is where you typically find the most useful part of the error message.

If you are still stumped, and you are using a package or base python functionality, check the documentation (and docstring) for information on how to use the package/function.

Otherwise, remember the search engine of your choice is your friend. As Python is a popular language it is highly probable that someone else came across your problem and communities like [Stackoverflow](https://stackoverflow.com/) will have likely have the answer.

[Overview](./00_overview.md) |
[The Tools](./01_tools.md) |
[Project Setup](./02_project_setup.md) |
[Reproducibility](./03_reproducibility.md) |
[Code Etiquette](./04_code_etiquette.md)
