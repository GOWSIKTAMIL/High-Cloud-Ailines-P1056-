# Objective

The objective of this project is to analyze airline operational performance using flight, passenger, route, and airline-related metrics. This dashboard helps identify trends in passenger load, flight volume, route efficiency, and carrier contribution, enabling data-driven decision-making to improve revenue optimization and operational planning.

# Project Highlights

This analysis mainly focuses on:

Flight Volume Trends

Passenger Load & Seat Availability

Load Factor Efficiency

Top Performing Routes

Monthly & Seasonal Flight Performance

Carrier-wise Passenger Contribution

Weekday vs Weekend Travel Patterns

These insights help identify performance gaps, travel demand peaks, and optimize fleet utilization.

# Dashboard Visualization

<img width="1543" height="699" alt="image" src="https://github.com/user-attachments/assets/a345775f-e9d7-4a9a-8e52-269df3199a4b" />

The dashboard combines KPIs, bar charts, line graphs, donut charts, and slicers for flexible filtering. Filters include Year, Quarter, Month, Week Type, Origin City, State, Country, and Carrier Name for dynamic analysis.

# Dashboard Insights
🔹 Top KPIs

Total Flights: 110,851

Total Passengers: 18,702,2609

Available Seats: 243,534,311

Load Factor: 0.7679 (≈ 77%)

These KPIs provide an instant overview of operational efficiency and passenger occupancy.

# Monthly Flight Performance

The line chart shows flight volume trends by month.

Performance gradually improves from February and peaks in June–July, showing higher demand during summer travel periods.

# Passenger Engagement by Month

Bar chart displays monthly passenger percentage growth, highlighting:

Highest engagement in February (19.60%) and January (18.92%)

Passenger engagement drops during off-peak travel months.

# Flights by Origin City

Cities like Washington, DC – Atlanta, GA, and Minneapolis, MN – Chicago, IL show higher flight activity, highlighting strongly connected routes.

# Weekday vs Weekend Travel

Donut chart shows:

71.21% Weekday flights

28.79% Weekend flights

Indicates higher business travel demand during weekdays.

# Carrier-Wise Passenger Contribution

The carrier bar chart shows:

Southwest Airlines Co. and Delta Air Lines Inc. have the highest passenger counts.

Smaller carriers show lower engagement—highlighting potential focus areas.

# DAX Formulas Used 
TotalFlights = COUNT(Flights[FlightID])

TotalPassengers = SUM(Flights[PassengerCount])

AvailableSeats = SUM(Flights[SeatCapacity])

LoadFactor = DIVIDE(
    SUM(Flights[PassengerCount]),
    SUM(Flights[SeatCapacity]),
    0
)

WeekdayFlights = CALCULATE(
    COUNT(Flights[FlightID]),
    KEEPFILTERS(Flights[Week_Type] = "Weekday")
)

WeekendFlights = CALCULATE(
    COUNT(Flights[FlightID]),
    KEEPFILTERS(Flights[Week_Type] = "Weekend")
)


(These formulas may be adapted based on your actual dataset and field names.)

# Conclusion & Recommendations

✔ Increase operations and capacity for high-demand months (June–July).
✔ Enhance route performance for top city pairs (e.g., ATL–DC, CHI–NY).
✔ Promote weekend travel offers to boost low occupancy days.
✔ Collaborate with top-performing carriers to drive more passenger movement.
✔ Identify low-performing carriers and provide operational support.
