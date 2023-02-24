# CI-CD-CDE-Jenkins

## CI (Continuous Integration)


Continuous Integration is a practice of automating the integration of code changes from multiple contributors into a single software project(implementing small segmets into the code).

It is a primary DevOps practice, allowing developers to frequently merge code changes into a central repository where builds and tests then run.

**Automated tools**  are used to assert the new code's correctness before integration. 

### Importance of CI

In order to understand the importance of CI, it is helpful to first discuss some ain points that often arise due to the absence of CI. Without CI, developers must manually coordinate and communicate when they are contributing code to the end product. This coordination extends beyond the development teams to operations and the rest of the organization.

Product teams must coordinate when to sequentially launch features and fixes and which team members will be responsible. 

## CD (Continuous Delivery)

Continuous delivery is an approach where teams release quality products frequently and predictably from source code repository to production in an automated fashion. 

### How does it work ? 

A continuous delivery pipeline could have a manual gate right before production. A manual gate requires a human intervention, and there could be scenarios in your organization that require manual gates in pipelines. 

The engineering team keeps a shippable version of the product ready after every sprint, and the business team makes the finall call to release the product to all customers, or a cross-section of the population, or perhaps to people who line in a certain geographical location. 


## CDE (Continuous deployment)

CDE goes one step further than continuous delivery. With this practice, every change that passes all stages of your production pipeline is released to your customer.

There is no human intervention, and only a failed test will prevent a new change to be deployed to production. 


Continuous deployment is an excellent way to accelerate the feedback loop with your customers and take pressure off the team as there isn't a release day anymore.

Developers can focus on building software, and they see their work go live minutes after they have finished working on it. 

![](CICD.png)


---

## Jenkins


Jenkins is an open-source automation server used to build, test, and deploy software projects. Essentially enables CI and CD pipelines, allowing software developers to automate their build, test and deployment processes. 

![](jenkins.png)


### How does it work ?

1. A developer pushes code changes to a GitHub repository.
2. Jenkins monitors the repository for changes and detects the new code.
3. Jenkins pulls the code changes from the GitHub repository to the Jenkins master node, which is the central server that controls the Jenkins environment.
4. The Jenkins master node delegates the build and test process to one or more agent nodes, which are typically separate servers or virtual machines that run the build and test jobs in parallel.
5. The agent nodes run the build and test jobs, and report the results back to the Jenkins master node.
6. Depending on the results of the build and test jobs, Jenkins may trigger additional stages of the CI/CD process, such as deploying the code changes to a staging environment or promoting the code changes to production.

If the tests fail, the process will be marked as failed and Jenkins will alert the relevant parties about the failure. 

If this happens it means that there is a problem with the code changes that were made and further investigation is required to find the root of this issue. 

It is up to developers to review the code, identify the issue, fix the problem, and commit the fixes back to the repository. 

Once the fixes have been committed, the Jenkins pipeline will automatically trigger a new build, which will repeat the build, test and deployment processes. 

This cycle will continue until all tests are marked as passed. 



### Benefits of Jenkins

- It is open source and it is user-friendly, easy to install and does not require additional installations or components
- It is free of cost
- Easily configurable: Jenkins can be easily modified and extended. It deploys code instantly and generates test reports. 
- Platform Independent: Jenkins is available for all platforms and different operating systems.
- Easy support: Because it is open source and widely used, there is no shortage in support from large online communities of agile teams.
- Developers can write the tests to detect the errors of their code as soons as possible. 
- Issues are detected and resolved almost right away
- Most of the integration work is automated. This saves both time and money over the lifespan of the project. 



---


## Git workflow

![](git_w.jfif)

In the diagram above we have the Git workflow. As we can see we have different stages. 

- `git add`: Adds any changes made into the staging area where the changes are ready to be commited.
- `git commit`: Commits previously added changes with descriptive message.
- `git push`: Pushes the changes to the remote repository from our local repository. With the `push` command often times we will need to specify the branch we would like to push to. 
- `git pull`: This command is used to fetch and download content from a remote repository to our local one to match that content. 
- `git checkout`: This command lets us navigate between branches created by git branch. Checking out a branch updates the files in the working directory to match the version stored in that branch and it tells Git to record all new comits on that branch. 


---

## SDLC (Software Developemnt Life Cycle)

![](SDLC-stages.png)



SDLC is a methodology used to develop software in a systematic and structured manner. It consists of several stages, each with its own set of activities.


1. **Planning**: This is the first stage of SDLC, where the project's objectives and requirements are indentified. In this stage, the project team outlines the project scope, and create a project plan. The planning stage is a foundation for the entire SDLC process and sets the project.s direction.

2. **Analysis**: In this stage, the project team analyzes the requirements gathered in the planning stage. The team identifies the users needs, their goals, and the software requiremenets.
The team creates use cases, user stories, and functional specifications. The analysis stage determines the software's functionality and provides a detailed description of the software.

3. **Design**:  In the design stage, the project team creates a detailed technical design for the software. The team determines the software's architecture, the software's components, and the data schema. The team creates prototypes and mockups to give stakeholders a visual representation of the software's design.

4. **Implementation**: In this stage, the project teamm starts to code the software. The team uses the software design to create the software's source code and create the user interface.
This stage where the software starts to take shape.

5. **Testing and Integration**: Here the teams test the functionallity and performance of the software. The team conduct functional testing, integration testing, and performance testing.
Here we can identify any bugs and errors.

6. **Maintenance**: Once the software is deployed, it enters the maintenance stage. In this stage, the project team provides ongoing supports for the software.
They fix bugs and errors, implements new features, and performs software upgrades.
The maintenance stage ensures tha the software continues to meet the user's needs and stays up-to-date with changing technologies.


Overall, the SDLC is a structured and systematic approach to software development that provides a framework for managing the software development process from start to finish.
