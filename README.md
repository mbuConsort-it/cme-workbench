# CME Workbench
A DevOps toolkit for kubernetes on AWS. The workbench makes processes in a microservice world visible for developers in a non-console way.
CME is short for Consort Microservice Experience.

The toolkit is build for a medium to large size microservice setup with more than one team working in local, dev and production environments.

The toolkit addresses some of the **real world challenges** like 
- cloud security, 
- automated documentation, 
- advanced testing, 
- tool integration and 
- cost control.

<div class="warning">
CME Workbench is advanced tooling and requires some time to adapt to your infrastructure! For example the UI is secured by JWTs issued by a state-of-the-art IAM service as well as any services involved.
</div>

## What is it good for?

CME Workbench is a Angular UI with several backend microservices. The UI is used by DevOps staff to tackle daily challenges ranging from "create a new microservice" to "calculate the monthly costs for project XY".

The Workbench connects otherwise independent products to speed up the DevOps livecycle. It adds metadata around a set of microservices and forms the base for complex use cases (like documenting data flows for German DSGVO aka "Verzeichnis von Verarbeitungstätigkeiten").

![sample screen](https://github.com/consort-it/cme-workbench/blob/master/img/cme-front-browser.PNG)

The Workbench provides 30% of all use cases for an enterprise level project. Your team can enhance the toolkit with own microservices and Angular Components.

**There is no commercial version of the toolkit and there are no licenses or fees.**

## Technical requirements

You should have access to at least one Kubernetes cluster as well as a AWS account.

![basic setup](https://github.com/consort-it/cme-workbench/blob/master/img/setup.PNG)

Typically you have a lot of tooling already in place. We provide a set of tooling adapters for the most common services like GitLab or Jenkins. Because **all components are open source** you can adapt the workbench to any DevOps configuration.

There is no setup necessary apart from installing the adapters in a separate Kubernetes namespace and a AWS Cognito Userpool. You can even run the CME Workbench UI locally.

## Directory of components

The CME workbench is composed of the following components:

Component | Description | Required
------------|----------|-------------
Angular UI | The user interface, can be started without any backend service for demo purposes | yes
GitLab Adapter | Creates microservices in new GitLab/GitHub repositories | no
Kubernetes Adapter | Reads runtime configuration from any Kubernetes Cluster | recommended
Jira Adapter | Reads tasks from Jira | no
Confluence Adapter | Used by Jenkins job to update documentation pages | no

