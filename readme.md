<h1>Crime Incident Data</h1>

<b>Download the dataset here:</b> https://cornell.box.com/s/0fsns32n29d29uwvq95tep11xnstn3hh

<h2>Overview</h2>
This dataset tracks incidents of crime across 27 cities across the United States from the period Jan 1, 2018 - Mar 15, 2020 and was created for the purpose of establishing a synthetic control for New York City crime trends. These cities were chosen based on population size and public crime data availability. 

<h2>Columns in this dataset</h2>
<ul>
  <li><b>std_date:</b> A standardized date, corresponding to an incident occurrence date (or incident reported date if not available)</li>
  <li><b>category_1:</b> First level of the tree excluding the root (Property, Violent, etc.)</li>
  <li><b>category_2:</b> Second level of the tree (Burglary, Theft, Assault, etc.)</li>
  <li><b>category_3:</b> Third level of the tree (Grand Larceny, Grand Larceny Auto, etc.)</li>
</ul>

<h2>Date range</h2>
Jan 1, 2018 - Mar 15, 2020

<h2>Granularity</h2>
Each row in this dataset corresponds to an incident of crime. While many cities have switched to NIBRS reporting where multiple crime types can be reported from a single incident, some cities may report based on UCR Traditional Summary reporting where only the most severe crime type is reported per incident. This dataset is simply an aggregation of each city’s crime regardless of reporting schemes, so some cities may appear to have more crime than others based on this difference in reporting. In some cases when cities changed their reporting methodology during the analysis period, a discontinuity of crime volume may be observed due to this change (i.e. Atlanta, Houston). 

<h2>Standardization framework</h2>
The standardized crime hierarchy is summarized in the tree below. Crime incidents for each city will map into a leaf of the tree. 

<img src=standard_tree.PNG/>

Note: Data quality of mappings across cities weakens at the third level of the hierarchy (i.e. Grand Larceny, Grand Larceny Auto, Theft from Auto, etc.) due to the differences in city reporting granularity and also differences in crime definitions across city/state lines. For this reason, we recommend rolling data up to the second level of the hierarchy (category_2) or higher for any further analysis. 

<h2>Definitions for category_2 values</h2>
<ul>
  <li><b>Homicide:</b> Murder and manslaughter (does not include justifiable homicide)</li>
  <li><b>Rape:</b> Forcible or aggravated penetration (does not include statutory rape)</li>
  <li><b>Robbery:</b> All taking of property through force or threat of force</li>
  <li><b>Assault:</b> Includes aggravated and simple assaults when possible</li>
  <li><b>Burglary:</b> Unlawful entry into structure (residential and commercial) to commit theft without use of force</li>
  <li><b>Theft:</b> Unlawful taking of property (includes motor vehicle theft)</li>
  <li><b>Other property crime:</b> Includes a broad set of property crimes such as arson, stolen property offenses, damage to property, trespass, and other miscellaneous property crimes. Excludes animal crimes, drug, theft, burglary, and white collar crimes. </li>
  <li><b>Drug:</b> All drug-related abuses including cultivation, distribution, sale, purchase, use, possession, transportation, or importation of any controlled drug or narcotic substance.  </li>
  <li><b>White collar:</b> Includes crimes of deceit or intentional misrepresentation, such as counterfeiting, fraud, and embezzlement (includes offenses such as check fraud, confidence game, and credit card fraud)</li>
  <li><b>Gambling:</b> All unlawful betting or wagering, tampering, or operation of game of chance (includes equipment violations)</li>
  <li><b>Arson:</b> Any willful or malicious burning or attempt to burn property</li>
</ul>

These definitions are modified from other crime frameworks, such as a previous Bureau of Justice Statistics analysis (https://www.bjs.gov/recidivism/#), FBI offense definitions (https://ucr.fbi.gov/crime-in-the-u.s/2019/crime-in-the-u.s.-2019/topic-pages/offense-definitions), and definitions from City Crime Stats (https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3674032).

<h2>Original data sources and mappings</h2>
Further details on the precise mappings and references to the original, city data sources can be found on the public document here: https://docs.google.com/spreadsheets/d/1b5MAHDuhgzULseHsw83YlgoGeSnv6jP7rJ6cCe1MIPA/edit?usp=sharing

<h2>Data availability and frequency per city</h2>

<img src=diagnostic.png/>
# crime-data-scripts
