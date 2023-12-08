# statsfordevs
[statsfordevs.com](https://statsfordevs.com/) is a collection of statistics by usage, popularity and employability of languages, frameworks, and libraries. 

#### Page Layout

Here is my proposed general layout of any given page.

##### Overview and History
This will contain a brief description of what the technology is used for currently and why is was created in the first place. Included is a timeline from it's early development and/or first release to today. 

##### Usage Statistics
For technology which can readily be tracked, for example from [Stack Overflow Survey Statistics](https://promptier.github.io/website/usage/languages.html), a chart will be present comparing it's usage with related technology in it's niche or that competes with it. For example, in the case of front-end frameworks, React, Angular and Vue all focus on creating responsive/reactive user interfaces, so they will be compared.

##### Popularity
There would be several ways to measure popularity, such as comparing, for example, Python's result in Google Trends against Javascript. Another method would be measuring growth of Subreddits. This would be possible thanks to [Subreddit Stats](https://subredditstats.com/). Despite the controversial Reddit API changes, they still seem to be collecing data which is presented via Plotly. One possible challenge to this is the fact there are sometines multiple subreddits involved for a particular technology, such as Python not only having a r/python forum, but also r/pythontips and r/learnpython.

##### Employment
This data will be collected from Indeed and/or Glassdoor search engines. Currently I can not find a way to easily scrape Indeed and have yet to try Glassdoor. Though I suspect they will be equally as difficult as they use Cloudflare as a CDN. Cloudflare is known for being very secure which detects scraping bots/scrawlers as adverseries in the same way they would detect a Ddos attack. Because of this, I have been manually searching keyterms and adding data. It is quite tedious and I would be open to any other solutions.

Regardless, data will be presented in a bar chart comparing similar technology. Such as Azure having 24,000 jobs in the US compared to AWS with 28,000.

Tracking Github repository stars would also be a useful measure of popularity. Luckily we can use [Star History](https://star-history.com), which in turn uses Github's API to track this as seen below. You can see here I have compared the repositories of front-end frameworks. 

<iframe style="width:100%;height:auto;min-width:600px;min-height:400px;" src="https://star-history.com/embed?secret=Z2hwX3RIQjRlaGs3ejlkWDhhNk5ad0NBbW1tS0ZNY0s5bjJyU2RZRQ==#sveltejs/svelte&facebook/react&Angular/angular&vuejs/core&Date" frameBorder="0"></iframe>

#### Charting Library
Currently I have been using [Chart.js](https://www.chartjs.org/) to present most data. It is a fairly easy library to use. The downside is it relies heavily on Javascript and is a bit slower than a library like [Charts.css](https://chartscss.org/). This library creates charts out of HTML tables whose data, labels, and legends are all whithin your page as is, as opposed to being dynamically rendered using Javascript. For example, this means the charts are easier to control with traditional CSS such as the chart title and labels conforming to the root font size via rem. 

I will likely experminent with both charting libraries and see where it goes. This project is very early and experimental and the goals will likely change over time. Please reach out to me if you are intested in contributing.
