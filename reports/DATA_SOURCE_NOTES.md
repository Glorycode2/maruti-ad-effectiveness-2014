# Data Source Notes

## Provenance

This dataset was digitized from a structured questionnaire survey originally
conducted at the Varun Motors (Maruti Suzuki) dealership in Visakhapatnam.

- **Sample size:** 100 respondents
- **Sampling technique:** Simple random sampling
- **Study area:** Visakhapatnam (Varun Motors)
- **Study period:** 12 May 2014 – 5 July 2014
- **Instrument:** Structured questionnaire (18 questions), personal interview, close observation
- **Original format:** Word document containing one frequency table per question
  (category-level counts and percentages, not individual respondent records)

This is **historical data (2014)**. It is presented and analyzed as such, no
dates, figures, or company details have been altered to appear current. Any
findings here describe customer perception in 2014, not present-day conditions.

## Known limitations

1. **Aggregate-only data.** The source document provides only summary frequency
   tables per question ("38% of respondents chose Theme & Concept"). No
   individual-level (row-per-respondent) records exist in the source. This
   means cross-tabulation across questions for the *same* respondent ("do higher-income respondents rate ads more positively?") is not possible
   with this data. Analysis here is limited to per-question distributions and
   between-question comparisons at the aggregate level.

2. **Arithmetic error in Q15 (source document).** The five response categories
   for "Which media would be most helpful for getting information about
   Maruti Suzuki?" sum to 110 respondents (15+20+25+35+15), while the source
   table's own "Total" row states 100. This inconsistency exists in the
   original 2014 document and has been preserved as-is rather than silently
   corrected, since we cannot know which individual values were mis-recorded.
   It is flagged here and should be noted wherever Q15 is presented.

3. **Typo in Q5 narrative text.** The Q5 table reports 54% Yes / 46% No
   (consistent, sums to 100). The accompanying interpretation paragraph in the
   source document states "45%" instead of 46%, a one-character transcription
   slip. The table values (54/46) are treated as authoritative.

4. **Near-duplicate question (Q12 / Q16).** "What do you think about Maruti
   Suzuki ads?" (Q12) and "What is your opinion about advertisements of Maruti
   Suzuki?" (Q16) are worded almost identically and report identical results
   in the source. This is most likely a copy-paste duplication in the original
   report rather than two independent survey items. Both are preserved in the
   raw data for transparency, but should be treated as one data point (not two)
   during analysis to avoid double-counting this finding.

## File

`survey_2014_aggregated.csv` — tidy format, one row per (question, response
category): `question_id, question_text, response_category, respondent_count, percent`
