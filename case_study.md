case\_study
================
JiyueQin
October 8, 2018

take a look at the dataset.

``` r
str(nyc_airbnb)
```

    ## Classes 'tbl_df', 'tbl' and 'data.frame':    40753 obs. of  17 variables:
    ##  $ id                            : int  7949480 16042478 1886820 6627449 5557381 9147025 11675715 715270 17876530 182177 ...
    ##  $ review_scores_location        : int  10 NA NA 10 10 10 10 9 10 9 ...
    ##  $ name                          : chr  "City Island Sanctuary relaxing BR & Bath w Parking" "WATERFRONT STUDIO APARTMENT" "Quaint City Island Community." "Large 1 BDRM in Great location" ...
    ##  $ host_id                       : int  119445 9117975 9815788 13886510 28811542 403032 56714504 3684360 11305944 873273 ...
    ##  $ host_name                     : chr  "Linda & Didier" "Collins" "Steve" "Arlene" ...
    ##  $ neighbourhood_group           : chr  "Bronx" "Bronx" "Bronx" "Bronx" ...
    ##  $ neighbourhood                 : chr  "City Island" "City Island" "City Island" "City Island" ...
    ##  $ latitude                      : num  40.9 40.9 40.8 40.8 40.9 ...
    ##  $ longitude                     : num  -73.8 -73.8 -73.8 -73.8 -73.8 ...
    ##  $ room_type                     : chr  "Private room" "Private room" "Entire home/apt" "Entire home/apt" ...
    ##  $ price                         : int  99 200 300 125 69 125 85 39 95 125 ...
    ##  $ minimum_nights                : int  1 7 7 3 3 2 1 2 3 2 ...
    ##  $ number_of_reviews             : int  25 0 0 12 86 41 74 114 5 206 ...
    ##  $ last_review                   : Date, format: "2017-04-23" NA ...
    ##  $ reviews_per_month             : num  1.59 NA NA 0.54 3.63 2.48 5.43 2.06 5 2.98 ...
    ##  $ calculated_host_listings_count: int  1 1 1 1 1 1 1 4 3 4 ...
    ##  $ availability_365              : int  170 180 365 335 352 129 306 306 144 106 ...
    ##  - attr(*, "spec")=List of 2
    ##   ..$ cols   :List of 17
    ##   .. ..$ id                            : list()
    ##   .. .. ..- attr(*, "class")= chr  "collector_integer" "collector"
    ##   .. ..$ review_scores_location        : list()
    ##   .. .. ..- attr(*, "class")= chr  "collector_integer" "collector"
    ##   .. ..$ name                          : list()
    ##   .. .. ..- attr(*, "class")= chr  "collector_character" "collector"
    ##   .. ..$ host_id                       : list()
    ##   .. .. ..- attr(*, "class")= chr  "collector_integer" "collector"
    ##   .. ..$ host_name                     : list()
    ##   .. .. ..- attr(*, "class")= chr  "collector_character" "collector"
    ##   .. ..$ neighbourhood_group           : list()
    ##   .. .. ..- attr(*, "class")= chr  "collector_character" "collector"
    ##   .. ..$ neighbourhood                 : list()
    ##   .. .. ..- attr(*, "class")= chr  "collector_character" "collector"
    ##   .. ..$ latitude                      : list()
    ##   .. .. ..- attr(*, "class")= chr  "collector_double" "collector"
    ##   .. ..$ longitude                     : list()
    ##   .. .. ..- attr(*, "class")= chr  "collector_double" "collector"
    ##   .. ..$ room_type                     : list()
    ##   .. .. ..- attr(*, "class")= chr  "collector_character" "collector"
    ##   .. ..$ price                         : list()
    ##   .. .. ..- attr(*, "class")= chr  "collector_integer" "collector"
    ##   .. ..$ minimum_nights                : list()
    ##   .. .. ..- attr(*, "class")= chr  "collector_integer" "collector"
    ##   .. ..$ number_of_reviews             : list()
    ##   .. .. ..- attr(*, "class")= chr  "collector_integer" "collector"
    ##   .. ..$ last_review                   :List of 1
    ##   .. .. ..$ format: chr ""
    ##   .. .. ..- attr(*, "class")= chr  "collector_date" "collector"
    ##   .. ..$ reviews_per_month             : list()
    ##   .. .. ..- attr(*, "class")= chr  "collector_double" "collector"
    ##   .. ..$ calculated_host_listings_count: list()
    ##   .. .. ..- attr(*, "class")= chr  "collector_integer" "collector"
    ##   .. ..$ availability_365              : list()
    ##   .. .. ..- attr(*, "class")= chr  "collector_integer" "collector"
    ##   ..$ default: list()
    ##   .. ..- attr(*, "class")= chr  "collector_guess" "collector"
    ##   ..- attr(*, "class")= chr "col_spec"
