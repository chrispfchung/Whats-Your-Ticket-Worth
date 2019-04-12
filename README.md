# **Whats-Your-Ticket-Worth?**
What are the features of a concert event that may affect a ticket's resale price? 

I built a linear regression model using 13 features with 1254 data points. My data came from SeatGeek and Last.FM API. My label is the average listed price based on what other people were selling at on SeatGeek.

**Motivation**<br>
I am curious about how ticket scalpers decide what price they put their tickets at on the market. I wonder if it's because the aritst is popular, the venue is famous, or whether the event is on a weekend. 

*Limitations*<br>
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

**Label**
*I took the average of the listed prices*
![Image](https://github.com/chrispfchung/Whats-Your-Ticket-Worth/blob/master/Images/Ticketmaster%20Resell%20Prices.png)

*EDA*<br>
- Pop by far has a lot more around 600.
- The rest of the genres hover <100.

![Image](https://github.com/chrispfchung/Whats-Your-Ticket-Worth/blob/master/Images/Event%20Genres.png)
![Image](https://github.com/chrispfchung/Whats-Your-Ticket-Worth/blob/master/Images/Event%20Regions.png)
![Image](https://github.com/chrispfchung/Whats-Your-Ticket-Worth/blob/master/Images/Month%20of%20Event.png)
![Image](https://github.com/chrispfchung/Whats-Your-Ticket-Worth/blob/master/Images/Start%20time%20of%20events.png)
![Image](https://github.com/chrispfchung/Whats-Your-Ticket-Worth/blob/master/Images/Average%20Price.png)

**Model**

![Image](https://github.com/chrispfchung/Whats-Your-Ticket-Worth/blob/master/Images/Reg%20Plot.png)


![Image](https://github.com/chrispfchung/Whats-Your-Ticket-Worth/blob/master/Images/Bottom%205%20coefficients.png)
![Image](https://github.com/chrispfchung/Whats-Your-Ticket-Worth/blob/master/Images/Mid%205%20coefficients.png)
![Image](https://github.com/chrispfchung/Whats-Your-Ticket-Worth/blob/master/Images/Top%205%20coefficients.png)

Findings:<br>
- The month of November has the greatest impact on the price, with the event coefficient 144 while the next highest month is at 28.
- Venue score is the highest coefficient but the value is between 0 and 1. In other words, price for venue score increase by 2.1 per .01. 
- Small capacity venues, events starting at 5 or 10, and events in August yield higher values.
- Events starting at 11, in a large venue, in October, yield exceptionally lower prices.
