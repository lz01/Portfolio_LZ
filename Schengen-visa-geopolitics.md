---
title: The geopolitics of Schengen visas
output:
  html_document:
    number_sections: TRUE
    toc: TRUE
    code_folding: show
    theme: readable
    highlight: tango
---


# Introduction


We are analyzing here the statistics of visas delivered by Schengen countries around the world. We will use two datasets, available on [kaggle](https://www.kaggle.com): one lists visa statistics of Schengen countries consulates around the world in 2017 and 2018 ([Schengen visas dataset](https://www.kaggle.com/ma7555/schengen-visa-stats)) and the other one contains [world population data](https://www.kaggle.com/theworldbank/world-bank-population-estimates-and-ranking). I published this analysis as a [notebook](https://www.kaggle.com/lamiaz/schengen-visas-geopolitics-revealed) on kaggle as well, so
if you want to see the R code to perform the analysis, you can find it there.

A Schengen visa allows a traveller to enter into the Schengen Area, which comprises the following 25 countries:
Austria, Belgium, the Czech Republic, Denmark, Estonia, Finland, France, Germany, Greece, Hungary, Iceland, Italy, Latvia, Lithuania, Luxembourg, Malta, the Netherlands, Norway, Poland, Portugal, Slovakia, Slovenia, Spain, Sweden and Switzerland.





<img src="figure/unnamed-chunk-2-1.png" title="plot of chunk unnamed-chunk-2" alt="plot of chunk unnamed-chunk-2" width="\textwidth" style="display: block; margin: auto;" />


People holding certain citizenships don't need a Schengen visa to enter the Schengen area, their passport is enough. But most citizenships do.
There are different types of Schengen visas.
A uniform visa allows one to enter the Schengen area and stay there for a short time (up to 90 days). Uniform visas can either allow for a single entry or for multiple entries within the visa's validity period. A consulate can also issue a visa that only allows its holder to be in the country that issued the visa to the exclusion of any other Schengen country (visa with limited territorial validity).

If a person needs to transit through an airport in the Schengen area before continuing their journey to a destination outside the Schengen area, they will need an airport transit visa (ATV).

We will look at statistics of visa issuance and refusal across Schengen states and countries asking for visas. We will also look at the distribution of consulates around the world, and how they can be indicators of geopolitical significance.




# Analysis of visa and consular statistics

## Number of visa applications per country

We first look at the number of uniform visa applications per country for the 20 countries that file the highest number of applications.

<img src="figure/unnamed-chunk-4-1.png" title="plot of chunk unnamed-chunk-4" alt="plot of chunk unnamed-chunk-4" width="\textwidth" style="display: block; margin: auto;" />

Russia is number one with around 3.7 million visa applications in 2018. It is followed by China (2.8 million) and India (1.1 million). In the top 10, we also find smaller countries such as Algeria, Belarus and Morocco, with around 0.7 million each.
We expect countries with a large population size to ask for more visas than countries with a smaller population. In order to take out this effect, we redo the same analysis, this time normalizing by population size and calculating the number of visa applications per 100.000 people.

<img src="figure/unnamed-chunk-5-1.png" title="plot of chunk unnamed-chunk-5" alt="plot of chunk unnamed-chunk-5" width="\textwidth" style="display: block; margin: auto;" />

After taking into account population size, the picture changes. Belarus which was already the fourth country that asked for the most visas, becomes the first once we normalize by its population. Belarus is one of the few countries present in Europe, with Russia, Turkey, Armenia and Kosovo, whose citizens need to ask for a visa to enter the Schengen area. It is understandable that due to its geographic location and connections with neighbouring countries, it should be the country with the highest rate per 100.000 people. Small countries like Kosovo, Koweit or Cape verde also have some of the highest normalized rate of visa applications. In order to have a better look at them, we can list the 20 countries with the highest rate of visa applications per person.


<img src="figure/unnamed-chunk-6-1.png" title="plot of chunk unnamed-chunk-6" alt="plot of chunk unnamed-chunk-6" width="\textwidth" style="display: block; margin: auto;" />


## Number of consulates per country

Let's first look at the number of Schengen consulates present in countries around the world. The 20 countries with the highest number of consulates are shown in the figure below.
<img src="figure/unnamed-chunk-7-1.png" title="plot of chunk unnamed-chunk-7" alt="plot of chunk unnamed-chunk-7" width="\textwidth" style="display: block; margin: auto;" />

We look again at the number of Schengen consulates present in a country, but this time normalized by the country's population size. Here we show the countries with the highest number of Schengen consulates per 100.000 people.

<img src="figure/unnamed-chunk-8-1.png" title="plot of chunk unnamed-chunk-8" alt="plot of chunk unnamed-chunk-8" width="\textwidth" style="display: block; margin: auto;" />
After taking into account population size, european microstates San Marino, Monaco and Andorra are now at the top. These microstates are not technically part of the EU nor the Schengen area, but they have very close relationships with the EU. San Marino and Monaco have an open border with the Schengen area (respectively with Italy and France), which means it is as if they are part of the Schengen area. Andorra doesn't have an open border, but, given that it is not possible to fly into Andorra, only enter through either Spain or France, it is also de facto in the Schengen area.

## Average number of visa applications per consulate

We now look at how the average number of visa applications treated by a consulate varies depending on the country where the consulate is located. Some countries have very busy consulates whereas others have consulates that treat few applications per year.
We show in the figure below the 20 countries with the highest number of visa applications per consulate.


<img src="figure/unnamed-chunk-9-1.png" title="plot of chunk unnamed-chunk-9" alt="plot of chunk unnamed-chunk-9" width="\textwidth" style="display: block; margin: auto;" />

Among the countries that have the busiest consulates, we find again countries such as Russia, Belarus, China, India, Algeria, Morocco and Turkey, which are the countries who file the most visa applications.

But there are also countries that have many consulates that are not very busy.
We now look at the interplay between the number of Schengen consulates in a country and the average number of visa applications they receive. We choose to only highlight certain countries to make the figure more readable.

<img src="figure/unnamed-chunk-10-1.png" title="plot of chunk unnamed-chunk-10" alt="plot of chunk unnamed-chunk-10" width="\textwidth" style="display: block; margin: auto;" />

We find that the number of Schengen consulates in a country depends both on the number of visa applications but also on the geopolitical importance of the country.
Geopolitical influence can make a Schengen state be present in a country or even have several consulates in it, even if each consulate is treating only a few applications.

Countries such as Australia, Brazil, Canada, Germany, Israel and Japan all have a large number of consulates considering the number of applications they receive, as they are influent on the world stage.
The USA, shown in red in the figure, appears as a clear outlier here, a sure sign of its geopolitical importance!

## Number of Schengen states with a consulate in the country

Another way to look at it is to find out how many out of the 25 Schengen states have a consular presence in a given country. We expect once again that both the number of visa applications and the geopolitical influence will play a role.

<img src="figure/unnamed-chunk-11-1.png" title="plot of chunk unnamed-chunk-11" alt="plot of chunk unnamed-chunk-11" width="\textwidth" style="display: block; margin: auto;" />

The 11 countries that have more than 20 Schengen states with a consular presence are the following:

Canada, China, Egypt, India, Israel, Japan, the Russian Federation, Turkey, Ukraine, the United Kingdom and the USA.

The 26 countries with 16 to 20 Schengen states with a consular presence are the following:

 Algeria, Argentina, Australia, Bulgaria, Croatia, Cuba, Ethiopia, France, Germany, Indonesia, Iran, Ireland, Kenya, Lebanon, Mexico, Morocco, Nigeria, Pakistan, Romania, Saudi Arabia, Serbia, South Africa, South Korea, Thailand, the United Arab Emirates and Vietnam.

## Schengen states issuing the most visas

Out of all the Schengen states, which ones issue the most visas? And does this depend on the state's population as well, with large states issuing more visas than small ones?

<img src="figure/unnamed-chunk-12-1.png" title="plot of chunk unnamed-chunk-12" alt="plot of chunk unnamed-chunk-12" width="\textwidth" style="display: block; margin: auto;" />

France is largely on top, issuing 3.35 million visas in 2018, almost double the second state, Germany, which issued about 1.84 million visas. We notice that there is a great disparity in between states with, on the one hand, France, Germany, Italy and Spain, all issuing more than 1.5 million visas, and, on the other hand, the ten states at the bottom all issuing less than 200.000 visas in 2018.

Let's see now how it varies if we take into account the Schengen state's population size.

<img src="figure/unnamed-chunk-13-1.png" title="plot of chunk unnamed-chunk-13" alt="plot of chunk unnamed-chunk-13" width="\textwidth" style="display: block; margin: auto;" />

When taking into account the state's population size, the top countries become Finland and the three Baltic states (Lithuania, Estonia and Latvia).

## Rate of refused uniform visas

When a person asks for a visa, it is not always accepted. A reason for the refusal is usually communicated to the person, but it can be quite vague. The main reasons usually provided are:

- Not justifying well enough the purpose and condition of your stay
- Not providing a good enough proof of sufficient means
- Being suspected of not intending to return to your home country

The exact criteria behind these categories, and the way one can make sure not to have their application fall into one, is not always entirely clear. Schengen states are afraid of illegal immigration following a legal entry into the Schengen area, and therefore limit visa issuance for the people they deem most at risk of wanting to illegally emigrate. But refusal rate can also depend on political choices made at the level of the Schengen state to limit visa issuance in general, to a particular country, or to a specific category of people. It is hard to tell, as the criteria and politics behind visa issuance are usually not public, leaving one to speculate.

### Rate of refused uniform visas per recipient country

We first look at the refusal rate per recipient country, limiting ourselves to countries that submitted more than 100.000 visa applications in the year.

<img src="figure/unnamed-chunk-14-1.png" title="plot of chunk unnamed-chunk-14" alt="plot of chunk unnamed-chunk-14" width="\textwidth" style="display: block; margin: auto;" />

Algeria is the country that has the highest refusal rate of visa applications, with 45.5% of applications being denied!
Four out of the six countries that have the highest refusal rates are in North Africa (Algeria, Egypt, Tunisia and Morocco).

Let's remember the lyrics of Cheb hasni, one of the most popular Algerian raï singers, who says in his song "The visa":

عولت انا نشوف العزيزة"

حرام عليكم

آه غبنتوني

"عكستوهلي حتي في الڤيزا




Which roughly translates to :

"I decided to go see my baby

Shame on you

Ah, you hurt me

You went against me even for the visa"

Being refused a Schengen visa is a central part of life in many countries.


### Rate of refused visas per Schengen state
The question that many visa applicants ask themselves, when they are understandably afraid of getting their application rejected is whether they can increase their chances by carefully choosing which country they should apply to.
Are some Schengen countries more likely to refuse or accept visa applications?
We can first address this question by looking at the average rate of refused visas per issuing state, to see if some Schengen states are more prone to accept or refuse visa applications.

<img src="figure/unnamed-chunk-15-1.png" title="plot of chunk unnamed-chunk-15" alt="plot of chunk unnamed-chunk-15" width="\textwidth" style="display: block; margin: auto;" />

Malta, Belgium, Portugal and France appear as the states that are the most likely to refuse a visa application. Finland, the three Baltic states and Iceland appear as the states the most likely to accept a visa application.

The drawback of this analysis is that it looks at visa applications in bulk, without differentiating between visa applications emanating from rich and geopolitically influent countries and those emanating from poorer countries. We just saw that the countries with the highest average refusal rates tend to be poorer and/or have less geopolitical clout. Certain Schengen states may receive more applications from countries that tend to get more visa applications refused on average, and this could alter the results we get.

In order to address this issue, we can look at, for each recipient country, how the average refusal rates from all Schengen states compare to the refusal rate by one particular state.
We are going to examine the top 5 countries from the previous figure: Malta, Belgium, Portugal, France and the Netherlands. We will only look at country-state pairs where the country has applied for more than 100 visas in 2018.

First, let's look at Malta, Belgium, the Netherlands and Portugal. Each dot represents a country-state pair.

<img src="figure/unnamed-chunk-16-1.png" title="plot of chunk unnamed-chunk-16" alt="plot of chunk unnamed-chunk-16" width="\textwidth" style="display: block; margin: auto;" />
Malta, Belgium, the Netherlands and Portugal all appear to tend to refuse visa applications more often than the other states, as we see a clear overrepresentation of dots above the diagonal line.

Let's now look at France, which we saw earlier is the state issuing the highest number of uniform visas.
<img src="figure/unnamed-chunk-17-1.png" title="plot of chunk unnamed-chunk-17" alt="plot of chunk unnamed-chunk-17" width="\textwidth" style="display: block; margin: auto;" />

France, on the contrary, shows a completely different picture. It doesn't have a higher refusal rate than its neighbouring Schengen states, it is average or even lower for a few countries. The only reason it appears as one of the states with the highest average refusal rates is that it receives more visa applications from countries that get refused more on average.

Let's now look at the countries that had the lowest average refusal rate of visa applications: Finland, Estonia, Lithuania and Latvia. We don't include Iceland as it only has two consulates.

<img src="figure/unnamed-chunk-18-1.png" title="plot of chunk unnamed-chunk-18" alt="plot of chunk unnamed-chunk-18" width="\textwidth" style="display: block; margin: auto;" />

Well, it doesn't seem anymore that Finland and the Baltic states are more accepting than other states! Their rates are more or less on both sides of the diagonal with a few more countries above the diagonal. The reason that they have a higher average acceptance rate is that they tend to receive more applications from countries that tend to get accepted more on average. But in fact they tend to refuse more visa applications than other Schengen states if we look at it for each country.

A reminder that averages can be misleading when they hide a sampling bias !


### Consulates with the worst refusal rates

Which consulates actually have the highest refusal rates?
We only consider consulates that received at least 10 applications in the year.
We rank the 10 consulates with the highest refusal rates in 2018.

<table class="table" style="margin-left: auto; margin-right: auto;">
 <thead>
  <tr>
   <th style="text-align:left;"> Schengen state </th>
   <th style="text-align:left;"> Country </th>
   <th style="text-align:left;"> Consulate </th>
   <th style="text-align:right;"> Refusal rate </th>
   <th style="text-align:right;"> Nb applications </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> Malta </td>
   <td style="text-align:left;"> ALGERIA </td>
   <td style="text-align:left;"> ALGIERS </td>
   <td style="text-align:right;"> 0.868 </td>
   <td style="text-align:right;"> 3717 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Belgium </td>
   <td style="text-align:left;"> CONGO (DEMOCRATIC REPUBLIC) </td>
   <td style="text-align:left;"> LUBUMBASHI </td>
   <td style="text-align:right;"> 0.867 </td>
   <td style="text-align:right;"> 83 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Portugal </td>
   <td style="text-align:left;"> VENEZUELA </td>
   <td style="text-align:left;"> VALENCIA </td>
   <td style="text-align:right;"> 0.800 </td>
   <td style="text-align:right;"> 15 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Portugal </td>
   <td style="text-align:left;"> NIGERIA </td>
   <td style="text-align:left;"> ABUJA </td>
   <td style="text-align:right;"> 0.756 </td>
   <td style="text-align:right;"> 5939 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Netherlands </td>
   <td style="text-align:left;"> CYPRUS </td>
   <td style="text-align:left;"> NICOSIA </td>
   <td style="text-align:right;"> 0.737 </td>
   <td style="text-align:right;"> 19 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Portugal </td>
   <td style="text-align:left;"> BRAZIL </td>
   <td style="text-align:left;"> BELO HORIZONTE </td>
   <td style="text-align:right;"> 0.723 </td>
   <td style="text-align:right;"> 83 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Belgium </td>
   <td style="text-align:left;"> CONGO (DEMOCRATIC REPUBLIC) </td>
   <td style="text-align:left;"> KINSHASA </td>
   <td style="text-align:right;"> 0.718 </td>
   <td style="text-align:right;"> 2289 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Sweden </td>
   <td style="text-align:left;"> NIGERIA </td>
   <td style="text-align:left;"> ABUJA </td>
   <td style="text-align:right;"> 0.659 </td>
   <td style="text-align:right;"> 3039 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Finland </td>
   <td style="text-align:left;"> ALGERIA </td>
   <td style="text-align:left;"> ALGIERS </td>
   <td style="text-align:right;"> 0.649 </td>
   <td style="text-align:right;"> 1307 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Hungary </td>
   <td style="text-align:left;"> ALGERIA </td>
   <td style="text-align:left;"> ALGIERS </td>
   <td style="text-align:right;"> 0.642 </td>
   <td style="text-align:right;"> 2713 </td>
  </tr>
</tbody>
</table>
Algeria, Nigeria and the Democratic Republic of Congo all have two consulates each in the list, the worst consulate being that of Malta in Algeria, which refuses an astonishing 86.8% of applications (3226 out of 3717).



## Share of multiple entries visas among uniform visas issued
When a consulate issues a uniform visa, it can give a single entry visa or generously decide to give a multiple entries visa (MEV) that can be reused for subsequent trips within the visa's validity period.
How often do consulates decide to issue multiple entries visa? Does this depend on the Schengen state?

<img src="figure/unnamed-chunk-20-1.png" title="plot of chunk unnamed-chunk-20" alt="plot of chunk unnamed-chunk-20" width="\textwidth" style="display: block; margin: auto;" />
There is a very high variability in how likely a Schengen state is to issue a multiple entries visa (MEV). Some countries such as Slovenia, Estonia, the Netherlands and Finland have a very high share of MEVs among the visas issued (higher than 89%). Countries such as France, Malta, Iceland, Sweden, the Czech Republic and Norway have a share in between 21% and 31%. That's quite a large difference!
But as we saw before for the refusal rate, certain Schengen states receive more visa applications from countries that are refused more on average. The same bias could be at play again for the share of MEVs among visas issued.

We are going to look at how the share of MEVs issued by a particular Schengen state relates to the average share of MEVs issued by all states to a particular country, like we did earlier for the refusal rate.

Let's first look at Slovenia, Estonia, the Netherlands and Finland, the four countries that have the highest average share of MEVs.

<img src="figure/unnamed-chunk-21-1.png" title="plot of chunk unnamed-chunk-21" alt="plot of chunk unnamed-chunk-21" width="\textwidth" style="display: block; margin: auto;" />

If Slovenia and the Netherlands are clearly above the diagonal line, issuing a higher share of MEVs than other states, Estonia is on both sides and Finland is clearly below the line. Finland is actually less likely to issue a MEV, compared to other states. The only reason its average share of MEVs is high is that it tends to issue more visas to countries that get more MEVs on average.

Let's now look at France, Sweden, the Czech Republic and Norway, some of the countries with the lowest average share of MEVs issued.

<img src="figure/unnamed-chunk-22-1.png" title="plot of chunk unnamed-chunk-22" alt="plot of chunk unnamed-chunk-22" width="\textwidth" style="display: block; margin: auto;" />

All four countries are clearly below the line, meaning that they are less likely to issue a MEV than other states, and tend to get more visa applications from countries that get a lower share of MEVs. Both factors explain their low average share of MEVs.

Finally, let's look at two interesting states, Spain and Italy.

<img src="figure/unnamed-chunk-23-1.png" title="plot of chunk unnamed-chunk-23" alt="plot of chunk unnamed-chunk-23" width="\textwidth" style="display: block; margin: auto;" />

Spain has a few dots on the diagonal, countries for which its share of MEVs is close to other states, but most dots are very low, below 25%. This probably indicates that Spain has decided on a very low rate of MEVs that it applies indiscriminately in most countries.

Italy is quite different. It has a very high share of MEVs, well above the diagonal line, for countries that tend to get more MEVs on average, and it applies a very variable rate of MEVs in other countries. 

Such patterns seem to indicate that the share of MEVs is something that is decided at the level of the state through general policies (or quotas) applied in its consulates. If the probability to get an MEV only depended on the applcation being submitted, we wouldn't expect to see such different distributions across Schengen states.

By drawing histograms, one for each Schengen state, that show the share of multiple entries visas issued among all uniform visas issued (with a dashed line for the average), we can look at inter-state variability in a single figure.

<img src="figure/unnamed-chunk-24-1.png" title="plot of chunk unnamed-chunk-24" alt="plot of chunk unnamed-chunk-24" width="\textwidth" style="display: block; margin: auto;" />

 In this figure, we can once again note that Italy, even though it has a somewhat high average share (72%), applies a very different rate in its various consulates, as we can see from the spread of the distribution.

## Relation between visa issuance rate and share of MEVs

Now, we can look at how the share of MEVs among visas issued relates to the general issuance rate.
Do Schengen states that tend to issue a higher proportion of multiple entries visas also tend to have a higher issuance rate in general? If such a correlation exists, it could be because Schengen states have similar general policies governing their issuance rate and their MEV rate. 


We find that the two variables are correlated (with a correlation of 0.42) meaning that the Schengen states that have a higher average issuance rate are also more likely to give multiple entries visas.

Correlation alone is not that informative, so we can look at it graphically to get a better idea of the relation between the two variables.

<img src="figure/unnamed-chunk-26-1.png" title="plot of chunk unnamed-chunk-26" alt="plot of chunk unnamed-chunk-26" width="\textwidth" style="display: block; margin: auto;" />

There seems to be a general connection between the two variables. Schengen states which have a higher average issuance rate like Finland, Estonia, Lithuania and Latvia also tend to have a higher average share of MEVs, whereas countries with a lower average issance rate like Malta, France, Portugal or Belgium also tend to have a lower average share of MEVs. Once again, we saw in our previous analyses that the average issuance rate hides a sampling bias of the countries of visa applicants.

But the relationship doesn't hold for all states, with for example the Netherlands, Slovenia and Germany having an average issuance rate but a high share of MEVs, and Sweden, Norway and the Czech Republic issuing fewer MEVs than other states.
This means that the policies behind the visa issuance rate and the share of MEVs are different.

## Who asks for airport transit visas and to go where?

Finally, we are going to look at a visa category we haven't considered yet, the airport transit visa (ATV), which allows its holder to transit through an airport in the Schengen area without actually entering the country. Which countries ask for the most ATVs?


<table class="table" style="margin-left: auto; margin-right: auto;">
 <thead>
  <tr>
   <th style="text-align:left;"> Country </th>
   <th style="text-align:right;"> ATVs applied for </th>
   <th style="text-align:right;"> Population </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> CUBA </td>
   <td style="text-align:right;"> 902 </td>
   <td style="text-align:right;"> 11489000 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> INDIA </td>
   <td style="text-align:right;"> 548 </td>
   <td style="text-align:right;"> 1354052000 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> ALGERIA </td>
   <td style="text-align:right;"> 436 </td>
   <td style="text-align:right;"> 42008000 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> NIGERIA </td>
   <td style="text-align:right;"> 382 </td>
   <td style="text-align:right;"> 195875000 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> USA </td>
   <td style="text-align:right;"> 338 </td>
   <td style="text-align:right;"> 327507000 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> GHANA </td>
   <td style="text-align:right;"> 291 </td>
   <td style="text-align:right;"> 29464000 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> IRAN </td>
   <td style="text-align:right;"> 215 </td>
   <td style="text-align:right;"> 82012000 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> TURKEY </td>
   <td style="text-align:right;"> 170 </td>
   <td style="text-align:right;"> 81917000 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> SENEGAL </td>
   <td style="text-align:right;"> 129 </td>
   <td style="text-align:right;"> 16294000 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> MEXICO </td>
   <td style="text-align:right;"> 122 </td>
   <td style="text-align:right;"> 130759000 </td>
  </tr>
</tbody>
</table>


By far, the country that asks for the most airport transit visas is Cuba, and it is even more striking given its smaller population size compared to Nigeria or India.
Cubans ask for ATVs to the Netherlands, France and Spain. By looking at the flight statistics out of Havana on [Flightstats](https://www.flightstats.com), we find that the only airlines flying out of Havana to Europe are KLM to Amsterdam, Iberia to Madrid, Air France to Paris and Edelweiss to Zurich. Other airlines fly from Havana to the Caribbean, North America, South America or Russia. The restriction on the flights available from Cuba forces cubans to ask for airport transit visas to Spain, France or the Netherlands if they want to travel to somewhere in Europe outside of the Schengen area, to Africa or to Asia.


# Conclusion
We saw that analyzing a public dataset of Schengen visas statistics can actually teach us a lot about the interplay of visa issuance and geopolitics, as well as help us make guesses regarding the policies that Schengen states adopt in the area. Schengen states have a different presence worldwide, issuing visas to many countries or only to a select few, adjusting their uniform visas issuance rate or more particularly their multiple entries visas isuance rate according to their own policies. We can only make educated guesses, as, in the end, we don't have access to all the missing data related to visas applications, such as the socio-economic profile of visa applicants. We could only look at data at the scale of countries and consulates. 
I hope you enjoyed this analysis and took away something from it, whether in terms of Schengen policies and visa statistics or drawing figures in R. I sure now have a better understanding of Schengen visas and of how variable their issuance rate can be. It's a good counterpoint to the direct experience many of us have had, asking for Schengen visas and feeling both stressed and a bit lost at how arbitrary the process of acceptance/refusal seemed from afar.
