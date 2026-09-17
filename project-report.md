# Are Young Nigerians Prepared for the Future of Work?

## An Analysis of Digital Access, Human Capital and Labour-Market Outcomes in Nigeria
## 1. Introduction

The rapid expansion of digital technologies is transforming the nature of work and creating new opportunities for economic participation. However, access to digital technology alone does not necessarily translate into meaningful employment or improved economic outcomes. Young people also require appropriate skills, education, and opportunities to effectively participate in an increasingly digital economy.

In Nigeria, internet access has expanded considerably over the past decade, while youth labour-market outcomes have followed more complex patterns. Youth labour-force participation and unemployment have not moved in the same direction as digital access, raising questions about whether increased connectivity is translating into greater economic opportunity.

This study examines the relationship between digital access, human capital, and youth labour-market outcomes in Nigeria. Using annual data from 2010 to 2025, the analysis explores trends in internet use, youth literacy, youth unemployment, youth labour-force participation, and ICT service exports.

The study is exploratory and focuses on identifying patterns and associations rather than establishing causal relationships. The analysis follows the framework:

**Digital Access / Use → Digital Capability → Economic Opportunity**

The findings are intended to contribute to discussions on how Nigeria can better prepare young people for participation in the digital economy.
## 2. Research Questions and Objectives

## 2.1 Research Questions

The study addresses the following research questions:

1. How has digital access and internet use in Nigeria changed over time?
2. How have youth human-capital indicators changed over the same period?
3. How have youth unemployment and labour-force participation changed alongside digitalisation?
4. Is there an observable relationship between digital access, human capital, and youth labour-market outcomes?
5. What do the findings suggest about how Nigeria can better prepare young people for the digital economy?

## 2.2 Research Objectives

The main objective of the study is to examine the relationship between digital access, human capital, and youth labour-market outcomes in Nigeria.

Specifically, the study aims to:

- Examine trends in internet use and digital access in Nigeria.
- Assess changes in youth literacy as an indicator of human capital.
- Examine trends in youth unemployment and labour-force participation.
- Explore the relationship between digital access and youth labour-market outcomes.
- Consider the implications of the findings for policies aimed at preparing young Nigerians for the future of work.
## 3. Data and Methodology

## 3.1 Data Sources

The study uses annual data for Nigeria covering 2010 to 2025. The indicators were obtained primarily from the World Bank World Development Indicators, with underlying data from organisations including the International Telecommunication Union (ITU), UNESCO Institute for Statistics (UIS), International Labour Organization (ILO), and International Monetary Fund (IMF).

The five indicators used in the analysis are:

| Indicator                        | Description                                                                     | Source                  |
| -------------------------------- | ------------------------------------------------------------------------------- | ----------------------- |
| Internet use                     | Individuals using the Internet (% of population)                                | World Bank / ITU        |
| Youth literacy                   | Literacy rate, youth total (% of people ages 15–24)                             | World Bank / UNESCO UIS |
| Youth unemployment               | Unemployment, youth total (% of labour force ages 15–24), modeled ILO estimate  | World Bank / ILO        |
| Youth labour-force participation | Labour-force participation rate for ages 15–24, total (%), modeled ILO estimate | World Bank / ILO        |
| ICT service exports              | ICT service exports (BoP, current US$)                                          | World Bank / IMF        |


## 3.2 Data Preparation

The data were collected and organised in Google Sheets before being analysed using Python. The dataset was inspected for missing values, consistency, and formatting issues.

Some indicators contained genuine gaps in the underlying source data. These missing observations were retained as missing rather than being replaced with zeros, averages, or interpolated values. This approach avoids introducing assumptions that could distort the analysis.

The cleaned dataset was subsequently used for descriptive and statistical analysis.

## 3.3 Analytical Approach

The analysis was conducted in several stages:

1. **Descriptive statistics** were used to examine the minimum, maximum, mean, median, and changes in each indicator.
2. **Trend analysis** was used to examine how the indicators changed over time.
3. **Correlation analysis** was used to identify the direction and strength of associations between selected variables.
4. **Year-to-year change analysis** was used to examine whether annual changes in internet use were associated with annual changes in youth unemployment and labour-force participation.
5. **Ordinary Least Squares (OLS) regression** was used to explore the relationship between youth unemployment, internet use, and ICT service exports.
6. **Variance Inflation Factor (VIF)** was examined to assess potential multicollinearity between explanatory variables.
7. **Breusch-Godfrey testing** was used to assess whether autocorrelation was present in the regression residuals.
8. **Heteroskedasticity and Autocorrelation Consistent (HAC) standard errors** were subsequently used to obtain more robust statistical inference.

## 3.4 Analytical Framework

The study uses the following conceptual framework:

Digital Access / Use → Digital Capability → Economic Opportunity

Digital access represents the ability to connect to and use digital technologies. Human capital, represented partly through youth literacy, reflects an important foundation for developing the capabilities needed to benefit from digital technologies. Economic opportunity is examined through youth labour-force participation, youth unemployment, and ICT service exports.

The framework does not assume that digital access automatically produces better labour-market outcomes. Instead, it provides a basis for examining whether the expansion of digital access has occurred alongside improvements in human capital and youth economic participation.

## 3.5 Limitations of the Methodology

The analysis is exploratory and does not establish causality. The relatively small number of annual observations limits the statistical power of the regression analysis, while the youth literacy indicator has particularly limited data availability.

In addition, labour-market outcomes are influenced by many factors that are not included in the models, including education, migration, demographic changes, economic conditions, and the availability of suitable employment opportunities.

The ICT service export indicator is measured in current US dollars and is therefore not adjusted for inflation. Consequently, changes in its value should be interpreted with this limitation in mind.
## 4. Results

## 4.1 Descriptive Statistics

The descriptive analysis shows that Nigeria experienced substantial growth in internet use between 2010 and 2024. Individuals using the Internet increased from 11.50% of the population in 2010 to 41.21% in 2024, representing an increase of approximately 29.71 percentage points.

Youth labour-force participation moved in the opposite direction over the broader period, declining from 69.39% in 2010 to 64.78% in 2025. Youth unemployment also declined overall, from 7.86% in 2010 to 5.34% in 2025, although the indicator experienced fluctuations during the period.

ICT service exports were highly volatile from year to year. They increased from approximately US$47.4 million in 2010 to approximately US$108.0 million in 2025, although the series reached a substantially higher maximum of approximately US$290.0 million during the period.

Youth literacy showed a more limited pattern because only four observations were available for the analysis. The available observations ranged from approximately 73.0% to 81.4%.

| Indicator                            | First observation | Last observation |    Change |
| ------------------------------------ | ----------------: | ---------------: | --------: |
| Internet use (%)                     |             11.50 |            41.21 | +29.71 pp |
| Youth literacy (%)                   |             79.16 |            81.36 |  +2.20 pp |
| Youth unemployment (%)               |              7.86 |             5.34 |  −2.52 pp |
| Youth labour-force participation (%) |             69.39 |            64.78 |  −4.60 pp |
| ICT service exports (US$)            |            47.43m |          107.98m |   +60.55m |


## 4.2 Internet Use

Internet use increased substantially over the period covered by the dataset. The share of individuals using the Internet rose from 11.50% in 2010 to 41.21% in 2024.

This represents a major expansion in digital connectivity. However, the increase in internet use did not correspond to a comparable increase in youth labour-force participation, which declined over the broader period.

## 4.3 Youth Labour-Force Participation

Youth labour-force participation declined from 69.39% in 2010 to 64.78% in 2025.

This result is important because it suggests that increased digital access did not automatically translate into greater participation of young people in the labour market.

However, labour-force participation is influenced by many factors beyond digital access. Changes in education, migration, demographic patterns, household circumstances, and decisions to remain outside the labour force may all affect participation.

## 4.4 Youth Unemployment

Youth unemployment declined overall from 7.86% in 2010 to 5.34% in 2025. However, the series did not follow a simple downward trend and experienced periods of increase and decline.

The decline in unemployment should therefore not automatically be interpreted as evidence that digitalisation created employment. A person who leaves the labour force is no longer counted among the unemployed, meaning that unemployment and labour-force participation need to be interpreted together.

## 4.5 Youth Literacy
Youth literacy showed an overall increase between the first and last available observations, from 79.16% in 2013 to 81.36% in 2024. However, the available observations show some fluctuation: the literacy rate declined between 2013 and 2016, remained relatively stable by 2021, and then increased by 2024.

Only four observations were available: 2013, 2016, 2021, and 2024. The limited number of observations means that the literacy results should be interpreted cautiously and should not be treated as a continuous annual trend.

## 4.6 ICT Service Exports

ICT service exports were volatile throughout the period. Although the value in 2025 was higher than the 2010 value, the series experienced substantial year-to-year fluctuations and reached a maximum of approximately US$290.0 million.

The fluctuations suggest that ICT-related economic activity did not follow a smooth upward path over the period. This also highlights that changes in ICT service exports should be considered separately from broader measures of digital access and youth labour-market outcomes.

## 4.7 Overall Pattern

Taken together, the descriptive results reveal contrasting trends. Internet use expanded substantially, while youth labour-force participation declined and youth unemployment also declined.

These contrasting trends suggest that increased internet access did not translate straightforwardly into increased labour-force participation. However, the decline in participation and unemployment cannot be attributed to internet access alone, because broader economic, demographic, educational, and labour-market factors may influence these outcomes.

## 4.8 Correlation Analysis

Correlation analysis was used to examine the strength and direction of the linear association between selected indicators. The correlation coefficient ranges from −1 to +1, where values closer to −1 indicate a negative association, values closer to +1 indicate a positive association, and values closer to 0 indicate a weak linear association.

The analysis produced the following results:

| Variables                                                | Correlation (r) | Interpretation                        |
| -------------------------------------------------------- | --------------: | ------------------------------------- |
| Internet use and youth unemployment                      |          −0.300 | Weak-to-moderate negative association |
| Internet use and youth labour-force participation        |          −0.831 | Strong negative association           |
| Internet use and youth literacy                          |          +0.244 | Weak positive association             |
| ICT service exports and youth unemployment               |          +0.126 | Very weak positive association        |
| ICT service exports and youth labour-force participation |          −0.725 | Strong negative association           |
| Internet use and ICT service exports                     |          +0.739 | Strong positive association           |

The strong negative correlation between internet use and youth labour-force participation indicates that the two variables moved in opposite directions over the observed period. However, this should not be interpreted as evidence that increased internet access caused lower labour-force participation.

Because the data are annual time-series observations, correlations between variables may partly reflect common trends over time. For example, internet use generally increased over the period while labour-force participation generally declined. This can produce a strong correlation even when there is no direct causal relationship.

The relationship between internet use and youth unemployment was weaker, with a correlation coefficient of approximately −0.300. This indicates that higher internet use tended to be associated with lower youth unemployment, but the relationship was not particularly strong.

The correlation between internet use and youth literacy was approximately +0.244. However, this result is based on only four paired observations and should therefore be treated as highly exploratory. The limited number of observations makes it unsuitable for drawing strong conclusions about the relationship between digital access and youth literacy.


## 4.9 Year-to-Year Change Analysis

To reduce the influence of common time trends, the analysis also examined the relationship between annual changes in internet use and annual changes in labour-market indicators.

The correlation between annual changes in internet use and annual changes in youth labour-force participation was approximately +0.338. This is considerably different from the strong negative correlation observed when comparing the raw levels of the two variables.

The difference demonstrates why relationships between variables measured as levels over time should be interpreted carefully. The strong negative relationship in the levels may partly reflect the underlying time trends rather than a direct relationship between changes in digital access and changes in labour-force participation.

The correlation between annual changes in internet use and annual changes in youth unemployment was approximately −0.662. This indicates that years with larger increases in internet use tended to coincide with decreases in youth unemployment. However, this remains an association and does not establish that changes in internet use caused changes in unemployment.

Although analysing annual changes helps reduce the influence of common trends, it does not eliminate other time-series issues or establish causality.

 ## 4.10 Regression Analysis

An Ordinary Least Squares (OLS) regression was used to further examine the relationship between youth unemployment, internet use, and ICT service exports.

The dependent variable was youth unemployment, while internet use and ICT service exports were included as explanatory variables. The analysis was conducted using the years for which the relevant variables were available.

## Model 1: Youth Unemployment and Internet Use

The first regression examined the relationship between youth unemployment and internet use alone.

The model produced an R² of 0.090, meaning that internet use alone explained approximately 9.0% of the variation in youth unemployment in the sample.

The coefficient on internet use was approximately −0.0554, with a p-value of 0.277. This indicates that a one-percentage-point increase in internet use was associated with an estimated 0.055-percentage-point decrease in youth unemployment. However, the coefficient was not statistically significant at conventional significance levels.

Therefore, while the estimated relationship was negative, the result does not provide strong statistical evidence of an association between internet use and youth unemployment in this simple model.

## Model 2: Youth Unemployment, Internet Use and ICT Service Exports

The second regression included both internet use and ICT service exports as explanatory variables. ICT service exports were measured in millions of US dollars to make the coefficient easier to interpret.

The model produced an R² of 0.306, indicating that approximately 30.6% of the variation in youth unemployment was explained by the two explanatory variables in the sample.

The coefficient on internet use was approximately −0.1496, with a p-value of 0.042. This indicates that, holding ICT service exports constant, a one-percentage-point increase in internet use was associated with an estimated 0.150-percentage-point decrease in youth unemployment. The coefficient was statistically significant at the 5% level in the conventional OLS model.

The coefficient on ICT service exports was approximately +0.0144, with a p-value of 0.077. This indicates a positive estimated association between ICT service exports and youth unemployment in this model, although the coefficient was not statistically significant at the conventional 5% level.

The overall F-test had a p-value of 0.112, meaning that the explanatory variables were not jointly statistically significant at the conventional 5% level in the standard OLS specification.

These results should be interpreted cautiously because the analysis is based on a small number of annual observations and does not establish causality.


## Regression Diagnostics

Several diagnostic tests were conducted to assess the reliability of the regression results.

**Multicollinearity**

Variance Inflation Factor (VIF) was used to assess whether internet use and ICT service exports were highly correlated with each other. Both variables had VIF values of approximately 2.20, indicating that there was no severe multicollinearity between the explanatory variables.

**Autocorrelation**

A Breusch-Godfrey test was conducted to examine whether the regression residuals were correlated over time. The test produced a p-value of approximately 0.025, providing evidence of first-order autocorrelation in the model.

Because the data consist of annual time-series observations, the presence of autocorrelation means that the conventional OLS standard errors may not provide reliable statistical inference.

**Heteroskedasticity and Autocorrelation-Consistent (HAC) Standard Errors**

To account for the detected autocorrelation, the regression was re-estimated using HAC standard errors with one lag. HAC estimation does not change the estimated regression coefficients; rather, it adjusts the standard errors and statistical inference to account for heteroskedasticity and autocorrelation.

Under the HAC specification, the internet-use coefficient remained approximately −0.1496, while the ICT service exports coefficient remained approximately +0.0144. The corresponding p-values were approximately 0.045 for internet use and 0.013 for ICT service exports.

The HAC results therefore provide stronger statistical evidence for the estimated associations within this specification. However, given the small sample size, annual time-series structure, and observational nature of the data, these results should still be interpreted as exploratory associations rather than causal effects.

## 4.11 Interpretation of the Statistical Results

The statistical analysis provides evidence of associations between digitalisation and youth labour-market outcomes, but the relationships are not straightforward.

Internet use increased substantially over the period, while youth labour-force participation declined. At the same time, youth unemployment declined overall. The contrasting movement of these indicators suggests that increased digital access alone cannot explain Nigeria's youth labour-market outcomes.

The regression results indicate a negative association between internet use and youth unemployment after accounting for ICT service exports. The estimated internet-use coefficient remained negative after applying HAC standard errors, while the ICT service exports coefficient remained positive. However, the small sample size, autocorrelation, time-series trends, and potential omitted variables mean that these results should not be interpreted as causal effects.

The year-to-year change analysis also provides additional context. Changes in internet use showed a weak positive association with changes in youth labour-force participation, compared with the strong negative association observed in the raw levels. This difference reinforces the importance of accounting for underlying time trends when interpreting relationships in annual data.

Overall, the findings support a cautious interpretation: digital access may be an important component of economic opportunity, but access alone is unlikely to be sufficient to ensure improved labour-market participation and outcomes for young Nigerians. The relationship between digitalisation and economic opportunity is likely to depend on broader factors including skills, education, labour-market conditions, and access to productive opportunities.

## 5. Policy Implications

The findings suggest that Nigeria's expansion of digital access needs to be accompanied by measures that enable young people to convert connectivity into productive economic opportunities.

First, continued investment in affordable and reliable Internet infrastructure is important because digital connectivity provides the foundation for participation in the digital economy. However, the contrasting movement of internet use and youth labour-force participation indicates that connectivity alone should not be treated as sufficient.

Second, greater emphasis should be placed on digital and technical skills development. Young people need the capabilities to use digital technologies productively, rather than simply having access to them. Skills programmes should therefore be connected to actual employment, entrepreneurship, and labour-market opportunities.

Third, education and training systems should be better aligned with changing labour-market requirements. Digitalisation may create new opportunities, but young people need relevant skills to take advantage of them.

Fourth, policies should support digital entrepreneurship, remote work, online services, and other forms of technology-enabled economic activity. This could help strengthen the connection between digital access and economic participation.

Finally, better data are needed to monitor whether digital expansion is translating into improvements in youth skills, employment, and economic participation. More consistent data would also allow future research to examine these relationships using larger samples and more detailed variables.

Overall, the evidence points towards a broader policy approach in which digital connectivity is treated as a foundation rather than an end in itself. The pathway from access to economic opportunity is likely to depend on the interaction between infrastructure, skills, education, labour-market conditions, and access to productive opportunities.

## 6. Limitations

Several limitations should be considered when interpreting the findings of this study.

First, the analysis is based on a relatively small number of annual observations. Most indicators contain between 15 and 16 observations, while youth literacy has only four available observations during the study period. This limits the statistical power of the analysis and makes estimates based on the literacy indicator particularly sensitive to individual observations.

Second, data availability varies across indicators. Missing observations, particularly for youth literacy and internet use in some years, mean that the number of observations differs across analyses. The missing values were retained as missing rather than being artificially estimated or replaced.

Third, the study uses observational time-series data. Therefore, the correlations and regression results identify associations rather than causal relationships. A relationship between internet use and labour-market outcomes does not establish that changes in internet use caused changes in employment or labour-force participation.

Fourth, the variables may be influenced by broader economic, demographic, educational, technological, and social factors that are not included in the models. For example, changes in education, migration, economic growth, demographic structure, and labour-market conditions may affect youth employment and participation independently of digital access.

Fifth, the presence of time trends and first-order autocorrelation means that conventional regression results need to be interpreted cautiously. HAC standard errors were therefore used in the regression analysis to account for the detected autocorrelation and to obtain more robust statistical inference. However, this adjustment does not eliminate the limitations associated with the small sample size or establish causality.

Finally, ICT service exports are measured in current US dollars and therefore do not account for inflation or changes in purchasing power. The indicator should therefore be interpreted as a measure of the monetary value of ICT service exports rather than as a direct measure of real ICT-sector growth.

Overall, these limitations mean that the findings should be treated as exploratory evidence rather than definitive estimates of causal effects. Future research using longer time series, more detailed youth-level data, and additional explanatory variables could provide a stronger basis for understanding the relationship between digitalisation and youth economic outcomes in Nigeria.
## 7. Conclusion

This study examined the relationship between digital access, human capital, and youth labour-market outcomes in Nigeria. The analysis focused on Internet use, youth literacy, youth unemployment, youth labour-force participation, and ICT service exports over the available period from 2010 to 2025.

The findings show that Internet use increased substantially over the period covered by the data. 

The statistical analysis also identified associations between Internet use and youth labour-market indicators. The regression analysis identified a negative association between Internet use and youth unemployment after accounting for ICT service exports. However, this association should be interpreted cautiously given the observational nature of the data and the limitations of the regression analysis. However, the observational nature of the data, small sample size, time-series trends, autocorrelation, and omitted variables mean that this relationship should not be interpreted as a causal effect.  At the same time, youth unemployment declined overall after experiencing higher levels during earlier years. These contrasting trends indicate that increased digital access does not automatically translate into greater labour-market participation or improved employment outcomes.

The findings therefore support a broader understanding of digital transformation. Internet access is an important foundation for participation in the digital economy, but connectivity alone may not be sufficient to produce improved economic outcomes for young people. The ability to convert access into opportunity also depends on digital skills, education, labour-market conditions, entrepreneurship opportunities, and access to productive economic activities.

For Nigeria, this suggests that efforts to prepare young people for the future of work should move beyond expanding connectivity alone. Digital infrastructure should be complemented by investments in relevant skills, education, employment pathways, entrepreneurship, and better labour-market information. Improving the availability and quality of youth-related data will also be important for evaluating whether these interventions are translating digital expansion into meaningful economic opportunities.

Overall, the study provides exploratory evidence that Nigeria's digital transformation and youth labour-market outcomes are related in complex ways. Understanding this relationship requires attention not only to whether young people have access to digital technologies, but also to whether they have the skills and economic opportunities needed to use those technologies productively.

## 8. Data Sources and References

The analysis uses publicly available international development and labour-market data.

## World Bank

The following indicators were obtained from the World Bank World Development Indicators database:

* Individuals using the Internet (% of population), indicator code `IT.NET.USER.ZS`.

* Literacy rate, youth total (% of people ages 15–24), indicator code `SE.ADT.1524.LT.ZS`.

* Unemployment, youth total (% of total labour force ages 15–24), modeled ILO estimate, indicator code `SL.UEM.1524.ZS`.

* Labour force participation rate for ages 15–24, total (%), modeled ILO estimate, indicator code `SL.TLF.ACTI.1524.ZS`.

* ICT service exports (BoP, current US$), indicator code `BX.GSR.CCIS.CD`.

## International Labour Organization

Youth unemployment and youth labour-force participation estimates are based on ILO modelled estimates as provided through the World Bank database. The World Bank identifies the ILO Modelled Estimates database (ILOEST) as the source for these indicators.

## International Telecommunication Union

Internet-use data are based on information collected through the International Telecommunication Union and published through the World Bank's World Development Indicators database.

## UNESCO Institute for Statistics

Youth literacy data are based on UNESCO Institute for Statistics data as published through the World Bank's World Development Indicators database.

## Data Processing and Analysis

Data preparation was initially conducted using Google Sheets. Statistical analysis and visualisation were conducted using Python, including Pandas, Matplotlib, and Statsmodels.

The analysis covers the available annual observations for Nigeria between 2010 and 2025. Because data availability differs across indicators, individual statistical analyses use the observations available for the variables included in each analysis.

### Source Links

* World Bank World Development Indicators: https://data.worldbank.org/

* World Bank indicator — Individuals using the Internet (% of population), `IT.NET.USER.ZS`: https://data.worldbank.org/indicator/IT.NET.USER.ZS

* World Bank indicator — Youth literacy rate, `SE.ADT.1524.LT.ZS`: https://data.worldbank.org/indicator/SE.ADT.1524.LT.ZS

* World Bank indicator — Youth unemployment, `SL.UEM.1524.ZS`: https://data.worldbank.org/indicator/SL.UEM.1524.ZS

* World Bank indicator — Youth labour-force participation, `SL.TLF.ACTI.1524.ZS`: https://data.worldbank.org/indicator/SL.TLF.ACTI.1524.ZS

* World Bank indicator — ICT service exports, `BX.GSR.CCIS.CD`: https://data.worldbank.org/indicator/BX.GSR.CCIS.CD
