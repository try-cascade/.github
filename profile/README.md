![Cascade logo](https://i.ibb.co/88LznWt/Risorsa-17s.png)

# Open-source containerized application deployment with observability

Cascade is an open-source **containerized application deployment** solution with **observability** built in. 
Users can add their containerized applications and Cascade will generate the Terraform config files to deploy each application alongside a collector container onto AWS.

It's **a containerized application deployment accelerator**; it builds and deploys a cloud infrastructure for containers with a side collector for distributed tracing.

Cascade is a fullstack deployment tool that's:
- **Easy to install**: runs on Docker 
- **Easy to use**: automates deployment process with a few clicks
- **Open source**: provides base Terraform templates to build upon

[![Version](https://img.shields.io/badge/npm-1.0.0-green)](https://www.npmjs.com/package/cascade-agent)

### Brief Overview
Plan in 3 Steps           |  Deploy and View Progress
:------------------------:|:------------------------:
![welcome gif](https://i.ibb.co/j418gnq/welcome.gif)|![deploying gif](https://i.ibb.co/PmGx7Rw/deploystack.gif)



## Table of Contents
- [Who it's for](#who-its-for)
- [What Cascade does](#what-cascade-does)
- [Prerequisites](#prerequisites)
- [How Cascade works](#how-cascade-works)
- [Cascade Compose](#cascade-compose)
- [Team](#team)

## Who it's for
Cascade was built for users who wish to:

- Deploy their containerized applications onto AWS ECS Fargate
- See logs and traces without manual effort

## What Cascade does

- Configures the minimum AWS infrastructure required to deploy a containerized app
- Reduces the need to navigate through the AWS management console
- Sets up logs and traces by default

## Prerequisites

- Instrument with [`cascade-agent`](https://www.npmjs.com/package/cascade-agent)
- [Configure AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-configure.html) 
- Run Docker daemon
- Define a container image file


## How Cascade works

Cascade depends on 3 parts:
1. [`cascade-agent`](https://github.com/try-cascade/cascade-agent): the instrumentation that generates traces, and sends it to AWS X-Ray
2. [`cascade-backend`](https://github.com/try-cascade/cascade-backend): the API server that creates a user-specific S3 bucket for container information, and generates Terraform config files for deployment
3. [`cascade-gui`](https://github.com/try-cascade/cascade-gui): the GUI where users can deploy their containerized application, access the generated Terraform config files, and view logs and traces


## Cascade Compose

You can run [Cascade with Docker](https://github.com/try-cascade/cascade-compose) by following these steps:
1. Run the Docker daemon
2. Clone the `cascade-compose` directory
3. `cd` into `cascade-compose` and execute `docker-compose up`

```bash
git clone https://github.com/try-cascade/cascade-compose.git && cd cascade-compose && docker-compose up
```

Cascade will now be ready to plan and deploy your containerized application. You can access the GUI at port 3000.

## Team

**SF Bay Area, CA**
- Anne Tiotuico ([LinkedIn](https://www.linkedin.com/in/annetiotuico/), [GitHub](https://github.com/AnneTiotuico))

**Austin, TX**
- Natalie Thompson ([LinkedIn](https://www.linkedin.com/in/natalie-thompson-61a116110), [GitHub](https://github.com/NatalieAThompson))

**Chicago, IL**
- Rona Hsu ([LinkedIn](https://www.linkedin.com/in/rona-h-a48640246/), [GitHub](https://github.com/Macaroni2629))

**Denver, CO**
- Yueun Kim ([LinkedIn](https://www.linkedin.com/in/yueunk/), [GitHub](https://github.com/yueunk))
