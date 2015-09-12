 - title card
    - Science x Python
        - What the Open Science movement can learn from Python
    * Hi folks - I'm bill mills, and Louie asked if I would drop in to talk about the intersection of science and python today, and where we might be going in the near future.

 - who am i
    - bill mills
    - physicist & scientific software developer
    - triumf / cern / mozilla
    * So, who am I - I'm bill mills, physicist and scientific software developer from Vancouver. In the recent past you could find me fooling around at these fine institutions, and lately I've found myself doing a lot of advocacy for this thing called the open science movement.

 - What is Open Science?

 - Open Science is a methodological movement that promotes:
    - transparency
    - reuse
    - reproducibility
    - collaboration
    * 'What is open science' is its whole own talk, but basically, it's an effort to make the process of doing science more transparent and more efficient - and if we had time to dig into it, you would all recognize a heavy influence from the lessons of the open source movement. A big part of this movement is how these ideals apply to the increasing amount of code we write for scientific applications.

 - The State of Scientific Computing
    - minimal code reuse
    - virtually no training
    - no credit for sw contributions
    - minimal discussion of sw in papers & conferences
    * As it stands today, the bulk of scientific computing practice could use a bit of work. We don't have a culture of code reuse or standardization; students recieve essentially no training in software engineering; sw contributions, regardless of how crucial they may be to an experiment, are not seen as resume-builders; and we rarely if ever cite or mention our software in our papers, discuss it at our conferences, or talk about it in any way. For the most part, we've treated computing like a second class citizen in the sciences.

<!--  - [frustrating.gif]
    * So as a result, grad school kind of felt like this - scientific computing is pretty frustrating, and also pretty isolating. -->

 - ...and then 'Big Data' happened.
    - The size of datasets in astronomy, genomics & collider physics is exploding
    - Ecology realizing there's a lot of cool ecology you can do in sw
    - Social Sciences got into text mining, leading to the 'Digital Humanities'
    * But really, it wasn't so bad - that relationship with computing kind of bumped along for a few decades - we figured things out, and after all, scientists wanted to focus on science, not on software engineering - but it's starting to get out of hand. More and more experiments are beginning to leave the terabyte scale and are looking at petabyte sized analyses - my current experiment can generate 200 TB of data every *week*; other fields like ecology are realizing that they can do some really cool stuff with climate and population models that's just getting left on the table by traditional field ecology; and text mining has grown both sophisticated and convenient enough (thanks NLTK) that the humanities are investing serious attention in computing, too. These huge demands and huge opportunities are awesome and exciting!...

- [debugging.gif]
    * ...but scientific computing culture isn't keeping up with the demands of scientific computing.

- Enter the Scientific Software Developer
    * So, at this point, a generation of classically trained scientists like me have found ourselves kind of squashed between the growing centrality of computing in science on the one hand, and the lack of training, supports or a culture of software openness on the other. My colleagues and I have all had similar experiences; trying to stay on top of the computing demands for our research became a full time job, to the point where programming was taking up the vast majority of our time. Do that for a bit, and there's a chance you'll get kind of not so bad at programming, at which point the rest of your lab looks to you as the 'computer person', and rely on your leadership to navigate these challenges. So, partially by necessity but mostly by sheer blind luck (?), a new breed of scientists are being created - the scientific software developer. 

- Two Futures:
    []
    * As people look to us for strategies on how to modernize scientific computing, we have scrambled to learn all we can from traditional software developers and from the open source movement, and contribute to this idea of open science that I started with. We've made some progress sharing code openly, particularly at the framework or collaboration scale; but there's still a lot of ground to cover. As scientific software developers emerge as a sub-discipline, now is the time to put serious thought into who we want these new scientists to be. If we aren't careful, they may end up scrambling to just soak up the computing demands from their colleagues, increasing our bandwidth for computing but missing the opportunity to improve our methodology. On the other hand, if we put some thought into what we want scientific computing to look like and bake those goals into this new role, we might have a chance of breaking out of this siloed, single use paradigm of development, and help build a real open movement in the sciences.

 - Meta-responsibilities
    - support collaborative coding 
    - write for reuse 
    - promote discoverability
    - build capacity
    * I put it to my colleagues, that these are the four meta-responsibilities beyond just hammering out code that scientific software developers need to take on, if we are to have the future we want. What I want to talk about for the rest of this talk (finally) is the example that the Python community has set on these fronts, and what I hope the sciences learn from all of you.

 - 1. Supporting Collaborative Coding
    * So, last time I was at TRIUMF, I was tasked with building this great glittering edifice of software tools for experimental design and control - and they were beautiful. Administration there gave me the leeway to do things mostly pretty much as I saw fit, and so I made the best set of tools I could. And when we introduced the beta versions to the community for user testing and eventual adoption...

 - [cares.gif]
    * ...nobody cared at all. The tooling I had thought I'd done such an awesome job on landed like a dead fish.

 - Post Mortem: the lab did not:
    - understand project motivation
    - have the skills to maintain the code
    - feel a sense of ownership.
    * When a new role arises in any work environment, it's easy to see them as that weird new kid - maybe easier to just ignore them and hope to not catch their cooties. Because my work was so non-transparent to the lab, everyone was a bit baffled as to why we were rocking the boat with all this modern tooling; it was all a bunch of web apps and none of them spoke *any* javascript at all, so when I handed the projects off they were way too cumbersome to maintain; but most of all, I think the real problem was that the community didn't feel a sense of ownership of the projects. They didn't get much say in how the projects were built or how they worked, and in the end they felt like someone else's problem. Which lead me to one of my most important pieces of advice for scientific software developers:

 - Build Code With our Colleagues, not For Them.
    * If we want the scientific community to feel that sense of ownership of our projects, we need to keep them involved in the development process. By having consistent RFCs out at every step of a project, by pushing some of the engineering tasks out to other scientists, we keep them participating - and after a while, participation leads to not only the skills necessary to maintain the project into the future, but also a personal investment in the project that will turn those collaborators into our biggest advocates, when they go back to their groups and labs. That investment, that sense of ownership and participation in these projects is what will not only lead to full integration of scientific software development in the lab, but lay the foundations of an open source movement in science. What's more, scientific budgets are tiny, particularly for a new-fangled role like scientific software development - it's going to be a very long time before developers in the lab aren't outnumbered a zillion to one; we need to act as central hubs and leaders for development, not single sources.

 - Fine Sure But How
    - Our code needs to emphasize:
        - Simplicity
        - Explicitness
        - Readability
    * OK - great high minded ideals there - but how are we going to pull this off? The problem being, that scientists are really motivated and primed to think like a programmer, but still they are scientsits first, and programmers a pretty distant second - they don't have a lot of domain knowledge in programming. If we want to keep scientists involved in the development process, we need to make sure there are clear on-ramps for their participation. This means in part designing code that a beginner or intermediate programmer can come to and understand without a ton of domain knowledge, and the way to do that is to focus on values like these; simplicity, explicitness and readability add up to code that someone who is motivated but inexperienced will be able to dig into, since everything is right there on the screen in front of you, rather than obfuscated away somewhere. Do these values sound familiar to anyone here?

 - This is Pretty Much PEP 20
    * Before I gave this talk, I asked the twitterverse, what should scientific software developers learn from the Python community? And the response was near unanimous - all of you called out PEP 20. Which in itself is really remarkable - PEP 20 is not some dead sea scroll sitting in a museum that no one has actually read - the values that add up to a warm welcome for newcommers and beginners were the first thing the Python community wanted to share with the scientific community. Contrast this active enthusiasm for newcommers with 1990s-style fixations on how much can you cram in one line of code, and it should be clear why scientific software developers need to study carefully what the Python community has brought to life in its living, founding documents.

 - Pragmatism First: Python 2.x to 3.x
    - short period from PEP 3000 to 3.0 (2 years)
    - long period of dual support (5+ years)
    - lockstep releases, warnings module
    * Another element to collaborating effectively with scientists is to understand their culture a bit, and one of the things that I absolutely love about scientific culture is their regard for actionable plans and concrete results. As scientific software developers pick up the reins of projects they will be managing, another great lesson from Python was the 2 to 3 migration. One thing that tends to leave scientists cold, is excessive discussion of spec. When I was just a baby scientific software developer, this used to drive me nuts - if we laid out a spec, we could do things right the first time! But what I came to appreciate was that often in scientific software, we don't actually know a priori what we want; these can be largely experimental and exploratory projects, and it pays to get something on the table soon. The way the python community got 3.0 out pretty quickly and iterated from there much more closely reflects scientific software development than a more theoretical or extended discussion of specifications. What's more, python was managed with great pragmatism and sensitivity to real developers; the PSF planned for it to take at least 5 years to shift the community, and helped scaffold that with the lockstep releases and 2->3 warnings module, helping people port their projects in a slow and systematic way as they had time. Iteration and patience are two things that practical scientific software collaborations are going to have to focus on, and Python modeled this really well in the 2.x->3.x migration. (also see this post by GVR on designing python to be 'good enough': http://python-history.blogspot.ca/2009/01/pythons-design-philosophy.html)

 - 2. Writing for Reuse, or Avoiding Peak Sphagetti
    * The second thing on my menu of meta-skills I want to see scientific software developers adopt and support is writing for reuse, or avoiding what I like to call peak sphagetti - we've all seen peak sphagetti before: it's that point in a project where so much technical debt has accrued that it becomes utterly unmaintainable, and the only thing left to do is just walk away. Project failure due to peak sphagetti is a tragic loss of effort and resources, and is often the result of reach exceeding grasp in project design and management - a not-uncommon mistake for new developers.

 - Reusable Engineering:
    - [lego.png]
    * The way to avoid peak sphagetti is of course a high degree of modularity, which means plastic bricks if you're making skyscrapers, or packages if you're writing code. Trouble is, it can be way harder to digest and use other people's code than to try and use tools you're already familiar with, and really scary to contribute your own code back for reuse on a package manager. Scientific software developers are going to need an example of how to lead people to effective code exchanges, and Python made some really good decisions both technically and culturally that serve as one possible example.

 - Good Decision #1: Python normalizes modularity
    * It's hard to do much of interest in Python without a few import statements, particulary for scientists who want to do weird esoteric things all the time; at the same time, one thing that's really nice for part-time programmers in Python, is that 'pip install whatever' is pretty easy; this combination of needing packages and packages being simple to use makes Python feel really packag-y right from the get-go. R is another language that does a good job of this, which perhaps unsurprisingly is science's other favorite language.

 - Good Decision #2: Python is aggressively modular
    * Another interesting thing about modularity in Python is that you'll end up making modules pretty much whether you like it or not, thanks to the automatic namespacing of imported modules. Throwing a bunch of functions into a file and importing them is not a totally unreasonable python module - and it required no real special engineering or tooling, at least for the core pattern of creating namespaced, reusable code.

 - Good Decision #3: PyPI is Friendly
    * There are basically two ways you can run your package manager: for end users, or for contributors. An end-user centric package manager is characterized by really strict gatekeeping; strict standards are set which submissions must adhere to, to ensure quality and uniformity for end-users. This has some value in scientific programming; we'd like scientists to consume existing packages rather than reinventing the wheel, so making this consumption as smooth as possible makes sense. There's just one problem - where are those packages coming from in the first place? A contributor-centered package manager is much simpler - it implements the least number of restrictions, and as much as possible, anything goes. This is how PyPI works, and I think this is a crucial example for the scientific community. One challenging thing about working with scientists as they develop software, is that they are often intensely shy about their code; I don't know how many times I've asked to see the repo, and been told, sheepishly, 'oh, I just need to clean things up a bit first' - and then I wait for infinite time for that to happen, because some arbitrary standard of niceness is not the problem; the problem that scientific software developers are going to have to provide serious guidance on, is with dealing with feelings of insecurity and self-consciousness about our code. One of the big challenges that scientific culture faces when trying to digest good programming practices like reuse, iteration and sharing, is that scientists are trained to be absolutely *terrified* of being publically wrong; the concept of releasing code that is anything less than shining perfection is really scary in that light. Python's package management philosophy is much less intimidating for newcomers, since there is no gauntlet to pass in order to offer code up to share.

 - Must-haves for code exchange:
    - Make it familiar
    - Make it natural
    - Make it friendly
    * What this all adds up to, is a recipe for successful code sharing that the community around PyPI has done a great job of modeling. Whether a project is in Python or not, scientific software developers need to tackle the problem of encouraging code reuse by making it seem like the normal thing to do in the lab's projects; looking for ways to make package use as natural and friction-free as possible; and making sure that contributorship is a safe and non-discouraging experience, particularly for first-time contributors. The proof is in the pudding, too - there is an exploding ecology of scientific python packages availalble, so it seems that the alchemy the python community has created around sharing works.

 - 3. Discoverability
    * How do you find out about new python projects, like new packages or whatever? Shout em out.
    [lead conversation, mention blogs and meetups]
    * Scientific computing is currently crippled by something we call the discoverability problem. It is really, really tough to find out if someone else is writing code, off in their lab somewhere, that does exactly what you want to do.

 - Live Demo Gods Forgive Me!
    - Tweet-length description of one of your current projects
    - Shout them out.
    [lead conversation; count how many respondants before an overlap is found; in a pinch, ask for hands up who is working on something similar]
    * Bam, there is exactly what I'm talking about - it took N people to call out what they're working on before we found a pair that has an overlap, and potentially ideas to share. I've done this exercise at a number of different science meetups, and the number seems to be about 8 - in a group of 8 people, there is often a pair working on things similar enough that they can learn from each other's techniques. The value of communication in a skills and tools-driven community is enormous, and so is the opportunity for us to capitalize on it, if we can minimize friction in communication.

 - Judging by meetup.com and planetpython.org alone,
    - A python meetup starts every 7 hours
    - Somebody blogs about Python every 3 seconds (ok 4ish hours but feels like...)
    * Tech in general and Python in specific has a tremendously vibrant meetup and blogging scene, and this level of rapid communication is vital for creating discoverability in scientific programming. 

 - Immediate Communication Matters
    - 5x impact factor for papers released immediately
    - Recall importance of including people in development discussions
    * I'm reminded of a study of scientific publishing that demonstrated that traditional scientific papers that were released immediately after completion rather than after years of editorial review recieved five times the citations they otherwise would have. Immediacy has been well demonstrated to be crucial in scientific communication for the sake of impact, but also for keeping people involved and participating in the development process, like we discussed previously.

 - The Pycon Communication Model
    - talks span crunchy to cultural
    - talks at all technical levels encouraged
    - diversity & ethics explicitly called out
    * Tech in general is setting an example for rapid and caual communication that the sciences could benefit from; conference talks and extensive blogging make it pretty easy to find out cool new things in your language of choice. What I think the Python community is doing particularly well (actually the javascripters are pretty good at this too, but that's my bias :), is ratcheting up the inclusivity in those communications. Was anyone in montreal for pycon earlier this year? I wish I could have gone, because the roster was amazing. It's pretty obvious that the organizers went to great lengths to get talks at every level of technical expertise, but also to create a whole track on culture, diversity and ethics, sending a strong signal that the Python community wants you here - whoever 'you' happen to be. Science conferences and science communication can set an absurdly high bar for technical sophistication that not only completely torpedoes most people's chances of actually learning anything in those talks, but creates a very narrow picture of what and who belongs there, that doesn't leave a lot of room for discussing new ideas. Science could benefit from a much broader communication model, composed of more diverse conferences like pycon, but also including blogging and informal meetups - low-stakes communication like this will open up scientific communications to a more diverse audience talking about newer, riskier ideas, and we absolutely need that if we are to fight our discoverability problem.

 - 4. Capacity Bulding
    * I started out by describing some of the woes that scientific computing has to wrestle with, and one of the big ones was training - scientists are very rarely taught software engineering. Which is going to make some of the other goals I laid out for scientific software engineers - collaborative coding and encouraging software reuse - much much harder. If we want good computing to be part of scientific discource, we need a scientific establishment that has at least basic training in good software engineering - so the last meta-responsibility that falls to the scientific software developer is leading the way on capacity building.

 - Education is Complicated
    - Undergrad Classes: no room in curriculum
    - Online resources don't provide (good) feedback
    - Workshops don't scaffold long-term practice
    * People think education is simple - but really it's just simple to do a bad job of it. The typical approaches to education, or applied cognitive science as I like to call it, in this space are all not quite getting us there; it's next to impossible to wedge another class into most undergrad curricula (and it can be doubly hard to get a scientific computing class to focus on good engineering over abstractions). Online resources scale beautifully, but miss out on the feedback necessary for the best learning experiences, particularly for beginners; and workshops set people off to a fantastic start, but don't on their own scaffold the regular practice necessary to truly learn a skill. On top of all that, there's only so much a scientific software developer can reasonably be expected to do besides, y'know, develop software. Who's going to show us how to attack the capacity building problem?

 - [pyladies.png]
    * About a year ago, I was studying this problem by interviewing people who might have some good ideas, and in my travels I came to speak with Rachel Sanders, founder of the Pyladies SF chapter - and I was blown away by what Rachel and Pyladies had accomplished. Not only was this group successfully fighting the disasterously bad gender split in tech as they had set out to do, and which by the way is a big mess in most fields of science, too, but they are doing it in a way that is both pedagogically unique and sound.

 - Pyladies is Awesome
    - peer driven / minimal power hierarchy
    - skills focused
    - pedagogically aware
    * What Rachel described to me were a series of bi-weekly meetups Pyladies SF was organizing. How they work, is there'll be about 6 or 8 people in a group, with at least one more advanced person to help keep people unstuck. The group would choose some tutorial or project off the web, and work through it independently for a week or two, then get together to share their progress, ask questions and catch each other up. This blew my mind with how awesome and genuinely unique it was compared to other things in the space. This model is so strong, because it is peer driven - rather than having to sit through lectures or work through a prescribed curriculum, the group relied principally on each other for support as they worked on their project, rather than some authority figure; working on projects kept the content extremely practical and skills driven, and working in groups put collaborative relationships front and center in the learning process - and there is an absolute mountain of evidence indicaitng that students consistently learn from their peers than from any teacher. There's one or two people here today who might recognize this story a bit - a group of peers regularly getting together to share skills around computing - does that sound familiar to anyone?

- Mozilla Study Groups
    - Of course after this chat with Rachel, I shamelessly ripped off Pyladies' model to form the basis of the Mozilla Study Group program that I founded at the Mozilla Science Lab earlier this year. At Study Group, students and scientists from all different fields get together to lead demos on tools they use in their research and ask each other questions on how to make progress with their current research, partucularly around programming. It's been a huge success with a dozen groups and probably about 50 events worldwide in its first six months, and I think it's a model that fits the Scientific Software Developer's roll beautifully, because it is so aggressively community driven; all the organizer has to do is book a room every week or two, manage an issue tracker and send some regular emails, which is certainly some work, but way less than running a full course solo. Once again the Python community has modeled a great solution for scientific computing.

 - TL;DR
    * Up to now, the world of scientific programming has been fragmented by fear (of sharing work), uncertainty (of how best to go about that), and isolation (even when work is made available / discoverability). But as this new cohort of scientists from every field embraces the centrality of computing in science, we have a chance to overcome those old divisions, if we can reimagine scinetific computing along the lines of the what Python has built - a community that is:

 - diverse
 - legible
 - practical
 - accessible
 - open
    *which all adds up to being as welcoming a community of practice as I have ever seen. That's the science I want to build - I'm Bill Mills, thanks everyone and as always, questions please!














===========================================================



Pythonic SSD: Collaboration
 - ssds lead the charge, but don't write it all
    - bdfl model is defacto how scientific software gets done
 - scientists often reluctant to adopt a sw solution they feel no ownership of
 - won't be able to create collaboration with inscrutable, expert-only code; will write ourselves into another silo
    - we pick up graduate students by the collar and belt and throw them face first into development in the lab; if we indulge in the self-congratulatory code elitism of the 1990s, cramming as much as we can into one inscrutable line of code, those new programmers are going to fail spectacularly, and that failure will not only make them hate coding - it makes them hate science.
 - pragmatic, accommodating attitude
    * scientists are not impressed by the new hip thing; just look at any lab's website, it's like bootstrap never existed
 - exactly the values espoused by PEP 20.

Pythonic SSD: writing for reuse
 - (avoiding peak sphagetti)
 - pythonic packaging is easy and free
 - lots of packages to build off of, easy to get started
 - prioritization of integrating systems important for science / reusability

Pythonic SSD: promoting discoverability
 - python has a vibrant and active speaking & meetup culture
    - PSF conference sponsorships?
 - tech blogs communicating nacent ideas - important model for scientific communications, immediacy hugely impactful
 - help us model software citation!
 
Pythonic SSD: Capacity Building
 - Mozilla Study Groups based on the pyladies model
    - skills focused
    - pedagogically aware
    - decentralized power structure

TL;DR

 * Up to now, the world of scientific programming has been fragmented by fear (of sharing work), uncertainty (of how best to go about that), and isolation (even when work is made available / discoverability). But as this new cohort of scientists from every field embraces the centrality of computing in science, we have a chance to overcome those old divisions, if we can reimagine scinetific computing along the lines of the what Python has built - a community that is
  - diverse
  - legible
  - practical
  - accessible
  - open

which all adds up to being as welcoming a community of practice as I have ever seen. That's the science I want to build - I'm Bill Mills, thanks everyone and as always, questions please!

===== orphan ideas ====

scikit learn philosophy?
bdfl management
pragmatism between 2 and 3
