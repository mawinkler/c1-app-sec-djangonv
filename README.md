# Cloud One Application Security with Django

- [Cloud One Application Security with Django](#cloud-one-application-security-with-django)
  - [Detailed Description](#detailed-description)
  - [Pre-Requisites for Usage](#pre-requisites-for-usage)
    - [Usage Instructions w/ MOADSD-NG](#usage-instructions-w-moadsd-ng)
    - [Usage Instructions w/ Docker only](#usage-instructions-w-docker-only)
    - [Exploit](#exploit)
  - [Support](#support)
  - [Contribute](#contribute)

Sample Django application for Cloud One Application Security demos, build and deployable to kubernetes with Jenkins.

## Detailed Description

This is a sample, vulnerable-on-purpose, Django application that can be used to demo Cloud One Application Security.

django-nV was created by the fine folks over at nVisium.

See:  http://github.com/nVisium/django.nV

## Pre-Requisites for Usage

* Docker
* A Cloud One Application Security account
* MOADSD-NG, Jenkins and Kubernetes

### Usage Instructions w/ MOADSD-NG

1. Create the Pipeline within Jenkins

2. Access the demoapp URL provided by MOADSD-NG

### Usage Instructions w/ Docker only

1. Download & run the container:

    ```
    docker run --rm -d -p 8000:8000 --name djangonv-app-protect -e TREND_AP_KEY=<KEY> -e TREND_AP_SECRET=<SECRET> howiehowerton/djangonv-app-protect
    ```

2. Access the app on port 8080

### Exploit

1. Follow the instructions in [exploits.md](exploits.md) to exploit the application.  Demonstrate that the exploits work against the vulnerable app.

2. Switch Cloud One Application Security rules from "Report" to "Mitigate".

3. Follow the instructions in [exploits.md](exploits.md) again. Demonstrate that the exploits **no longer** work.

## Support

This is an Open Source community project. Project contributors may be able to help, depending on their time and availability. Please be specific about what you're trying to do, your system, and steps to reproduce the problem.

For bug reports or feature requests, please [open an issue](../../issues). You are welcome to [contribute](#contribute).

Official support from Trend Micro is not available. Individual contributors may be Trend Micro employees, but are not official support.

## Contribute

I do accept contributions from the community. To submit changes:

1. Fork this repository.
1. Create a new feature branch.
1. Make your changes.
1. Submit a pull request with an explanation of your changes or additions.

I will review and work with you to release the code.
