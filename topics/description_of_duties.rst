Main Functions
--------------
I work as a software engineering intern, I work with an infrastructure team based mainly in Bangalore, India. 
Even so, this is still a multinational team, consisting of team members across India, Ireland, and the USA.
All of us are working on developing an internal tool for Qualcomm engineers. This tool is a full stack app that 
comes with a GUI interface and a CLI option. I don't work on the front-end part, I work on the back-end of the project, 
mainly developing and testing APIs and CLI.

My scope of work in this team project is quite broad. I am responsible for:

#. New feature implementation with unittesting, good coverage and pylint scores

    I get tasked to implement new software features, new APIs, or just enhancing current APIs by adding more functionalities
    requested by our clients. Normally, before I write code, I will first come up with the unittests that are 
    relevant to the task specification. This process is called Test Driven Development \(TDD\). I learnt this through
    a Python training provided by an engineer in Qualcomm. This will result in higher code coverage score because 
    I am only writing code that is needed by the unittests to pass. 
    Coverage is a measure, noting what parts of the code have been executed, mostly used to test the 
    effectiveness of tests that I have written. Pylint is a code analysis tool to identify errors in Python code and helps
    developers enforce good coding style and habits. I always strive for the highest possible coverage and pylint scores when coding.

#. Debugging and fixing bugs

    I also do spend some time debugging and fixing bugs from the tickets I got assigned to. 
    Some of the tickets are raised by us developers internally, while some others are raised by
    our clients from other teams. I also help out my team debugging together at times via pair programming, 
    I believe two pairs of eyes normally discover the bugs twice as fast.

#. Setting up and the maintenance of our project documentation via Sphinx

    Before I joined, the project documentation is only hosted on confluence. 
    It wasn't very detailed or tidy. So I took the initiative to suggest the team that we should 
    use Sphinx to document our project.
    The team liked the suggestion and so we started documenting our code. 
    Since then, Sphinx documentation is integrated into the release of our software, 
    and will continue to be included for the future releases.

#. Refactoring and rearchitecting parts of the codebase to meet requirements change with good standards

    Sometimes, I get tasked with some code refactoring tasks. The point of these tasks are basically to improve 
    code quality, readability, performance and maintainability. Some other times, refactoring is required because
    of change in requirements. In software engineering, requirements change all the time, and so must the software.
    When doing code refactoring, I always take it as a chance to improve the standard and the quality of the code architecture.
    The team mainly codes in Python in this project, and in Python, there is this thing called the ``Zen of Python``, 
    which is basically a collection of 19 "guiding principles" for writing computer programs that influence the design 
    of the Python programming language. The team is highly encouraged to follow the Zen of Python and any good software 
    engineering principles in general as closely as possible. 


Software/Technologies used
--------------------------

Development Environment
~~~~~~~~~~~~~~~~~~~~~~~
For my environment, I mainly connect and use the remote desktop located outside of Ireland.
The remote desktop is a Linux system desktop machine, where all engineers share resources
in a shared file system. For coding, I choose Visual Studio Code on my local machine as my preferred IDE.
There is an extension in VSCode that allows me to connect to my remote desktop and code as if I am 
using my remote desktop. I have a ton of other extensions in VSCode that improves my productivity
such as vim key binding plugin, intellisense plugins, python plugins and many others. For quick note
taking or drafting code snippets, I use sublime text for it. 

Project Tech Stack and Workflow
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
As for the team project I am working on, we use Python for the most part. Main components include: 
Python Flask for the GUI part, argparse library for the CLI, SQLAlchemy for the database management system.
For version control, we use Git. And we use GitHub for our source code management. Our workflow is as follows:
when we want to create a new feature or fix a bug, we create a feature branch based on the current
development branch. When we have completed the feature or fixed the bug, we create a pull request to merge
into the development branch. Here, we have some unittest checks automatically triggered to check if this new
pull request will break anything. If all goes well in code review and the tests, it will be merged into 
the development branch. When a release is ready, we will merge the development branch into the release 
branch. This way, the release branch will always be stable, and not prone to bugs. We then will also tag the
HEAD of the release branch and make a release on GitHub, along with all the release notes.

Issue Tracking System
~~~~~~~~~~~~~~~~~~~~~
Qualcomm uses Jira as the issue and project tracking tool. This is the main platform where we 
manage all our project related tickets. Whenever someone reports a bug, or want to start building 
a new feature, or have a query on something, Jira will be used to keep track of all issue tickets.
We can give description, comment, assign an engineer, CC people that should be aware of the ticket,
and many more. 

Documentation
~~~~~~~~~~~~~
For documentation, our team used to use Confluence for all sorts of topics. However, we have transitioned
to using Sphinx recently as it is the smarter and more efficient choice to document a project. Sphinx is 
a tool that makes it super easy to create intelligent and beautiful documentation. One amazing feature Sphinx has 
is the ability to automatically read the doc strings of the source code and generate documentation for it. 
Sphinx takes in plain-text files in ``reStructuredText`` format and transforms it into HTML, PDF, and any
other format desired. The main selling point is that everything is automatically generated, there is little 
to none effort required to style the documentation.

Tests
~~~~~
For writing unittests, we use the python built-in unittest library to write all our tests.
We also use pytest to run our tests, as they are both compatible to be used together. We also have
a unittest base class set up, so whenever a new test needs to be written, the developer just needs
to inherit that base class, and all the setUpClass and tearDownClass logic will be handled and taken
care of.

CI/CD
~~~~~
For CI/CD, we use Jenkins to handle all our builds. We have set up nightly builds, which will run all
test suites once every day to make sure everything in production and development is stable. We also set 
up a GitHub hook so that whenever a developer makes a pull request, a jenkins build will be triggered to run all tests.
The team will receive an email on the result of the build, if the build passes, that means the Pull Request is
safe to be merged, otherwise, there is still some work to do there.
