Matthew Taylor, Rowena Terrado, Ryan Barrett

## Introduction
It has been a constant goal of humanity to improve the lives of people through the quality of their health and well-being. The average life expectancy of a country’s population is a good indicator of this, but identifying what factors do affect life expectancy can be very helpful in achieving this improvement. Indicators relating to health, such as population habits and national investment in health infrastructure, seem to be most directly related, but other factors can be important as well. In this project, we will find if the quality of a country’s education system can be relevant in predicting life expectancy.

## Selection of Data
The data we’ve selected is sourced from the World Health Organization.  The data was compiled by the World Health Organization using data from the Global Health Organization (GHO) and the United Nations Education Scientific and Culture Organization (UNESCO).  The data consists of statistical data from 183 countries in 6 regions.  There are 17 records for each country representing annual data from the year 2000 through 2016. The data for each country consists of 32 features.  The regions are Americas, Eastern Mediterranean, Europe, South-East Asia, and Western Pacific.  The value we’re attempting to predict is life expectancy.

## Methods
Of the various prediction methods available to us, we’ve chosen to use linear regression as Linear regression is a better solution for a continuous variable such as life expectancy, measured in years.  As our question doesn’t deal with classification, we didn’t feel KNN regression or classification trees were appropriate.

- **Predictor:**
The value we’re trying to predict is life expectancy.  The column name for that feature is life_expect.  Our predictor features are educational spending (une_edu_spend) and literacy (une_literacy).
- **Preprocessing:**
A number of countries had missing or partial data.  Countries with no data were removed.  The average of the existing data was used for countries with only partial data.  204 records for countries with no data were removed.
- **Assumptions:**
For countries with partial data, it was assumed that there wouldn’t be huge swings in education spending or literacy rates.  This allowed us to use the average of these values for our calculations.


## Results

The results of our initial attempt showed that training based on only education spending was not a good predictor of life expectancy:<br><br>
<p align="center"><img height="400" width="600" src="https://i.imgur.com/2u9eOjD.png"></p><br>
However interestingly when the additional predictor of “Literacy Rate” was included the results changed drastically:<br><br>
<p align="center"><img height="400" width="600" src="https://i.imgur.com/kNUF376.png"></p><br>


This shows that while education spending itself might not be a good indicator of life expectancy, the actual outcomes that spending accomplishes such as literacy rate might be. With more data you could potentially begin to see exactly which outcomes lead to longer lives.


## Discussion
A country’s education expenditure may not be relevant to life expectancy due to circumstances surrounding the actual quality of education, as well as the individual choices of the members of a population when it comes to undertaking education. However, it is implied that a higher literacy rate leads to a higher average life expectancy for a country’s population.
A study performed by the Yale School of Medicine and University of Alabama-Birmingham discovered that education levels were independently linked to premature death rates, and were the best predictor of determining how many potential years of life can be lost by dying at a certain age. A lack of education can result in people making choices that endanger one’s health, or being unable to have a higher-paying job and therefore access to better nutrition or healthcare.
Further research can be performed on the quality of education, and what factors are related to individuals who are unable to obtain literacy or more years of education. For example, poverty may force a person to abandon school, as well as engage in risky behavior such as crime that may lead to a premature death.

## Summary
Overall, investment in education can be as important to a population’s life expectancy as investment in healthcare, but there must be more research done to make sure that correlation does not imply causation. Achieving equity in access to education within a population, though, can be a factor in increasing the quality and length of life.

## Bibliography

https://www.kaggle.com/mmattson/who-national-life-expectancy

https://ajph.aphapublications.org/doi/10.2105/AJPH.2019.305506

https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4435622/

https://www.nytimes.com/2019/06/03/upshot/education-impact-health-longevity.html


