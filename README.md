# Incoming Bills Dashboard

Invoice volume monitoring dashboard for Wasteology.

## Live URL

After enabling GitHub Pages:  
`https://wasteology.github.io/incoming-bills-dashboard/`

## Setup

1. Create repo `incoming-bills-dashboard`
2. Upload `index.html` to root
3. Go to Settings → Pages → Source: Deploy from branch (main)
4. Wait ~1 min, access at URL above

## Usage

1. Open the dashboard URL
2. Load 3 CSV files:
   - **Daily MTD** - daily invoice counts
   - **Monthly Trend** - monthly counts by vendor
   - **Alerts** - vendors below 25% threshold

## CSV Formats

### daily_mtd.csv
```
day,count,isWeekend
12/1,245,true
12/2,312,false
```

### monthly_trend.csv
```
month,vendor,count
Jan,All Vendors,12450
Jan,Waste Management,2450
Feb,All Vendors,13200
```

### alerts.csv
```
vendor,priorMonth,priorCount,currentMonth,currentCount,pct
ABC Disposal,Oct,120,Nov,15,12.5
```

## Sample Files

Use the `sample_*.csv` files included to test the dashboard.

## Refreshing Data

1. Export new CSVs from SQL Server
2. Reload dashboard page
3. Load updated CSV files
