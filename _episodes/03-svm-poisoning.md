---
title: "SVM Poisoning Attack"
teaching: 10
exercises: 30
questions:
- "What is a SVM poisoning attack?"
- "What is the general procedure for poisoning a machine learning model?"
- "What are some methods for protecting against poisoning attacks?"
objectives:
- "Follow instructions to replicate a poisoning attack on a SVM classifier trained on handwritten digits"
keypoints:
- "We are using a SVM model trained to recognize handwritten digits from the popular MNIST database"
- "As part of the poisoning attack, malicious data is being added to the training set"
- "The effectiveness of the attack is measured by evaluating on a test set with and without the poisoned samples"
---

## SVM Poisoning Attacks

Support Vector Machines (SVMs) are a popular type of machine learning algorithm used in many applications, including image classification, 
natural language processing, and anomaly detection. However, like many machine learning algorithms, SVMs are vulnerable to attacks that 
manipulate their training data.

One such attack is called a poisoning attack, where an attacker adds malicious data to the training set with the goal of manipulating the 
SVM's decision boundary. Poisoning attacks can be targeted, where the attacker wants the SVM to classify specific inputs incorrectly, or 
untargeted, where the attacker just wants to reduce the SVM's overall accuracy.

### Demonstration

In this demonstration on CHEESEHub, you will explore the effects of a poisoning attack on an SVM trained on a dataset of handwritten digits. 
We will use a simple gradient ascent algorithm to craft poison samples that can fool the SVM into misclassifying digits. 
We will evaluate the effectiveness of the attack by measuring the SVM's accuracy on a test set with and without the poison samples.

By the end of this lab, you will have a better understanding of how SVM poisoning attacks work and how to defend against them. 
You will also gain experience working with SVMs and gradient ascent algorithms in Python.

> ## Getting Started
> 
> You will need to create an account on [CHEESEHub](https://www.hub.cheesehub.org) to work through this exercise.
> Each container in this demonstration has a web interface and is accessible through your web browser, no other special software 
> is needed.
{: .callout} 

We will start by first adding the SVM Poisoning Attack application:

![Add SVM Poisoning Attack]({{ page.root }}/fig/svm-poisoning/add-svm.png)

Next, click the *View* link to go to the application-specific page and start the application container:

![Start Containers]({{ page.root }}/fig/svm-poisoning/start-container.png)

> ## Container Launch Errors
>
> If a container fails to start, you will see a flashing warning icon next to the container's name. Take a look at the logs to 
> determine the cause of failure and try deleting the application and restarting.
{: .callout}

Once the container has started, launch its web interface in a separate browser tab by clicking the *open* link next to the 
container's name:

![Launch Container]({{ page.root }}/fig/svm-poisoning/launch-container.png)

Click on **SVM Poisoning-Understanding.ipynb** to open a Jupyter notebook containing instructions on working through this 
demonstration:

![Open Notebook]({{ page.root }}/fig/svm-poisoning/svm-notebook.png)

Step through the instructions for each of the five parts, filling in the code where it is marked as **TODO**. To execute a 
code cell, you can either use the menu bar at the top or the key combination *Shift+Enter*:

![Complete the TODO]({{ page.root }}/fig/svm-poisoning/todo.png)

> ## What does the exercise tell us?
> Here we implemented a poisoning attack on the popular SVM machine learning algorithm which reduced the accuracy of the model 
> significantly. We also demonstrated one strategy for how to defend against such attacks and improve accuracy in the presence of 
> malicious examples.
{: .callout}

{% include links.md %}

