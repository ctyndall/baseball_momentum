
## Summary
There is often an idea that a team that plays well heading in to the postseason will fair better than a team that scuffles down the stretch. 

However, there is no noticeable difference in how far a team advances (Divisional Round, Championship Round, World Series, Winning World Series) when compared to their winning percentage over the last month, last week, or even last day of the season. In fact, over the course of the whole season, World Series Champions had 94.6 wins on average compared to 93.8 wins for those that lost in the first round which is nearly no noticeable difference. 

It doesn't matter how many wins you have going in to the playoffs, or how many wins you've had recently. All that matter is making it, and then a team's chances are about as good as any other.

The plot shows a blue dot for every team that made the playoffs for the past 20 years grouped according to how far they advanced.  The red triangles show the average wins for each group of teams.  The buttons and slider allows you to compare the winrates between the teams for any number selection of games, and compare how 'hot' teams were at different parts of the season and whether it affected their playoff results.

Before 1995, there was no Divisional Series round of the playoffs so any data before this year is not included.  Also, 1995 was a shortened season so I did not include it either.
  
## Design

#### Initial Design
I initially though that there would be some sort of correlation between wins down the final stretch of a season and how well a team did.  My very initial design (index_old.html) showed a bar graph for the winning percentage across various outcomes (win/lose each round).  I quickly realized that the winrates are rather similar no matter what the outcome was and I wanted a way to probe the data more deeply and be able to see individual teams.  Also, the scale was difficult to understand since the win percentage is generally between 0.50 and 0.60 for playoff teams.  With an axis starting at 0, the difference between these win percentages is difficult to judge.  I therefore decide to plots the number of wins in a given interval and to separate out individual teams so the data distribution could be viewed along with the group average.  Also, I changed the data to reflect only a single outcome for each team.  In the old version, teams that advanced were counted in the averages for each previous round which was skewing the data for the early rounds.

#### Final Design
The main finding for this plot is that the winrates of teams during the final month of a regular season has no impact on how well they do in the playoffs.  Furthermore, there is no selection of regular season games that shows correlation to playoff results for teams.

There are 4 outcomes for the playoffs, losing in one of the 3 rounds or winning it all\*.  The x-axis is categorical with a label for each of these outcomes.  The categories are ordered from worst results to best result so there is a left-to-right flow for comparisons between outcomes.  The y-axis shows the numer of wins for the final 30 games of the regular season.  The y-axis dynamically updates if a different selection of games is chosen, and adjusts to the max and min number of wins for the selection. A scatter point is listed for each team that made the playoffs, and a larger red triangle shows the average of all the teams that ended with that particular outcome.  The main conclusion is derived by looking at the triangles and noticing very little change in y-value across outcomes.  Further in-depth exploration can be performed by hovering over individual team circles and getting the team names, years, and wins.  If two teams had the same number of wins and the same outcome they are separated horizontally.  This give a histogram effect and further shows the distribution behind each of the averages.

To reflect the main finding and avoid clutter, I made the averages more opaque, larger, and used a sharper more striking triangular shape so that the reader will preattentively focus on those 4 data points.  On examination, the triangles all have vertical heights within one game of each other and reflect a very small difference in win rates.  Then the reader is free to explore individual teams or explore changing the game selection.  A few pre-determined buttons allow quick selection of Full Season, 1st Half, 2nd Half, Final Month (default), Final 10 Games, or Last game.  The brush slider should be the most difficult thing to realize has interactivity, which should allow the visualization to be understood before deeply exploring other options.

\* There is now a single game wildcard playoff round that is not included with this graphic.  This single game was added to make the wildcard teams have a more difficult time advancing throughout the playoffs, so perhaps a trend will be seen in the future.

## Feedback 

After iterating on an initial design and changing the data format form 6 categories to 4, I created index_2.html.  The new plot lacked a legend which was quickly pointed out upon showing to a coworker, and they said that it was unclear what the blue circles were.  Also, the blue circles are stacked on top of each other in several places, so only certain teams can be highlighted.

I changed the layout of the circles for index_3.html so that each and every team could be explored.  I added a legend and improved the category labels so that it is more clear what each group is.  I changed the average to a triangle in an effort to highlight its function as an average (since it appears to point at a location in the middle of the circles) and hopefully draw the readers attention since it is a sharper shape.  However, after showing to a couple people, they immediately focused on the individual team circles since they take up so much space, and got a bit lost on what the graphic was intending to show, and struggled to recognize the legend and identify what the shapes meant.  Also, the button selectors were another distracting focus of attention.  The average values were one of the last thing that people were focusing on.  They were able to grasp the finding of the chart after understanding what everything meant, but it required a bit a work piece together the various parts of the plot.

For index_final.html, I changed the title to describe the graph better, and made the x-axis label simpler.  I increased the size of the averages and made the teams more transparent (they are more opaque only on mouseovers).  I changed the selection box colors to be less eye-catching and moved them slightly farther from the main graphic.  The legend is separate its own box, due to a comment that it looked like part of the data before.  The legend has a white background and is placed near the title so it is more easy to find.

## Resources

https://en.wikipedia.org/wiki/Major_League_Baseball_postseason
http://alignedleft.com/tutorials/d3/
http://www.baseball-reference.com/
https://github.com/d3/d3/blob/master/API.md


```python

```
