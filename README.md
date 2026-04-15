# COT Analysis

The Commitment of Traders report is a Commodity futures reported by the Commodity Futures Trading Commission (CFTC) based on position data supplied by reporting firms (Futures Commission Merchants(FCMs), clearing members, foreign brokers and exchanges).

## Simple Workflow

                ┌──────────────────────┐
                │  Input Configuration │
                │ (Symbols, Exchanges) │
                └──────────┬───────────┘
                           │
                           ▼
                ┌──────────────────────┐
                │   Data Ingestion     │
                │     (Reports)        │
                └──────────┬───────────┘
                           │
                           ▼
                ┌──────────────────────┐
                │ Data Synchronization │
                │(Date + Naming Align) │
                └──────────┬───────────┘
                           │
                           ▼
                ┌──────────────────────┐
                │ Data Transformation  │
                │ (Column Extraction)  │
                └──────────┬───────────┘
                           │
                           ▼
                ┌──────────────────────┐
                │ Feature Engineering  │
                │   (Net + Signals)    │
                └──────────┬───────────┘
                           │
                           ▼
                ┌──────────────────────┐
                │    Data Storage      │
                │       (CSV)          │
                └──────────┬───────────┘
                           │
                           ▼
                ┌──────────────────────┐
                │  Consumption Layer   │
                │ (Trading / Analysis) │
                └──────────────────────┘

## How to run code

```sh
# activate your virtual environment
virtualenv .venv
source .venv/bin/activate

# clone repository
git clone https://github.com/ngohamah/cot_analysis.git
cd cot_analysis

# run jupyter notebook (ensure you have jupyter installed)
jupyter lab
```

## Where to find data

You may find the extracted data only in the ```data/``` folder and the data + signal infos in the ```signal``` for the different symbols queried.


## References
- [The Commitments of Traders Bible Book by Stephen Briese on Amazon](https://www.amazon.com/Commitments-Traders-Bible-Insider-Intelligence/dp/0470178426)
- [Learn more on the COT Report on Investopedia](https://www.investopedia.com/terms/c/cot.asp)
- [COT_Reports package by NDelventhal](https://github.com/NDelventhal/cot_reports)

