---
title: "Adversarial Attacks on Neural Networks"
teaching: 20
exercises: 30
questions:
- "What are adversarial attacks on neural networks?"
- "What are some methods for generating adversarial examples?"
- "What are some methods for protecting against adversarial examples?"
- "What situations are best suited for the binary thresholding protection method?"
objectives:
- "Follow instructions to replicate an adversarial attack on a neural network trained on handwritten digits"
keypoints:
- "We are using a trained neural network model trained to recognize handwritten digits from the popular MNIST database"
- "As part of the attack, adversarial examples are being added which trick the network into returning a different label"
- "The effectiveness of the binary thresholding method is demonstrated on grayscale images"
- "The effectiveness of training the neural network with the adversarial examples added to the training set is also demonstrated"
---

## Adversarial Attacks on Neural Networks

Generative Adversarial Attacks, a subset of adversarial attacks, have emerged as a significant threat in the realm of machine learning 
and artificial intelligence. These attacks exploit the vulnerabilities inherent in generative models, which are powerful tools used 
for generating realistic data such as images, text, or even audio.

### Demonstration

In this demonstration on CHEESEHub, you will explore the effects of an adversarial attack on a neural network trained to recognize handwritten digits.
We will use a simple gradient descent algorithm to craft attack that can fool the neural networks into misclassifying digits.
We will evaluate the effectiveness of the attack by measuring the models accuracy on a test set.

By the end of this lab, you will have a better understanding of how adversarial attacks work and how to defend against them. 

> ## Getting Started
> 
> You will need to create an account on [CHEESEHub](https://www.hub.cheesehub.org) to work through this exercise.
> Each container in this demonstration has a web interface and is accessible through your web browser, no other special software 
> is needed.
{: .callout} 

We will start by first adding the Adversarial Neural Network application:

![Add Adversarial Neural Network Attack]({{ page.root }}/fig/adversarial-nn/add-ann.png)

Next, click the *View* link to go to the application-specific page and start the application container:

![Start Container]({{ page.root }}/fig/adversarial-nn/start-container.png)

> ## Container Launch Errors
>
> If a container fails to start, you will see a flashing warning icon next to the container's name. Take a look at the logs to 
> determine the cause of failure and try deleting the application and restarting.
{: .callout}

Once the container has started, launch its web interface in a separate browser tab by clicking the *open* link next to the 
container's name:

![Launch Container]({{ page.root }}/fig/adversarial-nn/launch-container.png)

Click on **Gan_lab.ipynb** to open a Jupyter notebook containing instructions on working through this 
demonstration:

![Open Notebook]({{ page.root }}/fig/adversarial-nn/gan-notebook.png)

Step through the instructions for each of the three parts, filling in or editing the code where it is marked as **TODO**. 
To execute a code cell, you can either use the menu bar at the top or the key combination *Shift+Enter*:

![Complete the TODO]({{ page.root }}/fig/adversarial-nn/todo.png)

> ## What does the exercise tell us?
> Here we implemented an adversarial attack on a neural network model which caused it to misclassify digits. We then demonstrated 
> two strategies for how to defend against such attacks: binary thresholding and model training with augmented examples. 
> The key assumptions and issues with these strategies were also described. 
{: .callout}

{% include links.md %}

