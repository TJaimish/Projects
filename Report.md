<!-----

You have some errors, warnings, or alerts. If you are using reckless mode, turn it off to see inline alerts.
* ERRORs: 0
* WARNINGs: 0
* ALERTS: 6

Conversion time: 2.076 seconds.


Using this Markdown file:

1. Paste this output into your source file.
2. See the notes and action items below regarding this conversion run.
3. Check the rendered output (headings, lists, code blocks, tables) for proper
   formatting and use a linkchecker before you publish this page.

Conversion notes:

* Docs to Markdown version 1.0β34
* Mon Jan 30 2023 06:54:29 GMT-0800 (PST)
* Source doc: Report Writeup
* Tables are currently converted to HTML tables.
* This document has images: check for >>>>>  gd2md-html alert:  inline image link in generated source and store images to your server. NOTE: Images in exported zip file from Google Docs may not appear in  the same order as they do in your doc. Please check the images!

----->


<p style="color: red; font-weight: bold">>>>>>  gd2md-html alert:  ERRORs: 0; WARNINGs: 0; ALERTS: 6.</p>
<ul style="color: red; font-weight: bold"><li>See top comment block for details on ERRORs and WARNINGs. <li>In the converted Markdown or HTML, search for inline alerts that start with >>>>>  gd2md-html alert:  for specific instances that need correction.</ul>

<p style="color: red; font-weight: bold">Links to alert messages:</p><a href="#gdcalert1">alert1</a>
<a href="#gdcalert2">alert2</a>
<a href="#gdcalert3">alert3</a>
<a href="#gdcalert4">alert4</a>
<a href="#gdcalert5">alert5</a>
<a href="#gdcalert6">alert6</a>

<p style="color: red; font-weight: bold">>>>>> PLEASE check and correct alert issues and delete this message and the inline alerts.<hr></p>


SUPPLY CHAIN ANALYTICS Optimizing Vaccine Delivery for COVID-19 

Renaldo 

Hermawan 

Maaz 

Ahmad 

Lakshmi 

Priya 

Sankaran 

Jaimish 

Topre 

Shubham Bhardwaj


    Introduction 


    With the impending global pandemic crisis COVID-19, data analytics has become a vital tool for governments and health care agencies. As the situation is evolving, we can see numerous descriptive analysis everyday. We found that there is a need to optimize the global distribution system of vaccines. As of right now, there are no vaccines for the COVID-19, but experts are saying that it may take one year . Even then, the production capacity will be limited , and so there is a need to prioritize who will get the vaccine. We start the project by providing descriptive analysis for the confirmed cases, deaths and recovered cases all over the world. Through descriptive analysis we get a clear picture of how the infection is spread across the world.The next step is to perform predictive analysis. Forecasting an epidemic is different from traditional forecasting of demand hence we used the SIR model which predicts the number of infected people for the given population. This model is widely used in predicting infectious disease spread. Once we got the predicted demand/distribution of infection, we used linear programming to find the optimal distribution of the vaccines based on the number of infected cases in each country. 


    Datasets used 


<table>
  <tr>
   <td>
    <strong>Title </strong>
   </td>
   <td>
    <strong>Description</strong>
   </td>
  </tr>
  <tr>
   <td>
    Novel CoronaVirus 2019 Dataset
   </td>
   <td>
    Contains various datasets extracted from John Hopkins University on COVID-19 situation. It includes the time series of number of confirmed, deaths, and recovered cases from around the world. Source: <span style="text-decoration:underline;">Kaggle</span>
   </td>
  </tr>
  <tr>
   <td>
    COVID-19 global forecasting: Locations population
   </td>
   <td>
    Contains dataset on the population of the areas affected by the coronavirus. Data sources are multiple and based on google search by the dataset owner. Source: <span style="text-decoration:underline;">Kaggle</span>
   </td>
  </tr>
  <tr>
   <td>
    Vaccine Facilities Dataset
   </td>
   <td>
    We build a cursory list of the 5 largest manufacturers globally who are working on making a COVID-19 cure, based on our own research.
   </td>
  </tr>
</table>


Analysis/Modeling 


    Data Visualization 


    Python libraries, such as pandas, seaborn, folium and plotly are used to develop key insights from the aforementioned datasets. 


    The first step of the data visualization is to draw conclusions regarding the critically hit areas globally, due to the COVID-19. **Pandas **is used to understand and manipulate the nature of the data, which includes renaming, grouping and listing of various values from the dataset.


    Once the areas of significance are highlighted, **folium **package helps generate an interactive leaflet global map based on the longitude and latitude. The folium.circle function assigns a bubble to each region. The size of the bubble depends upon the value taking into account the state (confirmed cases, deaths and recoveries) of that region. In a similar manner, seaborn is used to comment on the growing concern with respect to the pandemic worldwide. The key takeaways are follows: 


        ● **Line plots **are used to visualize the overall trends globally and to demonstrate the deteriorating condition in some specific countries. 


        ● **Heatmaps **help pinpoint the regions that are affected the most, resulting in a key insight for the modelling to follow. 


        ● The growing number of confirmed cases are observed globally. Furthermore, a **mortality map **is generated to reflect the deaths to infections ratio. This gives a picture regarding the operational capacity of the healthcare facilities to deal with the pandemic. The ratio is the highest for Italy and Spain, creating a sense of concern with the demand more than the supply. 


        ● Given the nature of the time series data, the trends serve as a visualization tool for predictive modelling. 


        ● The regional criticality mapping indicates the magnitude of the disruption in the supply chain networks worldwide. In this state of urgency, responsiveness is the key for a supply chain to mitigate the consequences. 


        ● In the prescriptive modelling, the critical red zones are the priority for vaccine distribution. The proximity of these high priority regions, illustrated by the data visualization tools, is crucial for efficient distribution planning. 


    It is clear from the data visualization that the impact of the pandemic is becoming more widespread with each passing day. These uncertain times call for a strategic plan in place to satisfy the demand of the vaccine around the globe. In the given context of the pandemic, retail level demand forecasting is pointless. Therefore, the producer’s demand management plan should be based on flowcasting with the ultimate goal of fulfillment planning. 


    Interactive Visualization – Plotly 


    Interactive data visualisation was employed to get more detailed charts and graphs and features such as zoom-in or axis manipulation to compare different scenarios. The following section represents detailed information about various charts used to gain valuable insights. 


    **1. Global COVID-19 Scenario – (Bar Chart 1) **


    **Data manipulation: **A simple extraction of columns representing the global scenario on a timeseries. Cumulation of confirmed cases, recovered cases and total deaths daily using the sum function.


    **Goal: **The objective of employing this chart was to gain an overview of the global impact of the virus on a day-to-day basis using an interactive bar chart. 


    **Function: **To generate this graph, we have employed **_.iplot() _**function. Accurate and detailed mapping allowed us to access each value with our pointer almost immediately 


        **Key Insights: (i) **Visual observation of the chart indicated that COVID-19 virus is spreading at an enormous rate, almost exponentially. 


        **(ii) **Globally, the world has seen a spike in the number of cases after March 15, 2020. In these two weeks, the number of confirmed cases increased almost 5 folds! 


        **(iii) **The zoom-in feature of this interactive were used to calculate mortality, recovery rates and various other measures to better analyse the global situation. 


    

<p id="gdcalert1" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image1.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert2">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image1.png "image_tooltip")
**_Fig 1. Global Scenario COVID-19 _**


    **2. Number of Confirmed Cases for Different Countries – (Bar Chart 2) Data manipulation: **All the countries were grouped together for the latest observation date. 


    **Goal: **To inspect the current situation of countries that have been impacted most due to COVID-19 virus. To identify top countries that need the vaccines most. 


    **Function: **Plotly Express **(_px.bar()_) **was used to generate the bar plot. A remarkable feature is axis manipulation to compare countries with each other and determine the appropriate strategies. 


    **Key Insights: (i) **We now had a clear idea about the top 10 countries that have been impacted the most in the world, namely, US, Italy, Spain, China etc till the last observation date. 


        **(ii) **Relative comparison between Bar chart 1 (Fig.1) and Bar chart 2(Fig. 2) led us to conclude that the top 10 identified countries contribute to approximately 83% of the


        total worldwide confirmed cases. Therefore, almost 94% countries are still in the early stages of the outbreak and they can ensure steps to stop the spread of the virus. 


        (iii) Despite low population, Italy and Spain have a greater number of cases than China. We can hence suggest that these nations be prioritized along with the United States while distributing vaccines. Unequivocally, the United States has the greatest number of confirmed cases and with shortage in medical supplies, death toll can fire up. 

<p style="text-align: right">


<p id="gdcalert2" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image2.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert3">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


<img src="images/image2.png" width="" alt="alt_text" title="image_tooltip">
</p>


<p style="text-align: right">
<strong><em>Fig2. Number of Confirmed cases for different countries </em></strong></p>



    **3. Spread of the Virus and its impact – (Chart 3) **


    **Data manipulation: **Function country_data() is defined that returns a time series data frame of confirmed, recovered cases and death toll for a specific country from the input raw_data. Further, scatter_data variable is assigned to capture the desired country. 


    **Goal: **To inspect the spread of the virus by specifically taking one country at a time. Since top countries can be identified from the above two charts, more detailed analysis is carried out for a specific country. 


    **Function: **Plotly Express **(_px.scatter()_) **was used to generate the time series scatter plot. A remarkable feature is axis manipulation to compare countries with each other and determine the appropriate strategies. 


            **Key Insights: (i) **With the use of interactive nature of the chart, we were able to analyse the slope and spread of the virus. For example, United States analysis shows a steep rise in the number of confirmed cases and deaths from March 19, 2020. We can also observe the gradient of deaths to change rapidly after this date. The range of the death toll is significantly higher than countries like India.


            **(ii) **However, when compared with India on similar scales, the problem doesn’t even seem to have started. Despite being largely populated for a country, spread in India is not as prominent and if contained at this stage, countries like India can easily dodge this pandemic. 


    **4. Choropleth Maps - (Map 4) **


    **Data manipulation: **Inbuilt choropleth map or go.choropleth() function requires 3 letter ISO Country codes to plot values on the world map. For this we have reference the official documentation and acquired 3 letter codes from Github (<span style="text-decoration:underline;">Link</span> here). Some countries like South Sudan were not present in the Novel COVID-19 dataset and therefore some ‘blank’ marks appear on the map with no hover information. 


    **Goal: **To visually interpret the spread of the virus and gain insights on the ‘location’ factors that might affect COVID-19 virus spread and gain key insights about the data. 


    **Function: **Choropleth maps were generated using the inbuilt function **_go.Figure(go.Choropleth_()). **This map allowed the team to visualise data in ranges or in sub-parts. ‘zmin’ and ‘zmax’ values have been tampered to suit the best visualisation. 


            **Key insights: (i) **The most affected parts of the world are in the _‘western’ _part of the world. Surprisingly, out of 6 populated continents, Africa, South America and Australia are least impacted by this virus. If observed with geographical sense, all countries below the tropic of cancer have been affected the least. This information can be useful while conducting the ‘aftermath’ analysis. 


            **(ii)**Further, if closely observed, Spain and Italy seem _‘darker’ _in Fig 4., suggesting heavy death toll in the areas compared to the rest of the world. This can indicate that even with a lesser number of confirmed cases than the United States, healthcare facilities are not prepared to deal with such epidemics. Hence targeting these countries should be the topmost priority. This inturn concurs with our initial observations with seaborn lineplots & heatmaps.


    

<p id="gdcalert3" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image3.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert4">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image3.png "image_tooltip")
**_ Fig 3. Choropleth Map - Total Deaths _**


    Predictive Model 


    Modelling the outbreak of an Epidemic 


    There has been plenty of literature on modelling the propagation of epidemic diseases ever since smallpox (in 1776 by Daniel Bernoulli). Epidemic models arised due to the unique nature of propagation of diseases. 


    Broadly speaking there are two basic types of epidemic models 


        

<p id="gdcalert4" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image4.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert5">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image4.png "image_tooltip")



    Stochastic models use probability distributions to model the propagation of epidemics with one or more inputs being random variables, i.e. they depend upon the probability of exposure to the disease .


    By the 1920s , the mathematics of epidemics became well understood which led to the formulation of “Compartmental Models” which form the basis of deterministic approach. Most of the person-to-person transmitted diseases are well captured with compartmental methods. 


    Recent research in this area has been focused on the application of deep learning algorithms like LSTMs for outbreak predictions. 


    For the purpose of this project, the Compartmental Models proved the best. Note that we also tried support vector machine regression also , but the optimisation of hyper-parameters for good results requires a good GPU and TPU which were our technical limitations. 


    Amongst the 3 models under Compartmental Models we the “_SIR” _model is the most suitable,since it models human to human contact transferred disease (Source: <span style="text-decoration:underline;">SciPython</span>). 

Assumptions and Notations 


    Under the compartmental models , the total population is divided into different subsets . For the SIR model, 


    N :- Total population 


    S :- Population susceptible but not yet infected with the disease 


    I :- Population which is infected 


    R : - Population set which has recovered. 

_(Note :- It is possible to count number of fatalities under R itself, some texts mention it as recovered observation, many others treat it as Removed meaning, either deaths or recovered) _The model assumes that the size of population in each of these compartments change with time. And the rate of change can be explained by two factors , 


        �� :- Contact rate, is the indicator of number of people an infected person comes in contact with . An infected person comes in contact with average of (�� *N) people per unit time. 


        �� :- is the recovery rate , such that 1/�� is the average period of time an infected person can pass the disease on. (in our case it is 1/�� is 14 days ) 


    Further,the model assumes the following:- 


    1. N is sufficiently large such that the size of S,I,R are continuous variables. 2. The population is homogeneously mixed . This enables us to generalise the contact rate and recovery rate for the whole population. 


    3. Contact rate and Recovery rate do not change over time( if they do so they do at a very slow rate and can be assumed constant). There is no trend or seasonality in these figures.


        4. The change in number of infected changes with the interaction of Infected(I) with Susceptible(S). 


    To simplify the modelling some extra assumptions made by us are:- 


        1. We assume that once recovered , a patient develops the immunity to the disease and thus wouldn't get infected again. 


        2. The population set considered for the analysis does not include recent new births.This is partly to simplify the analysis and partly due to availability of data ,since population data sets are usually derived by a country's annual consensus study. 


    Mathematical Model 


    The model is governed by a system of ordinary differential equations( since we assumed that S, I and R are functions of time). 


    We know that the first order differentiation of a time dependent variable with respect to time represents its rate of change with time . Thus, 


    

<p id="gdcalert5" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image5.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert6">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image5.png "image_tooltip")



    The fraction of the population which is susceptible to the disease is S/N . We stated that the change in number of susceptibles population depends upon the interaction of susceptible and infected and the contact rate. 


    Also further we know that the number of susceptible populations will decrease as more and more people get infected . Thus we can represent , 

= <sup><em><span style="text-decoration:underline;">dS</span> </em></sup>

β_SN _


                        <sub><em>dT </em></sub>− <sub><em>I </em></sub>


    The right hand side of the equation gives us the decrease in size of S as some of the people get infected. Thus these same number of people are now in the infected set. Further there would be a fraction of infected population which recovered , thus the net change in the size of infected population will be ,

_<span style="text-decoration:underline;">dI</span> _

<sup>β<em>SN</em></sup>γ_I _= -  


                        _dT I _


    As it is clear, the change in size of the recovered population would be the ones from the infected set who recovered. 


                         = <sup><em><span style="text-decoration:underline;">dR</span> </em></sup>

<sub><em>dT</em></sub>γ_I _


    To solve this system of ODE we need some initial values. In our case , we wanted to predict the number of cases for every “Country-Province” pair. We used the total confirmed cases ,total recovered cases until the 30th March 2020 as our initial values for each pair. 


    **Contact rate **is set as 0.25. Although practically this contact rate would be different for different countries and regions, based upon the government actions , general public awareness etc . For simplifying the model we used the same contact rate for every country. 


    According to the reports of WHO and other sources , the **transmission period **for COVID viirus is 14 days and thus our **recovery rate **would be 1/14 . 


    Using the initial values and the system of ODEs, we then model SIR using the SCIPY library in python which supports differential equations . Output of the predictive model is then fed into the prescriptive model for further analysis. 


    Prescriptive Model - Linear Programming 


    Using the predicted number of infected people from the previous section, we then combine these numbers to find an optimal distribution of vaccines, such that social utility is maximized. The distribution can be modelled as a classical transshipment problem in the supply chain with limited supply. In our model, the supply comes from vaccine factories around the world, whereas demand is represented by the number of people that are infected in each country. 


    Decision variables 


    We only have one type of decision variable - the number of vaccines to be delivered from one vaccine factory to a particular area. 


        _X o_. _of vaccines to deliver from vaccine factory i to city_, _country pair j_, 

<p style="text-align: right">
<sub><em>ijk </em></sub>= _N k _</p>



    The demand nodes are modelled as a country pair j, k because the COVID-19 time-series is structured as such.


    Parameters 


    We define the following parameters in our model: 


    _I o_. _of population infected in city_, _country pair j_, 


    <sub><em>jk </em></sub>= _N k _


    _P o_. _of total population in city_, _country pair j_, 


    <sub><em>jk </em></sub>= _N k _


    _D easure of distance from vaccine factory i to city_, _ountry pair j_, 


    <sub><em>ijk </em></sub>= _M c k _


    _C roduction capacity of vaccine factory i _


    <sub><em>i </em></sub>= _P _


    These parameters are obtained from the datasets that we use. The number of population infected is obtained from the **COVID-19 time-series dataset**, whereas the number of total population is obtained from the **population dataset**. In our code, we calculated the distance from each vaccine factory to each city, country pair. This is made possible by **calculating the geographical distance through the coordinates **(latitude, longitude) of each vaccine factory and affected areas. Finally, the production capacity of each vaccine factory is obtained from the **vaccine facilities dataset **that we produced. It should be noted here that the production capacities stated in our report are arbitrary numbers as we have no information on their real capacities, especially since no COVID-19 vaccines have even been approved for production yet. 


    Objective function 


    Our overall goal is to maximize the total weighted demand for the vaccines globally, defined as: 

<p id="gdcalert6" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image6.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert7">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image6.png "image_tooltip")



    There are three factors that defines the weight of demand for the vaccines to be sent: 


        **1. Percentage of population infected **- The percentage of population infected in a particular area should affect how important it is to send vaccines to that area, and thus assign <span style="text-decoration:underline;">higher</span> <span style="text-decoration:underline;">weights for higher percentages of infected.</span> 


        **2. Population in an area **- The second factor is how big the population in a particular area. For example, suppose Singapore and China both have exactly 30% of its population infected, but China is vastly more populous. We should assign a higher weight to China due to its higher population. Thus, <span style="text-decoration:underline;">the higher the population of an area, the higher the weight</span>. The number here is scaled on a logarithmic scale with base 10,000 as cities' populations are very large. 


        **3. Distance from vaccine factories to the area **- Finally, the last factor is the distance from each vaccine factory to each area. The rationale is that we would want to send to areas closest to the vaccine factories first, for reasons of timeliness and costs. As such, <span style="text-decoration:underline;">the</span> <span style="text-decoration:underline;">higher the distances, the lower the weight</span>. This is the reason why this particular weight is


        given a negative number. Again, the number here is scaled on a logarithmic scale with base 1000 as distances between cities can range greatly. 


    Constraints 


    Finally, we define the constraints to be used in the model: 


    ∑ (Capacity constraint of vaccine factories) 

_j_,_k _

_X<sub>ijk </sub>_≤ _C<sub>i</sub> _


    ∑ (Demand constraint – Vaccines delivered to an area must not exceed no. of infected) 

_i _

_X<sub>ijk </sub>_≤ _I<sub>jk</sub> _


    _X _≥0 (Non-negativity) 


    _ijk _


    The first constraint is simply the capacity constraint - the number of vaccines sent from a vaccine factory cannot exceed its capacity. The second constraint limits the number of vaccines to be delivered to an area to the number of population that is expected to be infected. Otherwise, this will become an oversupply where the LP model sends all the capacity to one area. The last constraint is for non-negativity. 


    Conclusions and lessons learned 


    Descriptive Analysis 


    The data visualization has shown that the rate of the infection is still increasing in most countries. Furthermore, there’s an increase in the mortality rate for some of the countries, which suggests that the **healthcare industry is operating at full capacity **already. China has been able to reduce the number of new cases by a great deal. 


    In countries like India, where the spread of virus is negligible, government policies can still contain the spread of the virus and reduce the number of fatalities. However, containing the spread of COVID-19 by employing strict quarantine policies might not be possible for all countries.Countries like the United States and Italy have been struggling to handle new confirmed cases and the death toll is rising. This is why the efficient vaccine distribution is of paramount importance. The implications relevant to the global supply chains are as follows: 


        1. It is imperative that the **critical nodes of the supply chain **must be identified for process mapping. 


        2. The global positioning of the suppliers should provide **maximum coverage **to the healthcare facilities in dire need. 


        3. There should be redundancy in the supply chain from the design stage in the form of strategically positioned buffer capacity and inventory.


    Predictive Modelling - Limitations & Future Research 


    For the predictive model based on SIR there are certain limitations:- 


        **1. Contact ratio**:- As we mentioned ,contact ratio depends upon a lot of factors hence the contact ratio can be optimized based on each country to further improve the forecasts. As we see in the output that for some countries the predictions are way off the original case. One of the reasons for these errors is the mismatch of contact ratio. 


        **2. Additional factors :- **As it has been the case in most of the diseases , they impact different age-groups differently. Thus model predictions can be improved if age-segmentation is considered. 


    Further research in this area might be aimed at exploiting the emerging data science knowledge like supervised machine learning, deep learning and AI. Supervised machine learning methods like support vector machines promise great ability to capture patterns in data and with new concepts of hyper-parameter tuning , good results can be achieved. Other possible models are Deep learning based models like LSTMs. 


    Linear programming - Limitations & future research 


    Referring to the linear programming that we have built, there are several limitations that we have identified that affects the accuracy of the results: 


        **1. Actual number of vaccine production capacity **- As of right now, there is a lack of data on the COVID-19 vaccine production capacity, as it has not even been invented yet, and multiple companies are producing it. As such, the numbers that we have come up with are arbitrary and do not yet reflect true numbers. As the situation evolves, in the future we should have a clearer picture of vaccine production capacities and can yield more accurate results 


        **2. Objective function sensitivity to logarithmic scale base **- As we have decided to scale the population and distances weights using the logarithmic scale, we have yet to decide what is the optimal/accurate numbers to be used. Future research could research on other measures of weights that are fairer to the countries 


        **3. Population density **- our model currently does not take into account population density, due to lack of data. Future developments could take this into account. 


        **4. Costs **- our model disregards the costs necessary to send vaccines to the various areas, as we work with the assumption that human lives are priceless and we should save as many as possible. Future development of this project can work on minimizing costs when vaccine supply has exceeded demand. 


    Linear programming - Applications 


    However, we believe that this could have applications for various stakeholders: **1. For governments **- World governments such as the United Nations could utilize this tool to coordinate worldwide vaccination from the COVID-19. Individual nations could also utilize the same concept to coordinate the vaccination within their borders to individual provinces.


        **2. For companies **- Pharmaceutical companies can utilize this tool to predict which areas will be most in need of their vaccines. When there is a shortage of supply, the tool determines which areas are more important, taking into account the vaccine factories that they have and their locations.


    Contribution of Team members


<table>
  <tr>
   <td>
    Team member name 
   </td>
   <td>
    Contributions
   </td>
  </tr>
  <tr>
   <td>
    Renaldo Hermawan 
   </td>
   <td>
    ● Proposed the topic of COVID-19 
<p>

    ● Report proposal write-up 
<p>

    ● Built the base code for team members to use and modify ● Coding for the folium map visualization 
<p>
● Development, writeup and coding of linear programming
   </td>
  </tr>
  <tr>
   <td>
    Maaz Ahmad 
   </td>
   <td>
        ● Suggested ways to refine the topic of COVID-19, mainly regarding our area of focus 
<p>

        ● Data visualization to generate insights regarding the current state of affairs and further modelling 
<p>

    ● Highlighting regions of concern with descriptive analysis and the trends associated with their relevant data 
<p>

        ● Drawing conclusions with respect to the pandemic’s implications on global supply chain networks.
   </td>
  </tr>
  <tr>
   <td>Lakshmi Priya Sankaran 
   </td>
   <td>
    ● Report write-up 
<p>

        ● Worked to use predictive models as the input for linear programming 
<p>

        ● Coding and testing various forecasting methods like time series to compare MSE and to decide on a better model that suits our dataset.
   </td>
  </tr>
  <tr>
   <td>
    Jaimish Topre 
   </td>
   <td>
    ● Data Collection from various Opensource sources ● Data Cleaning and Feature Engineering for Predictive Model 
<p>

        ● Trials of various Machine Learning models for predictive analysis which did not qualify for our analysis.(Support-vector machines and linear regression) 
<p>

        ● Formulation and implementation of SIR epidemic model to predict the propagation of COVID-19 which serves as the input for Prescriptive(LP model) model 
<p>

    ● Report section:- Predictive Model
   </td>
  </tr>
  <tr>
   <td>
    Shubham Bhardwaj 
   </td>
   <td>
        ● Prepare a comprehensive descriptive analysis using advanced libraries. 
<p>

        ● Visualise the effect of pandemic on a world map for better presentations 
<p>

        ● Acquiring key insights to build a base for both predictive as well as prescriptive analysis.
   </td>
  </tr>
</table>

