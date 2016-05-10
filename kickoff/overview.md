# CC: Automation & Tooling

## Who we are ?
###### Vierbergen Tim
###### Verelst Tom


## Automation & Tooling
### From the idea of testing...
A year ago, we started thinking about a Competence Center about *testing*.  Unit testing, intergration testing, performace testing, .... Everyone doing Java know about writing tests. But front-end, that's a different story.  Testing front-end (javascript)  applications is only 'a topic' since the last years. From fat-clients with native applications to thin-clients with a lot of server-side processing to fat-clients in browsers. So, okay... testing.  Jasmine, mocha, QUnit, Unit.js, Screw-unit....
Tooling.  

Initial release of Jasmine: September 14, 2010 (5 years ago)

### ...to automated testing...
When do we test our applications? Scripting language aside, code syntax is getting *tested* during compilation. So we can say that compilation is the first step. Other failures such as logical functions are tested during specific tasks and sometimes included in what we call the build process. You can of course first compile without testing. The run testA, then testB and so on. The build process itself is nothing more then running specific thing such as compilation, tests and generating reports, step by step. Instead on running these ourself, we started creating scripts (build processes) that do these things for us.

### ...to building and deploying...

A build process for a java-app can be:

* Generating sources (sometimes).
* Compiling sources.
* Compiling test sources.
* Executing tests (unit tests, integration tests, etc).
* Packaging (into jar, war, ...).
* Running health checks (static analyzers like Checkstyle, Findbugs, PMD, test coverage, etc).
* Generating reports.

Since we are lazy we don't want to do this ourselves over and over again. We started automating these things with tools like Maven or Ant and to run the build continuously (cfr. Continuous Integration).

When a build is successful we sometimes want to do more tests (E2E tests, performace tests, etc) or even just make the software available for internal use or global testing, before shipping it. Again, we do not want to run this deployment ourselves time after time. Again we try to automate this process by making use of autodeployments. (internal dev/stagng servers, cloud solutions (Paas), container for easy maintenance with cool features...)

And again we can run tests on different environments, fully end to end tests, and so on.


### ...to reporting and statistics...

In each stage of this process, we want feedback of this system. Did all test pass? Went everything as smooth as before? Did performance go down after implementing a new feature? All these reports should get collected, centralized and made available for the right analysts, developers and managers so they can adjust the agile process and log bugs if needed. Again, there is more then one tool for this... (e.g. Testrail)

### ....To Continuous What ?

#### Continuous Integration: (Martin Fowler’s)
- Continuous integration (CI) is the practice, in software engineering, of merging all developer working copies to a shared mainline several times a day. (Wikipedia :-D)

- Continuous integration (CI) is a software engineering practice in which isolated changes are immediately tested and reported on when they are added to a larger code base.

- Is a strategy for how a developer can integrate code to the mainline continuously as opposed to frequently. (branching strategy?) You might claim that it's merely a branching strategy in your version control system.

It has to do with the size of the tasks you assign to a developer; If a task is estimated to take 4-5 man-days then the developer will have no incitement to deliver anything for the next 4-5 days, because he's not done with anything - yet.

So size matters:
small task = continuous integration
big task   = frequent integration
The ideals task size is not bigger than a day's work. This way a developer will naturally have at least one integration per day.


Martin Fowler’s updated list of principles for Continuous Integration:
1. Maintain a code repository
2. Automate the build
3. Make the build self-testing
4. Everyone commits to the baseline every day
5. Every commit (to baseline) should be built
6. Keep the build fast
7. Test in a clone of the production environment
8. Make it easy to get the latest deliverables
9. Everyone can see the results of the latest build
10. Automate deployment


#### Continuous Delivery
- Continuous Delivery (CD) is a pattern language used in software
development to automate and improve the process of software
delivery. (Wikipedia)

- Continuous Delivery is the continual delivery of code to an environment once the developer feels the code is ready to ship.  This could be UAT or Staging or could be Production.  But the idea is you are delivering code to a user base, whether it be QA or customers for continual review and inspection.

- There are basically three schools within Continuous Delivery:

    - Continuous Delivery is a natural extension of Continuous Integration
This school, looks at the Addison-Wesley "Martin Fowler" signature series and makes the assumption that since the 2007 release was called "Continuous Integration" and the one that followed in 2011 was called "Continuous Delivery" they are probably volume 1+2 of the same conceptual idea that has to do with continuous something.

    - Continuous Delivery has to do with Agile Software Development
This school takes off-set in the idea that Continuous Delivery is all about being able to support the principles in the agile movement, not just as an conceptual idea or a letter of intent but for real - in real life.
Taking off-set in the first principle in the Agile Manifest where the term "continuous delivery" is actually used for the first time:
Our highest priority is to satisfy the customer through early and continuous delivery of valuable software.
This school claims that "Continuous Delivery" is a paradigm that embraces everything required to implement an automated verification of your "definition of done".
This school accepts that "Continuous Delivery" and the buzz word or megatrend "DevOps" are flip sides of the same coin, in the sense that they both try to embrace or encapsulate this new paradigm or approach and not just a technique.

    - Continuous Deployment is a synonym to Continuous Delivery
The third school advocates that Continuous Deployment and Continuous Delivery can be used interchangeably to mean the same thing.
When something is ready by the hands of the developers, it's immediately delivered to the end-users, which in most cases will mean that it should be deployed to the production environment. Hence "Deploy" and "Deliver" means the same.

    - "Continuous Deployment" IS NOT "Continuous Release".

####Continuous Deployment
- Continuous Deployment is the deployment or release of code to Production as soon as it is ready.  There is no large batching in Staging nor long UAT process that is directly before Production.  Any testing is done prior to merging to the Mainline branch and is performed on Production-like environments


### Agile:
Continuous Delivery Vs. Agile
* Agile is less “continuous”
    - Sprints are numbered per version, dated and known.
    - Planed releases and security tests
    - Better control of additional or changed code

### Tooling
During this year we would like to focus on our delivery pipeline so we can create and document a preferred stack of tools.

 Proposals?
 (buildservers, containers, testing, feedback/reporting tools.)

 - codeship
 - docker
 - webpack
 - ...

Of course there is more to automation & tooling then CI (tooling).

- Unix scripting
- Git (crash course Tom) & hooks (web/post-receive/...)
- Proposals ???


### Members
Vierbergen Tim
Verelst Tom
Hubau Dieter
Moorkens Bas
Gregory Rinaldi
Michiels, Hans
Vergeylen, Yannick
