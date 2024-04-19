# 🔬 Tool Support for Evaluating the Performance of List-Based Algorithms

![Platforms: Linux, MacOS, Windows](https://img.shields.io/badge/Platform-Linux%20%7C%20MacOS%20%7C%20Windows-blue.svg)
[![Commits: Conventional](https://img.shields.io/badge/Commits-Conventional-blue.svg)](https://www.conventionalcommits.org/en/v1.0.0/)

## 🏁 Introduction

There are numerous algorithms that process a list of values. The purpose of this
algorithm all-hands assignment is to design, implement, test and then use in an
empirical study a tool that can automatically conduct doubling experiments to
measure the performance of an arbitrary list processing algorithm. The tool that
you implement, tentatively called `bosco`, should operate in a fashion that is
as general-purpose as is possible. This means that it should, whenever possible,
be able to automatically detect and invoke a list-processing function in a
provided Python source code file, determine the type of list that is input into
that function, and then generate data that is suitable for the purposes of
running a doubling experiment to identify its likely worst-case time complexity.

Ultimately, this algorithm all-hands assignment invites you to apply what you
learned in the algorithm analysis course, by implementing a benchmarking
framework that operates in the following fashion:

- Accept as input one or more Python source code files that contain one or more
functions that perform list processing. For the purposes of creating your
benchmarking framework you can assume that all list-processing algorithms will
implement some type of function that accepts as input a list and that it will be
this list whose contents are doubled during the execution of a doubling
experiment.
- Accept as input the fully-qualified name of a list-processing function that
should be subject to benchmarking through a doubling experiment.
- Accept as input the description of an input generation procedure that can
automatically generate data suitable for the purposes of conducting a doubling
experiment to evaluate the performance of the list-processing algorithm.
- Automatically extract the list-processing function from the provided Python
source code file(s) and then reflectively invoke the function to sort data that
was automatically generated.
- In a series of automatically completed benchmarking rounds, the tool should
conduct a doubling experiment by which it generates data sets of increasing size
and then uses them to evaluate the performance of the list-processing algorithm.
- The tool should produce diagnostic data that shows the execution time for each
round of the doubling experiment, a computed version of the doubling ratio based
on the collected data, and a statement about the likely worst-case time
complexity suggested by the doubling ratio.
- Your tool must be implemented with the Python programming language and use the
Poetry system for managing dependencies and packaging.
- Your tool must provide a command-line interface implemented through the use of
Typer and offer command-line arguments that fully support its configuration.
- Your tool can leverage Python source code that you previously implemented as a
part of a course project as long as you carefully document the source of any
Python code segments.

As you work to build and evaluate this system in a team-based fashion, please
keep in mind the following considerations and tasks:

- Organize your class, which comprises the team for this algorithm all-hands
project, into sub-teams organized around completing the following task:
    - **Infrastructure**: Using the provided GitHub repository for the `bosco`
    project, this members of this sub-team will define and implement a process
    for reviewing and merging the tool's source code, setup and configure GitHub
    Actions, make releases of the tool to PyPI, and handle all other
    infrastructure-related tasks.
    - **Benchmarking Framework**: The members of this sub-team will specify,
    design, implement, and test the `bosco` tool, ensuring that it correctly
    runs a doubling experiment for any type of list-processing algorithm that
    meets the stated expectations of the tool.
    - **List-Processing Algorithms**: The members of this sub-team will identify
    and commit a wide variety of list-processing algorithms, working in a
    separate GitHub repository that they work with the infrastructure team to
    create and manage. The members of this team are also responsible for running
    the `bosco` tool on each of the list-processing algorithms and confirming
    that the tool produces the expected output. When this team discovers that
    `bosco` does not work correctly for a specific list-processing algorithm,
    they will work with the members of the benchmarking framework team to ensure
    that the tool is correctly implemented to handle the identified issue.
    - **Experimental and Analytical Evaluation**: The members of this sub-team
    will complete the article published to the algorithm all-hands section of
    the Algorithmology web site. In addition to writing the article, the members
    of this team will perform a preliminary analytical evaluation of each
    function identified by the team tasked with finding the list-processing
    algorithms. The team members will use the results of their analytical
    evaluation to guide their use of the completed `bosco` tool when running a
    doubling experiment to evaluate the performance of each algorithm. This team
    will also write the final report and work with the course instructor to
    publish it to the Algorithmology web site by the following Friday.
- Meet in your assigned groups to discuss how your team is going to design,
implement, test, and evaluate your benchmarking framework. Make sure that you
give your benchmarking framework a descriptive name that reflects its purpose.
- Discuss with your team members which GitHub repository you are going to use to
coordinate your work. As you make this decision, please bear in mind that the
final version of your framework will be transferred to the course's GitHub
organization and so that it may be considered for use in follow-on projects.
- Specify, design, and implement a benchmarking framework that supports the
experimental evaluation of any list-processing algorithm function that you and
your team members agree your benchmarking framework should support.
- Collect a group of list-processing algorithms and use them to conduct a series
of doubling experiments that experimentally evaluate their performance with the
ultimate goal of determining which algorithm is the fastest and characterizing
the likely time complexity of each algorithm.
- Write and publish on the course web site a blog post that explains (a) how you
designed and implemented your benchmarking framework, (b) the list-processing
functions that you chose to use in your doubling experiments, (c) the runtime
results from your experimental study with the benchmarking framework that you
implemented and (d) the running time results from an analytical evaluation that
you conducted. Your blog post should clearly articulate (a) whether or not the
experimental and analytical results for your function are in alignment with each
other, (b) what is most likely to be the realistic runtime and true running time
of a list-processing function, and (c) why you judge that your function has this
runtime and running time.
- Present your findings to the entire class during the following week of the
academic semester during the follow-on algorithm all-hands session. One member
from each of the sub-teams should play a role in the presentation given during
the algorithm all-hands session.
- Please note that all of the work that you complete for this assignment should
be published to the course web site. Following the aforementioned requirements
for each of the sub-teams, your overall team must create and contribute to a
pull request on the course web site's GitHub repository and ensure that your
work is reviewed, revised, and published in advance of the Friday class session
for next week. Importantly, your implementation of the benchmarking framework
and the list-processing algorithms should be available in one or more additional
GitHub repositories that are referenced in the blog post that you write.

It is important to point out that your repository for this project was created
from the GitHub repository template called
[list-processing-tools-starter](https://github.com/Algorithmology/list-processing-tools-starter);
you can check this repository for any updates to this project's documentation or
source code! Finally, the teams and their corresponding functions will be
assigned through an announcement in Discord; check there for more details!

## 🤝 Seeking Assistance

Even though the course instructor will have covered all of the concepts central
to this project before you start to work on it, please note that not every
detail needed to successfully complete the assignment will have been covered
during prior classroom sessions. This is by design as an important skill that
you must practice as an algorithm engineer is to search for and then understand
and ultimately apply the technical content found in additional resources.

## 📚 Project Details

TODO: Please make sure that you complete and document the following steps:

- TODO: Sign your pledge in this file to indicate that you adhered to the Honor
Code while completing this assignment.

- TODO: Provide a reference to the GitHub repository that your team used to
store the work that your sub-team completed. Make sure to count and report the
number of commits that you made to this GitHub repository.

- TODO: Add a reference to the blog post that you and your team members wrote.

- TODO: Write at least two sentences to explain the key role(s) that you played
in completing this team-based project. Your response to this part of the
question should carefully explain the role that you took in your assigned
sub-team and how you contributed to the completion of the overall project.

- TODO: Write at least one sentence to describe the contributions of each of the
other people who are in your sub-team.
