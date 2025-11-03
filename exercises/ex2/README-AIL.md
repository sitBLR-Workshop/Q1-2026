# Exercise 2 - Exercise 2 Description

In this exercise, we will evaluate our basic prompt using the evaluation data set provided and the AI Core evaluation service.

## Exercise 2.1 Create a template for the bas prompt

After completing these steps you will have created and stored a prompt template, and evaluated it with a set of metrics. 

### 2-1-1 Create the prompt template
First let's create a prompt template for the basic prompt provided in the data folder.
1.  Go back to the `Prompt Editor` by clicking on it in the side menu.
2.  Configure the first message in your prompt as a `System` messages by clicking on `System`.
<br>![](/exercises/ex2/images/ail02-1.png)

3.  Copy the text for the system message from the `facility_prompt_basic.yaml` file located in the `data/prompts` folder and paste it into the message field.
4.  Add a second message by clicking on `+`. By default the new message is a user message, which is what we want.
<br>![](/exercises/ex2/images/ail02-2.png)

5.  Copy the text for the user message from the `facility_prompt_basic.yaml` file located in the `data/prompts` folder and paste it into the message field.
6.  Optionally, in the `Variable Definitions` you can provide a default value for your template variable `input`. Copy the following text into the default field.

```
Subject: Assistance Needed with Facility Management Coordination\n\nHi Support Team,\n\nI hope this message finds you well. My name is [Sender], and I've been utilizing Facility Solutions Company for our office building's management for the past year. Overall, I've been quite satisfied with the services provided, but I\u2019ve encountered an issue that I need your help with.\n\nRecently, I've noticed some inconsistencies in the coordination of our space utilization and security measures. Specifically, there have been a few instances where the security protocols were not followed correctly, and the space allocation for our new team members hasn't been managed as efficiently as before. This has caused some disruptions in our daily operations.\n\nI haven't taken any steps to address this issue internally yet, as I believe it would be best handled by your team of experts. Could you please look into this matter and provide a solution to ensure that our facility management runs smoothly again?\n\nThank you for your attention to this matter. I look forward to your prompt assistance.\n\nBest regards,\n[Sender]
``` 
<br>![](/exercises/ex2/images/ail02-3.png)

7. In the `Model Selection` section, choose the model you want to use for this exercise. Click on the icon next to the model name to open the model selection dialog.
<br>![](/exercises/ex2/images/ail02-4.png)

Check with the group, so that the workload of the hands-on is evenly distributed across the available models. 
<br>![](/exercises/ex2/images/ail02-5.png)

8. Now that we have filled everything out we can test the prompt. Scroll to the top and click on `Run`.
<br>![](/exercises/ex2/images/ail02-6.png)

You should see the model response in the text field to the right.

6.  Now that we have configured and testes our prompt we can save it as a template into the prompt registry. Click on `Save as Template` to store the prompt template in the prompt registry.
<br>![](/exercises/ex2/images/ail02-7.png)

7. Fill out the template information in the dialog that opens and click on `Save`.

Use the following value as Scenario: `AI-161-{{groupID}}`
Use the following value as Name: `{{groupID}}-facility-classification-base`
Use the following value as Version: `0.0.1`
<br>![](/exercises/ex2/images/ail02-8.png)

You should see a confirmation message that the prompt template was saved successfully.

### 2-1-2 Check your stored template
Let's check our stored template.
1. Open the `Prompt Management` view by clicking on it in the side menu.
2. Click on the `Templates` tab to view the stored prompt templates.
<br>![](/exercises/ex2/images/ail02-9.png)

3. Find your prompt template by filtering for your group ID in the search field.
4. Click on the prompt template to view its details.
<br>![](/exercises/ex2/images/ail02-10.png)

5. You should now see your stored prompt template.

## Exercise 2.2 Upload Evaluation Data Set

In the UI uploading the data set can be done as part of the evaluation configuration. So we will continue with the next step for now.

## Exercise 2.3 Configure and run the evaluation

Now that we have successfully prepared a prompt template, we can configure and run an evaluation with the AI Core evaluation service. 

### 2-3-1 Configure your Evaluation
1. Open the `Optimization` view by clicking on it in the side menu.
You should see a list of optimization and evaluation runs.

2. Click on `Create` in the top left.
<br>![](/exercises/ex2/images/ail02-11.png)

A Dialog to chose between `Optimization` and `Evaluation` opens.

3. Select `Evaluation`.
<br>![](/exercises/ex2/images/ail02-12.png)

4. First we need to select the prompt template we want to evaluate. Click on the selection icon to open the template selection.
<br>![](/exercises/ex2/images/ail02-13.png)

5. Now choose your prompt template from the list by clicking on it and then clicking `Select`. 
You can use the filters to find your prompt template more easily.
<br>![](/exercises/ex2/images/ail02-14.png)

6. Next we need to select the model which we want to evaluate. Click on the selection icon to open the model selection.
<br>![](/exercises/ex2/images/ail02-15.png)

7. Browse the available models and select the model you want to use for this exercise. Normally, you can configure multiple models to compare them for your use-case. For this hands-on session let's coordinate chosing different models across groups and chose one model each. This allows us to distribute the workload of the hands-on evenly across different models and later compare them as we are all using the same user. 
Click on the model that was chosen for your group and then click `Select`.
<br>![](/exercises/ex2/images/ail02-16.png)

8. Finally, we need to select a dataset artifact to be used during the evaluation. Click on the selection icon to open the artifact selection.
<br>![](/exercises/ex2/images/ail02-17.png)

9. Since we have not yet uploaded the data we will create the dataset artifact now. Click on `Add` in the top right to create a new Data Set Artifact.
<br>![](/exercises/ex2/images/ail02-18.png)

10. In the dialog that opens, provide the following information:
- Scenario: `AI-161-{{groupID}}`
- Type: `Dataset`
- Name: `{{groupID}}-eval-data`
- Description: `Artifact for evaluation flow`

11. In the section `Upload File` provide the following information:
- Object Store: `default`
- Sub-folder path: `/T-01`
- Overwrite existing file: Yes

Then open the file selection by clicking on the browse icon.
<br>![](/exercises/ex2/images/ail02-19.png)





### 2-3-1 Check available models
1. First let's explore some available models for the evaluation. Open the `Model Library` view by clicking on it in the side menu.
2. Browse the available models. 
3. Discuss with the group who will evaluate which model to distribute the workload evenly.

### 2-3-2 Check avialable metrics
1.

### 2-3-3 Configure your Evaluation
1. Open request 2-3-3 Configure the Evaluation in the Bruno API client.

### 2-3-4 Start the Evaluation

## Summary

You ha've now ...

Continue to - [Exercise 3 - Excercise 3 ](../ex3/README.md)
