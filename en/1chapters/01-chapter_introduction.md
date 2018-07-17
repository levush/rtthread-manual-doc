# Introduction #

[RT-Thread] (http://www.rt-thread.org) is an open source embedded real-time operating system developed by the Chinese open source community (following the GPLv2+ license agreement, when the logo product uses RT-Thread It is applied in commercial products according to its own non-open source code. It contains various components related to real-time embedded systems: real-time operating system kernel, TCP/IP protocol stack, file system, libc interface, graphics engine, etc.

This manual is the manual for the RT-Thread open source embedded real-time operating system.

## RT-Thread's Software Structure ##

![RT-Thread Software Structure](../../figures/System_Arch.png)

The RT-Thread real-time operating system is a layered operating system that includes:

* The underlying porting and driver layer. This layer is closely related to the hardware and consists of Drivers and CPU porting.
* Hard real-time kernel, this layer is the core of RT-Thread, including the implementation of objects in the kernel system, such as multi-threading and its scheduling, semaphores, mailboxes, message queues, memory management, timers, etc.
* Component layer, these are peripheral components based on RT-Thread core, such as file system, command line shell interface, lwIP light TCP/IP protocol stack, GUI graphics engine, etc.

In the design and subsequent development direction, RT-Thread will try to maintain the characteristics of RT-Thread itself:

* Compact core and peripheral components;
* Clear, simple, low-coupling system structure;
* Object-oriented, UNIX-like programming style;
* The way to be as compatible as possible with the POSIX portable operating system interface;

## Development, Maintenance ##

The main development members of RT-Thread are from China. They mainly use RT-Thread development and maintenance in their spare time. They also accept developers, enthusiasts, and professional embedded companies to donate code to RT-Thread. In Shanghai, there is also a service company specializing in RT-Thread technology services: [Shanghai Ruiside Electronic Technology Co., Ltd.] (http://www.rt-thread.com).

RT-Thread is developed and released in one year. Each version of RT-Thread sets a target, and the next year's development cycle is developed, evolved, and promoted in the form of a test version per quarter. The released version includes two types:

* One is the official version (or stable version, maintenance version), such as the official version of 2.0.x, which is the bug fix version of the 2.0.0 official version. Functionally, no new features are added, and emphasis is placed on fixing bugs;
* One is a test version (or development version), such as the 2.1.0 beta version. It evolves with a one-year target set, a well-established version that is relatively less stable, but with new features and an exploration of new routes;

Each development version will set development goals in advance, usually through mail and forums. At the same time, there will be one or two developer conferences in China each year. The conference will discuss the goals of the new version, or the larger version. New directions.

In the development activities, RT-Thread is similarly divided into three parts according to the above software architecture:

* Kernel (kernel), this is the core of RT-Thread, but also fundamental;
* Component, based on the core, divides some functional modules into independent component modules, achieving low coupling between components and components, and high internal cohesion within components;
* branching, this is a chip migration supported by RT-Thread, peripheral drivers, etc.;

Each of these three parts has a maintainer, and the maintainer should ensure the normal operation of the relevant parts. The current RT-Thread development version is placed on [github.com] (http://github.com). Every developer and enthusiast is welcome to submit a pull request to RT-Thread. After receiving the pull request, each component and branch maintainer will decide whether to merge into the development branch. The code submitted by developers and enthusiasts should conform to the RT-Thread programming specification and affect other components as little as possible.
