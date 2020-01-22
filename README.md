# The 2020 Demmy Awards
For the past few years, my friends and I have taken to creating "fantasy" political drafts. It started with the obscene Republican primary race for the 2016 election. It then moved onto a Trump Cabinet draft (where we'd try to guess who we would fire next). Finally, the most recent was a draft of the 2020 democratic primary candidates a.k.a. The Demmys.

The Demmy draft started on May 15, 2019 and finished on June 15, 2019. It was an auction style draft with each drafter having 200 "Democracy Bucks" that could be spent on candidates that they thought would do well. The drafter order was picked randomly and the candidates were nominated by the drafters.

Ultimately, this is a fun exercise for me to improve my Python, numpy, pandas and general data analysis/vis skills. As such, it is likely to change a lot as I go through and edit items; however, I hope it will be educating and fun no matter what.

**Democracy + Gambling = Friendship**

# The Draft
The draft was started on May 15, 2019 with the current list of democratic candidates (21 + Biden) that were running. It was an auction style draft, where everyone would get $200 Democracy Bucks to divide up and out bid each other for candidates that they felt would last longer in the race. A minimum of $1 would be required to get a candidate, so if you spent your all your money on only 2 candidates you'd be SOL to get any after that. No freebies!

The draft order was randomly determined as:
1. Michael
1. Jeff
1. Kevin M
1. Sara
1. Daniel
1. Kevin K

## Point Rules
Point rules can be summarized as getting 1 point per day per candidate as long as the candidate has not officially announced their exit. You also get 50 bonus points for picking the candidate that gets the final nomination.
1. Each candidate accumulates 1 point per day they stay in the race starting inclusive of the final date of the auction (which was June 15, 2019)
1. 50 points for picking the winning candidate. No bonus points for candidate becoming running mate.
1. Candidates in the race accumulate points until the day of the actual vote at the Democratic National Convention (DNC)
1. A vote will be held on what to do if a candidate drops from the democratic primary and begins running as 3rd part
## The 22/24 Compromise
As mentioned above, at the beginning of the auction there were only 21 candidates announced to run and it was assumed Joe Biden would also run (making him a bit of a wild card in the draft). With 6 drafters, it was implied that this would allow 4 drafters to get 4 candidates, while 2 drafters would end up with 3; however, this was not an explicit rule.

Of course, like all good pedantic friend groups, we began to quibble over this ambiguity. Some (like Daniel) felt we should not have any cap on candidates, while others (like Kevin K, who had spent a majority of his money already) felt that not being guaranteed a 3rd candidate would have changed his whole strategy from the beginning (arguably true). Furthermore, more candidates had joined the race so a vote was held on May 29th with six options:
1. Restart the auction draft with the new list and guarantee everyone gets 4 candidates
1. Restart the auction draft and have no min/max number of candidates
1. Change draft style to a snake draft where everyone gets 4 candidates
1. Keep going down the current auction draft with no candidate max/min
1. Keep going down the current auction draft, add the two new candidates, but still keep the max total number of candidates at 22 (meaning that there would still be an uneven distribution of candidates)

In the end, Option 6 was voted as the best option. It was also decided that these would be the final rules and any more late comers to the race (looking at you Bloomberg) would not be considered.

# Analysis
## Points to Date
The original idea for this project was to generate a plot of points accumulated as a function of time. I thought this would be interesting to see since it might give an indication of what would look like an early lead or a potential upset. Ultimately, I found this plot to be kinda boring and lackluster so I'm in the process of researching to see if there's another data vis method that could represent the data adequately but look better.
![Points To Date](figs/point_total.png)

## Candidate Values
Candidate values were the first metric I thought to include as a way of measuring a drafters efficiency in use of their dollars. What can be seen here is that many of the people considered early "front runners" often have lower values because their bidding was typically more fierce and resulted in a higher end price. The candidates with the highest value tended to be ones that went for very low prices (e.g. Gravel for $3) and so they appear to have an inflated effect.
![Candidate Value](figs/candidate_values.png)
![Candidate Values Ordered](figs/candidate_values_ordered.png)

## Candidate Points
In the end, what wins the game is total candidate points, not any kind of efficiency or value. Here we see the individual candidates contributions grouped by drafter. A bolded score indicates that that candidate has dropped out and so cannot contribute any more points beyond what they are capped at.
![Candidate Points](figs/candidate_points.png)
![Candidate Points Ordered](figs/candidate_points_ordered.png)


# Sources:
1) Plot inspiration taken from [here](https://www.machinelearningplus.com/plots/top-50-matplotlib-visualizations-the-master-plots-python/#15.-Ordered-Bar-Chart)