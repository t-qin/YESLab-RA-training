# Task for week5

The major task is to check the Chinese texts are displayed correctly in the PsychoPy experiment. Below are several steps to guide you through the process.

## Step 1: Download the PsychoPy experiment
[guilt task chinese gitlab](https://gitlab.pavlovia.org/YesLab/guilt_sad_guilt_task_chi) \
[facial trait chinese gitlab](https://gitlab.pavlovia.org/YesLab/guilt_sad_trait_task_chi)

## Step 2: Run the experiment on your computer
You may need PsychoPy 2021.2.3 for running experiments
### Asthetic settings
- Set the font to "Songti SC" for Chinese texts
- Adjust letter height and position
- If the text is not wrapped correctly, you may need to return lines manually
### Chinese texts in code components
- Make sure we used unicode for Chinese texts, which should be `u"中文内容"`
- If you have seen `$somevaribles` in the text box, it indicates that the content of this text component is defined by a variable. You may need to search for the variable in the code component and replace it with Chinese texts. Open the *_last_run.py* file and search for the variable name will make it easier to locate the variable in the code component. But make sure you make every change in the psychopy builder.

## Step 3: Debugging
If you have extra time, you can explore uploading the experiment to Pavlovia and check if the Chinese texts are displayed correctly. Here's a tutorial of how to upload the experiment to Pavlovia: \
[Launch your study to pavlovia](https://www.psychopy.org/online/usingPavlovia.html)