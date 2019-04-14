# football-zero-inflated-poisson-fit
Fitting a zero inflated poisson distribution for an english premiership club that specializes in shooting blanks


This notebook is inspired by a book called [PREDICT FOOTBALL MATCHES](http://www.sportspredictionseries.com/) by David Langan.

Idea is to fit a number of discrete probability distributions, namely

- Poisson
- Zero Inflated Poisson
- Negative Binomial
- Geometric
- Uniform

to goal frequency data to predict english premiership football match scores from the 2012-2013 season. The data used starts at the beginning of the season to the 20th Jan 2013. 

Author uses Excel which proved quite nifty for the task especially its tool called Solver for estimating distribution parameters.

I successfully followed the book instructions via Excel since I wanted to see if someone who's not stats savvy(as I was at the time) can actually use what is in the book. As in the models did predict scores in Excel.

Fortunately and unfortunately, I found Excel a bit boring though given my current SQL skills and web developer history. Attempted to follow what's in the book using SQL but hit a road block when attempting to estimate the zero inflated poisson and negative binomial distributions. Also, noted that to fit these distributions given the relatively small dataset, it seems as if the least squares method is ideal compared to the maximum likelihood method which is a breeze say for a 1 parameter poisson distribution fit. 

Excel uses solver when estimating the zero inflated poisson/negative binomial distribution parameters. From what I can see, for one to fully grasp what solver does and how it does it, a command of multivariate calculus is must, am not there yet.

So to fit the zero inflated poisson distribution using the least squares method, had a choice between R and Python. Although I never attempted the project in R, am convinced this is piece of cake in R given its massive set of statistical libraries but my issue with R is the hosting of Shiny, R's web front.

I decided to try this with python since if I ever do operations research work this is a programming language I have to master, it's early days to say am mastering it but at the moment the focus is the stats and applied mathematics.

Obviously,the first step in such an endevour it's to research the web for code I can just adapt for my needs, so far I haven't found anything that suited my needs.

what I found is curve fitting using the maximum likelihood method and have to say I found the code confusing and have my doubts whether the optimization will converge for such a small dataset. 
