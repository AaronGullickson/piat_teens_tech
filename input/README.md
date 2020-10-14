# Data Source Description

The data we will use come from the [Pew Research Center](https://www.pewresearch.org/), a "nonpartisan fact tank that informs the public about the issues, attitudes and trends shaping the world." The Pew Research Center fields numerous surveys on a variety of topics both within the US and internationally. We will use a 2018 survey entitled [Teens and Tech](https://www.pewresearch.org/internet/dataset/teens-and-tech-survey-2018/) which collected data from over 700 US adolescents between the ages of 13 and 17, and interviewed these respondents about a variety of tech issues, including social media use.


From the full Pew data, I have extracted and recoded the following variables for our use as an analytical dataset. To load this dataset in R, you just need to run the setup code chunk in the full_report.Rmd R Markdown document. The name of the dataset in R is `pew`. 

* **soc_media_insecure**: Respondents were asked whether social media made them feel confident or insecure. I have coded all of the insecure responses as TRUE and confident responses as FALSE. This kind of TRUE/FALSE coding is called a "boolean" variable and it will allow us to use this outcome as a quantitative variable in the final models. In that case, the TRUE/FALSE will be scored as quantative variables with 1/0. The model results will then tell us the change in the probability of giving the insecure response.
* **gender**: respondent's gender was recorded as a binary response of either Male of Female.
* **parent_ed**: Highest educational degree among the respondent's parents.
* **internet_use**: respondents were asked how often they used the internet, either on a computer or through a phone. The categories were less often, several times a week, about once a day, several times a day, and almost constantly.
* **age**: the age of the respondent.
* **race**: the race of the respondent. The survey only reported the categories of White, Black, Hispanic, and Other.
* **income**: respondents' were asked to report their family income in brackets (e.g. $50,000-$59,999). I have converted this into a quantitative variable by taking the midpoint value of each bracket (e.g. $55,000 for $50,000-$59,999). Values are reported in thousands of US dollars.
* **metro_area**: whether the respondent lived in a metro area (i.e. city) or non-metro area.
* **hhsize**: The number of people (including adults and children) who live in the household with the respondent.

