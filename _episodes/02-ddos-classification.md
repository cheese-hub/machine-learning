---
title: "DDoS Classification using Machine Learning"
teaching: 10
exercises: 30
questions:
- "What is a DDoS attack?"
- "How can we use machine learning to train a model to identify attack and benign network traffic?"
objectives:
- "Follow instructions to train and test a machine learning model that identifies DDoS attack traffic."
keypoints:
- "We are utilizing a specific model, logistic regression to classify network traffic data into benign and attack classes"
- "The data being used is not raw network traffic data, but pre-processed data that is conducive to machine learning analysis"
- "When a lot of training data is provided, machine learning is able to learn fairly accurate models"
---

## DDoS Attacks

Distributed denial-of-service (DDoS) is an attempt by nefarious actors to overwhelm a server or network by flooding it with 
spurious network traffic that prevents legitimate users from accessing the server or network. The attacker often uses several 
other previously *hacked* sources to conduct this attack, hence the term *distributed*, as there is no single source of 
attack. 

In order to use machine learning to perform real-time detection of such attacks so that they can be mitigated as soon as possible, 
we will need to train the model on a well-labeled, comprehensive dataset. Such a dataset needs to include network traffic corresponding 
to various kinds of modern DDoS attacks. In this demonstration, we use the [DDoS Evaluation Dataset](https://www.unb.ca/cic/datasets/ddos-2019.html) 
published by the Canadian Institute for Cybersecurity. This dataset includes a *training* and *test* dataset of network traffic data 
that has been labeled with either the kind of DDoS attack or as *benign* in the case of background traffic data.
We will demonstrate how the data can be used to train and test simple classification models (*logistic regression*) that discriminate between:
- Attacks based on NetBIOS versus benign traffic
- Attacks based on Portmap versus benign traffic
- Attacks based on NetBIOS versus attacks based on SYN

### Demonstration

The demonstration on CHEESEHub illustrates the application of machine learning to this dataset via a single container using Jupyter 
notebooks. The Python *scikit-learn* library is used to conduct the machine learning training and testing, and *Pandas* is used to 
ingest and manage the datasets which are provided in the form of comma separated value (csv) files. Since the original dataset is too 
large to process efficiently on limited computing memory, the demonstration only uses a small subset of the dataset. Our intent here 
is to simply demonstrate the use of machine learning for this analysis task; various other approaches including parallel processing of 
chunks using a library like *Dask*, or other big data technologies such as *Apache Spark* can be used to work with the entire dataset. 

Briefly in this demonstration you will do the following:

1. Ingest the data into Pandas and inspect it to identify the various data fields and their types. 
2. Identify a reasonable set of *numerical* fields that can be used in the machine learning model.
3. Prepare the necessary datasets with appropriate output label values for training and testing the model.
4. Study the performance of the learned model on the test dataset.

> ## Getting Started
> 
> You will need to create an account on [CHEESEHub](https://www.hub.cheesehub.org) to work through this exercise.
> Each container in this demonstration has a web interface and is accessible through your web browser, no other special software 
> is needed.
{: .callout} 

We will start by first adding the DDoS Traffic Classification application:

![Add DDoS Traffic Classification]({{ page.root }}/fig/ddos-classification/add-ddos.png)

Next, click the *View* link to go to the application-specific page and start the application container:

![Start Containers]({{ page.root }}/fig/ddos-classification/start-container.png)

> ## Container Launch Errors
>
> If a container fails to start, you will see a flashing warning icon next to the container's name. Take a look at the logs to 
> determine the cause of failure and try deleting the application and restarting.
{: .callout}

Once the container has started, launch its web interface in a separate browser tab by clicking the *open* link next to the 
container's name:

![Launch Container]({{ page.root }}/fig/ddos-classification/launch-container.png)

Click on **ddos-classification.ipynb** to open a Jupyter notebook containing instructions on working through this 
demonstration:

![Open Notebook]({{ page.root }}/fig/ddos-classification/ddos-notebook.png)

Step through the instructions for each of the five sections, filling in the code where it is marked as **TODO**. To execute a 
code cell, you can either use the menu bar at the top or the key combination *Shift+Enter*:

![Complete the TODO]({{ page.root }}/fig/ddos-classification/todo.png)

> ## What does the exercise tell us?
> Here we used a specific machine learning algorithm, *logistic regression* to perform classification where there are only two 
> classes. Despite using only a small subset of the original dataset, we observe very good classification performance due to the 
> overabundance of DDoS attack training data. Feel free to redo the steps by choosing a different set of fields for the training 
> process and study the performance of the model.
{: .callout}

{% include links.md %}

