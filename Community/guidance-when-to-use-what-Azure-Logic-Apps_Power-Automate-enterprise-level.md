# Guidance why how what in Power Platform / Azure Logic Apps for enterprise level solutions

## first thoughts

* personal productivity !== Enterprise scale
* maker roles are not educated about CI/CD pipeline, support, maintainability, lifecycle, documentation
* this leads to technical debt, because maker role is defined as "job is NOT to make apps, but likes/needs to solve problems" --> will sooner or later abandon solution
* connectors exposed to makers on Power Platform guide makers into the wrong way (SAP connector means, this is most likely not a personal productivity improvement, but a mission critical business process)
* Power Automate flows can have huge impact but also there are downsides (run history data only available 28 days, runs in user's context etc.), which makes it unsuitable for enterprise scale solutions
* Power Automate is more a gateway drug to foster citizen development, mvp approach, POC
* it takes more than just the ability to code to have a sustainable solution. 
* people confuse "low code" with "low effort" 

## Bob's thoughts - just for discussion Luise, not thinking this would be the article

Computers are fantastically stupid. No matter how stupid you might imagine them to be, they are even stupider than that. They need to be told how to do _everything_. The art of development is to _express_ what we want the computer to do in sufficient detail that it can do it.

There is a huge spectrum in this expression. At one extreme, we program in machine language. At the other, we can use fairly high level tools such as Excel or Power Apps. Somewhere in the middle are "higher-level" languages like JavaScript or COBOL. I mention COBOL here because it was the first of its kind - it was designed to be readable by humans, so a programmer could review their work with a business person.

As you move along this spectrum, you gain _productivity_ - you don't need to teach the computer to draw characters on the screen, for example - but you lose _flexibility_. COBOL would seem very inflexible to modern programmers, and a tool like Excel is super limited to showing a few specific data structures (mainly rows and columns). The extreme of easy (but inflexible) is a single button that can do one thing - play an audio file of someone saying "that was easy" or maybe destroying an evil lair. It's so easy to push, but it can only do one thing.

Part of the key to fusion development is to allow makers to innovate with maxiumum productivity and a fast, easy learning curve so they can focus on the problem at hand. But inevitably they will hit "the brick wall" as we used to call it in the consulting startup where I used to work. At that point, it makes sense to bring the programmers in to fill any gaps, and most low-code tools have a way to do this:

| Tool | Extensibility |
|------|---------------|
| Power Apps | custom components, custom connectors, web services |
| Power Automate | custom connectors, web services, flexible triggers like queue or webhook |
| Power BI | custom visuals, custom connectors |
| Excel | macros, add-ins |

-----------------

There's more to this fusion dev thing, however, than breaking down brick walls. There is also the issue of addressing technical debt when a maker solution becomes mission critical.

I once worked with a company that made gaming machines. Someone had made an innovation that allowed the machines to be modified in the field, and it made a huge difference in their business. But the innovation was based on a single spreadsheet, which became unwieldy and brittle. Only that one person really knew how to update the spreadsheet, and company leaders worried that if they suddenly left, the company would go out of business! It was a classic case of technical debt, and after some consultation, we were able to put an estimated dollar amount to that debt - to write a robust and maintainable application that would replace the spreadsheet and grow with the company's needs.

The answer here is not that the spreadsheet was bad! Imagine if that someone had to convince their superiors to bring in programmers before the idea of modifying machines in the field could be tested. Chances are it wouldn't have happened. Indeed, it's the sad truth that many IT departments, in order to minimize risk and make their work more predictable, actively discourage employees from this kind of innovsation. The classic "The IT Department of 'No'" is not the answer!

The key is to:

(HERE's where we disagreed in our discussion Luise and I think you can convince me of your position ... you have a ton more experience than me in this area. Just putting it out there as I'm writing stream of consciousness right now ...)

The key is to (pick one or more :) )

a. recognize the debt early enough to avoid putting the organization at risk, and reaizing that the benefit exceeded the technical debt many times over, provide the resources to build a production-ready app

b. provide the developer with an understanding of what constitutes a production ready app and the tools to manage it (did I get that right?)

c. build maker tools with the full lifecycle in mind (like Power Apps seems to do a reasonable job here) so they can be "promoted" without needing to remake them (starting to happen! But it's out of the dev's control, the tool vendor needs to do it, yes?)


A COUPLE OTHER directions for this whole fusion thing:

To reflect on the working title for this article ... is "when to use what" actually able to change during the life of a solution? Like maybe it starts in Power Automate (friendlier and more available to makers) and at some point it migrates to "Logic apps" with dev, test, and staging, checked into source control, CI/CD, etc. ?? 


