# Background

I want to develop a platform for

* Model registry - a database for model meta data, and management of local models (download, remove, etc.)
* Evaluating open source LLMs
* Training of fine tuning the model to fit custom needs
* Deploying models for inferencing both on premise and cloud
* Helping customer to integrate LLMs into their own workflows

# Brainstorm

Points above is from user's perspective. But from implementation perspective, I'll brainstorm some key ideas:

* For both evaluation and training, we need a module to prepare datasets
  - datasets for training, validating and testing
  - datasets for model evaluation
  - tools for data preparation
    * data cleaning
    * data argumentation
    * self-instruct
    * etc.
* For evaluation
  - A module to compute metrics like perplexity, EM, etc.
  - Visualization tools to plot loss/metric curves during training
  - custom model arena
* For advanced model development and research
  - model parameter visualization
    * to see for example, if there is parameter explosion
    * which neurons are activated
    * just like scanning of human brain
* For deployment, dockerizing the model would be a good idea

Workloads often comes as workflows, from the perspective workflow:

* research
  - control group and experiment group
    * versioning
    * reproducibility
    * snapshot of every step of the workflow
* production
  - user data collecting
  - update dataset
  - retrain model
  - evaluate model / regression test
  - deploy model

IMPORTANT: This is just a brainstorm, not a plan. You need to think creative and refine it with me.

# Requirement Documentation (In progress, need further supplementation)

[Insert refined requirement here]

# For you to do

Can you continue to brainstorm with me to refine the project scope with horizontal thinking(not in-depth thinking) and then write comprehensive requirement documents to add to the `Requirement Documentation` section?