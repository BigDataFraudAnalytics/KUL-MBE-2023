# Accounting fraud detection using machine learning

Programming code for 5 machine learning algorithms (i.e., Weighted Random Forest, Balanced Random Forest, UnderBagging, Basic Decision Tree, and Basic Random Forest) using 3 data (sub)sets (i.e, 28 raw accounting variables, 14 financial ratio variables, 28 raw accounting and 14 financial ratio variables). These algorithms are build in the context of our Master's Thesis and are capable of detecing accounting fraud in publicly traded U.S. firms by using readibly available financial statement data. We evaluate the performance of our models using three metrics: AUC-ROC, NDCG@k, and the AUC-PR.
## Authors

- Quintelier Quinten
- Vermeulen Emiel


## Necessary libraries

To use the algorithms, first make sure you have installed the following required packages:

- numpy
- pandas
- scikit-learn
- scikit-optimize

```bash
  pip install numpy pandas scikit-learn scikit-optimize
```


## Running
Each zipfile is a self-contained package that includes the runcode, tuning code, data_reader function, evaluate function, and output file required to reproduce our research results for a specific algorithm, simply download the zipfile for the desired algorithm, extract it, and open the folder in your preferred IDE.
## Dataset description
The file "data_FraudDetection_JAR2020.csv" is the dataset used for each algorithm, which contains the fraud labels, feature variables (i.e., 28 raw accounting and 14 financial ratio variables), and identifier variables (e.g., fyear, gvkey, and p_aaer). The variable "misstate" is the fraud label (1 denotes fraud, and 0 denotes non-fraud). The 28 raw accounting data items are: act, ap, at, ceq, che, cogs, csho, dlc, dltis, dltt, dp, ib, invt, ivao, ivst, lct, lt, ni, ppegt, pstk, re, rect, sale, sstk, txp, txt, xint, prcc_f. The 14 financial ratios are: dch_wc, ch_rsst, dch_rec, dch_inv, soft_assets, ch_cs, ch_cm, ch_roa, issue, bm, dpi, reoa, EBIT, ch_fcf. The variable "p_aaer" is used for handling the serial fraud issue.

The description of the 28 raw accounting variables are as follows:
- act -- Current Assets, Total
- ap -- Account Payable, Trade
- at -- Assets, Total
- ceq - -Common/Ordinary Equity, Total
- che -- Cash and Short-Term Investments
- cogs -- Cost of Goods Sold
- csho -- Common Shares Outstanding
- dlc -- Debt in Current Liabilities, Total
- dltis -- Long-Term Debt Issuance
- dltt -- Long-Term Debt, Total
- dp -- Depreciation and Amortization
- ib -- Income Before Extraordinary Items
- invt -- Inventories, Total
- ivao -- Investment and Advances, Other
- ivst -- Short-Term Investments, Total
- lct -- Current Liabilities, Total
- lt -- Liabilities, Total
- ni -- Net Income (Loss)
- ppegt -- Property, Plant and Equipment, Total
- pstk -- Preferred/Preference Stock (Capital), Total
- re -- Retained Earnings
- rect -- Receivables, Total
- sale -- Sales/Turnover (Net)
- sstk -- Sale of Common and Preferred Stock
- txp -- Income Taxes Payable
- txt -- Income Taxes, Total
- xint -- Interest and Related Expense, Total
- prcc_f -- Price Close, Annual, Fiscal

The description of the 14 financial ratio variables are as follows:
- dch_wc -- WC accruals
- ch_rsst -- RSST accruals
- dch_rec -- Change in receivables
- dch_inv -- Change in inventory
- soft_assset -- % Soft assets
- dpi -- Depreciation index
- ch_cs -- Change in cash sales
- ch_cm -- Change in cash margin
- ch_roa -- Change in return on assets
- ch_fcf -- Change in free cash flows
- reoa -- Retained earnings over total assets
- EBIT -- Earnings before interest and taxes over total assets
- issue -- Actual issuance
- bm -- Book-to-market
