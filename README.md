# Technical Challenge - Lalamove
## Tech/Infrastructure Intern

This exercise is designed to assess some basic knowledge of writing applications. These include, but are not limited to:
- Writing code in Golang
- Use the standard library for solving various algorithmic tasks
- Implement well-documented third-party libraries

Bonus points for:
- Thorough test cases
- Separation of logic
- optimising the amount of API calls

# Preamble
We use a lot of Open Source software at Lalamove, and we want to be able to track when new versions of all of these applications are released. The open source community has mostly settled on using Github and its releases feature to publish releases and are also mostly using Semantic Versioning as their versioning structure.

## The Challenge
We want you to write a simple application that gives us the highest patch version of every release between a minimum version and the highest released version.
It should be written in Go, reads the Github Releases list, uses SemVer for comparison and takes a path to a file as its first argument when executed. It reads this file, which is in the format of:
```
repository,min_version
kubernetes/kubernetes,1.8.0
prometheus/prometheus,2.2.0
```
and it should produce output to stdout in the format of:
```
latest versions of kubernetes/kubernetes: [1.13.4 1.12.6 1.11.8 1.10.13 1.9.11 1.8.15]
latest versions of prometheus/prometheus: [2.7.2 2.6.1 2.5.0 2.4.3 2.3.2 2.2.1]
```

In this repository you will find two go files, one main.go which contains a skeleton for you to start developing your application, and one main_test.go, which contains some test cases that should pass when the application is ready. You run the tests by writing `go test`, and there are some cases that aren't tested for - can you figure them out?

We will run your application through a number of test cases not mentioned here and compare the output with an application that produces the correct output.
