# notes

## Ideas for dev projects

- extract and standardize layout engines
  - let the Figure have a LayoutEngine attribute
  - let it do _what ever it wants_ at draw time
  - can relax fixed figure size!
  - flex-box style layouts
  - R-style "view port" based layout
- improve hatching API
  - we think the backends have enough flexibility for arbitrary fill
  - need to add user-facing API code
- path strokes
  - beyond dash pattern
  - arrow heads
  - vary
- 3D improvements
- arrows
- nested tick labels
- improved twin/parasite/secondary support

# Proposal

## Proposal purpose

> Limit to one sentence (maximum of 255 characters, including spaces)

> 169 characters

To support the continued maintenance, growth, development, and community
engagement of Matplotlib, the foundational plotting library of the Scientific
Python Ecosystem.




## Proposal Summary

> A short summary of the application (maximum of 500 words) (auto-filled from
> LOI; update if needed)

> The initial call trimmed this to 250 words, and then updated it back to 500
> this is a (very) cut down version I got to.  Not sure if we want to stay with
> the shorter version or stick with the original version

> 229 words


Matplotlib is the foundational data visualization library for the Scientific
Python Ecosystem, with over a million users, including researchers in
bio-medical imaging, microscopy, and genomics.
For the past 18 years Matplotlib has been maintained by a vibrant, primarily
volunteer, community.  However given the sheer size of the project and
adoption, we need to supplement the volunteer community with supported full
time maintainers working on the project.  For the past 17 months CZI EOSS
support for developers has had a positive effect on the project by
complementing and enabling, not replacing, volunteer work: we propose to
continue this effort.

The primary component of the proposed work is the continued maintenance of the
library.  Maintenance tasks are essential for the project's health; though each
individually is small, they are frequently time critical and tedious.  In
addition to on-going and routine maintenance, there are substantial, but
incremental, enhancement to Matplotlib that require long blocks of dedicated
effort to implement.  Finally, supported developers improve the management of
the project.  We now have the time and bandwidth to make strategic decisions
about the direction of the project to ensure the long term health and viability
of Matplotlib.

An important part of project management is community management: fostering,
diversifying, and growing our community.  We must ensure that our community is
open and welcoming to everyone who wants to join, with opportunities to
contribute in a spectrum of roles as their interests and skills develop.


> original
> 463 words

Matplotlib is the foundational data visualization library for the Scientific Python Ecosystem, with over a million users, including researchers in bio-medical imaging, microscopy, and genomics.  For the past 18 years Matplotlib has been maintained by a vibrant, primarily volunteer, community.  However we have grown too big and widely used to continue on solely volunteer effort.  For the past 17 months CZI EOSS support for developers has had a positive effect on the project by complementing and enabling, not replacing, volunteer work.  We propose to continue this effort.

The primary component of the proposed work is the continued maintenance of the library.  Maintenance covers a wide range of tasks including triaging and fixing bugs, reviewing Pull Requests, tagging and building releases, and keeping the continuous integration services running.  These tasks are essential for the project's health; though each individually is small, they are frequently time critical and tedious.  It is unfair and impractical to rely solely on volunteers to accomplish such tasks.

With only volunteer effort we had an ever growing backlog of Issues and PRs.  This risks missing good ideas and is both discouraging to new contributors and distracting to the core developers.  In contrast, with CZI support we have decreased our backlog of open Issues and PRs despite an increase in the number submitted over the last 17 months.

In addition to on-going and routine maintenance, there are substantial, but incremental, enhancement to Matplotlib that require long blocks of dedicated effort.  Without funding, this type of project can drag out for months to years or stall altogether.  Examples include fixing long-standing rendering and performance issues, deep-dive explanatory documentation, homogenizing and smoothing the API, and new user-facing functionality.  Projects to be pursued with the funding requested here will be selected in consultation with down-stream biomedical libraries.

Finally, supported developers improve the management of the project.  We now have the time and bandwidth to make strategic decisions about the direction of the project to ensure the long term health and viability of Matplotlib.  An important part of project management is community management: fostering, diversifying, and growing our community.  This requires dedicated effort, over long periods of time, beyond what can be sustained by volunteers alone.  We must ensure that our community is open and welcoming to everyone who wants to join, with opportunities to contribute in a spectrum of roles as their interests and skills develop.

We propose to continue full support (1 FTE) for Elliott Sales de Andrade and partial support (.2 FTE) for Thomas Caswell.  The effort will be split with approximately .75 FTE for maintenance, .25 FTE for medium sized enhancements, and .2 FTE for community and project management.  We also propose to fund Code of Conduct incident response training.




## work plan

> A description of the proposed work the applicants are requesting funding for,
> including resources the applicants will provide that are not part of the
> requested funding. For software development-related work (e.g., engineering,
> product design, user research), specify how the work fits into the existing
> software project roadmap.  For community outreach related activities (e.g.,
> sprints, training), specify how these activities will be organized, the
> target audience, and expected outcomes (maximum of 750 words)

> It is almost certain that good ideas, critical bugs, and beneficial
> contributions are being unintentionally overlooked.


> For example issues and PRs for 3D plotting had developed a particularly bad
> backlog, Elliott was able do devote significant time to resolving many of these
> issues and completing several stalled PRs.


> 750 words

The proposed work can be broadly classified into three parts:

- on-going and routine maintenance of Matplotlib;
- implementation of several mid-sized features;
- community and project management.

These tasks underpin the long term health of the library but are ill-suited to be accomplished solely with volunteer effort.

The primary component of the proposed work is the continued maintenance of Matplotlib.  Maintenance covers a wide range of tasks including triaging and fixing bugs, reviewing Pull Requests, tagging and building releases, and keeping the continuous integration services running.  These tasks are essential for the project's health; though each individually is small, they are frequently time critical and tedious.  It is unfair and impractical to rely solely on volunteers to accomplish such tasks.

Prior to 2020, with only volunteer effort, we had an ever growing backlog of Issues and PRs.  A large backlog of open Issues and PRs is discouraging to new contributors and distracting to the core developers.  With CZI support we have decreased our backlog of open Issues and PRs despite an increase in the number opened over the last 15 months.  This has been done both by closing isolated issues and by identifying clusters of issues that can be fixed via larger improvements in the library.

Maintaining Continuous Integration (CI) is a core part of our quality assurance process.  With every PR and merge we run our full test suite, including building the documentation, on a variety of platforms and software versions.  While the service providers offer free resources to open source projects, configuring and maintaining the system requires specialized knowledge; it is tedious, time consuming, and unappealing to volunteers -- but fixing it is time critical.  Current CZI support enabled Matplotlib to survive a major disruption to our CI infrastructure with almost no noticeable fallout.

In addition to routine maintenance, there are substantial but incremental improvements that require concentrated effort.  Examples include fixing long-standing rendering and performance issues, deep-dive documentation, making the API more self-consistent, and new user-facing functionality.  CZI support to date has enabled finishing a 5 year old documentation PR, implementing hi-dpi support for Tk, and modernizing parts of the C++ code base.  Work is on-going to add a color-blind simulation filter to the UI to facilitate accessible visualization.  Candidates for future work include overhauling automatic Axes layout and expanding our API for hatching.  Funding would allow us to tackle about 10 such medium-sized, self-contained projects over two years.  Without funding, this type of project can drag out for months or stall altogether.

The most valuable aspect of the Matplotlib project is the community.  While the code is what enables our users to get their jobs done, the people who build and support the code, are the heart of the project.  As with the code, we need to deliberately maintain, support, and grow the community.  This requires dedicated effort, over long periods of time, beyond what can be sustained by volunteers alone.  We must ensure that our community is open and welcoming to everyone who wants to join, with opportunities to contribute in a spectrum of roles as their interests and skills develop.

The lack of diversity in open source is a bigger problem than can be solved by a single project alone; to that end we propose to collaborate with other ongoing and proposed efforts.  NumFOCUS is currently conducting research on Contributor Diversification and Retention to collect baseline measurements of our demographics and produce recommendations on best practices for attracting and retaining diverse contributors.  We will use the resources from this proposal to implement those recommendations, which should be preliminarily available in Q2 2022.  Additionally, Matplotlib is supporting a proposal to the Essential Open Source Software for Science Diversity and Inclusion Grants RFA led by Melissa Mendonça to create and fund a Contributor Experience Lead (CEL) role across NumPy, SciPy, Pandas, and Matplotlib which would run concurrently with this proposal.  We will use resources from this proposal to support the CEL.

We propose to continue full support (1 FTE) for Elliott Sales de Andrade and partial support (.2 FTE) for Thomas Caswell along with travel and equipment support for 2 years.  The effort will be split with approximately .75 FTE for maintenance, .25 FTE for medium sized enhancements, and .2 FTE for community and project management.  We also propose to fund Code of Conduct incident response training.




## Milestones and Deliverables

> List expected milestones and deliverables, and their expected timeline. Be
> specific and include (where possible) any goals for metrics the software
> project(s) are expected to reach upon completion of the grant (maximum of 500
> words)

> 203 words

Quantitatively evaluating maintenance work can be tricky---some Issues or PRs take minutes to review while others can take days to weeks of effort---but we believe that there is value in looking at the throughput of issues and PRs supported by the grant.  The total number of open issues and PRs is dependent on both how many come in and the amount of work done by volunteers.  We will aim to hit the following metrics:


- Initial response to all issues / new PRs within a week
- Resolve majority of new issues / PRs within 1 month
- Resolve 75 issues / quarter
- Merge or close 75 PRs / quarter

We will aim to complete 10 mid-sized projects of similar scope to those described above.  The exact projects will be determined in collaboration with the community and downstream bio libraries.

We will target a feature releases (3.N.0) every 6 months with 2-3 patch releases (3.N.X) between feature releases.

As mentioned above, Matplotlib is involved in on-going and proposed work on improving diversity in our community.  We will implement the recommendations of those efforts and, if funded, support the Matplotlib Contributor Experience Lead.




## Diversity, Equity, and Inclusion (DEI) Statement

> Advancing DEI is a core value for CZI, and we are requesting information on
> your efforts in this area. Describe any efforts the software project(s)
> named in this proposal have undertaken to increase diversity, equity, and
> inclusion with respect to their contributors and audience.  Please see
> examples from applications funded in previous cycles (maximum of 250 words)


Matplotlib is committed to being an open and welcoming project.  We believe that transparency and explicitness of process and in communication are key to building an inclusive, equitable, and diverse project.  In our effort to be welcoming, we have worked at being more explicit about our norms and values and how the project operates.  To this end, we have put major effort into documenting our governance and defining leadership roles, and clarifying specific expectations for new code and community contributors.  We have started two initiatives to lower the barrier of entry for individuals to get involved in developing Matplotlib: a triage role in the project and an "incubator" channel on our gitter.  It is critical that all contributors, independent of experience level both in general and with the project, feel safe to make mistakes and learn in our community.  We strive to embody these values in our interactions on GitHub, our mailing list and community discussion forum (discourse), and in our social media.  We hope that these practices will empower and encourage people from varied backgrounds and experiences to participate in Matplotlib.



## Short description

> Short description of software project (200 words maximum) (required)

> 125 words
> this is what we put is for round 3 and is lifted from the website


Matplotlib is a Python 2D plotting library for producing publication quality
figures in a variety of hardcopy formats and interactive environments across
platforms.  Matplotlib can be used in Python scripts, the Python and IPython
shells, the Jupyter notebook/lab, web application servers, and four graphical
user interface toolkits.

Matplotlib tries to make easy things easy and hard things possible.  You can
generate plots, histograms, power spectra, bar charts, error charts,
scatterplots, etc., with just a few lines of code.

For simple plotting the pyplot module provides a MATLAB-like interface,
particularly when combined with IPython.  For the power user, you have full
control of line styles, font properties, axes properties, etc., via an object
oriented interface or via a set of functions familiar to MATLAB users.


## 3a. Progress Report:

> Provide a short summary of progress towards the deliverables in your
> currently funded proposal (maximum of 250 words)

The EOSS3 grant builds on the work of EOSS1 and supports one developer at 30%
(Thomas Caswell), one graduate student (Hannah Aizenman) with partial summer
support for her advisor (Michael Grossberg), and a full time Research Software
Engineer (Elliott Sales de Andrade).  Elliott's funding has a two-month delay
from Caswell and Aizenman.

Elliott has focused on the maintenance and support aspect of the grant.  As
part of ongoing maintenance, he increased automation of the release process and
CI infrastructure, enabling us to make 1 feature and 2 bug-fix releases in
cycle 3 to-date, with an additional 2 feature and 6 bug-fix releases in
cycle 1.  Elliott implemented or shepherded to completion several mid-sized and
high-impact projects including toolkit-specific work (Hi-DPI improvements) and
internal refactors (deprecation cleanup, internal storage refactors, c/c++
extension improvements).

Hannah is making progress on her thesis and is on-track to graduate in Q2 2022.
She has completed her thesis proposal and submitted a paper on this work to
IEEE VIS 2021 (currently under review).  We have begun preliminary discussions
with MNE-Python, DeepLabCut, and scanpy to identify a biology partner to work
with on a proof-of-concept implementation.  We have submitted a proposal to
present an update to the wider community at SciPy 2021 in July.




> Previous progress report:

The current grant is supporting one developer at 40% (Thomas Caswell), one
graduate student (Hannah Aizenman) with partial summer support for her advisor
(Michael Grossberg), and a full time Research Software Engineer.  For the latter
we ran a search and hired Elliott Sales de Andrade who started in mid-March.

Elliott has focused on the maintenance and support aspect of the grant.  We hit
our target of a net reduction of open PRs by 50/quarter and are making progress
on reducing the number of open issues.  Our initial estimates of the effort per
issue closed were too optimistic; however, we merged several mid-sized and
high-impact projects (documentation, JavaScript modernization, and a complex
axes layout helper).  Additionally we drafted new governance and contributor
onboarding guidelines and had 2 feature and 4 bug-fix releases.

We presented our new architecture ideas to the scientific library development
community at the SciPy 2020 maintainers track.  We designed the prototype API to
have a clean separation between the DataSource, Artist, and rendering layers.
We started implementing sample DataSources and Artists to formalize and
validate the interface between them.  Because the prototype is still developing
rapidly, we are postponing working with a downstream partner until the API has
stabilized.


## Existing support:

> List active and recent (previous two calendar years) financial or in-kind
> support for the software project(s), including duration, amount in USD, and
> source of funding. Include in this section any previous funding for these
> software projects received from CZI (maximum of 250 words)

- EOSS-0000000100, (Jan 2020 - May 2021) 1yr, 250k$, CZI
- EOSS3-0000000149, (Jan 2021 - Jan 2022) 1yr, 250k$, CZI

- NF small development grant (5k$ to support documentation, completed)
- NF small development grant (3k$ to support a hosted mac mini, 3yr)

- Google summer of code (2020, 2021) 1 full time student per summer, in-kind, Google
- Google season of docs (2020) 2 part-time technical writers (3 and 6 months),
  in-kind, Google


## Value to Biomedical Users (required):

> Briefly describe the expected value the proposed scope of work will deliver
> to the biomedical research community (maximum of 250 words) (auto-filled from
> LOI; update if neeeded)

Scientific Python libraries in biomedical and other fields rely on Matplotlib for visualization.  The use of Python and Matplotlib in biomedical contexts is rapidly increasing.  The attached figure shows the growth over time of the term "matplotlib" in journals classified with a range of biomedical topics. There has been dramatic growth in the number of references.  For example, in the category of Biochemistry, Genetics and Molecular Biology the yearly citation have increased from 25 in 2012 to 334 in 2020.  Given that citing software is not yet standard, we expect these numbers to under represent the actual usage.

The proposed work will help ensure the health and continuing growth of this foundational component.  Matplotlib is a direct dependency of many other packages in the Scientific Python Ecosystem.  These include other general purpose tools, such as scikit-learn, networkx, pandas, xarray, and scikit-image that are used by biomedical researchers, and biomedical-specific projects such CellProfiler, scanpy, starfish, nipy, MNE-python, DeepCutLab.  All of these projects have received CZI funding.
