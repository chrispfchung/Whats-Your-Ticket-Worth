# **Whats-Your-Ticket-Worth?**<br>
**Question**<br>
What are the features of a concert event that may affect a ticket's resale price? 
<br>
**What I did**<br>
I built a linear regression model using 13 features with 1254 data points. My data came from SeatGeek and Last.FM API. My label is the average listed price based on what other people were selling at on SeatGeek.

**Motivation**<br>
I am curious about how ticket scalpers decide what price they put their tickets at on the market. I wonder if it's because the aritst is popular, the venue is famous, or whether the event is on a weekend. 

*Limitations*<br>
I do not have historical data of successfully sold ticket prices. My data is also pulled one time for consistency across price, dates, and upcoming events.

**Data**<br>
Features:<br>
Highest Price (of ticket)<br>
Lowest Price<br>
Event Genre<br>
Time of Day<br>
Day / Month<br>
Weekend/Weekday<br>
Ticket Listing Count<br>
Venue Score (based on estimated sales value of secondary ticket market)<br>

**Label**<br>
*Average of the listed prices*<br>
![Image](https://github.com/chrispfchung/Whats-Your-Ticket-Worth/blob/master/Images/Ticketmaster%20Resell%20Prices.png)

*EDA*<br>
*Count of the top ten genres*<br>
- Pop by far has a lot more around 600.
- The rest of the genres hover <100.
![Image](https://github.com/chrispfchung/Whats-Your-Ticket-Worth/blob/master/Images/Event%20Genres.png)<br><br>


*Count by region*<br>
- NYC has a lot more events than Long Island. I grouped the event cities by region to prevent too many features.
![Image](https://github.com/chrispfchung/Whats-Your-Ticket-Worth/blob/master/Images/Event%20Regions.png)<br><br>

*Month of event* <br>
- Most of the events between Feb. and May. This could be because I collected data from February onwards to a year. Many events may not have been posted yet.
![Image](https://github.com/chrispfchung/Whats-Your-Ticket-Worth/blob/master/Images/Month%20of%20Event.png)<br><br>

*Average Price of event* <br>
- Prices are mostly between $100 and $300. 
![Image](https://github.com/chrispfchung/Whats-Your-Ticket-Worth/blob/master/Images/Average%20Price.png)<br><br>

**Model**<br>
- Final model<br>
![Image](https://github.com/chrispfchung/Whats-Your-Ticket-Worth/blob/master/Images/Reg%20Plot.png)<br><br>

*Bottom 5 Coefficients<br>
![Image](https://github.com/chrispfchung/Whats-Your-Ticket-Worth/blob/master/Images/Bottom%205%20coefficients%20updated.png)<br>

*Middle 5 Coefficients<br>
![Image](https://github.com/chrispfchung/Whats-Your-Ticket-Worth/blob/master/Images/Mid%205%20coefficients.png)<br>
*Top 5 Coefficients<br>
![Image](https://github.com/chrispfchung/Whats-Your-Ticket-Worth/blob/master/Images/Top%205%20coefficients.png)<br>

Findings:<br>
- The month of November has the highest coefficient with 144 with the event coefficient 144 while the next highest month is at 28.
However, there are very few events in November compared to the other months so the result should be taken with a grain of salt.
- Venue score is the highest coefficient but the value is between 0 and 1. In other words, price for venue score increase by 2.1 per .01. 
- Small capacity venues, events starting at 5 or 10, and events in August yield higher values.
- Events starting at 11, in a large venue, in October, yield exceptionally lower prices.
