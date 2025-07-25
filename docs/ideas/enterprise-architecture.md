---
title: Enterprise Architecture
layout: default
parent: Ideas
nav_order: 1
permalink: /ideas/enterprise-architecture
---

# Enterprise Architectrue (draft)

> July 2025

## 1. Introduction
Term Architecture was adopted into IT from the construction industry. You will not start building a house directly, but create the plans based on which the house is built. In IT, it works in the same way. Before writing code right away, it is only logical to think about what you want to build and how it will work.

Standard software development lifecycle consists of four main phases: Design, Develop, Test, and Deploy. This is relevant primarily from the perspective of one development team or a Scrum team.  Analysis for one team is usually done by a system analyst working closely with the team. The architect comes into the picture when you are working with several development teams. End-to-end visibility of the solution becomes limited from the perspective of an individual team. From experience, two or three development teams can still agree on the solution reasonably well. However, with more development teams, efficient agreement is becoming more challenging, and the role of the Architect comes into place.

Till now, we focused more on IT environment and the role of **IT Architect**. However, in most organisations, IT is only one of many departments, and it makes more sense to plan and design how the whole organisation should work. Here comes the role of **Enterprise Architect**, that is not only focusing on IT but on the organisation as a whole and looking at the ways and how the whole organisation should work and evolve.

## 2. Architecture Domains
It was already explained that the main goal of Enterprise Architect is to design how the organisation should work as a whole. The best way to achieve this task is to clearly understand where we are now (**as-is** state), and what state we want to be in the future (**to-be**). Only after that can we start identifying necessary changes that will get us to the state where we want to be. Usually, there are a lot of changes that need to be done and it is quite common to deliver these changes within several iterations. States between as-is and to-be architecture are also known as **Transition Architecture**.

A complex solution needs to be described in adequate complexity. Therefore, enterprise architecture describes the solution from different perspectives, so-called architecture domains:
- Business Architecture;
- Data Architecture;
- Application Architecture;
- Technology Architecture.

In the following chapters, we will look into each domain more in detail and describe key concepts and artefacts.

## 3. Business Architecture
The goal of every organisation is to generate value. To achieve this, a company uses resources, and one of the most important resources a company has are people. One of the first objectives of business architecture is to identify **Value Streams**. Value streams represent key objectives of the company. These objectives should be clearly communicated and visible to all employees, as every employee should participate in delivering those values. One of the key questions is whether all resources are utilised in the best possible way due to its scarcity.

The next step is to evaluate whether we have all the necessary skills, knowledge, and resources we need to deliver the value streams we identified. Sometimes it can happen that we are missing something. Missing parts are identified by the evaluation of existing capabilities and creating a **Capability Map** for the organisation as well as mapping these capabilities into the value streams.  We can realise that we are missing some key capabilities we need, or, on the other hand, some capabilities we have are no longer needed. 

Value streams and capability maps represent only a high-level perspective. Going into the detail, we will end up with the capabilities of individual **Roles** within the company as well as individual **Tasks** and **Processes** those roles are responsible for. Good starting points to understand the organisation are to look at organisational structure. People tend to be categorised based on the capabilities they have. Similarly, we can start looking into the company processes and understand daily tasks for individual roles. **Business Process Modelling Notation** ([BPMN]) helps with the proper visualisation and validation of company processes.

## 4. Data Architecture
Data Architecture focuses on key entities (objects) from the real world we need to describe and a list of attributes we need for that description. Data view represents one of the oldest diagrams for the description of the software, Entity Relationship Diagram. These can be quite complex. We need to make sure that collected data has necessary quality, is consistent and later on also available and ready to support key business decisions. Every organisation works with data from the beginning, but only lately more and more companies focus os real time analytics and reporting to support all company data with real data. With the ability to store data come more and more problems. We need to know who is the owner, who has access, where the data are stored and how they are secured. Most of the answers provide data architecture artefacts and related fields of Data Governance.

## 5. Application Architecture
This domain is the core for analysis and design of the software. There are quite a lot of notations created for better understanding of the functionality. Historically quite common is Unified Modelling Language, even though it is less used due to its complexity and readability by inexperienced users. There are a few more notations that can be used, like Archimate or C4 model. Lately, I found the C4 model particularly helpful due to its simplicity of elements and efficient description for respective audiences. 

The concept of monolithic building software is already overcome, and now comes into place the world of Microservices and Restful APIs. In this area, domain-driven design can be particularly useful, and all mentioned notations have proper support for that. At the same time, I would like to highlight the difference between diagramming and modelling, where diagramming represents a single view at a time for the purpose of one single change, while modelling is trying to describe software in a holistic way and maintain updated documentation of the software all the time.

## 6. Technology Architecture
Technology Architecture describes what technologies are used in building the solutions. It represents the used technology tech stack that is used for building the specific applications as well as how this application will be deployed and will run. Currently, we have two options for the place where the application will run. It is basically on-prem or in the cloud, where we have three main cloud providers: AWS, Azure, GCS. Regardless of the place, there are also four main options for how the application can run. It is either on physical HW, or in the virtualised environment, or being containerised. For containerised applications, we can use either Kubernetes or server-less. Both options are quite useful but give us different levels of control over the underlying infrastructure. 

## 7. Conclusion
The role of the enterprise architect is pretty wide. The person should be senior enough to bring a new perspective on the problems and be able to solve them in an efficient way. At the same time, you can ask whether you need an enterprise architect. Maybe not, but you always need to have someone who facilitates communication between teams and makes strategic decisions about technical solutions. 
Know why you are making decisions and have some documentation so you can learn from the past.

[BPMN]:
[UML]: https://en.wikipedia.org/wiki/Unified_Modeling_Language