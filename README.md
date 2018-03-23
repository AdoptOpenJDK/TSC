# AdoptOpenJDK TSC and Knowledge Base

## Contribution

We welcome any contributions big or small from experienced OpenJDK folks to those who are brand new to software projects!

To start, make sure you sign up to the [AdoptOpenJDK Slack](https://adoptopenjdk.net/slack.html), say hello and please read 
the [Contribution Guide](https://github.com/AdoptOpenJDK/TSC/CONTRIBUTING.md).

# Knowledge Base

## Overview

TBA - Diagrams to come

## Dependent Projects
These projects are located in the following repositories in rough order of importance with regards to understanding how 
the build farm is put together and works.  Each repository maintains its own set of issues, pull requests and 
documentation:

* [Technical Steering Committee (TSC)](https://github.com/AdoptOpenJDK/TSC) - The Technical Steering Committee and Knowledge Base starting point
* [openjdk-infrastructure](https://github.com/AdoptOpenJDK/openjdk-infrastructure) - Infrastructure as Code and documentation for build farm hosts
* [openjdk-build](https://github.com/AdoptOpenJDK/openjdk-build) - Code and instructions for building Adopt OpenJDK Binaries
    * [openjdk-docker](https://github.com/AdoptOpenJDK/openjdk-docker) - Scripts for creating Docker images of OpenJDK binaries.
    * [openjdk-installer](https://github.com/AdoptOpenJDK/openjdk-installer) - Installer files for creating platform packaged OpenJDK binaries

* [openjdk-tests](https://github.com/AdoptOpenJDK/openjdk-tests) - Instructions and CI automation scripts for all AdoptOpenJDK testing, code for app, performance and regression testing Adopt OpenJDK Binaries
    * [openjdk-systemtest](https://github.com/AdoptOpenJDK/openjdk-systemtest) - Code and instructions for load and system testing AdoptOpenJDK Binaries
    * [openjdk-stf](https://github.com/AdoptOpenJDK/openjdk-stf) - The System Test Framework, a harness for executing [openjdk-systemtest](https://github.com/AdoptOpenJDK/openjdk-systemtest)
    * See [Private Repos](https://github.com/AdoptOpenJDK/TSC#private-repos) for JCK related test repos
* [openjdk-website](https://github.com/AdoptOpenJDK/openjdk-website) - Code and instructions for https://www.adoptopenjdk.net
    * [openjdk-api](https://github.com/AdoptOpenJDK/openjdk-api) - Code and instructions for https://api.adoptopenjdk.net
    * [openjdk-website-backend](https://github.com/AdoptOpenJDK/openjdk-website-backend) - Code for pulling the GitHub releases API into the website 

### Release AdoptOpenJDK binaries

* [openjdk8-releases](https://github.com/AdoptOpenJDK/openjdk8-releases/) - AdoptOpenJDK main binary releases for OpenJDK 8 with HotSpot
* [openjdk8-openj9-releases](https://github.com/AdoptOpenJDK/openjdk8-openj9-releases/) - AdoptOpenJDK main binary releases for OpenJDK 8 with Eclipse OpenJ9
* [openjdk9-releases](https://github.com/AdoptOpenJDK/openjdk9-releases/) - AdoptOpenJDK main binary releases for OpenJDK 9 with HotSpot
* [openjdk9-openj9-releases](https://github.com/AdoptOpenJDK/openjdk9-openj9-releases/) - AdoptOpenJDK main binary releases for OpenJDK 9 with Eclipse OpenJ9
* [openjdk10-releases](https://github.com/AdoptOpenJDK/openjdk10-releases/) - AdoptOpenJDK main binary releases for OpenJDK 10 with HotSpot
* [openjdk10-openj9-releases](https://github.com/AdoptOpenJDK/openjdk10-openj9-releases/) - AdoptOpenJDK main binary releases for OpenJDK 10 with Eclipse OpenJ9

### Nightly AdoptOpenJDK binaries

* [openjdk8-nightly](https://github.com/AdoptOpenJDK/openjdk8-nightly/) - AdoptOpenJDK main binary nightlies for OpenJDK 8 with HotSpot
* [openjdk8-openj9-nightly](https://github.com/AdoptOpenJDK/openjdk8-openj9-nightly/) - AdoptOpenJDK main binary nightlies for OpenJDK 8 with Eclipse OpenJ9
* [openjdk9-nightly](https://github.com/AdoptOpenJDK/openjdk9-nightly/) - AdoptOpenJDK main binary nightlies for OpenJDK 9 with HotSpot
* [openjdk9-openj9-nightly](https://github.com/AdoptOpenJDK/openjdk9-openj9-nightly/) - AdoptOpenJDK main binary nightlies for OpenJDK 9 with Eclipse OpenJ9
* [openjdk10-nightly](https://github.com/AdoptOpenJDK/openjdk10-nightly/) - AdoptOpenJDK main binary nightlies for OpenJDK 10 with HotSpot
* [openjdk10-openj9-nightly](https://github.com/AdoptOpenJDK/openjdk10-openj9-nightly/) - AdoptOpenJDK main binary nightlies for OpenJDK 10 with Eclipse OpenJ9

### Clones of OpenJDK Forests 

* [openjdk-jdk8u](https://github.com/AdoptOpenJDK/openjdk-jdk8u)
* [openjdk-jdk9](https://github.com/AdoptOpenJDK/openjdk-jdk9) - **TODO** move this to jdk9u
* [openjdk-jdk10](https://github.com/AdoptOpenJDK/openjdk-jdk10)

### Private repos

Due to security or licensing concerns the following repos are private.  Please raise an issue on the 
 [Infrastructure Project](https://github.com/AdoptOpenJDK/openjdk-infrastructure) if you think you need access.

* [secrets](https://github.com/AdoptOpenJDK/secrets) - For holding some secrets
* [JCK8](https://github.com/AdoptOpenJDK/JCK8) - code and documentation for running JCK8
* [JCK9](https://github.com/AdoptOpenJDK/JCK9) - code and documentation for running JCK9+
* [JCK-results](https://github.com/AdoptOpenJDK/JCK-results) - for storing JCK results
* [openjdk-website-staging](https://github.com/AdoptOpenJDK/openjdk-staging-webiste) - for staging website PR's

# The TSC

*NOTE* This section is a DRAFT and has not yet been fully discussed or ratified by the AdoptOpenJDK community at large.

## Proposed List of TSC Responsibilities
The TSC exercises autonomy in setting up and maintaining procedures, policies, and management and administrative structures as it deems appropriate for the maintenance and operation of these projects and resources.

Included in the responsibilities of the TSC are:

* Managing code and documentation creation and changes for the listed projects and resources
* Meeting monthly to discuss progress and other TSC issues
* Setting and maintaining standards covering contributions of code, documentation and other materials
* Managing code and binary releases: types, schedules, frequency, delivery mechanisms
* Creating new repositories and projects under the _AdoptOpenJDK_ GitHub organisation as required
* Setting overall technical direction for the AdoptOpenJDK organisation, including high-level goals and low-level specifics regarding features and functionality
* Has a relationship with the AdoptOpenJDK security group for dealing with vulnerabilities in an appropriate manner
* Setting and maintaining appropriate standards for community discourse via the various mediums under TSC control

## TSC Members

TSC members can nominate new members at any time. Candidates for membership tend to be people
who have a competency for community management and a high tolerance and patience for process
minutiae as the TSC delegates most of its responsibilities to other teams.

Every Dependent Project not currently incubating can appoint someone to the TSC who they elect
at their own discretion.

### Current Members
| Avatar | Information |
|---|:---|
|TBA|TBA |

## Proposed Rules for TSC Membership
* No single company can occupy more than 1/3 seats on the TSC
* The appointing of TSC members occurs on an annual basis and is based on a meritocracy. 
* Candidates with the intention of becoming a member of the TSC should briefly outline where they'd like to see the project going - all in a transparent manner that is available to the public.

Thanks!
The AdoptOpenJDK Community.
