---
layout: default
---

# Project Overview

The largest chunk of the work for this course will be developing your semester project.  It will be worth a total of 45 points, plus an additional 12 points associated with your weekly updates.

Your final grade on the project will be based on three factors:

## 1. Functionality (20 points)

Early in the semester we will develop a set of ambitious goals for your project.  You will earn points based on how well you meet these goals, with a series of milestones over the course of the semester. In some circumstances these goals may be adjusted based on revised information and any changes that we may need to introduce to your project.  The instructors will be in regular communication about your progress and you will be heavily involved in any such changes.

## 2. Code Quality (20 points)

While the ultimate functionality of your code is clearly important, being able to write code that is reliable, reusable and easy to understand by other programmers is also a high level goal for this course.  Code quality will be judged based on:
+ **_Code Style_**: Have you chosen a style that is informative?  Are you consistent in your style?
+ **_Code Readability_**: Is your code easy for others to read and understand based on your maintenance of documentation, code comments, and a clean layout with short clear functions?
+ **_Code Modularity_**: Have you built useful functions and classes that are organized with a meaningful file and directory structure? 
+ **_Code Reliability_** Do you have thorough unit test coverage with effective use of in-code asserts and/or other error checking, and do you avoid undefined behaviors?

You will be getting regular in-class advice and feedback on these topics throughout the semester.


## 3. Individual Contributions (5 points)

While the larger portion of your project grade will be based on the overall group project, it is important that each group member provides a meaningful contribution.  Based in part on ratings by your teammates (and audited by the instructors using progress reports, git logs, and the work agreement if needed) you will receive a qualification for how effective of a contributor you were to the group project.

+ **_Proficient Contributor_**: You have met all of the expectations and delivered your portion of the project.  You worked diligently on the project throughout the semester and were a reliable member of the team.  You will receive the full five points for this section.

+ **_Inconsistent Contributor_**: While this person has participated and contributed to the project, they have done so inconsistently and haven't fully met the group's expectations. They might have missed some tasks or not been substantially involved in the discussions or implementation.  No points will be giving for individual contributions, but the student will still receive other project points.

+ **_Minimal Contributor_**: This denotes a member who has not actively participated in the project. Their contribution is negligible or missing, and their lack of involvement has hampered the group's overall progress.  Not only will no points be given out for individual contributions, but the overall project grade will be substantially reduced.

Additionally, we have two other categories that will be given out sparingly.

+ **_Resilient Contributor_**: You have showcased exceptional efforts, going above and beyond base expectations to enure that your group turns in a working project. You will receive the full five points from contributions AND may recoup some points back (typically 5) from the previous two grading factors, replacing lost points in other areas of the project.  This rating will typically be given to a student who put forth significant extra effort to make up for another group member's failure to meet expectations.

+ **_Exemplary Contributor_**: You went substantially beyond project requirements, turning in code that is impressive on all levels.  You will receive the full 45 points on the project, but this qualification also recognizes the incredible effort that you put forth.


# Project Topics

Each group will work on a component of a larger, modular agent-based system.  Depending on which components are chosen by teams, we will be producing either a game, a scientific simulation, or both.  Individual components will require different sets of skills.

Each executable will be composed of at least three modules:
1. A **World**, which implements the environment where the agents will be interactions.
2. One or more **Autonomous Agent** classes, which define the types of agents in the system and their capabilities, and
3. An **Interface**, which can either be a mechanism for a human to interact with the system or data collection tools to merely output the results of a simulation.

Each of the eight groups will work on one Module.  Ideally we will aim have at least two groups working on modules from each category.  Each module should have features about it that make it challenging to implement.  We will also build a simple version of each module type live in class, as well as talking about how to deal with the specific challenges.

## World Modules

World modules must implement the mechanisms of interactions between agents and the world or agents and each other, as well as any background activity of the world.  Some possible types of world modules include:

+ A world where lots of actions happen in the background and need to be processed efficiently.  For example, a resource acquisition game with forests growing, animal herds wandering around, or seasons changing.  May types of systems could have significant background events.
+ A world where player actions may have substantial secondary effects that need to be continuously monitored.  For example, in a game like https://splix.io/, agents leave a trail behind them and they system must identify closed loops or players braking each other's trails.  Many more complicated changes due to player actions are also possible.  Keeping such a system running in real-time is critical for fun game play.
+ A world that handles a many types of agent-agent interactions. For example, a wizard arena where agents cast spells at one another that have rules for how they interact. A challenge here would be balancing the different types of interactions an making sure that all of the combinations are handled appropriately and efficiently.
+ A real world scientific simulator environment.  For example, a traffic simulator to analyze travel time, or an ecology simulator to understand biological system stability.  A challenge here would be learning enough about the real-world systems for the simulation to be accurate.

The above examples illustrate types of challenges groups could tackle, but you should skin them however you want.  A D\&D-style dungeon?  A puzzle game?  A military tactics simulator? Space exploration? Any style is okay, although it must be agent-based and we do recommend that you don't make the world overly complicated.

## Autonomous Agent Modules

The above worlds all have agents moving through them.  These can be in the form of players (see next section) or those agents can be autonomous.  Some groups will be building capabilities for autonomous agents.  Some possible modules for autonomous agents include:

+ Manual AI that must be coded in C++ for a given game, but comes with a large toolbox of pre-defined behaviors for things like finding the shortest path, intercepting another agent, patrolling a given area, etc.  It should be a non-trivial set of available behaviors that are designed in coordination with the needs of the world teams.
+ Dynamic / Programable (Interpreter).  In this case you wouldn't build all of the behavior tools yourself, instead you would write a language to let the end-user do so more easily.  The world would provide interaction capabilities used to generate the agent from a config file.
+ Machine Learning AI - this would be an AI system that is trained in the given world type.  The underlying representation can be whichever one you are most interested in or familiar with, such as neural networks, evolved agents, etc.  One challenges associated with this project type is that you will likely want to make use of an external library that you would need to find and learn.

## Interface Modules

Interface modules provide mechanisms for the system user to interact with or at least observe the results of the world and agents.  Some interfaces may give the user control over an agent, while others would simply collect data and either display it to the screen or at least save it to file.  More specific options might include:

+ A 3D first-person interface to control an agent.  Such a project would require you to learn an external 3D graphics library in C++, such as Open-GL.
+ A web-interface to control an agent.  While this project would probably focus more on a top-down view of the world, it would be fully accessible on the web.  This project would require you to learn a C++-to-WebAssembly compiler like Emscripten.
+ A network-based interface.  This project would allow a user to control an agent from over a network, and ideally allow many different users to all interact with the same world.  Again, it would require students to identify and learn an external networking library.
+ A data-collection and analysis module.  This project wouldn't build an interface to an agent, but it would collect substantial information from a run.  For example, it might track the density of where different types of agents spend their time, or catalog the interactions among agents.

Other types of user-interfaces could also be available and can be proposed by students.


# Project Groups

You will be in a group of three to four people to work on one of the above modules as a semester-long project.  Students will have the opportunity to discuss potential project ideas with each other and propose groups to the instructors.  The instructors will also help students form groups as needed, trying to match appropriate skill combinations and interests.

Once groups are formed, members will devise a working agreement with a plan for how they will all contribute to the project and support one another.  Here is an [example agreement](example_agreement.html).