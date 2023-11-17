# Brainstorm for Project "DemoAI"

## Background

OpenAI's GPTs hold significant importance, yet they rely on proprietary data and models. In today's landscape, private data stands out as the most valuable asset, compelling companies to create their own models and platforms to manage the entire data-to-model-to-agent workflow. This represents the prevailing direction in the field.

Furthermore, aside from fostering innovation and progress, open-source platforms also champion data privacy. By granting users control over their data and its utilization, these models play a vital role in upholding privacy standards. This underscores why the shift towards open-source AI is not merely a passing trend but an imperative for the future of AI development.

While open-source platforms and communities like HuggingFace facilitate AI innovators in sharing their models, they may fall short, especially for non-AI companies. Existing products tend to be complex and disjointed, posing entry barriers. For instance, while they excel in model sharing, they may lack support for tasks such as advanced dataset preparation methods like self-instruction, model evaluation on custom datasets, and even comprehensive model metadata.

Other platforms focused on agents are commendable, but they don't necessarily endorse open-source principles. As prompts have become the new code, we believe that the open-sourcing of prompts has naturally become the "new open-source" done right.

I want to build a platform to help companies to build their own models and agents. This is a very ambitious project. I need to start with a minimum viable product (MVP) and then gradually add more features. I need to brainstorm with you to define the MVP.

I want to develop a platform for

* Model registry - a database for model meta data, and management of local models (download, remove, etc.)
* Evaluating open source LLMs
* Training of fine tuning the model to fit custom needs
* Deploying models for inferencing both on premise and cloud
* Helping customer to integrate LLMs into their own workflows
* Helping customer to develop their own agents
* share prompts and agents (reproducibility is the key)

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

For bleeding edge trends, we need to support AI agents.

* Evaluation
  - Agent models
  - Agent frameworks
  - datasets for evaluation
* Agent Management
  - Agent store
* Agent workspace
  - runtime/execution environment
  - history management
    * history fork

IMPORTANT: This is just a brainstorm, not a plan. You need to think creative and refine it with me.

# Requirement Documentation (In progress, need further supplementation)

## Background and Introduction

## User Stories

## 

# For you to do

Can you continue to brainstorm with me to refine the project scope with horizontal thinking(not in-depth thinking) and then write comprehensive requirement documents to add to the `Requirement Documentation` section?