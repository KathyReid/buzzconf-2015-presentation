



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

So, as technologists, software developers, body devs - what are the challenges and approaches for overcoming them, as we adopt the human body as a development platform?


# Physical environment

## The challenges

As we saw earlier, one of the challenges for mobile developers on the Android platform is the variance in the models that they have to develop for. There's a few thousand different Android models on the market. Imagine if there were six billion!

SLIDE: Six billion environments

Every human being is different, and as development platforms, each one of us differs markedly along a number of attributes. Age, medical history, socioeconomic indicators - each person is of themselves a different development platform.

SLIDE: Body attributes

* Age - riskier as we age. Changes to skin, co-morbidities.

* Previous medical history
  * infection risk - One of the greatest challenges to body development is actually the rising threat of antibiotic resistance. In under 10 years, we're facing a situation where will not have last-line antibiotics. Bacteria are getting stronger, and we're running out of drugs to hit them with.

  * This becomes worse if the development platform - the person - has a compromised immune system. Has anyone ever had to maintain he 'dodgy server'? All the lights are green, all the monitoring is green, but you just know that as soon as you start the install that something's going to fail? Development on a human body with previous infection risk or compromised immune system is similar.

  * allergies - different materials used in implantables. It's also not just allergies we have to be worried about - for instance material that's supposed to be encapsulated or enclosed can sometimes leak out. Take the case of Quinn Norton for instance - she had rare earth magnets implanted in the tip of one of her fingers so that she could sense some radio frequencies. Now, she can't have an MRI because of the metal that has leaked into her bloodstream.

  * leftovers - the I have some silicon neatly tucked up behind my liver story. Talk about scar tissue, and how implanting devices where previous devices have been leaves scar tissue. Portacath inserted, fibrous scar tissue, makes it more difficult to implant one again.

* Psychology is an important factor in the physical environment. Academically, the Cartesian split of a separate body and mind has now long fallen out of favour. However, we're now in an era where we're able to develop the body faster than we're able to develop psychological approaches to support that advancement.

  * Indeed, there's a growing body of medical literature where people are rejecting their implantable medical devices - and subconsciously disabling them - something called 'Twiddler's Syndrome' - references at the end of the talk.

  * Another important psychological factor is the fear or repulsion have for implantable technology and for body development. One of my work colleagues recoils in disgust every time I tell her about the chip I want to have implanted in my hand. There's a lack of acceptance for these practices - and also reports of discrimination against those who practice body development within the workplace.

* We also have to consider socioeconomic factors. Firstly, you have to be able to afford the implantable technology. Then, what happens when it needs replacing - because most technology, eventually, needs replacing. Does it need code updates? Are they affordable? Is ongoing maintenance required?


  So, there's some key challenges here. Everyone is different, and we have medical histories and different things wrong with us - we're not equivalent physical environments.

## Overcoming these challenges

  There's a couple of approaches that we could take here.

### Medical only

One approach is to have only qualified medical practitioners undertake body development. While I don't for one minute want to minimise the skill, and training, and knowledge that medical practitioners have, this still isn't a realistic approach. Each of us owns our own body, and the technically minded, and relentlessly curious amongst us are going to explore it.

We must strike an appropriate balance between curiosity and stupidity.

### A balanced approach

So, here I'm going to borrow a little from ITIL and COBIT  - and essentially posit a change plan for body development.

* Establish a baseline - know your body, what it's been through, and how it responds. Understand and document dependencies in your body - your development environment - just as you would with a technical environment. Know what normal looks like.

* Plan your changes - make sure you have things like antibiotics and painkillers and support people on hand. Make sure you've coded up your RFID chip *before* you implant it. Make sure the NFC chip you're implanting isn't locked.

* Monitor - what are you going to do if you develop an infection? What does an infection look like - *this* is what an infection looks like. Make sure there's money set aside for maintenance.

* Back out - and if it's not working, if it doesn't look right, if it doesn't feel right, if you're not able to embody the development, back it out.


# Environment [de]commission

Environmental setup and decomm is quite challenging when we look at the human body as a development platform. Short of human cloning - which is still some decades away - there's no real way of creating a new development environment.

Even with cloning, _growing_ a new environment still takes at least 18 years ;-)

However, one approach here is the emerging field of body on a chip technology. Scientists have been able to replicate the functions of major organs, and build them into components no larger than computer chips.

SLIDE: Lung on a chip

This makes it much easier to test new pharmaceuticals, understand how different technologies will interoperate together - and shake out some risks before moving to something like implantation.

So, I think that's probably going to be the approach - at least for the foreseeable future.

## end of environment lifecycle considerations

The other consideration we need to have here is at the other end of the lifecycle. What happens to implantable devices when someone dies? Do the implantable devices need to be removed before burial or cremation? What if the person has an active device? Something that transmits or which can be scanned?

My father was one of the first people to have a device called a Cardioverter Defibrillator implanted in the early 1990s. The device was designed to monitor, and if necessary, correct an arrhythmia he had by delivering electric shocks directly to the heart. It saved his life several times - an incredibly valuable piece of medical equipment.

Unfortunately, he passed away around 10 years ago, from a completely different illness. Before he passed away, he actually had to visit a cardiologist, and have his defibrillator - in effect - turned off.

Will we need to do something for people who have other pieces of technology implanted? How will we know? What risk does that pose? If technical components are inadvertently buried or cremated with a person, will they present an environmental risk?

# Development approach

So, we've talked now about the physical environment of the human body as a development platform, and talked a little around how those environments are commissioned and decommissioned. If we turn our attention now to the development approach for the human body as a platform, we can explore some of the unique challenges this presents.

The good news in this space is that a lot of the maturity in development platforms spurred by development on PCs, the web and mobile and wearable platforms can be re-utilised for the body as a development platform.

For instance, toolchains for developing code - IDEs, automated testing frameworks, libraries, collaborative version control etc can often be repurposed for body development - so I won't spend a lot of time talking about these.

As with previous platforms, developers have to make some _strategic choices_. Just as mobile developers have to make a choice between iOS, Android, or HTML5, body devvers face similar challenges.

## Development choices

* Dangerous Things and RFID and NFC implants
* Northstar V1 for backlighting tattoos
* Circadia

NOTE: Remember to mention I'm not affiliated with these companies in any way.

## Overcoming challenges

In terms of development, it's not really about challenges, it's about choices. To guide those choices, there are some key takeaways.

* Ensure there's a strong community around the products you're using
  * You don't want to be in the situation where you have something implanted, and then the development on that ends, and then there's a problem, and there's no one around who can help you with it.
* Ensure the code and platform is open - many eyes make for shallow bugs
  * Also means that it's more extensible and extendable.
  * openness is important - imagine if say Volkswagen made implantable devices! These things are going inside your body - if you don't know what's in them or how they're coded, can you really trust them?

  There's actually a very famous case of a lady in the United States called Karen Sandler - she has a medical condition that requires the use of a pacemaker. But when she went to get the pacemaker installed, the biomedical company who manufactured the pacemaker wouldn't release the code. So, she actually refused to have the recommended model implanted, and instead opted to have a non-wireless model - an older model - implanted.


# Testing and quality assurance

So, as we talk about testing and quality assurance, I'd first of all like to see a show of hands. How many of us in the room are familiar with say test-driven development - where you might use something like PHPUnit or other frameworks to write unit tests - and then automatically run those tests using something like Selenium? Great - so that's *Test Driven Development*.

Are there any people here who practice in an Agile based environment, where you write user stories and acceptance criteria? Yep, and you use something like *behavior driven development* to help test against those acceptance criteria?
OK, great.

Both of these approaches - test driven development and behaviour driven development - offer benefit to body development. Writing test cases for the board or the chip that's going to be implanted is a great idea. Writing acceptance criteria and behaviour driven tests for the use case the body dev project is intending to serve is a great idea.

"As an office worker, I want to load my workplace's access credentials into the chip in my hand so that if I forget my access card, I can get into the office building"

That's a great behaviour driven development test case.

But for body development, we need to be aware of the mind. What we do to the body has an affect on the mind. Cancer survivors who've lost body parts don't just have to do physical rehabilitation - they usually do some form of psychological therapy as well - treating the body and the mind.

So, what we need for body development is really an addition to behaviour driven development. We need

*Embodiment driven development*

This approach extends behavior driven development to ensure that the *experience* that the person - the platform - has is a positive one.

I'm not talking about the pain or the infections or the other inconveniences of surgery that are required for implantable technology. I'm talking about the ability of the person - the platform -

* to embody
* to embrace
* to accept

the development that has been made a part of their body.

*Has the development also become a part of their mind?*

This approach touches on the phenomena that have been reported for patients with implantable medical equipment - pacemakers and defibrillators and the like - where the person psychologically rejects the technology. There is a dissonance between their body and their mind.

The challenge here is that we are only just starting to understand what embodiment looks like - there's no 'easy' test for this - and a lot of the work in embodiment is actually based in psychology.

## Solutions

So, user experience will have a large role to play here in the future - devising approaches and tests to determine whether body development has been 'embodied'.

# Release and deployment

Again, with release and deployment, body development, implantables can build on the great work that's already been done for platforms like the web and mobiles. Practices such as tagging of releases, distributed version control using tools such as Subversion and Git are widespread.

## Challenges

The body as a development platform does however present some unique challenges. Making changes to code may be as simple as doing a git push, but how does this actually get transmitted to the implantable device?

* wireless

Wireless methods of deployment are increasingly being used to configure medical devices such as glucose meters, pacemakers and implantable defibrillators. However, if the device that's implanted doesn't support secure wireless, then it may be susceptible to unauthorised editing.

* bluetooth

Bluetooth suffers very similar issues - and of course with wireless and Bluetooth the nagging question remains of whether long term exposure to radio frequencies damages cells in any way. The empirical evidence seems to suggest not, but really we haven't been implanting devices in people long enough to know for sure, and I think this will be an emerging area of research.

* NFC

NFC has a different range, and therefore uses less power than wireless or bluetooth, so it's probably an ideal candidate in at least the short to medium term as the preferred way to release and deploy to the human body.

Of course, it does have some drawbacks, such as the data that can be stored on an NFC device, and how *active* it is - and of course having an NFC reader close by all the time is not so practical.

* Snip, rip, slip, clip

Of course, if the implant fails, or the person doesn't embody the development, the release - the deployment - may need to be rolled back. In this case, it's a case of snipping the skin, ripping out the implant.

And if the device fails, you may have to slip in a new one and clip the skin back together.

Not a great approach.

I suspect what we'll see here are devices that can be more easily implanted or removed, and the rise of power cells that use the body's own electricity, therefore lengthening the timespan that an active device can stay in the body.

Some challenges and approaches there.

# The Body Development Manifesto

So, in conclusion, what I'd like to leave you with, to reflect upon is this:

We have development best practices now for PC based development, for web based development, and for mobile and wearable type development. We are in a transhumanist world, and very quickly we will be in a post humanist world.

We desperately need best practices to manage this transition well.

I think I've asked the right questions, and together we'll arrive at the right answers.

Thank you.

# References

{\rtf \li720 \fi-720 \sl480 \slmult1 \sa0 Duarte, B. N. (2014). Entangled Agencies: New Individual Practices of Human-Technology Hybridism through Body Hacking. {\i{}NanoEthics}, {\i{}8}(3), 275\uc0\u8211{}285.\
Esch, M. B., King, T. L., & Shuler, M. L. (2011). The Role of Body-on-a-Chip Devices in Drug and Toxicity Studies. {\i{}Annual Review of Biomedical Engineering}, {\i{}13}(1), 55\uc0\u8211{}72. http://doi.org/10.1146/annurev-bioeng-071910-124629\
Hacking, I. (2005). The Cartesian vision fulfilled: analogue bodies and digital minds. {\i{}Interdisciplinary Science Reviews}, {\i{}30}(2), 153\uc0\u8211{}166. http://doi.org/10.1179/030801805X25963\
Norton, Q. (n.d.). The Next Humans - Body Hacking and Human Enhancement. Retrieved from http://www.ambiguous.org/quinn/bodyhacking.pdf\
Thomas, D. (2005). Hacking the body: code, performance and corporeality. {\i{}New Media & Society}, {\i{}7}(5), 647\uc0\u8211{}662.\
}
