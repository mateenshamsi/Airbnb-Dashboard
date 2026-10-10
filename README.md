# Airbnb-Dashboard

A Power BI project exploring Airbnb listings, pricing, guest ratings, review activity, and host trust indicators across cities. The report brings these topics together in three pages to help users compare markets and understand patterns in the dataset.

## Dashboard Pages

### Overview
- Summary cards for listings and other key dataset fields.
- A time-based comparison of listings by host joining year (`host_since`).
- Room-type breakdowns covering entire places, private rooms, shared rooms, and hotel rooms.

### Rating
- City-level listing distribution, split by Superhost status.
- Cumulative listing share to show how listings are concentrated across cities.
- Average price comparisons by room type.
- Average guest ratings by city.

### Reviews
- Monthly review share across cities.
- Review frequency by reviewer, with a cumulative percentage chart.
- Host trust indicators based on identity verification and profile-picture availability.

## Questions Explored

- Which cities account for the largest share of listings?
- How do average prices differ across room types?
- How do guest ratings compare between cities?
- How does each city's share of reviews vary by month?
- How frequently do reviewers contribute reviews?
- What proportion of hosts have identity verification and a profile picture?

Review activity describes engagement in the available data; it does not directly measure bookings or occupancy. The `host_since` field represents when a host joined Airbnb, rather than when an individual listing was created.

## Tools and Techniques

- **Power BI Desktop** for report design and visualization.
- **Power Query** for importing CSV files, promoting headers, and setting data types.
- **DAX** for listing counts, distinct host and reviewer counts, average prices and ratings, city rankings, cumulative percentages, and trust indicators.
- **Data modeling** to connect listings and reviews through `listing_id`.

## Data Model

| Table | Contents |
| --- | --- |
| `Listings` | Listing and host identifiers, city and neighbourhood, property and room types, price, guest ratings, and host trust attributes. |
| `Reviews` | Listing identifiers, review identifiers, review dates, and reviewer identifiers. |

## Repository Contents

- [Airbnb dashboard.pbit](Airbnb%20dashboard.pbit) — Power BI template containing the report layout, queries, model definition, and calculations.
- `README.md` — Project overview and setup instructions.

## How to Open the Dashboard

1. Download `Airbnb dashboard.pbit` from this repository.
2. Open the template in Power BI Desktop.
3. Provide the matching `Listings.csv` and `Reviews.csv` source files.
4. In **Transform data**, update the **Source** step in each query to point to your local CSV file. The template currently references files in `D:\Airbnb+Data\Airbnb Data\`.
5. Select **Close & Apply** to load the data, then explore the **Overview**, **Rating**, and **Reviews** pages.

**Data availability:** The source CSV files are not included in this repository. A `.pbit` template contains report and model definitions without imported data, so the matching source files are required to populate the visuals. Results depend on the data loaded.

## Author

[Mateen Shamsi](https://github.com/mateenshamsi)
