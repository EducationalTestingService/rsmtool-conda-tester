## Introduction

This project is to test the Linux and Windows conda packages for [RSMTool](https://github.com/EducationalTestingService/rsmtool). We do not test macOS packages; we assume that if Linux packages work, so will the macOS packages.

To test a new package version that has been already built and uploaded to the official RSMTool conda [channel](http://anaconda.org/desilinguist), create a new branch, change the `RSMVERSION` values in both `.gitlab-ci.yml` and `azure-pipelines.yml` to the version you want to test, and submit a pull request for the branch. If both builds pass, merge the PR. 

The packages are tested by creating a new conda environment with the specified RSMTool version installed. The code for RSMTool is also checked out in a separate directory and then the tests are run with the installed rsmtool package in the environment.

These builds should only be run right before doing an RSMTool release.
