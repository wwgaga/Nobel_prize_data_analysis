# Nobel_prize_analysis
## Introduction
The Nobel Prize, established in 1895 by Swedish chemist and industrialist Alfred Nobel, consists of annual international awards in various categories, 
recognizing exceptional achievements in academia, culture, and science. These awards, including Chemistry, Literature, Peace, Physics, and Physiology or Medicine, 
were first presented in 1901 and are esteemed as the most prestigious accolades within their respective domains.
## Data gather
1. Gather data by accessing APIs
The Nobel Prize website provides a free REST-based API for developers to access up-to-date information on Nobel Prizes and Laureates.
This data is freely available and is synchronized with updates on the official website, including announcements of new Laureates.
Here I access the API at this endpoint: https://api.nobelprize.org/2.1/laureates.
In addition, the official Nobel Prize website is : https://www.nobelprize.org/about/developer-zone-2/.
3. Download data manually:
The Kaggle website provides a dataset encompassing Nobel Prize laureates(winners) from 1901 to 2000. The website is : https://www.kaggle.com/datasets/bahramjannesarr/nobel-prize-from-1901-till-2020. 
This dataset can be directly obtained in CSV format directly from the Kaggle website.
## Data access
Since API featched data The fetched API data, represented as 'df,' comprises 980 rows and 101 columns.
Notably, the majority of these columns (92 out of 101) contain missing values. 
Additionally, some columns contain the same information presented in English, Swedish, and Norwegian, indicated by the '.en,' '.se,' and '.no' suffixes in the column names.

The columns can be categorized as follows: 
1. Name-related columns:: 'knownName.en', 'knownName.se', 'givenName.en', 'givenName.se',
       'familyName.en', 'familyName.se', 'fullName.en', 'fullName.se',
       'knownName.no', 'givenName.no', 'familyName.no', 'fullName.no',
       'orgName.en', 'orgName.no', 'orgName.se', 'nativeName', 'penName',
       'penNameOf.fullName';
2. Birth-related columns: 'birth.date', 'birth.place.city.en', 'birth.place.city.no',
       'birth.place.city.se', 'birth.place.country.en',
       'birth.place.country.no', 'birth.place.country.se',
       'birth.place.cityNow.en', 'birth.place.cityNow.no',
       'birth.place.cityNow.se', 'birth.place.cityNow.sameAs',
       'birth.place.countryNow.en', 'birth.place.countryNow.no',
       'birth.place.countryNow.se', 'birth.place.countryNow.sameAs',
       'birth.place.continent.en', 'birth.place.continent.no',
       'birth.place.continent.se', 'birth.place.locationString.en',
       'birth.place.locationString.no', 'birth.place.locationString.se';
3. Death-related columns: 'death.date', 'death.place.city.en', 'death.place.city.no',
       'death.place.city.se', 'death.place.country.en',
       'death.place.country.no', 'death.place.country.se',
       'death.place.country.sameAs', 'death.place.cityNow.en',
       'death.place.cityNow.no', 'death.place.cityNow.se',
       'death.place.cityNow.sameAs', 'death.place.countryNow.en',
       'death.place.countryNow.no', 'death.place.countryNow.se',
       'death.place.countryNow.sameAs', 'death.place.continent.en',
       'death.place.continent.no', 'death.place.continent.se',
       'death.place.locationString.en', 'death.place.locationString.no',
       'death.place.locationString.se'
4. Founded-related columns: 'founded.date', 'founded.place.city.en', 'founded.place.city.no',
       'founded.place.city.se', 'founded.place.country.en',
       'founded.place.country.no', 'founded.place.country.se',
       'founded.place.country.sameAs', 'founded.place.cityNow.en',
       'founded.place.cityNow.no', 'founded.place.cityNow.se',
       'founded.place.cityNow.sameAs', 'founded.place.countryNow.en',
       'founded.place.countryNow.no', 'founded.place.countryNow.se',
       'founded.place.countryNow.sameAs', 'founded.place.continent.en',
       'founded.place.continent.no', 'founded.place.continent.se',
       'founded.place.locationString.en', 'founded.place.locationString.no',
       'founded.place.locationString.se', 'foundedCountry.en',
       'foundedCountry.no', 'foundedCountry.se', 'foundedCountryNow.en',
       'foundedCountryNow.no', 'foundedCountryNow.se', 'foundedContinent.en'
5. Other columns:  These include 'gender' and other columns.
