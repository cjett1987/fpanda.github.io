


## Data Dictionary

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
| Numeric   | Nth Take       | Take Rate                 | The percent of Program Customers that take delivery of the next Program order after the first order of a Diet Cycle. Take Rates are calculated for Program-only orders, or for all autoship orders. |                                                                                                                                                                                                         |                                                                       | NSDATAMART | 

## Customizing

### Configuration variables

Cayman will respect the following variables, if set in your site's `_config.yml`:

```yml
title: [The title of your site]
description: [A short description of your site's purpose]
```

Additionally, you may choose to set the following optional variables:

```yml
show_downloads: ["true" or "false" to indicate whether to provide a download URL]
google_analytics: [Your Google Analytics tracking ID]
```

### Stylesheet

If you'd like to add your own custom styles:

1. Create a file called `/assets/css/style.scss` in your site
2. Add the following content to the top of the file, exactly as shown:
    ```scss
    ---
    ---
    @import "{{ site.theme }}";
    ```
3. Add any custom CSS (or Sass, including imports) you'd like immediately after the `@import` line

*Note: If you'd like to change the theme's Sass variables, you must set new values before the `@import` line in your stylesheet.*

### Layouts

If you'd like to change the theme's HTML layout:

1. [Copy the original template](https://github.com/pages-themes/cayman/blob/master/_layouts/default.html) from the theme's repository<br />(*Pro-tip: click "raw" to make copying easier*)
2. Create a file called `/_layouts/default.html` in your site
3. Paste the default layout content copied in the first step
4. Customize the layout as you'd like

### Overriding GitHub-generated URLs

Templates often rely on URLs supplied by GitHub such as links to your repository or links to download your project. If you'd like to override one or more default URLs:

1. Look at [the template source](https://github.com/pages-themes/cayman/blob/master/_layouts/default.html) to determine the name of the variable. It will be in the form of `{{ site.github.zip_url }}`.
2. Specify the URL that you'd like the template to use in your site's `_config.yml`. For example, if the variable was `site.github.url`, you'd add the following:
    ```yml
    github:
      zip_url: http://example.com/download.zip
      another_url: another value
    ```
3. When your site is built, Jekyll will use the URL you specified, rather than the default one provided by GitHub.

*Note: You must remove the `site.` prefix, and each variable name (after the `github.`) should be indent with two space below `github:`.*

For more information, see [the Jekyll variables documentation](https://jekyllrb.com/docs/variables/).

## Roadmap

See the [open issues](https://github.com/pages-themes/cayman/issues) for a list of proposed features (and known issues).

## Project philosophy

The Cayman theme is intended to make it quick and easy for GitHub Pages users to create their first (or 100th) website. The theme should meet the vast majority of users' needs out of the box, erring on the side of simplicity rather than flexibility, and provide users the opportunity to opt-in to additional complexity if they have specific needs or wish to further customize their experience (such as adding custom CSS or modifying the default layout). It should also look great, but that goes without saying.

## Contributing

Interested in contributing to Cayman? We'd love your help. Cayman is an open source project, built one contribution at a time by users like you. See [the CONTRIBUTING file](docs/CONTRIBUTING.md) for instructions on how to contribute.

### Previewing the theme locally

If you'd like to preview the theme locally (for example, in the process of proposing a change):

1. Clone down the theme's repository (`git clone https://github.com/pages-themes/cayman`)
2. `cd` into the theme's directory
3. Run `script/bootstrap` to install the necessary dependencies
4. Run `bundle exec jekyll serve` to start the preview server
5. Visit [`localhost:4000`](http://localhost:4000) in your browser to preview the theme

### Running tests

The theme contains a minimal test suite, to ensure a site with the theme would build successfully. To run the tests, simply run `script/cibuild`. You'll need to run `script/bootstrap` once before the test script will work.
