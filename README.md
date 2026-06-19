# Maruti Suzuki Advertising Effectiveness at Varun Motors, Visakhapatnam (2014)

A re-analysis of a real customer survey on how advertising influenced car-buying decisions at a Maruti Suzuki dealership. Cleaned, explored, and visualized using Python and pandas.

## Problem Statement

Dealerships and car manufacturers spend heavily on advertising, but not all of that spend translates into customer attention or sales. This project asks three questions a marketing team would actually care about: which media channels reach customers, what makes an ad memorable or persuasive, and whether advertising at the *dealership* level performs differently from advertising done by the *company* as a whole. The original study was conducted at Varun Motors, a Maruti Suzuki dealership in Visakhapatnam, India, to answer exactly these questions.

## Data Source

This dataset comes from a structured questionnaire survey of 100 customers, conducted at Varun Motors between May and July 2014, using simple random sampling. It covers 18 questions from demographics, ad awareness, media preferences, to customer satisfaction.

This is real, historical data. It was originally recorded as aggregate frequency tables (e.g 38 of 100 respondents picked X) inside a Word document, not as individual-level survey records. I digitized those tables into a clean CSV for analysis. Full provenance, along with two data quality issues I found in the original source (and chose to document rather than silently fix), are in (DATA_SOURCE_NOTES.md).

## Methodology

Everything was done in Python (pandas + matplotlib) in a Google Colab notebook. See (maruti_ad_analysis.ipynb).

Steps:
1. Loaded the digitized CSV and checked its shape and structure
2. Filtered individual questions out of the combined table to inspect them one at a time
3. Sorted response categories to identify the top answer per question
4. Pivoted pairs of related questions side-by-side to compare them directly 
5. Charted everything as bar charts to make the comparisons readable at a glance

## Key Findings

**Varun Motors' own advertising is rated noticeably better than Maruti Suzuki's company-wide advertising.** 50% of respondents rated Varun Motors' dealership-level ad efforts as Excellent or Good, compared to only 30% who rated Maruti Suzuki's general advertising the same way. On the negative end, only 23% rated the dealership's ads poorly, versus 45% for the company-wide ads. A meaningful gap between how the same customers feel about local versus national advertising from the same brand.

**Internet is the clear leader across two independent questions.** It came out on top both for "which media gets your attention" (30%) and "which media is most helpful for getting information" (35%). Two differently-worded questions agreeing on the same answer makes this a more reliable signal than either one alone.

**TV advertising underperforms at every stage.** Only 32% of respondents had even seen a Maruti Suzuki TV ad. Only 28% said it influenced their buying decision, meaning TV's actual influence on the full sample is even smaller than the awareness number suggests.

**Brand ambassador campaigns and radio jingles both land well.** 65% said ambassador campaigns influenced their buying decision, and 68% recalled hearing Maruti Suzuki's radio jingles, both notably higher than recall for traditional print or TV ads.

**Customers care about concept over discounts.** When asked what they like in an advertisement, 38% picked "theme and concept", more than picked "offers and discounts" (20%). People remember a good idea more than a good deal.

## Limitations

This data is from 2014 and describes customer sentiment at that point in time, not today's. It's also aggregate-only. I have per-question totals, not individual respondent records, so I can't check things like whether higher-income respondents responded differently from lower-income ones across questions. Two minor inconsistencies in the original source data (one question's category counts don't sum to its stated total, and one question appears to have been asked twice with identical results) are documented in the data source notes rather than corrected, since I have no way to know which underlying numbers were actually mis-recorded.

## Conclusions & Next Steps

The clearest takeaway is that dealership-level, localized advertising effort seems to resonate more with customers than broad company campaigns, which is a useful insight for any dealership deciding where to put its own marketing budget versus relying on what the parent company provides. A natural next step would be repeating this survey today to see whether the same patterns (Internet's dominance, TV's weak performance, the local-vs-national satisfaction gap) still hold twelve years later, or whether the media landscape has shifted enough to change the answer.
