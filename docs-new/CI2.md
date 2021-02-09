---
layout: default
title: Continuous Integration
parent: Changes
---

# Continuous Integration

[Deliverable (.pdf)](../assets/deliverables-new/CI2.pdf){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 }

{: .no_toc }

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>

---

At the beginning of implementing continuous integration to our project we decided to use Travis CI as it was widely available and a popular choice for Continuous Integration. However, we soon ran into a couple of issues. We kept getting errors about our build.gradle file, however it was working fine when built locally. Because of this issue, we decided that Github Actions will be easier to set up and use, as well as that it has better documentation, if any errors occurred.

We have set up our CI to work with VSC (which we are using Github), so when anyone pushes code into a branch and makes a pull request, the continuous integration checks if there is a file with an extension .yml in .github/workflows folder, which is the configuration file for CI. If it exists, it runs the file, and after everything is done the person will be notified of the result (whether everything passed or failed). In the case of everything passing, the branch then can be merged to development.

The continuous integration infrastructure is depicted by the diagram below

![](../assets/static/new/CI2.001.png)

After the changes are pushed to the development branch, they are tested by other developers, if everything is working as expected, then the development branch is merged to the production branch, which is the stable branch for use.

Github actions runs a file called gradle.yml, as seen below:

![](../assets/static/new/CI2.002.png)

It creates a virtual machine that is running the latest version of ubuntu and executes the given steps.

First it downloads the repository, configures Java 1.8 JDK, grants permission to use gradle wrapper command gradlew and then runs ./gradlew build which builds gradle.

The build command checks all of the code as well as runs all of the tests. Once everything is completed, it produces a result.

Github Actions allows us to check what the CI is executing and if there is an issue; where the issue is located. This helps track issues with both CI (whether mistakes were made writing the config file for CI) as well as any other issues regarding tests failing and code not being built.
