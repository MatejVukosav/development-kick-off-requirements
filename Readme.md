

# Motivation
The purpose of this document is to list things that are very important to us as Android developers to begin the development phase. Conditions will be first listed and then explained.

1. Completed functional specification reviewed by lead dev
2. Project onboarding document written by lead dev
3. Edge cases thought through and defined in functional specification
4. UI hand-off by designer  and animations fully defined
5. Test cases written by QA

One note about additional features. We are aware that in reality, because of the clients, whole feature set usually isn’t defined before development starts and they will usually request additional features as development goes on, but no matter that we would like for that additional features to be also checked against this points.

# Completed functional specification reviewed by lead dev
Functional specification should be fully written before re-estimations. It should always be up to date, maintained by a project manager. Lead project developer should review functional specification to immediately catch possible complicated features and to think about them as soon as possible, and maybe even change some of them in cooperation with UX/UI/PM.  Also,  it is useful for him to be accustomed with the full feature set early on so he can design the architecture according to the app requirements.

# Project onboarding document written by lead dev
Lead developer on a project should write project onboarding document prior to development. As he has already reviewed functional specification in this moment he should be familiar with the feature set and with potential problems. The format of the document isn’t fixed, it can be a Google document, Confluence page, README file on the source control, whatever, as long as it is the single source of truth. Onboarding document should have:
Technical stuff like source control repo url, urls to various documentations, access to client stuff, test usernames and passwords, and any other informations related to the development.
List of the technologies and libraries used during the development such as programming language, DI framework, ORM, networking, caching, user handling, communication between components (callbacks, event bus, RxJava, …), image loading libraries, etc… We do provide technology guidelines, but lead dev can choose different technologies depending on the situation.
General development instructions like how to make a build, when to run tests, when to use leak canary, when to run findbugs, how do we handle Crashlytics, and generally everything that doesn’t match standard development flow.
Architecture overview, not necessarily in too many details, but to provide general guidelines to the developers doing the app.
Typical (or couple of them) data flow between app components to serve as a guideline to the developers.
List of everything that has to be custom built and that is different than standard Android components,  e.g. Rosetta SRE wrapper, Rosetta resource libs, custom views and animations, etc.
List of standard Google technologies that we will use, like GCM, Firebase, etc.
List of dangerous permissions used and situations that we ask the user for them. This would be great if it were in the functional specification.
If it isn’t defined in the functional specification this would be a good place to define all of the analytics libraries and events that we use.

# Edge cases thought through and defined in functional specification
There should be some time spent on thinking through all the edge cases that could occur in the app. Maybe even organize a meeting with all the members of the team in order to brainstorm and try to mess up the app as much as possible in the thought experiment. We lose much time on the edge cases that we run into during the development and if would save us a lot of time if they were known in advance and documented in the functional specification. Also, a bigger estimation would be given if they were known.
UI hand-off by designer and animations fully defined
UI hand-off was part of the process for some projects and we found it useful. The idea is to have a meeting with the designer prior to development where he would introduce us with the design, the main ideas behind the particular design, explain us some details, introduce us to must haves and good to haves, explain more complicated animations in more details and so on.
We always want to build the killer app, and that’s way it is necessary to have all the UI components ready before the development starts, and that includes animations too. Our motto is design driven development and it is hard to be driven by something that still hasn’t been done. We usually treat animations and eye candies like second order citizens and leave them to be done at the end of the project. We should do them as a part of the normal development process while the screen which holds the animation is being done. That being said we shouldn’t sign off the screen as been done and send it to the QA until animations and eye candies are done. For that to work the animations should be defined prior to the development.
# Test cases written by QA
It would be very beneficial for us to have all the test cases written by QA and saved to test rails before the development of particular feature starts. With test cases provided we know more precisely what is expected from a feature, and we can run the test cases for the feature ourselves, at least on the device we are developing on, and by doing that reducing the time needed to pass the QA phase. 

