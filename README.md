Download Link: https://assignmentchef.com/product/solved-cop-2800-java-programming-project-5-histogram
<br>
5/5 - (6 votes)

Using <a style="font-size: 16px;" href="https://wpollock.com/lister.php?file=Java/MsgBox3.java&amp;nodir&amp;dl&amp;linenums">MsgBox3.java</a><span style="font-size: 16px;"> or </span><a style="font-size: 16px;" href="https://wpollock.com/lister.php?file=Java/Average.java&amp;nodir&amp;dl&amp;linenums">Average.java</a><span style="font-size: 16px;"> as examples, create a Java non-</span><acronym style="font-size: 16px;" title="Graphic User Interface">GUI</acronym><span style="font-size: 16px;"> stand-alone application that displays a histogram.  A </span><em style="font-size: 16px;">histogram</em><span style="font-size: 16px;"> is a kind of non-</span><abbr style="font-size: 16px;">GUI</abbr><span style="font-size: 16px;"> bar chart (see example </span><a style="font-size: 16px;" href="https://wpollock.com/Java/BarChart.gif">bar chart</a><span style="font-size: 16px;">) that shows how many times a given value occurs in an input sample.  The more times a given value appears, the longer the bar becomes for that value.  With a histogram, you draw the chart sideways.</span>

This program can be used to examine all sorts of frequency data.  In the <a href="https://wpollock.com/Java/Proj-Histogram.htm#Example">example below</a> I used this histogram program to analyze the scores of a previous COP 2800 Exam #1.  I entered in all the question numbers that were answered incorrectly, for each and every student exam.  (For instance, on the first student answered questions 1, 3, 4, and 19 incorrectly, so I input: <code>1 3 4 19</code>.  The next student had questions 4, 17, 19, and 22 incorrect, so I continued by entering <code>4 17 19 22</code> this time.  I kept this up for each student’s exam.)  The <a href="https://wpollock.com/Java/Proj-Histogram.htm#Output">output</a> shows 8 questions were much harder than the rest, and that two questions were so trivial nobody answered them incorrectly.  (I have used this information to update my test bank.)

To actually draw the horizontal lines of the histogram, you <big><strong>must</strong></big> use the <code>utils.TextKit.lineOfStars</code> method you created in <a href="https://wpollock.com/Java/Proj-TextKit.htm">TextKit Project</a>.  This project will require the use of arrays and input.

<h2>Requirements:</h2>

Write a Java non-<abbr>GUI</abbr> program that will accept as input integer values, each value is a number between 1 and 25, with one value per line.  The input might contain any number of values.  The user will indicate the end of the list by signaling <em>EOF</em>, which on DOS/Windows systems is done by hitting a <code>control-<abbr>Z</abbr></code>.  (On Unix and Macintosh systems <em><abbr title="End Of File">EOF</abbr></em> can be signaled by hitting a <code>control-<abbr>D</abbr></code> instead.)

The output shall consist of 25 lines of stars (asterisks), one line for each of the possible input values (the numbers <code>1</code> to <code>25</code>).  The number of stars drawn shows how many times each value was entered as input.  Each line should be labeled with the value it is showing the bar for.  So, if the input was:

<pre class="Indent">    C:TEMP&gt; <strong> java Histogram </strong>    Enter integers &lt;= 25, one per line, hit control-Z when done:    <strong>1    2    4    2    1    2    <em>control-Z</em></strong></pre>

Then the output would be:

<pre class="Indent">     1: **     2: ***     3:     4: *     5:     6:     7:     8:     9:    10:    11:    12:    13:    14:    15:    16:    17:    18:    19:    20:    21:    22:    23:    24:    25:</pre>

Your Java program <strong><big>must</big></strong> use the method called <code>lineOfStars</code> to create the stars for each line of output.  This method <strong><big>must</big></strong> take a single <code>int</code> parameter which says how many stars to draw.  This method <strong><big>must</big></strong> be a <code>static</code> method of a class called <code>TextKit</code>, which <strong><big>must</big></strong> be in a <code>package</code> called <code>utils</code>.  This should be the method you created for the previous project.  You are <big><strong>not</strong></big> allowed to modify your <code>utils.TextKit</code> class in any way from what you completed in the previous project without the approval of your instructor.

Your program will have its class in the default, nameless package and not in the <code>utils</code> package (where <code>TextKit</code> is located).

<h2><a name="Example"></a>Sample Output:   COP 2800 Exam I Analysis</h2>

(Note only a few of the more than 100 values actually typed by me are shown here.)  You can read the input data from a file too, using a command line such as:

<pre class="Indent">C:TEMP&gt; <strong> java Histogram &lt; data.txt</strong></pre>

(To practice using the data I used, download <a href="https://wpollock.com/Java/HistogramData.txt">HistogramData.txt</a> and use that as the input file as shown above.  This technique is known as <em>input redirection</em> and is very useful when testing.)

<pre class="Indent">C:TEMP&gt; <strong> java Histogram </strong>Enter integers &lt;= 25, one per line, hit control-Z when done: <strong>15161122332...16<em>control-Z</em></strong><a name="Output"></a>	 Histogram showing how many students	 answered each question wrong:   1: **  2: *****  3: *****  4:   5: ***  6: **  7: *****  8:   9: ** 10: *************** 11: ***** 12: ******** 13: ************* 14: ******** 15: ******* 16: *************** 17: *** 18: ************** 19: ******************* 20: ********** 21: ******* 22: ******** 23: ************* 24: ************** 25: ****************C:TEMP&gt; </pre>