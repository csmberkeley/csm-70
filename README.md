# latexer
Thing to create worksheets.

# Overall Structure

![Image](scripts/x.pdf?raw=true)

# Setting up your machine
1. Create a directory.
2. git clone https://github.com/kstukalova/latexer.git
3. Make sure you have pdflatex set up on your machine. If it isn't download MacTex.

![alt text](https://github.com/kstukalova/latexer/blob/master/scripts/setting_up.gif "Logo Title Text 1")

# Creating a worksheet
1. git pull
2. git checkout BRANCH
3. Go to latex and create worksheetXX directory
4. Inside new directory create Latex files called meta.tex and worksheetXX.tex
5. Copy from an existing worksheet.
5. Update the date, title, worksheet number.
6. Go back to src and type make worksheetXX. This will generate meta.pdf and worksheetXX.pdf in src/pdf/worksheetXX/.

![Demo CountPages alpha](https://j.gifs.com/nZXOBp.gif)](https://youtu.be/9_qXN9onpmc)


# Adding a question (and meta)

![Demo CountPages alpha](https://j.gifs.com/mw6yLR.gif)](https://youtu.be/JzXQ5t4YkeU)
### Each worksheet has problems and introductory material. This section will go over both. The main difference is the header of the topic specific Latex file and the way that problem is imported into the main worksheetXX.tex.
1. git pull
2. git checkout BRANCH
3. Go to tpics
4. Create new directory with new topic name or enter an existing directory.
4. If creating new topic, create problems directory inside new topic directory.
4. Create tex file that will contain your problem. Give it a descriptive name. If there are images in your problem, put them in the same directory and name them problem_name\*
4. If you are writing a problem, start the latex file with \question. Otherwise you can just start writing
4. Go back to the main worksheet and edit the \section field as necessary. Edit the \subimport fields to reflect the path to your new problem.
4. If you wrote a question it should be surrounded by \begin{questions} and \end{questions}
4. Go back to src to make worksheetXX (the worksheet you included your problem in).
4. To write the solution, go to your topic specific latex file and surround the solution in \begin{solution} and \end{solution}. After \begin{solution} you can write [1 in] and this will leave a 1 inch space in the worksheet for the student answer.
4. Go back to src and make worksheetXX_sol

# Tips
* Pattern match always.
* Special commands:
  * \texttt{} will create programming text
  * \lstlisting will create a block of programming text
  * Special symbols (inside math environment)
    * \P
    * \E
    * \var
    * \cov
  * How to make boxes:
    * \fbox{\begin{minipage}{16.3cm}
    * CONTENT GOES HERE
    * \end{minipage}}
* Naming conventions:
  * Always create worksheet directories as worksheetXY where X,Y are in [0, 9]
  * Put images in same folder as the problem they are used in. Name them the same name as the problem.
* Common errors and debugging:
  * Replace tabu with \fbox{\begin{minipage}{16.3cm} CONTENT \end{minipage}}
    * Remove \\ after each line
  * If make all isn’t working try doing “make worksheetXX” for the worksheet that doesn’t compile and then do make all
 
>>>>>>> 01087e9e8e9521b038c76c0dbcd0d67df9fe78a4
