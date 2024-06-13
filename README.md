# Agriplace - Backend Assignment

## Introduction

As part of any Debian or Ubuntu operating system there is a file called `status` located in `/var/lib/dpkg/status` that holds information about software packages.
Please write a small program using Python that exposes some details about installed packages via a JSON REST API.

### The API should allow for the following operations:

- Retrieve a list of all installed packages
- View the details of an installed package: name, description, dependencies and reverse dependencies
- Dependencies (other packages that the package depends on) including a reference to how to fetch the details of a dependency
- Reverse dependencies (packages that have it as a dependency) including a reference to how to fetch the details of those packages

### Nice to have:

- Build a small FE application that allows you to visualize and navigate the packages

## Considerations

- Use Python (whichever version you are comfortable with)
- You may use the framework of your choice, or none at all, it's entirely up to you
- Write the logic for parsing the status yourself
- You may encounter alternates in the dependency list. They are presented as separated by the | (pipe) character. Try to parse and return alternates in the response.
- When returning dependencies, only return a reference (details link) if the dependency is included in the package file
- You can find an example file here: [example status file](status). Use this file as a source file if you do not use a Debian/Ubuntu OS.
- Keep track of the time spent working on the assignment. Whatever the result, please do not spend more than 8h working on the assignment. While progress with the assignment is important there are many other factors that we will consider so don’t get stuck on trying to finish everything.
- Treat this assignment as you would treat delivering production ready code
