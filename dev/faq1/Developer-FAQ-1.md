#### General Information
  * [Who should read this FAQ?](#who-should-read-this-faq)
  * [How does the NUnit 3.0 project structure differ from earlier versions?](#how-does-the-nunit-30-project-structure-differ-from-earlier-versions)
  * [Where can I get the source code for a release of NUnit?](#where-can-i-get-the-source-code-for-a-release-of-nunit)
  * [Will building from source interfere with my production copy of NUnit?](#will-building-from-source-interfere-with-my-production-copy-of-nunit)
  * [Where is NUnit development hosted](#where-is-nunit-development-hosted)

#### Getting Started

  * [[I want to get involved with NUnit Development. Where do I start?|FAQ:Getting-Started]]
  * [[What tools are needed to build NUnit?|FAQ:Tools-Needed]]
  * [[What areas need work]]?
  * [[How do I become a committer]]?

#### Development Process

  * [[How can I manage my working copy of NUnit?|FAQ:Working-Copy]]
  * [[I just have one change to submit. Is there an easy way?|FAQ:Casual-Contributor]]
  * [[Coding Standards|Coding-Standards]]
  * [[How can I publish my branch on GitHub?]]
  * [[How do I request merging of my branch into the NUnit trunk?]]
  * [[How can I submit a merge request by email?]]

#### Version Control

  * [[How to update your copy of the source]]
  * [[How to create a patch with your changes]]
  * [[How to apply a patch from someone else]]

#### Building NUnit

  * [[Building NUnit on Windows 8.1]]
  * [[How to build NUnit from source using MsBuild]]
  * [[How to build NUnit from source using Visual Studio]]
  * [[How to build NUnit from source using Visual C# Express]]
  * [[How to build NUnit from source using SharpDevelop]]
  * [[How to build NUnit from source using MonoDevelop]]

## Who should read this FAQ?

This FAQ is aimed at NUnit developers and contributors, authors of addins and anyone else who needs to build NUnit from source.

Depending on the nature of your interest, different sections of the FAQ and different questions will apply to you.

### How does the NUnit 3.0 project structure differ from earlier versions?

Through the 2.6 series, NUnit was maintained as a single large project.
Development of NUnit 3.0 is being carried out as a set of separate, but
coordinated projects.

The overall NUnit 3.0 platform is called the **NUnit Extended Testing Platform**
and consists of the following projects:

* The **NUnit Framework** holds the Assertions, Constraints
and other types referenced by users in their tests. It also contains the
the low-level code used to actually discover and execute tests.

* **NUnitLite** is a lightweight version of NUnit in a single assembly.
It runs in resource-poor environments and is actually developed as part
of the NUnit Framework project, using a common codebase.

* The **NUnit-Console** program is an updated version of the existing console
runner, designed to work with NUnit 3.0.

* The NUnit **Test Execution Engine** is a new component, which will provide a 
common API to be used by all programs that run NUnit tests. It is actually
currently maintained as a part of the NUnit-Console project, but may be 
split off when its features are stabilized.

* The **NUnit-GUI** project will create a new interactive runner for NUnit 3.0
to replace the old "nunit.exe" program. Work has not yet been started on this project.

* The **NUnit Visual Studio Test Adapter** allows running tests under the Visual
Studio 2012 / 2013 Test Explorer window.

* Other projects will be added as time goes on, including additional interactive
runners, a configuration program and a Visual Studio extension.

### Where can I get the source code for a release of NUnit?

The source code for each release of NUnit is available as a [[download|http://nunit.org/?p=download]], with a name like "NUnit-2.6.2-src.zip." You would normally not want to use a release version of the source when working on bug fixes or features for NUnit, since that source becomes out of date very quickly.
		 
However, you may want to use a release version of the source...

  * To create a debug version of a particular release and step through it.
  * To make your own local changes to NUnit
  * To learn how NUnit works

### Will building from source interfere with my production copy of NUnit?

No. NUnit is capable of existing on a machine in many different builds and versions. However,
you should ensure that you don't use the same version number in your builds as one of the
installed NUnit versions.

### Where is NUnit development hosted?

NUnit development is currently hosted on [[Launchpad|http://launchpad.net/nunit-xtp]] but
we are in the process of moving it to [[GitHub|https://github.com/nunit/]].

GithHub provides an environment that encourages individuals to work on
open source projects with a very low entry barrier. No special permission
is needed to fork any repository and all your changes can be pushed to your fork on GitHub.
GitHub also makes it easy to merge your changes into the main project using Pull Requests.

Since we are anxious to have increased community involvement in NUnit
development, GitHub seems to be an ideal host for us.  See
[[Migration to Github]] for the current status of this ongoing change.

**Note:** *Versions through 2.5.2 were maintained on [[Sourceforge|http://sourceforge.net/projects/nunit]],
where you can still find the code for older releases.*

### I want to get involved with NUnit development. Where do I start?

#### Discussing NUnit

Most likely, you want to do more than just talk about NUnit, but
discussing future directions and options is one of the key things
we do as a community.

Currently, such discussions take place on the [[nunit-discuss group|http://groups.google.com/group/nunit-discuss]] on Google groups. This is where both developers and users get together and it's usually the first place where new ideas are brought up, discussed and either accepted or passed over.

If you join us there and participate in the discussions, we'll get to know you and your contributions.

#### Joining GitHub

NUnit is maintained on [[GitHub|https://github.com]] so your next step will be to 
[[set up your GitHub account|https://github.com/signup/free]].

GitHub provides a handy list of the steps you should follow after setting up your account
at [[Bootcamp|https://help.github.com/categories/54/articles]]. We won't repeat the instructions here.

**Note:** *While we're in transition, it's still possible to work on some NUnit projects
on Launchpad. We don't recommend this for new contributors. All code will be on GitHub soon.*

#### Clone and Build NUnit

You should clone the NUnit project you want to work on and make sure you are able to build it
from source and run tests successfully. Ask us for help if you run into problems.

#### Joining the Developer List

Discussion of the actual development of NUnit takes place on the [[nunit developer list|https://groups.google.com/forum/#!forum/nunit-developer]]. You should join the
list and introduce yourself. Tell us a bit about your background and what you would
like to work on.