## What is Webstra Services?
Well, it's just an GithHub Organization that I have created to organize some of my personal (portfolio) projects into one application which will be hosted in Kubernetes.
The idea was to have a few simple web applications which are  hosted in a single environment with one login for all applications.
I hope it will become a nice little set of tools for myself (and others if they are interested in using them). Furthermore, the project doubles as a larger scale portfolio which I can use to show off some of my work.

## Can you use it?
Absolutely. There will be a registration page and anyone can use the services in any way they see fit, though please do so **at your own risk**. I will always aim for code to be production-level and thoroughly tested, but this is and will always be a hobby project.

*Everything you see is likely a work in progress and subject to change as this will be a long-term project which I work on in my spare time. If you have any suggestions feel free to let me know by opening up an issue in any of the various repositories.*
  
## Some design decisions:
Due to the nature and potential scale of this project, I spent some time thinking out out to best way to structure this project. I've noted down some of my thoughts and considerations:
##### Microservice vs Monolith
The age-old discussion. I've never been a massive fan of the microservice architecture as I have never had a good use case for it. Until now....

This type of project is a good example of where I think it is very well suited. Mainly due to the fact that I want to have the ability to use various technologies or databases for the individual services so I can show off different skillsets while still using one form of authentication for all the services and not restricting myself to one database technology or one programming language. 

For example, if I want one of my services to be URL shortner in Python that has its own MySQL database but also uses a Redis Cache for frequently used URL's, that can easily be built into the project regardless of what database or backend technologies are used for other services and I can still choose to have a different microservice built in Golang and another one running in Rust. It allows me a bit more flexibility to choose whatever tools & technologies I think are best suite for the service.
It is essentially a best-of-breed-solution whilst still being a suite....

## Basic Architecture
Being fairly unexperienced with larger projects involving Docker and Kubernetes, I've tried map out what I think the k8s cluster will look like and thought out a few applications I want to include in the project. These are still subject to change or might not ever be built.
![Webstra Services Architecture (4)](https://user-images.githubusercontent.com/82543732/194874656-1489c827-a3b6-4a98-8629-951a43cd9b4e.png)




