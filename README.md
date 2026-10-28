# IndabaX-Eswatini-VAT-File-Pay-Predictive-Analytics-Challenge-by-IndabaX
About
The data covers VAT returns filed with the Eswatini Revenue Service. Each row is one VAT return, meaning one taxpayer for one filing period.

Train.csv has two target columns:

Column	Classes	                                 Meaning
FILING	ON_TIME, LATE_1_7, LATE_8_30, LATE_31PLUS	Days after the due date that the return was filed
PAYMENT	NONE_DUE, ON_TIME, LATE_1_30, LATE_31PLUS	NONE_DUE means nothing was owed (a nil or refund return); 
                                                otherwise, days after the due date that payment was made
A small number of FILING and PAYMENT values in Train are blank because the outcome was not yet known on 1 July 2025.

Columns in both Train and Test

ID: unique return identifier
Taxpayer_ID: taxpayer identifier, the same across Train and Test
Class, Division, Sector: nature of business
Filing Frequency: Monthly, Quarterly or Annually
Taxpayer Type: individual or non-individual
Segment: taxpayer size segment
Organization Type: type of organisation
Start Date, End Date: the tax period
Obligation Due Date: the date the return and payment were due
Columns in Train only

Return figures: I_O_Ratio, Zero_rated_IO, Exempt_IO, Effective_Output, Zero_Rated_Share, Exempt_Shares, VAT Refundable/Payable, Refund_Position, NIL_FILER
Dates: Filing date, Payment Date
These only exist once a return has been filed, so they are not available for Test. Use them to describe a taxpayer's earlier returns, for example their previous VAT payable or how often they file nil returns.

Submit one row per Test ID, with a probability between 0 and 1 in each of these eight columns:

FILING_ON_TIME, FILING_LATE_1
