



# Introduction

### Welcome to country

I wish to begin by acknowledging the Wathaurong people of the Kulin nations, the traditional owners of the land on which we are gathered today. We pay our respects to the local people for allowing us to have our gathering on their land and to their Elders; past, present and future.

Thanks everyone for coming today, and a huge thanks to Ben and Rick for convening an event as amazing as Buzzconf.

### Audio impaired

If there are any hearing impaired members of the audience, let me know and I can provide you with a transcript of the presentation to follow along to.

### License

This presentation is licensed under Creative Commons universal - you're free to share and re-use this presentation. Please use it to do awesome things.

### Audience advisory

This talk is self-rated as being suitable for Mature Audiences. It contains

* Medical references and images of a medical nature
* Strong themes
* Occasional coarse language

# Overview

Firstly, I'd like to see a show of hands. How many people in the audience today come from a software development, programming or systems administration background? And you're familiar with the concepts of test-driven development, behaviour-driven development, continuous integration, continuous development?

Yep, OK, great.

And how many people here today come from a bio-sciences, medical, bioinformatics background?

OK, great.

Today we'll be talking around the convergence of these two disciplines. We will explore the evolution of computing platforms, and draw out key differences between the earlier platforms that have shaped approaches to development best practice.

We'll then move to discussing the human body as a development platform

- [ ] TODO: NEED TO PROVIDE A SUMMARY HERE

# Evolution of computing platforms

## Early computers

This might seem counter-intuitive, but in order to look forward to the future of development platforms, I'm going to start by taking an historical perspective.


SLIDE: Betty Jennings and Frances Bilas working on ENIAC

As most people in the audience would know, early computing platforms  - from around the 1930s to the 1940s - were physically large, taking up entire buildings or floors of buildings. Here, we can see Betty Jennings and Frances Bilas working on an early computer called ENIAC - the Electrical Numeric Integrator and Calculator. Using vacuum tubes for logical processing, these platforms had a very large physical footprint.

SLIDE: The bug removed from a computer by Grace Hopper

Development was done by manually moving dials and levers, or physically plugging in different switches and registers together. The development process was laborious, manual - and subject to the vagaries of such a large physical footprint. Indeed, it was during the early days of computing that the term 'bug' was coined - from an actual bug. Development work would be halted by errors such as vacuum tubes overheating and needing to be replaced. Obviously, building new development platforms represented huge investment - and so these early computers were limited to the military and advanced academic institutions.

## Transistors and integrated circuits

In the 1950s and 1960s, the invention of the transistor and later, the integrated circuit reduced the footprint of computing platforms - at least slightly.The equipment took up half a building instead of a full one.

SLIDE: IBM 608

Development had progressed slightly, and instead of manual switches and registers, programmes were run on advanced technology, like punch cards.

SLIDE: Punch cards

However, development was still hindered by the physical nature of the work - programming with punch cards was laborious, precise, meticulous, and required significant rework in the event of an error. There weren't syntax checkers or integrated development environments for punch cards to check that the code was at least syntactically valid before being input into the computer.

The rise of integrated circuits and tape-based storage helped to address this issue, and eventually this led to a movement away from the mainframe as the development platform and to the ..

## PC as the platform

SLIDE: ZX Spectrum

PC as the platform. What a mighty fine piece of engineering there, my very first computer. Oh, I miss you, ZX Spectrum with your 48k of RAM and your tape drive.

Love the ZX Spectrum. Aaah.

Even PCs though weren't without challenges as a development platform. Firstly, it was difficut to code for different environments. Code written in BASIC for the ZX Spectrum wouldn't work for instance with a slightly different variant of BASIC for the Apple IIe. Test and production environments were also difficult to achieve. You had to have one machine for development, package the software on to cassette tape, which itself was subject to the vagaries of heat, dust, accidentally being overwritten by the Top Gun soundtrack...

Then you had to transfer this via high speed network to your deployment machine - your production machine. Did I say high speed network? Well, it was for its time. Sneakernet.

SLIDE: Nike high tops

That's right, the media containing the software was deployed, whilst wearing this fashionable network transport device, then physically loaded onto the target host. Assuming of course, it was compatible.

## Web as a platform

So, PCs overcame some of the challenges of the mainframe era - they were physically much smaller, had better input devices, and more rapid development tools. But deploying to different environments, and testing, were still cumbersome activities.

Then in the early 1990s, this chap - SIR Tim Berners-Lee, invented a little thing called the World Wide Web.

SLIDE: Tim Berners-Lee

Over the next 10 to 15 years, development platforms shifted away from the standalone PC to networked web servers. We saw the rise of software as a service, and highly-available, redundant platforms that were robust, and could survive partial outages.

From a development perspective, I could write code locally on my own machine, and using the magic of the web, then deploy to a production environment in another country, on another continent - no Sneakers required. Testing was much easier - I could deploy to different servers easily and test against different platforms, and different configurations.

As long as I had a standards compliant web browser - you know, like IE - I could use the software.

Life was good.

There was just one minor problem.

I couldn't take the web with me. It wasn't portable. I couldn't check AOL or Myspace on the move.

## Mobile as a platform

SLIDE: iMac

Or, not really portable. And so, the next evolution sought to unchain us from our desks, and using near-ubiquitous wifi, we began to have mobile development platforms.

App Stores were born. iTunes, Google Play. Suddenly the device itself wasn't the platform in its entirety - the platform needed an ecosystem to feed it updates and updates and more updates.

Just like we'd seen with early PCs, heterogeneity was a problem again. Certain software only worked on certain models of phone. And heaven help early Android developers, with hundreds of different models to have to test with.

SLIDE: which model?

Of course, there was the choice of whether to develop for Android, iOS, or use some sort of hybrid development technique like Phonegap to bridge the divide between native app development and HTML5.

## Wearables

Then came wearables. Not _really_ a development platform in their own right - more an extension of mobile devices. But they did extend the challenges for developers.

Easy to acquire, easy to dispose of.

But, similarly to mobiles, massive choice.What to develop for? Pebble? Gear?

What's the lifespan of the device? 12 months? 2 years?

And before I start to talk about the next evolution - implantables and the body as a development platform, I'd like to take a moment to compare and reflect.

## Comparison of environments

So, why have I just given us all a brief history lesson. Well, for each era or evolution of development platforms -

* early computers
* mainframes
* PCs
* Web based applications
* Mobile
* Wearables

there were a set of limitations. Those limitations were surmounted as each new platform evolved, but each new platform brought with it a new set of challenges to be addressed.

Now, if you take a look at the next slide, you'll see the point I'm making by providing the quick history lesson.

SLIDE: Comparison of environments

* physical footprint
* setup and tear down of environments
* development approach
* testing and QA
* release and deployment

So, what would this table look like if we extended it to include the human body as a development platform - with implantable technology, programmable technology inside the body, and/or controlling or interacting with bodily functions?

SLIDE: Human body as a dev environment with question marks


# The body as a development platform

## Fundamental assumptions

I'd like to first of all explore some fundamental assumptions around the body as a development platform. There's a huge amount of debate in this area, and this set of assumptions serves as a foundation for the ideas presented here.

This is sometimes called 'bio-hacking' or 'body-hacking' or 'grinding'. This movement assumes that to augment the human body is a 'hack' - an act of volition that is somehow seditious or defiant, or contrarian. There is an element of doing something that is somehow not quite proper, or authorised.

SLIDE: Ninja

That brings me to the first assumption;

* ASSUMPTION 1: If you can't open it, you don't own it. And yes, we do own our own bodies.

SLIDE: Assumption 1

For this reason I prefer to call this field 'body development' or 'body dev' or 'functional body modification'.

It's not a hack if you own the infrastructure. I do not view functional body modification or body development as an act of sedition, as an act of defiance. Yes, it may be an act of self-expression, but equally it may be an act of self-improvement, of personal growth, of realising - or extending - one's potential.

The next major topic of debate in this space is whether or not it's ethical to be functionally enhancing and modifying our bodies with technology. Where do we draw the line? Implanting pacemakers and cardioverter difibrillators, and insulin pumps is now standard medical practice - with the key differentiator being that we're entirely reliant on a medical infrastructure and medical practitioners and medical technicians to do so.

On this point I take the utilitarian rather than Kantian philosophical view - body dev is neither wholly good nor wholly bad. How you modify your body, and what you do with your modification matters.

This gives us assumption number 2.

SLIDE: Assumption 2

* ASSUMPTION 2: It's ethically neither absolutely right nor absolutely wrong to functionally modify your body. But doing it well minimises harm.

But isn't this all a bit esoteric? We're talking about something that's way way off into the future?

No. The societal implications, the ethical implications, and the response mechanisms for a world where bodies are heavily modified - whether by medical professionals or body developers - are here now. And we need to tackle them.

* ASSUMPTION 3: We're already deeply in the trans-human era and we need to prepare for the post-humanist world.





Which brings me to my next




# Other notes

http://www.theguardian.com/artanddesign/architecture-design-blog/2015/aug/14/body-hackers-the-people-who-turn-themselves-into-cyborgs


DUARTE  - The
first discusses entangled agencies between organic and
inorganic entities that are in a relation, mutually
influencing one another, allowing individuals to register
differences to which they were not articulated previous-
ly


DUARTE - They consider the body a highly
malleable material, a transformable, improvable,
augmentable entity. This attitude towards human corpo-
reality corresponds to certain trends in performance art.
The new forms of embodiment are based on the deploy-
ment of novel and often highly advanced technologies.
