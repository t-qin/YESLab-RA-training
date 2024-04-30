# YESLab online experiment manual

![img_book](book.png)

---------------------------------------
## Daisy Chaining
This is a very powerful tool for linking and passing information between different platforms.
### Tutorials
[Youtube tutorials: an overview](https://www.youtube.com/watch?v=WpTjVQH-jzw)
[Assign randomized ID on Qualtrics](https://www.qualtrics.com/support/survey-platform/common-use-cases-rc/assigning-randomized-ids-to-respondents/)
[Link two Pavlovia experiments/ Link toward Pavlovia](https://discourse.psychopy.org/t/daisy-chaining-between-2-psychopy-pavlovia-experiments/32750)
[Link toward/ from Qualtrics](https://www.qualtrics.com/support/survey-platform/survey-module/survey-flow/standard-elements/passing-information-through-query-strings/)
[Qualtrics primer (e.g., ResponseID, …)](https://docs.google.com/presentation/d/e/2PACX-1vShEbK65azEWNKDoT4Z8n9raYYg_1Ael0-jHNyiIm7o9_PvBRVTE7w7fOb7WFC_moqaALa6qhxQ_Hcy/pub?start=false&loop=false&delayms=10000&pli=1&slide=id.g4cadf9cf8d_0_0)
[Link Qualtrics toward/from SONA](https://www.sona-systems.com/help/qualtrics/)

## PsychoPy: sync online
[Psychopy py to js crib sheet](https://discourse.psychopy.org/t/psychopy-python-to-javascript-crib-sheet/14601)
### Some common issues
-	Py: random.random() VS Js: Math.random()
-	Py: thisExp VS Js: psychoJS.experiment
-	Py: win VS Js: psychoJS.window

### Troubleshooting
1. ReferenceError: It means a variable has not been defined. \
**Example**: ReferenceError: win is not defined\
**Solution**: I extracted window size from the default experimental setting at the beginning of the experiment, but didn’t pre-define it. Put “const win;” into code section “before experiment”\
**Example**: testing is not defined\
**Solution**: The variable “testing” is not defined. Check the js file to make sure we have defined this variable. If it is still not working, try to clear your browsing history and restart the experiment. Of note, whether the variable is defined in the “before experiment" section or "begin experiment” section won’t affect much except specific circumstances (i.e., the circumstance above). Since js will call the function experimentInit to run all codes in “begin experiment” section at the beginning, all vars will be defined if they are put in the “begin” section

2. TypeError: Wrong variable type \
**Example**: TypeError: array.slice is not a function\
**Solution**: This error is evoked by applying .slice function to a variable that is not an array. Search “.slice” in the js code and resolve the problem\
**Example**: TypeError: Assignment to constant variable.\
**Solution**: used “const varA” to define a variable then changed its value. Replace “const” by “let” or “var”\
**Example**: Cannot read properties of undefined (reading ‘0’)\
**Solution**: Undefined variable in if statement condition. Try to figure out which variable is undefined and resolve it. This can also caused by using the wrong term (“var” VS “const”)

3. AttributeError: Wrong function name\
**Example**: AttributeError: TrialType has no attribute (or key) 'sendExperimentData'\
**Solution**: This error is evoked by calling a function that doesn’t exist. Of note, if you have a nested loop, current version of PsychoPy(2023+/2024) has a bug of calling this[Name of outside loop].sendExperimentData(). You should manually comment this line out.

## Debugging for PsychoPy Builder
**General suggestions**
-	You may have a testing variable to skip some trials in the testing mode
-	If you want to test the aesthetics of slider, text, and other stimuli, it is recommended to open a new builder window and simply add those components for testing. You won’t want to run your whole experiment time-to-time just to adjust the font size

## Debugging for .js
[How to use Node.js in VS Code](https://code.visualstudio.com/docs/nodejs/nodejs-tutorial)

## PsychoJS (from PsychoPy)
[Getting started](https://psychopy.github.io/psychojs/index.html)
[PsychoJS API](https://psychopy.github.io/psychojs/module-core.PsychoJS.html)

## jsPsych
[Tutorial](https://www.jspsych.org/7.3/)
[Document of plugins](https://www.jspsych.org/7.3/plugins/html-keyboard-response/)
