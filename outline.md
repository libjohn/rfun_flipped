Outline for modules
================
John Little
2020-06-29

<!-- READ THIS -->

<!-- file is generated from outline.Rmd. Please edit that file:  i.e. edit outline.Rmd -->

<!-- READ THIS       ^^^     Yeah, you!!  Eyes up here ^^^                             -->

## Introduction to R - Refactoring the Workshop

Refactor existing workshop for smaller video segments and flipped
presentation

1.  Download software & run locally
      - [R](https://cran.r-project.org/) &
        [RStudio](https://rstudio.com/products/rstudio/download/) are
        not the same thing
          - [RStudio keyboard
            Shortcuts](https://support.rstudio.com/hc/en-us/articles/200711853-Keyboard-Shortcuts)
      - Cloud Options
          - <https://rstudio.cloud>
          - <https://vm-manage.oit.duke.edu/containers>
      - R v Python
          - R is a *data first* (i.e. analysis) programing language
          - Python is a general programming language
          - Are there libraries/packages relevant to your work?
          - Is there a supportive community?
              - [Rfun](https://rfun.library.duke.edu/)
              - [R Community](https://community.rstudio.com/)
              - [R Ladies](https://rladies.org/) | Locally, [R Ladies,
                RTP](https://www.meetup.com/rladies-rtp/)
          - ML leans towards Python, [or does
            it](https://www.tidymodels.org/learn/)?
          - Programmer/Coder v Analyst
              - [how to choose a programming
                language](https://medium.com/better-programming/how-to-choose-a-programming-language-for-a-project-7c7a3e5a4de6)
              - [how to choose a
                religion](https://www.wikihow.com/Find-the-Right-Religion-for-You)
2.  An RStudio project & reproducibility
      - **You are your most frequent collaborator** separated by time
          - **A simple test**: Identify specific computational steps
            from a six-month old project?
          - **A simple goal**: Reproduce your computation on a different
            computer
          - Initial **Reproducibility in a nutshell**
              - Do everything with a script
              - Avoid point & click
              - Use relative paths
              - Write your code to run on any similar environment
              - Read more: [Initial steps toward reproducible
                research.](https://kbroman.org/steps2rr/) Karl Broman
      - **RStudio Projects enable *Reproducibility***
        1.  **Relative files paths**
              - `read_csv("data_raw/raw_data.csv")`
                  - ProTip: `..` to move up one level in the directory
                    structure
                  - Avoid absolute paths
                      - avoid `setwd()`
                      - e.g. `setwd("d:/rfiles/myrproject")`
        2.  ***Restart R and run all chunks***
              - avoid: `rm(list=ls())`
        3.  R Markdown & **literate coding**
              - A script integrates code and natural language
              - Explain and describe your analysis within your workflow
              - Render reports in multiple formats
                  - Notebooks, slide decks, web pages, dashboards,
                    e-books, journal articles
        4.  **File structure** matters
              - [*Practice of Reproducible
                Research*](https://www.practicereproducibleresearch.org/)
                by Kitzes, Turek, Deniz

<!-- end list -->

    EXAMPLE File Structure...
    
    project_name (folder)
    |-- project_name.Rproj
    |-- README.md
    |-- license.txt
    |  data_raw
    |  |-- raw_data.csv
    |  |-- README.txt
    |  data_clean
    |  code_source
    |  |--data_cleaning.Rmd
    |  |--analysis.Rmd
    |  images
    |  reports_results

3.  Get Data & Code Repository
    
      - Access your own data file (e.g. CSV)
      - [Download](https://github.com/libjohn/intro2r-code) & Expand a
        GitHub repository
      - Click on \*.Rproj

4.  Tour of the RStudio environment
    
      - Create a blank project
      - Console | Files / Packages / Help | Environment | Script Editor
      - R Markdown
      - Switch to your other project (from Section 2)
      - [Keyboard
        Shortcuts](https://support.rstudio.com/hc/en-us/articles/200711853-Keyboard-Shortcuts)

5.  Tidyverse & other library packages
    
      - Packages extend the functionality of base R into your domain
        
        | Practice | Frequency | Command                         |
        | -------- | --------- | ------------------------------- |
        | Install  | once      | `install.packages("tidyverse")` |
        | Load     | each time | `library(tidyverse)`            |
        

      - [**Tidyverse**](https://tidyverse.org):
        
        1.  an opinionated collection of packages with consistent
            web-based documentation and a supportive community
        2.  a Meta-package that loads 8 helper packages and installs
            many consistent utilities
        
        | Name    | Purpose                                   |
        | ------- | ----------------------------------------- |
        | readr   | importing CSV data                        |
        | dplyr   | transforming data                         |
        | ggplot2 | visuazlizing                              |
        | tibble  | rectangular grid / data frame             |
        | tidyr   | pivot                                     |
        | forcats | categorical data / factors                |
        | stringr | string data / manipulate natural language |
        | purrr   | iteration                                 |
        

      - **Other package repositories**
        
          - [CRAN](https://cran.r-project.org/web/packages/)
          - [Tidyverse Packages](https://www.tidyverse.org/packages/)
          - [BioConductor](https://www.bioconductor.org/packages/release/BiocViews.html#___Software)
          - [ROpenSci](https://ropensci.org/)
          - [MetaCran](https://www.r-pkg.org/)

6.  Demo & R Markdown
    
      - Base R, in the console
          - A big calculator
      - RStudio & Tidyverse
      - RMarkdown Notebook: reproducible literate coding = Prose +
        Coding + Reports + RStudio projects + version control
        (git/GitHub)
      - [R Markdown](https://rmarkdown.rstudio.com/lesson-1.html)
          - Code Chunks: Separate prose from code
              - [Literate
                Programming](https://en.wikipedia.org/wiki/Literate_programming)
                (e.g. Jupyter notebooks, R notebooks)
              - [R Markdown
                Cheatsheet](https://rmarkdown.library.duke.edu/slides/index.html#5)
          - Integrate a natural language explanation of your analysis
            along with your code snippets. An approach used within
            computational sciences to create a functional record of
            *reproducibile* research. You are your most frequent
            collaborator, six months from now, or six months ago.
          - Create a new, blank R Notebook
              - R **Notebook** v. R Markdown **Document\[s\]**
          - Many types of R Reports
              - **slides**, documents, web pages, **e-books**, journal
                articles, web sites, **dashboards**, interactive **HTML
                widgets**, etc.
          - Save the file (`*.Rmd`)
          - Preview the file
              - (Share with others, so they don’t have to recreate your
                compute environment.)

7.  [`dplyr`](https://dplyr.tidyverse.org/) package
    
      - “A grammar of data manipulation, providing a consistent set of
        verbs that help you solve the most common data manipulation
        challenges”
          - `mutate()` adds new variables
          - `select()` pick variables / columns
          - `filter()` subset data by row
          - `summarise()` reduces multiple values into a summary
          - `count()` a special case of `summarize()` to tally
            occurances
          - `arrange()` sort rows
      - [RStudio Keyboard
        Shortcuts](https://support.rstudio.com/hc/en-us/articles/200711853-Keyboard-Shortcuts)

8.  [`tidyr`](https://tidyr.tidyverse.org/) package
    
      - Make messy data into **tidy data**
          - Every variable is a column
          - Every row is an observation
          - Every cell is a single value
      - i.e. **pivots**
      - People who like `pivot_longer()` also like `dplyr::left_joint()`

9.  Exploratory Data Analysis (EDA): `ggplot2()` & `skimr`
    
      - `skimr::skim()` from
        library[(skimr)](https://docs.ropensci.org/skimr/)
      - ggplot2(): a brief overview of visualization

10. [`ggplot2()`](https://ggplot2.tidyverse.org/): an introduciton to
    the grammar of graphics, & interactive plots via `plotly`

11. R Markdown

12. Assignment `<-` & pipe `%>%`

-----

## Future modules

20. Large Data

21. Regression

22. Dashboards

23. Slides (Xaringan)

24. Mapping and Geocomputation / Spatial Analysis

25. Version Control: git and GitHub

## Quick Start

1.  make a folder
2.  drag starwars.csv
3.  Make existing folder and RStudio project
4.  Open an R Markdown Notebook
5.  `library(tidyverses)`
6.  `read_csv(starwars.csv)`
7.  `ggplot(data = starwars, aes(hair_color)) + geom_bar()`
8.  `summary(starwars)`
9.  `skimr(starwars)`
10. `left_join(starwars, fivethirtyeight)`
11. `summarize(gender)`
12. Transform data: five dplyr verbs …
13. `count` / `group_by` & `summarize`
14. Make barchart an interactive ggplotly
15. Quick Linear Regression
16. Save Notebook report, and as MSWord file

## Resources

    - RStudio Primers
    - DataQuest.io
    - Master the Tidyverse
    - Rfun 
    - R for Data Science
    - Grolemund practical programming
    - ggplot2
    - Text Mining by Silge/Robinson
    - Shiny
    - Plotly for R
