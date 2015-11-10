# Data-Representation-and-Querying-Project-2015

car parking
https://data.gov.ie/dataset/galway-city-car-parking-locations

## Introduction

This project provides the design and documentation for the dataset "Galway City Car Parking Locations" which is available at https://data.gov.ie/dataset/galway-city-car-parking-locations

### Tim Daiber


Heading | Description  
---------|-----------
"X" | The State the crime has occured in. 
"Y" | The Type of crime (Statistic arrests per 100.000).
"ObjectID" | Crime that occured Assault (Statistic arrests per 100.000).
"Name" | The amount of urban population that persides in the state.
"Type" | Crime that occured Rape (Statistic arrests per 100.000).
"NO_SPACES" | Crime that occured Assault (Statistic arrests per 100.000).
"Lat" | The amount of urban population that persides in the state.
"Long" | Crime that occured Rape (Statistic arrests per 100.000).
"EastITM" | Crime that occured Assault (Statistic arrests per 100.000).
"NorhtITM" | The amount of urban population that persides in the state.
"EastIG" | Crime that occured Rape (Statistic arrests per 100.000).
"NorthIG" | Crime that occured Assault (Statistic arrests per 100.000).


 ```json
 [
    {
        "X":"-9.053499750875776"
    ,"Y":"53.273082469830108"
    ,"OBJECTID":"1"
    ,"NAME":"Market St"
    ,"TYPE":"Pay/Surface Carpark"
    ,"NO_SPACES":"88"
    ,"Lat":"53.273"
    ,"Long":"-9.054"
    ,"EastITM":"529691.955"
    ,"NorthITM":"725294.803"
    ,"EastIG":"129726.012"
    ,"FIELNorthIGD12":"225265.639"
     }
  ]
 ```



[Apps4gaps](http://apps4gaps.ie/) have asked you design a simple API to any of their datasets.
Their datasets are available on [data.gov.ie](https://data.gov.ie/data).
They have only asked that you design the API, not implement it.
They have stipulated that the API must be provided through HTTP.
The data should be made available through a set of URLs, potentially using a variety of HTTP methods.

Apps4gaps want you to submit your work in the form of a README.
The README should explain your API design, similar to the [Hacker News API Documentation](https://github.com/HackerNews/API/blob/master/README.md).
The README should be written in [GitHub-flavoured](https://help.github.com/articles/github-flavored-markdown/) [MarkDown](https://help.github.com/articles/markdown-basics/).

> From Joshua Bloch's "How to Design a Good API and Why it Matters"

> *Characteristics of a Good API*
> - *Easy to learn*
> - *Easy to use, even without documentation*
> - *Hard to misuse*
> - *Easy to read and maintain code that uses it*
> - *Sufficiently powerful to satisfy requirements*
> - *Easy to extend*
> - *Appropriate to audience*


## Instructions
1. Create a GitHub repository with a blank README.md file.
You can do this by either creating a git project on your computer, or simply by going to github.com and creating a new repository with a README.md file in it.
You can just use github.com to edit the README.md if you want to.
The following is an example of a starter README.md.
    
    ```markdown
    # Project title
    ## Data Representation and Querying Project 2015
    ### Student Name
    
    ## Introduction
    This project provides the design and documentation for the dataset "Dataset title" which is available at [data.gov.ie](http://data.gov.ie)...
    ```
    
1. Find a dataset at the [Apps4gaps open data site](https://data.gov.ie/data) that you want to use for this project.
Make sure you describe the dataset in your README, so that a user will fully understand what the data set contains.
You might also want to upload to your GitHub repository the data set itself.
Below is a suggested starter description for a dataset.

    ```markdown
    ## About the data
    This dataset was received in Comma Separated Values (CSV) format, and was downloaded from [*insert page name*](insert url).
    The CSV file contains 1001 rows, the first being a header row with the names of each field.
    There are six values on each line, which are as follows:
        - **year**: the year that the car was purchased.
        - **price**: the price of the car.
        ...
    ```
    
1. Design a set of URLs which you think would be useful for querying the dataset.
Bear in mind the users of your API, and their needs.
It might be helpful to suggest, in your README, the kinds of users you imagine will use the API.
You also might want to enable your API to respond to HTTP requests other than those using the GET method.
For instance, you might want your API to respond to POST requests.
Decide what kind of data will be available at each URL (and for each HTTP method).
Clearly explain in your README what the returned data is, and what format it will take.
You could describe each URL similar to the following.
    
    ```markdown
    ## List of cars for a given year
    You can get a list of cars purchased in a given year using the GET method at the following URL:
    *http://carsapi.com/year/[year]*
    where you replace [year] with the year.
    For example, the URL:
    *http://carsapi.com/year/2005*
    will return a list of cars purchased in 2005.
    The data will be returned in JSON format, with the following properties for each car:
        - *price*: the price of the car.
        - *model*: the model of the car.
        ...
    An example of a response would be:
        ```json
        [ {"price": 20000, "model": "Skoda", ...}, {...}, ...]
        ```
    ```
    
## GitHub
Your project must be available as a repository in your GitHub account in order to submit it.
The easiest way to do this, given that your project need only contain a README.md file, might be to just use the github.com web application.
Otherwise, you can use [git](https://git-scm.com/) on the command line, or [GitHub Desktop](https://desktop.github.com/).
The computer labs have git installed, but not GitHub Desktop for technical reasons.
I have created a short introduction to the git command line [here](https://github.com/ianmcloughlin/git-basics/).
If you are confused as to the use of GitHub, and you must seek clarification before the project deadline.

## Submission
On the course Moodle page there is a link where you can submit your GitHub repository's url.
You must do this before the submission deadline.
Any changes made to your repository after the submission deadline will not count towards your mark.

## Plagiarism
All work must be the student’s own, with any content from outside parties being clearly attributed to those parties.
Submissions may be filtered through plagiarism prevention services.
Students should consult the lecturer in case of confusion regarding this issue.
Students are bound by GMIT’s Code of Student Conduct and GMIT’s Policy on Plagiarism, both available on the GMIT website.

## Grading
This assignment is worth 50% of your mark for this module.
The grading scheme is as follows.


Category | % | Acceptable | Excellent
---------|--:|------------|----------
**Usefulness** | 10 | The selected dataset is conducive to creating a useful API. | The API provides an easy-to-use portal into a useful and interesting dataset.
**Clarity** | 10 | The README is clear, typo-free and easy to read. | The README is clearly written and covers all necessary aspects of the API with extensive examples and comments.
**Presentation** | 10 | The README is well laid-out and makes appropiate use of headings and links. | The README is easy to read, quick to understand, and makes use of appropriate headings, links, code examples, lists and tables.
**URLs** | 10 | A set of URLs have been designed that enable querying of the selected dataset. | The URLs have been designed in such a way that the dataset can be queried extensively and in a number of ways. The API provides an intuitive interface to the user.
**Responses** | 10 | The API responds with meaningful data in an appropriate format. | The API sends well thought-out responses that will reduce the number of API calls users will have to make.

## Resources
- [Mastering Markdown](https://guides.github.com/features/mastering-markdown/)
- [How to Design a Good API and Why it Matters](http://lcsd05.cs.tamu.edu/slides/keynote.pdf)
