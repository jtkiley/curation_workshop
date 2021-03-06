---
title: 'Data Curation: Meeting notes'

---

# 2018-03-16 (TH, JK, HT)

- Software
	- Just conda.
	- Installing textblob is easy in conda.
- Presentation
	- Can quicktime record screens?
- Next steps
	- (Jason) Slides.
	- (Tim): Next round on notebook; iterate from there with (Hovig/Laura).


# 2018-02-21 (TH, JK, HT)

- Framing: data curation as a process – workflow
    - Series of hands-on practices
    - Walk-thru of our steps – clean workflow
    - Connection to our central narrative
- Introduction
    - What is Python?
    - How do you deal with unstructured data (vs. numerical data)?
    - How do you define a Research Q (how to pull right kind of data)?
- Workflow steps
    1. Fetch the data (APIs?)
    2. Convert it (into csv?)
    3. Merge with Compustat(?) – or look at charts, pre-post Bitcoin drop
    4. Create a Pandas dataframe
    5. Convert text into numbers (DTM?)
    6. Use text blob to run a basic count / analysis
    7. Visualize it
- Reflections
    - Does what we’ve presented seem doable?
    - Other questions, concerns?
    - How might you use this approach & workflow in your own research?
- Conclusion
    - Parting words form presenters: next steps for participants



# 2018-02-08 (TH, JK, LN, HT)

Tim Hannigan notes from Call Feb 8/18; AOM - Big Data and Managing in a Digital Economy Workshop

Abstract: The emerging trend of big data scholarship in management opens a number of doors for interesting research. Within this growing scholarly field, there is an opportunity, evident from examples in other disciplines, for moving research forward using thoughtful curation, which we define as access, cleaning, selection, and analysis, with an eye toward a theoretically relevant objective. In an active learning workshop, we review a methodology forcuration, describe a practical skillset with freely-available tools, and provide participants witha hands-on experience of working through a high-quality example.

Basic python skills: Pandas, Jupyter, Yelp

Agenda:

* who’s going; Hovig, possibly Jason; Laura is not sure
* Conference taking place April 18-20, 2018 in Surrey, UK
* how we should do it

Content Analysis PDW:

* Jason is now a co-organizer
* diffusing some of these tools for that community
* using it to plug materials that people use themselves; demonstrating the workflows for teaching; base a methods class on this


Laura:

* has demo code for transforming text into a dataframe
* Github repo; we can make it private for now; academic you can get unlimited private repo’s; Jason can set this up
* binder-ize it down the road

Scope:

* intro to Python workshop?
* drinking from a fire-hose in an hour and a half
* we provide them with the sample code and practice
* we might want to give them some work up front; there are a lot of intro to Python courses up front (what is a variable? what is an object? how does it work on a broad level?)
* we can claim and start clearly that people have a min

Can we “tailgate” before the event as well? In chatting with people, or whether they’ll put signs up for us.. We can quickly walk people through… stretch our time

We only have 1.5 hrs; we should be limited in our scope; our learning goal might be to convince people not to use Excel; why a reproducable workshop is essential for creating good data

Pulling lessons from the classroom:

* Hovig has been teaching a basic data class
    * there is a hetergeneity of audience skills
        * what’s the difference between using Excel file or using Python? What are advantages? 2.5-3 mins (Hovig has done this before)
    * he can do a simple intro
* Jason has been using Azure notebooks; could we steer them towards that?
    * as a way to avoid software issues
* Binder;
    * two months ago switched from beta
    * if you publish a paper, you get a binder-badge
    * you don’t need to worry about your software stack ; uses docker containers and Jupyter
    * https://mybinder.org
* do we give it them on Jupyter; just need to get them to install anaconda?
    * the downside is that they need to install software
    * the upside is that they leave the workshop with software

When we have them in the room, do we survey the group a bit?

* do we create a Google form to ask them 8 questions?

I need to get in touch the organizers and ask them if we can contact people? It would be nice if we got the first workshop slot


It takes more time, but you have documentation;

* good data hygene
* data versioning is big outside of management
* data handling practices

Doing workflow is a great way to do things, but if you’re stuck with time, then you wont

* these kinds of things aren’t intuitive

If we have an hour and a half; in practical terms are we thinking hands on, or discussion

* having a call and response
* one person runs through the practical, somebody else is able to reflect upon it
* collect ideas on the side, and see what we can offer

It’s important at some point to acknowledge:

* people aren’t used to doing this sort of work
* within the people who are more comfortable with analysis, even there, there’s a difference between using things that are purpose built (Excel is number based)
* when dealing with unstructured data, these tools are fit for purpose


A potential outline:

* we walk them through an entire workflow: the code with Jupyter notebooks; extract data using api like NYTimes; to Pandas to CSV; to a bar graph
* going from no data to some structured data
* this is a narrative; here’s what we want to accomplish; we step them through that; in the reflection portion “did you notice this? here’s why we did that”
* we provide jumping off points
* handwave over the Python and assume they’ll do some of this stuff on their own
* then have the final 30 mins as a reflection period
* if we put together a document of how to install software tools, then tossed it around doctoral students
    * tell them to install Anaconda

We need to determine:

* what will the narrative be? Where do we start from? Where do we want to get to?
