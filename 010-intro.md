# Introduction

This thesis describes the education and pedagogy of data science,
how these findings can be applied to the biomedical sciences,
and how data science education differs from computer science education.
It is organized in the way you would go about creating a set of domain specific data science learning materials.
First you figure out who your learners are and what are their relevant prior experiences with
data and programming;
Section **1.x** introduces learner personas as a means to identify your learner audience
and the process of creating and using personas are described in Chapter **xxxxx2?** and **xxxxx3?**.
Once we have our audience identified,
their background, relevant prior knowledge, perception of needs, and special considerations
are used to create a set of learning materials.
Section **1.x** introduces these learning materials,
and how it's effective the materials are to meet the learning objectives;
The details of these learning materials and their effectiveness are described in chapter **xxxxx4?**.
In section **1.x** we look more closely into how learning works,
by looking at the formative assessment questions that are asked throughout the learning materials,
and how they play a role in the final summative assessment question that aims to summarize the learning objectives.
Details of this experiment are described in Chapter **xxxxx5?**.
Finally Chapter **xxxxx6?** summarizes the impact of my work in data science education,
and my plans for the future.

## History of Data Science

Figure **xxxxx** gives an overview of how
statistics, data science, and computational programming and education
have co-evolved in the last half century.

### Where the term came from

Statistics and computer science has always been associated with "data science".
In 1962, John Tukey describes data analysis as "intrinsically an empirical science"
and points to electronic computers as being vital to data analysis [@tukeyFutureDataAnalysis1962, @pressVeryShortHistory].
This scientific approach to data analysis,
with hypothesis driven exploration, was later called "Exploratory Data Analysis", and in 1977,
Tukey calls for exploratory data analysis to be used along with confirmatory data analysis by understanding
the data first before calculating any confirmatory statistic [@tukeyExploratoryDataAnalysis1977].

<!-- Somewhere in this timeline there was an article about statistics and putting things off to other domains -->

By 1974, Peter Naur defines "data science" as: [@pressVeryShortHistory]

> The science of dealing with data, once they have been established, while the relation of the data to what they represent is delegated to other fields and sciences.

While data science did not take on mainstream adoption as a term for the type of skills needed to work with data,
statisticians realized that many of the kinds of insights they have come from using computational tools [citation_needed].
In 1997, C. F. Jeff Wu at the University of Michigan calls for a rebranding of "statistics" and "statisticians" in favor of "data science" and "data scientists", respectively,
since many other "good" names were already taken (e.g., computer science, information science, material science, cognitive science).
In 1998, John Chambers is awarded the ACM Software System Award for the S system for graphics and data analysis.
By 2001, the field of "data science" was born with William Cleveland's plan to expand the technical areas of statistics.
Cleveland proposed 6 technical areas and how university resources should be allocated [@clevelandDataScienceAction2001]:

1. Multidisciplinary Investigations (25%): data analysis collaborations in a collection of subject matter areas
2. Models and methods for Data (20%): statistical models; methods of model building; methods of estimation and distribution based on probabilistic inference.
3. Computing with Data (15%): hardware systems; software systems; computational algorithms
4. Pedagogy (15%): curriculum planning and approaches to teaching for elementary school, secondary school, college, graduate school, continuing education, and corporate training
5. Tool Evaluation (5%): surveys of tools in use in practice, surveys of perceived needs for new tools, and studies of the processes for developing new tools
6. Theory (20%): foundations of data science; general approaches ot models and methods, computing with data, teaching, and tool evaluation; mathematical investigations of models and methods, computing with data, teaching, and evaluation

Since universities have been traditional institutions for innovation,
along with government research labs,
and corporate research organizations,
they can shape what is taught to new graduates to progress data science [@clevelandDataScienceAction2001].
In 2002 the "Data Science Journal" was launched,
and by 2003, the "Journal of Data Science" was launched
to present and share ideas.

Hal Varian, Google’s Chief Economist, mentions in McKinsey Quarterly in 2009,
computer engineers was the sexy job in the 1990s,
statisticians would be the sexy job in the next 10 years.
Varian alludes to the need to visualize and learn from the ubiquitous amount of data and many of these skills will need to be transferred to managers who need to understand the data themselves.
As data science becomes a more common term,
in 2010 Hilary Mason and Chris Wiggins write "A Taxonomy of Data Science" [@masonTaxonomyDataScience2010] and
Drew Conway creates "The Data Science Venn Diagram"
that aims to clarify what is data science and what skills are needed to be a competent data scientist [@conwayDataScienceVenn].
Mason and Wiggins's Snice taxonomy (aka OSEMN) states that a data scientist, in rough chronological order,
obtains, scrubs, explores, models, and i(n)terprets data.
In 2012 Tom Davenport and D.J. Patil publish "Data Scientist: The Sexiest Job of the 21st Century" in the Harvard Business Review, which talk about the types of insights data science can bring,
while also describing the multitudes of skills a data scientist needs to incorporate into analysis,
mainly around working with unstructured data to create and present an analysis [@davenportDataScientistSexiest2012].
Davenport and Patil also talk about the high cost and scarcity of data scientists,
and how businesses must balance the need to stay competitive with the nonstop flow of data,
and waiting for the next wave of talent that is more accessible due to a data scientist's rarefied skills become taught in
classes.
Patil is later named the First U.S. Chief Data Scientist in 2015.
Meanwhile, data science has started to impact the growth of open source in the academic, scientific, and research domains [citation_needed]. Arfon Smith, Kyle Niemeyer, Dan Katz, Kevin Moerman, and Karthik Ram start
the Journal of Open Source Software in 2016, and by 2018,
The National Institute of Health (NIH) released its first Strategic Plan for Data Science
that provides a road map for the biomedical data science ecosystem.

While "data science" may be a relatively new term,
it may evolve just like the evolution of "statistics", "machine learning", and "artificial intelligence"
in mainstream terminology.
But, the core skills of obtaining, cleaning, analyzing, and communicating data insights will remain the same.

<!--
1962	1		ds	John Tukey describes data analysis as "intrinsically an empirical science"
1974	1		ds	Peter Naur defines "data science"
1977	1		ds	Tukey coins "Exploratory Data Analysis"
1997	1		ds	C. F. Jeff Wu calls for "statistics" to be rebranded as "data science"
1998	1		ds	John Chambers is awarded the ACM Software System Award
2001	1		ds	William Cleveland calls to expands technial areas of statistics with data science
2002	1		ds	Data Science Journal founded
2003	1		ds	Journal of Data Science founded
2009	1		ds	Hal Varian claims statisticians would be the sexy job in the next 10 years
2010	1		ds	Hilary Mason and Chris Wiggins write "A Taxonomy of Data Science"
2010	2		ds	Drew Conway creates "The Data Science Venn Diagram"
2012	1		ds	Tom Davenport and D.J. Patil publish "Data Scientist: The Sexiest Job of the 21st Century"
2015	1		ds	Patil is named the First U.S. Chief Data Scientist
2018	1		ds	Journal of Open Source Software founded
2018	1		ds	NIH releases its first strategic plan for data science

-->

## Computational History

### R

John Chambers, Rick Becker, Doug Dunn, Jean McRae, and Judy Schilling
implement the S language in the statistics research department at Bell Laboratories in 1976.
It was the first implemented statistical computing language [@beckerBriefHistory1994].
It's need grew from the necessity of interacting with data using Exploratory Data Analysis
techniques and graphical output [@beckerBriefHistory1994].
In 1988, a commercial version of S was implemented, S-PLUS, but it was eventually
succeeded by R which was in development in 1991 by
Ross Ihaka and Robert Gentleman at the University of Auckland, New Zealand,
and later open sourced in 1995.
The Comprehensive R Archive network (CRAN) was founded in 1997 by the R Core team
as a means to serve as a software repository for users to submit packages that can be
used by other R users.
R's first stable v1.0 version was released in 2000.

<!--
1976	1		r	S language implemented at Bell Labs
1988	1		r	Commercial S-PLUS implemented
1991	1		r	R starts development
1995			r	R is open sourced
1997			r	CRAN is founded
2000			r	R v1.0
-->

The release of additional
data manipulation (`{reshape}` v0.4 in 2005 and `{plyr}` v0.1.1 in 2008)
and visualization (`{ggplot}` v0.2.2 in 2006 and its successor, `{ggplot2}` v0.5.1 in 2007)
tools in CRAN by Hadley Wickham
focused R in exploratory data analysis [@wickhamPracticalToolsExploring2008, @tukeyExploratoryDataAnalysis1977].
Joseph J. Allaire finds RStudio in 2009 [citation_needed]
<!-- look for JJ's 2020 keynote when PBC was announced -->
Wickham believed a lot of the work needed to explore and understand data was being overlooked by statisticians:

> There are definitely some academic statisticians who just don’t understand why what I do is statistics,
> but basically I think they are all wrong.
> What I do is fundamentally statistics.
> The fact that data science exists as a field is a colossal failure of statistics.
> To me, that is what statistics is all about.
> It is gaining insight from data using modelling and visualization.
> Data munging and manipulation is hard and statistics has just said that’s not our domain.

He continued to improve and create a domain specific language (DSL) in R focused around the data science workflow
({reshape2} v1.0 in 2010, {dplyr} v0.1.1 and {tidyr} v0.1 2014).
During this time, RStudio Inc. works on developing the RStudio IDE and is released in 2011 to make interacting and programming
in the R programming language much easier and also provides tools to make exploratory data analysis easier.
In 2012, RStudio Inc. releases `shiny`, a dashboard framework that can be written in R which
lowers the barrier of entry to create, interact, analysis, and publish graphics and data on the web.
These ideas around "tidy data" principles for exploratory data analysis [@wickhamTidyData2014]
cumulated in the release of the `{tidyverse}` in 2016,
which hosts a multitude libraries for the data science DSL in R.
For this work and "influential work in statistical computing, visualization, graphics, and data analysis" and
"making statistical thinking and computing accessible to a large audience",
Wickham was awarded the international COPSS Presidents' Award in 2019 [@InstituteMathematicalStatistics2019].

His work has prompted the `{caret}` (first release in CRAN in 2007 as v2.27) package to be superseded by
the `{tidymodels}` package (first released in CRAN in 2018 as v0.0.1)
for it's consideration of tidyverse principles that where objects share a common philosophy, grammar, and data structure
to make things more interoperable in data and analysis pipelines [@wickhamR4ds, @kuhnTidyModeling2021].
In 2020 RStudio Inc, announced that they have been ******* as a Public Benefit Coorporation (PBC) [citation_needed],
and RStudio PBC employees develop, maintained, and advocate for a plethora of R packages.

<!--
Hadley Whickham and the tidyvesrse:

2005			tidy	reshape on CRAN
2006			tidy	ggplot on CRAN
2007			tidy	ggplot2 on CRAN
2008	10		tidy	plyr on CRAN
2018			tidy	Hadley Wickham's thesis
2009			tidy	Rstudio Inc founded
2010			tidy	reshape2 on CRAN
2012			tidy	Rstudio releases Shiny
2014			tidy	"Tidy Data" published
2014			tidy	dplyr on CRAN
2014			tidy	tidyr on CRAN
2016			tidy	tidyverse on CRAN
2018			tidy	tidymodels on cran
2019			tidy	Hadley Wickham awared COPSS Presidents' Award
2020			tidy	Rstudio PBC announced

- 2005 {reshape} v0.4 on CRAN [@wickhamReshapingDataReshape2007]
- 2006: {ggplot} v0.2.2 on CRAN
- 2007: {ggplot2} v0.5.1 CRAN
- 2008: Oct 2008 v0.1.1 {plyr} on CRAN [@wickhamSplitApplyCombineStrategyData2011]
- 2008: Hadley Wickham's thesis
- 2009: RStudio founded
- 2010: {reshape2} v1.0 on CRAN
- 2012: RStudio releases Shiny, dashboarding system
- 2014: "Tidy Data" published
- 2014: {dplyr} v0.1.1 on CRAN
- 2014: {tidyr} v0.1 on CRAN
- 2016: Initial {tidyverse} 1.0.0 released on CRAN [@wickhamWelcomeTidyverse2019, @ReleasesTidyverseTidyverse]
- 2018: tidymodels v0.0.1 on CRAN
- 2020: RStudio PBC

international COPSS Presidents' Award in 2019 for "influential work in statistical computing, visualisation, graphics, and data analysis" including "making statistical thinking and computing accessible to a large audience".
-->

### SciPy From Travis Oliphant

Python started off as a project by Guido van Rossum for developers to write in an interactive high-level programming language that can
talk to the underlying operating system but still able to interact with native C libraries [@severanceGuidoVanRossum2005].
Python was first released in 1991 and v1.0 was released in 1994 [@severanceGuidoVanRossum2005].
As python gained in popularity, it started to make its way into the scientific research community.
In 1999, the `multipack` library was released to bring scientific computation by wrapping around C and Fortan libraries.
As the scientific community began to grow,
The SciPy community and python package was created in 2001 by Eric jones, Travis Oliphant, and Enthought.
However, the scale of the `scipy` project was too much to maintain,
and spawned the creation of smaller `scikit` projects.
During that time,
a more interactive Read-Evaluate-Print-Loop (REPL),
`IPython`,
similar to other mathematical and programming software like Wolfram Mathematica,
was created by Fernando Pérez to make scientific computing and exploration easier [@ipythondevelopmentteamHistory].
Since much of scientific computation relied on matrix and array objects,
the scientific community was slowly being split between the `numeric` and `numarray` libraries.
In 2005, Travis Oliphant starts creating the `numpy` library to keep the array objects in python cohesive,
since it was used by `scipy`.
In 2006, `numpy` was released.
Since then, many other libraries have been built on top of the NumPy array:
`theano` in 2008, `pandas` in 2009, and `scikit-learn` in 2010.
These libraries have been paramount to the growth of Python in the data science space [citation_needed].
As a means to help sustain and support these critical open source libraries,
NumFOCUS was founded in 2012 as a 501(c)(3) public charity status as a nonprofit in the United States along with the first PyData
conference series, the educational program of NumFOCUS centered around community organization.
Travis Oliphant and Peter Wang also found Anaconda Inc that year
with the goal of supporting the open source python community and help the SciPy ecosystem scale to "big data" [citation_needed].
In 2013, Anaconda releases the `blaze` package to help scale the SciPy ecosystem.
The next iteration of scientific computing interactivity came with Project Jupyter in 2014
with the goal of bringing the interactivity of `IPython` to other programming languages and with a common user interface,
Jupyter Notebooks.
The `dask` project spins off of `blaze` in 2015 with a focused around making multi-core parallelization and distributed computing easier in the SciPy ecosystem.

As "artificial intelligence" gains popularity with the resurgence of neural networks,
tools like TensorFlow was released by Google in 2015,
and PyTorch was released by Facebook in 2016,
both with Python as one of the primary languages.
As more computation happens on a browser interface, and the success of Jupyter Notebooks and it's extensive widget system,
Jupyter Lab was released in 2017 as the next iteration of notebook interfaces in the browser.
Travis Oliphant leaves Anaconda Inc in 2018 to start QuanSight to help sustain the open souce PyData ecosystem
by connecting community members with compaines that use the technonologies.


<!--
1991: Python created by Guido van Rossum
1994: Python v1.0
1998: Multipack, what will later be called SciPy project, starts with the intent to bring Python to scientific computation by wrapping around C and Fortran libraries.
1999: SciPy Released as "multi-pack"
2001: Eric jones, Travis Oliphant, and Enthought created the SciPy community and Python package. However, the scale of the project was too vast and it spawed the scikit projects.
2001: Fernando Perez starts IPython

2005: Numeric and Numarray projects were merged by Travis Oliphant to create NumPy. to keep the array object
cohesive since it was used by SciPy

2006: NumPy is released
2008: Theano
2009: Pandas
2010: scikit learn
2012: NumFOCUS founded. and first PyData conference series around community organization. Anaconda Founded.
PyData is an educational program of NumFOCUS
2013: Blaze project was started to help scale the PyData ecosystem
2014: Jupyter
2015: Jan: Dask project was started
2015: Nov: Tensor Flow
2016: Pytorch
2017: Jupyter Lab
2018: QuanSight, also trying to build open souce partnerships for sustainable oss

Company-backed vs community-back

Complmentary product model, anaconda enterprise, rstudio pro

- Travis Oliphant Keynote Dask Summit 2021: https://www.youtube.com/watch?v=9xquY7fmPjo
- Keynote Business of Open Source, PyData: https://www.youtube.com/watch?v=MCEUPosJuIY
-->

## Software Carpentry and Scientific research computing History

Software Carpentry was founded in 1998 by Greg Wilson and Brent Gorda with the goal of
teaching researchers the computing skills to get their work done more efficiently and effectively.
These workshops are primarily focused around general programming skills for scientific computation.
These teaching materials were made open source in 2005 with support from the Python Software Foundation (PSF).
Software Carpentry continues to grow with the support from the Alfred P. Sloan Foundation and Mozilla Science Lab in 2012.
<!--
and NumFOCUS was also founded as a 501(c)(3) public charity status as a nonprofit in the United States with the mission to support open source projects and help sustain them.
-->
The following year, 2013, the first workshops geared towards Librarians were run.
By 2014, Data Carpentry is founded by Karen Cranston, Hilmar Lapp, Tracy Teal, and Ethan White
with support from the National Science Foundation (NSF)
with the goal of creating materials focused around data literacy aimed at novices in specific research domains.
James Baker is able to expand on Library Carpentry with support from the Software Sustinability Institute (SSI) with the goal of teaching information sciences and best practices in data structures.
Software Carpentry Foundation is also founded under NumFOCUS in 2014.
In 2015, Data Carpentry gets support from the Gordon and Betty Moore Foundation and
in 2018, with the help of Community Initiatives, Software Carpetnry, Data Carpentry, and Library Carpentry
merge together to form The Carpentries.
From 2012 to 2020, The Carpentries have run 2,700 workshops across 71 countries and have touched at least 66,000 novice learners across the 45 open access lessons [@CarpentriesHowWe, @jordanCarpentries2020Annual].
