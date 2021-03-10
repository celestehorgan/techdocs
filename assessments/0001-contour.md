# Docs assessment

## Introduction

Prepared by: Celeste Horgan (@celestehorgan)
Date: March 2021

This is an assessment of your project documentation and website (if present), prepared for you and your project by the CNCF techdocs team.

This document aims to:

- Measure existing documentation quality against the CNCF’s standards
- Recommend specific and general improvements
- Provide examples of great documentation as reference 
Identify key areas which will net the largest improvement if addressed 

## How this document works

The assessment is divided into three sections: 

- **Project documentation:** for end users of the project; aimed at people who intend to use it
- **Contributor documentation:** for new and existing contributors to the project
- **Website:** branding, website structure, and maintainability

Within each section you receive a rating on different criteria. The full definition of each criteria is defined in [the criteria](criteria.md). We recommend reading each criterion’s definition.

## Project documentation 


| Criteria | 1 = (Is not present or requires significant work) | 2 | 3 = (is present, but needs work) | 4 | 5 = (is executed extremely well or no improvement required) |
| ---                       | --- | --- | --- | --- | --- |
| Information architecture  |     |     |     | ✅   |     |
| New user content          |     |     |  ✅  |     |     |
| Content maintainability   |     |     |    |     |     |
| Content creation processes |     |     |     |    |     |

**Comments**

- **Information Architecture**: Content is generally well structured and easy to understand, but there is some room for improvement by making some small changes to section titles and  menu order.

- **New user content**: Project Countour benefits from a straightforward Getting Started Guide with lots of code snippets. It could use improvement in areas like guiding the user from the Getting Started Guide through the bulk of the documentation content and examples. 

- **Content maintainability**:

**Recommendations**

- **Information Architecture – Titling**: 
    - **The guides section:** Having "Guides" as a top-level section which appears in the nav before documentation is a bit confusing. I recommend having documentation as the second link beside Getting Started. 
        - **Guide titles**: The content in this section seems to be task/tutorial topics – as such I recommend titling them all using action (-ing) verb phrases. 
            - Good: "Using Gateway API with Contour"
            - Not good: "External Authorization Support"
        - **Titles alone are not enough**: I also recommend providing a short description of the content in each guide on the /guides root, to help users decide if the content is relevant to their interests without clicking in.
    - **Resources**: There is a resources subsection in the docs and one in the top nav. Both have different content. Either rename the top nav resources section "Videos" or rename the 

- **New user content**:


## Contributor documentation 


| Criteria | 1 = (Is not present or requires significant work) | 2 | 3 = (is present, but needs work) | 4 | 5 = (is executed extremely well or no improvement required) |
| ---                       | --- | --- | --- | --- | --- |
| Communication methods documented  |     |     |     |     |  ✅   |
| Beginner friendly issue backlog         |     |     |     |     |   ✅  |
| “New contributor” getting started content  |     |     |     |     |  ✅   |
| Project governance documentation |     |     |     |     |   ✅  |

**Comments**

On the whole, Project Contour does an excellent job of documenting things for new contributors and making the process as smooth as possible. No major feedback in this area, but some minor suggestions to imrpove an already good process.

Project governance is clearly documented in the communtiy repo, new contributor documentation is clearly signposted on the website, in the docs section of the website, and in the repo. Great job team!

**Recommendations**

One major suggestion: update [SITE_CONTRIBUTION.md](https://github.com/projectcontour/contour/blob/main/SITE_CONTRIBUTION.md) to Hugo when ready.

- Do a backlog clean of `kind/docuentation` and ensure that all issues are still valid. Close any which are not. For example [this issue](https://github.com/projectcontour/contour/issues/2053) was opened in 2019.
- Improve stub issue descriptions [like this one](https://github.com/projectcontour/contour/issues/2183). A great example of how to write an issue like this without providing too much detail is [this one](https://github.com/kubernetes/website/issues/13864): walk someone new through the steps of thinking through the problem.


## Website


| Criteria | 1 = (Is not present or requires significant work) | 2 | 3 = (is present, but needs work) | 4 | 5 = (is executed extremely well or no improvement required) |
| ---                       | --- | --- | --- | --- | --- |
| Branding and design  |     |     |     |     |   ✅  |
| Case studies/social proof |     |     |     |  ✅  |     |
| Maintenance planning |     |     |   ✅  |     |     |

**Comments**

- **Branding and design**: The Project Contour website looks very professional and consistently branded! No major improvements needed.

- **Case studies/social proof**: Project Contour's [resources page](https://projectcontour.io/resources/) lists a number of great talks given on the project and shows that it's an active member of the cloud native community. While ideally we would see a logo wall of users or case studies, for a project of contour's size this is a great addition to the site.

- **Maitenence planning**: 
    - **Monorepos**: Having a docs+code monorepo is risky in the long term, as it couples all docs builds with code builds and vice versa. If docs CI fails because Netlify is temporarily down, for example, this means that all your code builds can potentially fail as well. Coupling docs in a repository with code can also make a code repo's size expand expoentially, especially as projects pick up steam, write more blog posts (with images), and add other multimedia.

**Recommendations**

- **Branding and design**: one extremely small styling suggestion which would make a great first issue:
    - for `<h2>` elements on documentation pages, change the margin from `margin-bottom: 2rem` to `margin-top: 1rem; margin-bottom: 1rem` or (preferred) `margin-top: 1.5rem; margin-bottom: 0.5rem;`. In general it's better to have padding above an h2 rather than below it, as this helps seperate each section of a page.

- **Maitenence planning**: Unless you have very good reasons for staying in a docs+code monorepo, we strongly suggest migrating documentation to its own repository and maintaining it seperately.


## Recommendations

_From the recommendations above, pull out the top 1-3 concerns for this particular project and expand on them in enough detail that you could either:_
    - _Pass the work off to a contractor or other member of the CNCF techdocs team_
    - _Write a GitHub issue for the project team and place it in the backlog and someone not involved in the docs assessment process could execute on it_




