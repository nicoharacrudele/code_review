## Code Review Instructions

1. To start, [**fork**](https://guides.github.com/activities/forking/) your team members' repository (team and repository URL's listed [here](https://github.com/PHY3009/code_review/blob/master/code_review_teams.md)).

2. [**Clone**](http://gitref.org/creating/#clone) the repository to your computer.

3. Read their 10 minute plan (should be in the README.md file in their project's root 
directory.

4. Open up the ipython notebook or python script and review the code. **Note: do not 
review > 400 lines of code per hour. Reviewing faster than this can cause losses in review 
effectiveness. Thus, it should take ~ 1 hour to review 400 lines of code, and shorter 
amounts of code should take relatively less.

 Comments/thoughts/suggestions can be added to ipython notebooks via comments in code cells
 and/or text in Markdown cells. In scripts, please only use comments. If you find a 
 bug/error in the code please point it out, and if you can, please try to fix it! Remember
 to be polite and respectful by following the [code of conduct](http://software-carpentry.org/conduct.html).

 While reviewing the code, follow the checklist below from the [Mozilla Science Lab](http://mozillascience.github.io/codeReview/review.html):
	* **Are functions as simple as possible?** We insisted in our submission guidelines that 
	functions be short, but this is really a simple proxy for our true goal: to ensure that 
	functions are modular. A modular function is one that does exactly one thing, and does 
	it well - by insisting on breaking code up into the simplest possible functions, we make 
	them easy to test, easy to understand, and easy to review. Can any of the functions in 
	this new submission be broken up into simpler steps?

	* **Is the code efficient?** If some really slow operation is performed in the code, it 
	should be performed as infrequently as possible. For example, diagonalizing a matrix can 
	be a slow computation. If the new code needs to do a slow operation like this, it should 
	do it once only, and store the result for use, rather than recomputing it every time it 
	needs to use it. Not sure which operations are slow? Assume they all are! Don't repeat 
	any operation unnecessarily - we call this well factored code.

	* **Is the usage of each function clear?** Try and put yourself in the mindset of someone 
	coming to this code for the first time; how would they know how to re-use the existing 
	code? The documentation for each function should have, at a minimum, a short description
	of the function, and a specification of its inputs and outputs.
 
	* **Have edge cases been considered?** Users will invariably do all kinds of things with 
	your code that they aren't supposed to. If the user does something unexpected (atypical 
	inputs, clicking on things they're not supposed to...), will this new code break, or will 
	it roll with the punches? For example, if a function takes a numerical input, is there a 
	situation where division by 0 could be triggered?

	* **Does the new code reinvent any wheels?** New code should be just that - new. If it's 
	reproducing functionality you have elsewhere in the code, it shouldn't be repeated here. 
	This is another reason for insisting on splitting functions up into small and reusable 
	pieces; shared functionality can be written, reviewed and debugged just once, rather than 
	over and over again in different contexts.

	* **Does the new code successfully address the needs of the project?** By sketching out 
	that ten-minute plan and having had a conversation with your contributors about what their 
	new contribution is trying to address, you created a clear goal for this new work; does 
	this contribution push the project forward by addressing those plans and discussions?

	* **Does the new code respect the structure of the project?** A healthy project is a well 
	organized project with a high degree of standardization. If the rest of the code has 
	established variable naming conventions, file structure, or other patterns, does this new 
	code uphold those patterns?

5. [**Add**](http://gitref.org/basic/#add) and [**commit**](http://gitref.org/basic/#commit) 
comments/edits/bug fixes to Git.

6. [**Push**](http://gitref.org/remotes/#push) the changes up to your copy of the 
repository on GitHub.

7. [Create a **pull request**](https://help.github.com/articles/creating-a-pull-request/) 
on the original repository to turn in your review. **When making the pull request, you must
write a brief (100 - 200 word) summary of the comments/edits/bug fixes included in your 
pull request.**

8. Be prepared to discuss each review (you will be doing 2) with your team for 5 minutes 
during class. These discussions should highlight what you think is the most helpful aspect 
of your review. The peer tutor will facilitate these discussions.

## Grading rubric

<table>
  <tr>
    <th></td>
    <th>Poor/Unacceptable 0% – 59%</td> 
    <th>Limited 60% – 69%</td> 
    <th>Fair/Adequate 70% – 79%</td> 
    <th>Good 80% – 89%</td> 
    <th>Exceptional 90% – 100%</td> 
  </tr>
  <tr>
    <th>Ten Minute Plan (20%)</td>
    <td>Instructions (as documented <a href="https://github.com/PHY3009/code_review/blob/master/Ten_Minute_Plan.md">here</a>) were not followed.</td> 
    <td></td> 
    <td></td> 
    <td></td> 
    <td>Ten Minute Plan exists in the README.md file in the projects root directory and the project has been set up as per instructions <a href="https://github.com/PHY3009/code_review/blob/master/Ten_Minute_Plan.md">here</a>.</td> 
  </tr>
  <tr>
    <th>Code Review (60%)</td>
    <td>No comments/edits or bug fixes were included with the pull request.</td> 
    <td>Comments/edits/bug fixes identified with the code, but the issues identified are only somewhat helpful for improving the code. No summary was provided with the pull request.</td> 
    <td>Comments/edits/bug fixes identified with the code, but the issues identified are only somewhat helpful for improving the code. A summary of the comments/edits/bug fixes included in the pull request was written when the pull request was submitted, but it is not clear.</td> 
    <td>Comments/edits/bug fixes identified key issues with the code and would be very helpful for improving the code. A good summary of the comments/edits/bug fixes included in the pull request was written when the pull request was submitted.</td>
    <td>Comments/edits/bug fixes identified key issues with the code and would be exceptionally helpful for improving the code. An exceptional summary of the comments/edits/bug fixes included in the pull request was written when the pull request was submitted.</td> 
  </tr>
  <tr>
    <th>Oral Discussion (20%)</td>
    <td>Feedback was neither relevant nor constructive to improving the code. Feedback was not respectful nor polite.</td> 
    <td>Feedback was not relevant nor constructive to improving the code.</td> 
    <td>Constructive feedback on the code was politely presented, but the feedback was not focused on key aspects which would be most important for improving the code. Clarity was lacking.</td> 
    <td>Key constructive and relevant feedback on the code was politely presented. Clarity was lacking.</td>
    <td>Key constructive and relevant feedback on the code was clearly and politely presented.</td> 
  </tr>
</table>