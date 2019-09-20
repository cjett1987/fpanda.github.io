


## Data Dictionary

<form><input type="text" name="search" value="" id="Abbreviation" placeholder="Search on that table" autofocus />


| Data Type | Abbreviation   | Name                      | Definition                                                                                                                                                                                          | Notes                                                                                                                                                                                                   | Equation                                                              | Database   | 
|-----------|----------------|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|------------| 
| Numeric   | CAC            | Customer Acquisition Cost | Media cost divided by Number of First Time Customers for specified period.                                                                                                                          |  Includes all New Customers, including Program and ALC                                                                                                                                                  | Total Media spend divided by total FTO (spend/FTO)                    | NSDATAMART | 
| Numeric   | FTO            | First Time Order          | First Order from a de-duplicated Customer, no matter if it is Program or ALC                                                                                                                        |                                                                                                                                                                                                         |                                                                       | NSDATAMART | 
| Numeric   | nonFTO         | Non First Time Order      | Not the First Order from a de-duplicated Customer, no matter if it is Program or ALC                                                                                                                |                                                                                                                                                                                                         |                                                                       | NSDATAMART | 
| Numeric   | CPO            | Cost Per Order            |  Media Cost divided by number of First Time and Restart Program orders.                                                                                                                             | Any order placed by a Customer is included. For example, if a Customer Orders some products as an ALC order while on a Program or other Autoship, this ALC Order counts as part of the CPO calculation. | Total Media spend divided by total Program Starts (spend/prog_starts) | NSDATAMART | 
| Numeric   | FCST           | Forecast                  |                                                                                                                                                                                                     |                                                                                                                                                                                                         |                                                                       | NSDATAMART | 
| Numeric   | UPD FCST       | Updated Forecast          |                                                                                                                                                                                                     |                                                                                                                                                                                                         |                                                                       | NSDATAMART | 
| Numeric   | PROG STARTS    | Program Starts            | The number of Customers that have started an Autoship sequence within a defined time period.                                                                                                        |                                                                                                                                                                                                         |                                                                       | NSDATAMART | 
| Numeric   | Spend          | Media Spend               | The amount of money spent directly on marketing media.                                                                                                                                              | Excludes creative and administrative expenses.                                                                                                                                                          |                                                                       | REPORTSDB  | 
| Numeric   | ASP            | Average Sales Price       | The average Revenue per Order for a specified period of time.                                                                                                                                       |                                                                                                                                                                                                         |                                                                       | NSDATAMART | 
| Numeric   | RPC            | Revenue per Customer      | The amount of Revenue per New Customer for 9 months from Shipment date.                                                                                                                             | Is calculated from Revenue.  Marketing usually uses the Revenue amount as the bases but may also use:Net Revenue, Net Net Revenue                                                                       |                                                                       | NSDATAMART | 
| Numeric   | COGS           | Cost of Goods Sold        | The cost  of the Product sold to a Customer.                                                                                                                                                        | COGS data is held in MAS500 and is not used to calculate Gross Profit at the Order level.                                                                                                               |                                                                       | NSDATAMART | 
| Varchar   | Channel        | Advertising Channel       | The method by which we expose consumers to  advertising.                                                                                                                                            | Advertising channels include TV (long-form and short-form), Web ads, social media, email, affiliates, blogs and newletters, search results, mobile apps, print media, direct mail, and SMS.             |                                                                       | NSDATAMART | 
| Numeric   | Rev            | Revenue                   | The amount of money that Nutrisystem actually received during a specific period.                                                                                                                    | Includes the discounted product price, shipping, handling, and sales tax. Does not include Cancelled Orders.                                                                                            |                                                                       | NSDATAMART | 
| Numeric   | NetRev         | Net Revenue               | Revenue minus Gift Card Adjustment during a specific period.                                                                                                                                        |                                                                                                                                                                                                         |                                                                       | NSDATAMART | 
| Numeric   | Gross Profit   | Gross Profit              | Revenue minus Cost of Goods Sold (COGS) on a FIFO basis.                                                                                                                                            |                                                                                                                                                                                                         |                                                                       | NSDATAMART | 
| Numeric   | Gift Card  Adj | Gift Card Adjustment      | The estimated and actual ratio of Nutrisystem Revenue to face-value of Gift cards that are purchased at a discount and presented for payment for products purchased from Nutrisystem.               |                                                                                                                                                                                                         |                                                                       | NSDATAMART | 
| Numeric   | LOS            | Length of Stay Finance    | The # of calculated days that a Customer paid for program orders from start to Program cancellation for a maximum of 9 months.                                                                      |                                                                                                                                                                                                         |                                                                       | NSDATAMART | 
| Numeric   | Nth Take       | Take Rate                 | The percent of Program Customers that take delivery of the next Program order after the first order of a Diet Cycle. Take Rates are calculated for Program-only orders, or for all autoship orders. |                                                                                                                                             

</form>
