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

## Brainstorm

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

## Requirement Documentation (In progress, need further supplementation)

### Background and Introduction

- Purpose and scope of the document
- Project overview
- Target user groups
- Timeline and milestones

### User Stories

* Detailed description of the primary users and their goals
* Use cases and scenarios for each user type

### Functional Requirements

- Evaluation Module
  - Dataset preparation and management
    - data cleaning
    - data augmentation
    - data transformation
  - Model evaluation metrics and tools
  - Visualization of model performance
  - custom model arenas
- Training Module
  - Fine-tuning algorithms and techniques
  - Model versioning and tracking
  - Support for various preprocessing techniques
- Deployment Module
  - Model packaging and distribution
  - Support for various deployment environments (cloud, edge, on-premise)
  - Monitoring and logging tools
- Collaboration and Version Control
  - Collaboration tools and workflows
  - Version control system integration
- Automation and Testing
  - Continuous integration and continuous deployment (CI/CD)
  - Unit and integration testing
- User Interface and Experience
  - Web-based interface for managing projects and models
  - Mobile application for convenient access

### Non-functional Requirements

* Performance
  * response time
  * throughput
  * resource usage
* Usability
  * user interface design
  * ease of use
  * accessibility
* Scalability
  * large datasets
  * large models
* Reliability
  * fault tolerance
  * recovery
  * backup
* Security
  * data protection
  * privacy
  * authentication
* Technical constraints, limitations, and considerations
  * hardware
  * software
  * network
* Legal and regulatory requirements
  * data privacy
  * data protection
  * intellectual property
  * etc.

### Project Stakeholders and Roles

- Developers: They are responsible for writing and maintaining the codebase of the project. They work closely with other stakeholders to ensure the software meets the requirements and is of high quality.

- Data Scientists: They analyze and interpret complex digital data to help the project make better decisions, build better products, and offer more personalized user experiences.

- ML Engineers: They design, build, and deploy machine learning models that are integral to the project. They work closely with data scientists to understand the data and implement appropriate models.

- End Users: They are the people who will be using the final product. Their feedback is crucial in shaping the product and making it more user-friendly.

- IT Infrastructure Managers: They oversee and maintain all aspects of an organization's IT infrastructure to ensure the project has the necessary resources to run smoothly and efficiently.

### Risk Management and Mitigation

#### Potential Risks and Challenges

1. **Project Delays**: Unforeseen circumstances or dependencies can lead to delays in project timelines.

2. **Budget Overruns**: The project may exceed the allocated budget due to unexpected costs or underestimation.

3. **Scope Creep**: The project's scope may expand beyond its original objectives, leading to additional work.

4. **Technical Difficulties**: The project may encounter technical issues that are difficult to resolve.

5. **Staff Turnover**: The loss of key team members can impact the project's progress and quality.

#### Proposed Mitigation Strategies

1. **Project Delays**: Implement a robust project management system to track progress and dependencies. Regularly update and communicate timelines to all stakeholders.

2. **Budget Overruns**: Conduct thorough cost estimation at the start of the project. Regularly monitor and control project costs.

3. **Scope Creep**: Clearly define the project's scope at the outset. Any changes to the scope should go through a formal change control process.

4. **Technical Difficulties**: Ensure the team has the necessary skills and resources to address technical challenges. Consider bringing in external expertise if needed.

5. **Staff Turnover**: Develop a succession plan for key roles. Foster a positive work environment to retain staff.

### Validation Metrics

* Test strategy and approach
* Test deliverables and milestones
* Testing strategy
* Description of the test cases and scenarios
* Description of the metrics used to validate the platform against the specified requirements
* Expected accuracy, precision, recall, and F1 score for model evaluations
* Expected latency, throughput, and resource usage for deployment and inference
* Measures to verify and validate the platform's functionality and performance
* Testing strategy and approach

### Implementation Notes

* Any implementation-specific considerations or constraints
* Recommendations for technology stack or tools
* Technologies and tools to be used for platform development
* Platform architecture and component interactions
* Deployment considerations (e.g., infrastructure, hosting)

### Conclusion

* Recap of the requirements
* Next steps for development
*Summary of the requirements
*Next steps for development
* Recap of the requirements and their importance
* Next steps for development and validation
* Recap of the requirements and their importance to the platform's success
* Next steps for development and validation

## For you to do

Can you continue to brainstorm with me to refine the project scope with horizontal thinking(not in-depth thinking) and then write comprehensive requirement documents to add to the `Requirement Documentation` section?
