# British Airways Data Science Job Simulation

My work for the [British Airways Data Science job simulation on Forage](https://www.theforage.com/). It has two tasks: estimating lounge demand at Heathrow Terminal 3, and predicting whether a customer will complete a booking.

**Certificate:** [View completion certificate](BritishAirways_Forage_Certificate.pdf)

| Task | What I did | Main result |
|---|---|---|
| [1. Lounge eligibility](task1-lounge-eligibility/) | Built a lookup table that estimates the share of passengers eligible for each BA lounge tier, by flight group | Haul type drives eligibility. Short-haul has a higher eligible share than long-haul. The lookup came within about 2% of actual eligible passengers across 10,000 flights |
| [2. Booking prediction](task2-booking-prediction/) | Cleaned the booking data, created new features, trained a Random Forest and explained which variables matter | ROC AUC about 0.80. Booking origin and route explain about three-quarters of the model's predictive power |

## Repository structure

```
├── data/                          # datasets go here (not included, see data/README.md)
├── task1-lounge-eligibility/
│   ├── lounge_eligibility_analysis.ipynb
│   ├── Lounge_Eligibility_Lookup_Task_1.xlsx   # submitted lookup table + justification
│   └── images/
└── task2-booking-prediction/
    ├── booking_prediction.ipynb
    ├── BA_Booking_Prediction_Summary.pptx      # submitted one-slide summary
    └── images/
```

## How to run

```bash
pip install -r requirements.txt
```

Download the two datasets from the simulation and put them in `data/` (see [data/README.md](data/README.md)). Then open the notebooks in Jupyter or Colab.

## Tools

Python, pandas, scikit-learn, matplotlib, Excel, PowerPoint
