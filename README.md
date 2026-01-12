Earthquake Activity Analysis in the Philippines (PHIVOLCS Data)
Tools Used
Excel – data cleaning and feature engineering
Tableau – exploratory analysis and interactive dashboards

1. Project Background & Objective

The Philippines lies along the Pacific Ring of Fire and experiences frequent seismic activity.
This project analyzes a PHIVOLCS earthquake catalog containing tens of thousands of recorded seismic events to answer the following questions:

How severe are earthquakes in the Philippines overall?

Which regions experience the most frequent and severe activity?

When do earthquake surges occur?

What factors best predict whether an earthquake is felt by the population?

The goal is to translate raw seismic data into actionable insights that support monitoring, preparedness, and risk awareness.

2. Dataset Overview

The dataset includes:

Timestamp (DateTimePH)

Latitude & Longitude

Depth (km)

Magnitude

Region / General Location

Felt indicator (Yes / No)

Each row represents one earthquake event, making the dataset suitable for event-based trend and frequency analysis 

Julius AI_ Chat with Your Data …

.

3. Data Preparation & Feature Engineering

To make the data analysis-ready, the following transformations were applied:

Extracted Date, Month, Week, and Hour from timestamps

Created Magnitude Classes (Micro → Major) based on standard seismic definitions

Categorized Depth into Shallow, Intermediate, and Deep

Flagged Felt Earthquakes using the reported indicator

These derived fields enabled time-based aggregation, severity analysis, and geographic comparisons.

4. Key Insights & Findings
4.1 Earthquake Severity Distribution

Insight
The earthquake catalog is overwhelmingly dominated by low-magnitude events.

~78.5% of earthquakes are Micro (<3.0)

~17.4% are Minor (3.0–3.9)

Only a very small fraction reach M ≥ 6.0 

Julius AI_ Chat with Your Data …

Implication
Dashboards and alerts should emphasize frequency and clustering of small events, while treating large earthquakes as high-impact outliers rather than the norm.

4.2 Regional Concentration of Earthquakes

Insight
Seismic activity is not evenly distributed geographically.

Region XIII has the highest number of recorded events

Region XI stands out for having both high event counts and higher magnitudes

Some regions experience fewer events but higher intensity outliers 

Julius AI_ Chat with Your Data …

Implication
Risk assessment should distinguish between:

Most frequent regions and

Most severe regions

A simple risk metric such as event count × high-percentile magnitude can help prioritize monitoring.

4.3 Temporal Trends & Earthquake Surges

Insight
Earthquake activity occurs in distinct temporal spikes rather than evenly over time.

The largest monthly surge occurred in October 2025, with a +315% month-over-month increase

The largest weekly spike occurred in early December 2023

Rolling 7-day analysis highlights short-term seismic swarms 

Julius AI_ Chat with Your Data …

Implication

Monthly aggregation is ideal for detecting regime changes

Weekly and daily views are better suited for investigating short-term clusters and aftershock sequences

4.4 Magnitude as a Predictor of “Felt” Earthquakes

Insight
Magnitude is a strong predictor of whether an earthquake is felt by people.

Mean magnitude (Felt = Yes): 3.54

Mean magnitude (Felt = No): 2.17

Probability of being felt rises sharply at ~2.5–3.0 magnitude

Events ≥3.0 are almost always reported as felt 

Julius AI_ Chat with Your Data …

Implication
Magnitude alone can be used as a simple, interpretable predictor for felt reports, making it useful for early public communication and alert systems.

4.5 Magnitude vs Depth Relationship

Insight
There is almost no linear relationship between magnitude and depth.

Pearson correlation ≈ 0.047 

Julius AI_ Chat with Your Data …

Implication
Depth should not be treated as a direct predictor of magnitude. Instead, depth is better used:

As a categorical risk modifier

Or analyzed within specific regions or tectonic contexts

5. Tableau Dashboard Design

An interactive Tableau dashboard was created featuring:

Monthly earthquake trends

Regional rankings by event count

Magnitude distribution

Depth distribution

Hour-of-day activity

Magnitude vs Felt boxplots

Interactive geographic map colored by magnitude class 

Julius AI_ Chat with Your Data …

The dashboard enables drill-down analysis from national trends to regional and event-level detail.

6. Key Takeaways

The Philippine earthquake landscape is dominated by frequent low-magnitude events

A small number of regions account for a disproportionately high share of activity

Seismic activity occurs in bursts, not steady patterns

Magnitude is the clearest indicator of public impact

Depth plays a secondary, non-linear role

7. What This Project Demonstrates

This project showcases my ability to:

Clean and engineer real-world datasets

Apply domain knowledge to analysis

Use Tableau for insight-driven storytelling

Validate findings using statistical summaries

Communicate results clearly to non-technical audiences
