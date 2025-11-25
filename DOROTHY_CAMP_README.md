# Dorothy Camp Kirby School - Suspension Data Dashboard

## Overview
This interactive HTML dashboard visualizes suspension data from Dorothy Camp Kirby School, a Juvenile Court School operated by Los Angeles County Office of Education. The dashboard helps school administrators explore patterns and disparities across different student populations from the 2017-18 through 2023-24 academic years.

## Files Included

### 1. Raw Data
- **ev2_DorothyCamp_DataSummary.csv** - Original raw data file containing suspension records

### 2. Data Processing
- **clean_dorothy_camp_data.py** - Python script that cleans and transforms the raw CSV data
  - Handles missing values (marked as "*" in original data)
  - Fixes encoding issues
  - Converts data types appropriately
  - Outputs clean JSON format

### 3. Clean Data
- **dorothy_camp_clean_data.json** - Cleaned data in JSON format, ready for visualization

### 4. Interactive Dashboard
- **dorothy_camp_dashboard.html** - Interactive HTML dashboard with visualizations

## How to Use

### Quick Start
1. Ensure all files are in the same directory
2. Open `dorothy_camp_dashboard.html` in a web browser
3. The dashboard will automatically load and display the data

### Dashboard Features

#### Key Metrics Cards
- **Total Enrollment**: Cumulative student enrollment across all years
- **Total Suspensions**: Total number of suspension incidents
- **Students Suspended**: Unduplicated count of students who received suspensions
- **Average Suspension Rate**: Mean suspension rate across all periods

#### Interactive Filters
- **Academic Year Filter**: Select a specific year or view all years
- **Student Group Filter**: Filter by specific student populations or view all groups

#### Visualizations

1. **Suspension Rate Trends Over Time**
   - Line chart showing how suspension rates changed across academic years
   - Identifies trends and patterns over time

2. **Suspension Rates by Student Group**
   - Horizontal bar chart comparing suspension rates across different student populations
   - Shows data for the latest academic year
   - Helps identify disparities between groups

3. **Suspension Types Breakdown**
   - Doughnut chart showing distribution of suspension reasons:
     - Violent incidents (with injury)
     - Violent incidents (no injury)
     - Weapons possession
     - Drug-related
     - Defiance only
     - Other reasons

4. **Enrollment vs Suspensions**
   - Dual-axis bar chart comparing enrollment numbers with total suspensions
   - Shows the relationship between school population and suspension incidents

5. **Gender Comparison**
   - Line chart tracking suspension rates by gender over time
   - Compares Male, Female, and Non-Binary students

#### Detailed Data Table
- Comprehensive table with all data points
- Rows highlight total statistics in yellow
- Fully responsive and scrollable

## Student Groups Tracked

The dashboard tracks suspension data for the following student populations:
- **English Learners (SE)**
- **Female (GF)**
- **Male (GM)**
- **Non-Binary Gender (GX)** - Available starting 2019-20
- **Foster Youth (SF)**
- **Homeless (SH)**
- **Socioeconomically Disadvantaged (SS)**
- **Students with Disabilities (SD)**
- **Total (TA)** - Overall school totals

## Data Privacy Note

Some data values are suppressed (displayed as "N/A") when student counts are too small to protect individual privacy, as required by educational data privacy regulations.

## Key Insights to Explore

Use this dashboard to investigate:
1. **Trend Analysis**: How have suspension rates changed over time?
2. **Equity Gaps**: Are certain student groups suspended at higher rates?
3. **Incident Types**: What types of incidents lead to most suspensions?
4. **Gender Disparities**: Are there differences in suspension rates by gender?
5. **Vulnerable Populations**: How do suspension rates compare for foster youth, homeless students, and students with disabilities?

## Technical Details

### Technologies Used
- **HTML5** - Page structure
- **CSS3** - Styling and responsive design
- **JavaScript (ES6)** - Data processing and interactivity
- **Chart.js 4.4.0** - Data visualization library

### Data Processing
The cleaning script handles:
- Conversion of "*" values to null (privacy-suppressed data)
- Fixing character encoding issues (e.g., "2019Ð20" → "2019-20")
- Converting numeric strings to integers/floats
- Standardizing field names to camelCase for JSON
- Filtering out "Not Reported" categories

### Browser Compatibility
- Modern browsers (Chrome, Firefox, Safari, Edge)
- Responsive design works on desktop, tablet, and mobile devices

## Regenerating Clean Data

If you need to re-process the data:

```bash
python3 clean_dorothy_camp_data.py
```

This will regenerate `dorothy_camp_clean_data.json` from the raw CSV file.

## School Context

**Dorothy Camp Kirby School** is a Juvenile Court School serving students in the Los Angeles County juvenile justice system. The unique context of a juvenile court school is important when interpreting this data:
- Students are typically in the school for shorter, variable durations
- The population faces significant challenges and trauma
- High suspension rates may reflect the complex needs of this population
- Data should be interpreted within the context of therapeutic and rehabilitative goals

## Questions This Dashboard Can Help Answer

1. Has the school made progress in reducing suspension rates over time?
2. Which student groups are disproportionately affected by suspensions?
3. What are the primary reasons students are being suspended?
4. How do suspension patterns differ between male and female students?
5. Are there years with notable changes that correlate with policy or program changes?
6. How do suspension rates for English Learners compare to the overall population?
7. What support might be needed for students with disabilities given their suspension rates?

## Support and Maintenance

For questions or issues with the dashboard, ensure:
1. All files are in the same directory
2. You're opening the HTML file in a modern web browser
3. The JSON data file is properly formatted
4. JavaScript is enabled in your browser

---

**Data Source**: California Department of Education - Suspension and Expulsion Data
**School**: Dorothy Camp Kirby School (School Code: 0121905/121905)
**District**: Los Angeles County Office of Education
**Data Years**: 2017-18 through 2023-24
