# Hotel Pricing Intelligence for Amsterdam
## Data-driven detection of overpriced and underpriced hotels (Booking.com Case Study)

This project analyzes hotel pricing in Amsterdam using data collected from the Booking.com public API (via RapidAPI).
The goal is to understand what drives hotel prices and identify properties that appear overpriced or underpriced compared to the market.

The analysis combines price, star rating, review score, review count, and location to build a holistic mispricing detection framework.
The final output includes visual analysis, mispricing examples, and pricing recommendations.

## Project Overview

Hotels on Booking.com aim to balance competitive pricing with strong revenue performance.
However, mispriced hotels — either too high or too low — reduce visibility, harm conversion, and lower guest satisfaction.

This project helps answer:

✔ Which factors influence hotel pricing in Amsterdam?  
✔ Which hotels appear overpriced or underpriced compared to their peers?  
✔ How can pricing be improved to increase competitiveness and fairness?

## Data Source

Data was collected using the Booking.com Hotel Availability API (via RapidAPI).

Endpoints used:  
/searchDestination — Fetch destination ID for Amsterdam  
/searchHotels — Retrieve listings, prices, ratings, and location details

Data extracted:  
hotel_id, name  
priceBreakdown.grossPrice.value  
accuratePropertyClass (star rating)  
reviewScore, reviewCount  
latitude, longitude

Dataset size: 220 hotels (1-night stay, standard room for 2 people)

## Methods & Analysis Steps

The analysis follows a structured pipeline:

**1️. Price distribution by star category**  
Examines typical price ranges and identifies outliers.

**2️. Review score vs star rating**  
Evaluates guest satisfaction versus expected hotel class.

**3️. Price vs review score**  
Checks whether higher ratings correlate with higher prices.

**4️. Price vs review count**  
Shows how trust/popularity influence pricing stability.

**5️. Location-based pricing**  
Maps hotels across Amsterdam to identify premium and budget zones.

**6️. Mispricing detection**  
Hotels flagged as mispriced if they show:  
Price far outside category norms  
Weak review score or review count  
Location that does not justify pricing  
Or a combination of these signals

**7️. Pricing recommendations**

Clear, actionable adjustments for both overpriced and underpriced hotels.

## Key Findings
**1. Amsterdam is a mid–upper range hotel market**  
Most hotels fall into the $200–$400 price band.

**2. 3★ and 4★ hotels form the biggest group**  
They dominate the supply and are spread widely across the entire city.

**3. Star rating alone does not predict price**  
0★, 2★, 3★, and 4★ hotels all overlap in the $200–$500 mid-range.

**4. Review score better reflects real value**  
Some 0★ hotels score as highly as 5★  
1★ sometimes outrank 2★
➡ Review score is essential for validating price.

**5. Review count signals trust & popularity**  
High-trust hotels cluster predictably in the mid-market pricing band.

**6. Location is the strongest price driver**  
Premium clusters: Old Centre, Museum Quarter, De Pijp  
Mid-range hotels: widely spread across the city  
Budget hotels: outer districts + central hostels

**7. Mispricing exists on both extremes**   
Some 3★ hotels charge $1,800+ with weak reviews  
Some high-performing hotels are priced far below peers

## Recommendations
### For Overpriced Hotels

Reduce prices to category norms  
Avoid premium pricing until trust is established  
Align pricing with location quality  
Improve service, amenities, and visual presentation

### For Underpriced Hotels

Increase prices 10–30% toward peer median  
Use dynamic pricing for weekends & events  
Highlight strong reviews to justify higher pricing  
Raise prices gradually while monitoring conversion

## Tools & Technologies

Python  
Pandas (data cleaning & wrangling)  
Plotly (interactive visualizations)  
Mapbox (location maps)  
Jupyter Notebook  
Canva (presentation)

## Author

Anna Igumnova

Data Analyst — Pricing & Hospitality