Outline for modules
================
John Little
2020-07-13

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
          - R is a *data first* (i.e. analysis) programming language
          - Python is a general programming language
          - Are there libraries/packages relevant to your work?
          - Is there a supportive community?
              - [Rfun](https://rfun.library.duke.edu/)
              - [R Community](https://community.rstudio.com/)
              - [R Ladies](https://rladies.org/) | Locally, [R Ladies,
                RTP](https://www.meetup.com/rladies-rtp/)
              - [TidyTuesday](https://github.com/rfordatascience/tidytuesday)
                weekly practice sessions (+ David Robinson’s [recorded
                live feed of TT on
                YouTube](https://www.youtube.com/watch?v=NY0-IFet5AM&list=PL19ev-r1GBwkuyiwnxoHTRC8TTqP8OEi8)
                )
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
        | ggplot2 | visualizing                               |
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

6.  Assignment `<-` & pipe `%>%`

7.  R, RStudio IDE, R Markdown
    
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
            *reproducible* research. You are your most frequent
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

8.  [`dplyr`](https://dplyr.tidyverse.org/) package
    
      - “A grammar of data manipulation, providing a consistent set of
        verbs that help you solve the most common data manipulation
        challenges”
          - `mutate()` adds new variables
          - `select()` pick variables / columns
          - `filter()` subset data by row
          - `summarise()` reduces multiple values into a summary
          - `count()` a special case of `summarize()` to tally
            occurrences
          - `arrange()` sort rows
      - [RStudio Keyboard
        Shortcuts](https://support.rstudio.com/hc/en-us/articles/200711853-Keyboard-Shortcuts)

9.  [`tidyr`](https://tidyr.tidyverse.org/) package
    
      - Make messy data into **tidy data**
          - Every variable is a column
          - Every row is an observation
          - Every cell is a single value
      - i.e. **pivots**

10. dplyr revisited
    
      - People who like `pivot_longer()` also like `dplyr::left_joint()`

11. Exploratory Data Analysis (EDA): `ggplot2()` & `skimr`
    
      - `skimr::skim()` from
        library[(skimr)](https://docs.ropensci.org/skimr/)
      - ggplot2(): a brief overview of visualization

12. [`ggplot2()`](https://ggplot2.tidyverse.org/): an introduction to
    the grammar of graphics, & interactive plots via `plotly`

13. R Markdown

-----

## Future modules

20. Large Data

21. Regression

22. Dashboards

23. Slides (Xaringan)

24. Mapping and Geocomputation / Spatial Analysis

25. Version Control: git and GitHub

## Quick Start - Demonstration

1.  Make a data folder

2.  Drag favorability.csv into the data folder

3.  Make existing folder and RStudio project

4.  Open an R Markdown Notebook

5.  `library(tidyverses)` plus other libraries

6.  IMPORT data See Also *RStudio data import wizard*

7.  ATTACHE data

8.  EDA: Visualize `ggplot(data = starwars, aes(hair_color)) +
    geom_bar()`

9.  EDA: `skimr::skim(starwars)`

10. EDA: summary(fav\_rating)

11. `left_join(starwars, fivethirtyeight)`

12. Transform data: five dplyr verbs …
    
      - `count` / `group_by` & `summarize`

13. Interactive visualization ggplotly

14. Quick Linear Regression

15. Reports: notebooks, slides, dashboards, word document, PDF, book,
    etc.

## Resources

  - [RStudio Primers](https://rstudio.cloud/learn/primers)

  - [DataQuest.io](https://www.dataquest.io/data-science-courses-directory/)

  - [Tidy Tuesday](https://github.com/rfordatascience/tidytuesday)
    practice

  - [Rfun](https://rfun.library.duke.edu/) - R we having fun yet‽

  - [ReMaster the
    Tidyverse](https://github.com/rstudio-education/remaster-the-tidyverse)
    
      - Update of [Master the
        Tidyverse](https://github.com/rstudio/master-the-tidyverse)

  - [R for Data Science](https://r4ds.had.co.nz/) by Wickham and
    Grolemund

  - [Introduction to Data Science](https://introds.org/) by
    Çetinkaya-Rundel

  - [*Hands-On programming*](https://rstudio-education.github.io/hopr/)
    by Grolemund

  - [*ggplot2: Elegant Graphics for Data
    Analysis*](https://ggplot2-book.org/) by Wickham

  - [*Interactive web-based data visualization with R, plotly, and
    shiny*](https://plotly-r.com/) by Sievert

  - [*Data Visualization A practical
    introduction*](https://socviz.co/makeplot.html#makeplot) by Healy

  - [*Text Mining with R*](https://www.tidytextmining.com/) by Silge &
    Robinson

  - [Shiny](https://shiny.rstudio.com/)

  - [Statistical Inference via Data Science: A ModernDive into R and the
    Tidyverse](https://moderndive.com/) by Ismay and Kim
