---
title       : Comparing Mortgage Rates
subtitle    : What's the points?
author      : Eileen CM
job         : Developing Data Products MOOC
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : [mathjax]            # {mathjax, quiz, bootstrap}
logo        : savings.png
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

Many mortgage lenders will allow you to buy down or lower your interest rate by
paying "points" at the beginning of your loan.  
 
  
   
* 1 point = 1% of your mortgage amount
* Some lenders may only require a fraction of a point
* It requires more money at settlement, but gives you lower monthly house notes
* Points are tax deductible

---

The main question:
##  Do the points lower your rates enough?  
 
 
That will depend on several factors:
 
>  * how much lower the new rate is
>  * the term (length) of your mortgage
>  * how long you will stay in the house
>  * the opportunity cost of your money - your lost earnings from paying the points
 
  
   
> The Mortgage Comparison app allows you to enter all other these variables.

---

The Mortgage Comparison shiny app shows the monthly payment for each interest rate
and a chart has a red line showing the difference over time.  The red line eventually hits zero, and after time it would be cheaper to pay points up front.

The server.r uses formulas from Interest Theory.  Your monthly payment will be:

$$\frac{mortgage-amount}{\frac{1-v^n}{\frac{i}{12}}}$$ where $$v^n=\frac{1}{(1+\frac{i}{12})^n}$$
and n is the number of months that the loan lasts.

A mortgage of $200,000 at 4% over 30 years will have a monthly payment of

```
## [1] "$954.83"
```

---

So when it comes time to buy, remember my app.
 
  
  
You'll find it at: http://eileencm.shinyapps.io/shinyapp_attempt
 
 
Now all you have to do is find a house!
 
(That's a whole 'nother problem.)

---

