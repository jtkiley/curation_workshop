---
title: 'Data Curation Workshop'


---

# Common issues in study execution

1. One co-author passes primary data management responsibility to another co-author.
1. At some point (or many points), you would like to re-pull data to add variables or observations.
1. You later notice that some data was gathered with overlapping identifiers (e.g., ticker symbols over time), and subsequent data was merged with those identifiers.
1. Your coauthor has models that you can't replicate, and you can't figure out why.


# A philosophy of data management.

Data management (or curation) is a process of transforming data from an initial, raw state to a research-appropriate state.
We can think of this as a highly iterative process with four interrelated steps: access, cleaning, selection, and analysis.
In general, we seek to move from the data we can get toward data that we can use to examine our theoretical questions.
To best promote that goal in a reproducible and robust way, we suggest four principles and some associated implications.

1. **Others (and you) should be able to reproduce your study.**
1. **Data management errors happen, and you should be able to detect and repair them easily.**
1. **Data management is iterative and ongoing, and practices should be designed to match this nonlinear flow.**
1. **Good data tools are built well once and used repeatedly.**

While what we recommend below is specific to Python and dataframes (which we'll be introducing you to today), it also applies good practice basic to most data-intensive research processes outlined above.

# Implications for practices.

1. **You should know about the data you gather.** This includes documenting data retrieval and providing a reference for unclear measures. Screenshots of data queries or sections of data manuals can work well as documentation with minimal effort.
1. **All changes to pulled data should be in code that runs.** There are two parts here. All changes should be in code, because that's authoritative, reproducible  evidence of what you did. It should run because you will often want to make a change somewhere in the middle of the data management pipeline. When it runs, you can simply make changes where necessary and rerun your notebook or scripts.
1. **When developing your code (and after), you should look at the data often.** Looking at your data helps with data issues, error detection, and idea generation. For example, `df.merge(df2, on=['id', 'year'], how='left')` in pandas works a little differently than `merge 1:1 id year using . . .` in Stata. Pandas will duplicate left side data if there are multiple matches, but Stata will give an error about unique identification in the using data. When you switch, it's easy to not see until later. Once the code for a particular dataframe is relatively stable, I tend to trim back to displaying it once after prepping, so I can reference the prepped version later. I also examine the data separately once it is assembled. That includes things like histograms of variable distributions and correlations. Often, there is strong evidence that corroborates (or counters) your theoretical mechanism(s). Most of us tend to pull a lot of data, and there is often something there that can help support or refine your theoretical story.
1. **Your data should always be built by running your code as is.** This practice ensures that your code is authoritative. That goal is undercut if you simply cut and paste commands without ensuring that the script runs cleanly. In pandas and Jupyter, use "Kernel:Restart Kernel and Run All Cells." In Stata, use the `do` command to run your `do` file.
1. **When naming your clean dataset, use a name that uniquely identifies it.** In many studies, one co-author will perform most or all of the data management, and others may use it to run models. Like a software release, you want versions distributed to the team to be right and relatively stable. I find that the date and project name work well (e.g., `20180418_workshop.dta`). Whenever discussing results or changes, asking about the data version can help clarify whether you are all working with the same underlying data.
1. **Use file-sharing services (e.g., Dropbox) for distribution and storage, not work-in-progress files.** Many project teams find themselves confused about the latest draft or the latest data when the dropbox folder is used "live." While version control (e.g., git and Github) can solve this problem and provide a number of helpful productivity and documentation benefits, it's still a software development tool that assumes a lot knowledge of its users.
1. **(More advanced) Capturing your known good code to reuse makes future projects better.** We recommend two effective approaches. First, for some common datasets, you can download a new copy once a year and process it with the same code as the prior year (with any needed changes). This prevents duplicated code in projects, and it helps manage the lack of data versioning and change transparency in most of our datasets. Second, you can write general purpose tools for reuse that you can capture in a small, private python package. For example, these do things like read and write lists for pulling data (e.g., event lists for abnormal returns data).
