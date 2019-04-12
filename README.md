

# **Whats-Your-Ticket-Worth?**
What are the features of a concert event that may affect a ticket's resale price? 

I built a linear regression model using 13 features with 1254 data points. My data came from SeatGeek and Last.FM API. My label is the average listed price based on what other people were selling at on SeatGeek.

**Motivation**
I am curious about how ticket scalpers decide what price they put their tickets at on the market. I wonder if it's because the aritst is popular, the venue is famous, or whether the event is on a weekend. 

*Limitations*
I do not have historical data of successfully sold ticket prices. My data is also pulled one time for consistency across price, dates, and upcoming events.

**Data**
Features:
Highest Price (of ticket)
Lowest Price
Event Genre
Time of Day
Day / Month
Weekend/Weekday
Ticket Listing Count
Venue Score (based on estimated sales value of secondary ticket market)

- Pop by far has a lot more around 600.
- The rest of the genres hover <100.
![Image](file:///Users/chrischung/Desktop/Screen%20Shot%202019-04-12%20at%202.28.55%20PM.png)

**Model**
![Image](file:///Users/chrischung/Desktop/Plot%20actual%20vs%20predicted.png)
