**Assignment 3 & 4: Critique by Design**

For this assignment, I chose to redesign a visualization exploring price parity by state from [Howmuch.net](https://howmuch.net/articles/regional-price-parities-by-state). I chose this visualization because I found the visualization type the original authors used interesting visually, but confusing to read. There seemed to be multiple ways I could apply principles from our course in eliminating unnecessary details and streamlining the design while preserving the story the visualization was trying to communicate. 

The dataset used for the original visualization is available [here](https://data.world/makeovermonday/2021w17). In my redesign, I used Tableau Prep to clean the dataset to include only the information the original visualization communicates, i.e. state price indices for "All goods" in the most recent available year (2019).

**Initial Critique**

The original visualization is visually interesting, as it uses a unique spiral shape as well as diverging color palettes to show how far above or below each state's average prices are from the national average. However, it is cluttered and a little difficult to read, and uses multiple pre-attentive attributes to convey the same information. For example, difference from the national average is conveyed both using color (diverging gradient, with higher values above the national average being increasingly saturated red, and those lower than the national average increasingly saturated blue) as well as shape (bar height). The spiral shape also poses some challenges for text design. Towards the middle of the spiral, the text direction changes and one observation (MN, Minnesota) is upside-down, inexplicably. This makes it hard to read and makes its value misleading, as its actual price index is 98 but because it is upside-down it looks like it has a price index of 86. The spiral has the advantage of being able to fit many observations within a small space--however, the design sacrifices clarity. There were some inaccuracies in the way the data was presented in the original visualization as well. For example, the article says that this data is current as of December 2020, but the latest year in the data is 2019. Finally, using red and blue color palettes in a US context can have political connotations, while this is not a political data story. Different contrasting colors may be more appropriate.

<iframe width="800" height="600" src="https://cdn.howmuch.net/articles/regional-price-parities-by-state-cfce.jpg"></iframe>

**Intial Redesign and Feedback**

I had two ideas for how to approach a redesign. Because this is state data, my inital idea was to create a choropleth map using a similar diverging color scale to indicate distance above and below national average. This could help highlight geographic trends such as those mentioned in the article that accompanied the original visualization--with coastal states having the highest prices compared to the national average. 

My other idea was to simply "unwind" the spiral bar graph and have a bar graph with two colors (no gradient)--with states above the national average in orange, and those below the national average in blue. I was worried about readability with this option, since there are a lot of states and even with abbreviating state names, it could be a dense visualization. 

I created two initial versions of both the choropleth map and the bar chart and asked for feedback on these preliminary designs. Respondents were F/28 and F/31.

<div class='tableauPlaceholder' id='viz1707245570410' style='position: relative'><noscript><a href='#'><img alt='Choropleth Map ' src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;TS&#47;TSWD_assgt34&#47;ChoroplethMap&#47;1_rss.png' style='border: none' /></a></noscript><object class='tableauViz'  style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> <param name='embed_code_version' value='3' /> <param name='site_root' value='' /><param name='name' value='TSWD_assgt34&#47;ChoroplethMap' /><param name='tabs' value='no' /><param name='toolbar' value='yes' /><param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;TS&#47;TSWD_assgt34&#47;ChoroplethMap&#47;1.png' /> <param name='animate_transition' value='yes' /><param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' /><param name='display_overlay' value='yes' /><param name='display_count' value='yes' /><param name='language' value='en-US' /><param name='filter' value='publish=yes' /></object></div>                
<script type='text/javascript'>                    
  var divElement = document.getElementById('viz1707245570410');                    
  var vizElement = divElement.getElementsByTagName('object')[0];                    
  if ( divElement.offsetWidth > 800 ) { vizElement.style.width='1000px';vizElement.style.height='827px';} else if ( divElement.offsetWidth > 500 ) { vizElement.style.width='1000px';vizElement.style.height='827px';} else { vizElement.style.width='100%';vizElement.style.height='877px';}                     
  var scriptElement = document.createElement('script');                    
  scriptElement.src = 'https://public.tableau.com/javascripts/api/viz_v1.js';                    
  vizElement.parentNode.insertBefore(scriptElement, vizElement);                
</script>

__Comments on the choropleth map:__
- Color palette makes it hard to distinguish within states that are below the national average--bleed together/all look similar
- Confusing to read
- Not clear what the metrics are ("price index" is not intuitive)
- Needs a title and subtitle to explain the price index and what it measures
- Hard to read smaller East Coast states

__Comments on the bar graph:__
- Hard to read the state names
- Lots of info for one visualization--not sure how to change this since you still need to show all 50 states
- Much better than choropleth map
- Still needs explanation of price index but more intuitive to figure out

**Final Redesign**

<div class='tableauPlaceholder' id='viz1707245776970' style='position: relative'><noscript><a href='#'><img alt='Price Index by State vs. National Average (2019)The price index reflects the average price of all goods in each state compared with the national average (set at 100). States here are shown by difference from the national average--for example, the price  ' src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;TS&#47;TSWD_assgt34&#47;PriceIndexvs_NationalAverage&#47;1_rss.png' style='border: none' /></a></noscript><object class='tableauViz'  style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> <param name='embed_code_version' value='3' /> <param name='site_root' value='' /><param name='name' value='TSWD_assgt34&#47;PriceIndexvs_NationalAverage' /><param name='tabs' value='no' /><param name='toolbar' value='yes' /><param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;TS&#47;TSWD_assgt34&#47;PriceIndexvs_NationalAverage&#47;1.png' /> <param name='animate_transition' value='yes' /><param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' /><param name='display_overlay' value='yes' /><param name='display_count' value='yes' /><param name='language' value='en-US' /><param name='filter' value='publish=yes' /></object></div>                
<script type='text/javascript'>                    
  var divElement = document.getElementById('viz1707245776970');                    
  var vizElement = divElement.getElementsByTagName('object')[0];                    
  vizElement.style.width='100%';vizElement.style.height=(divElement.offsetWidth*0.75)+'px';                    
  var scriptElement = document.createElement('script');                    
  scriptElement.src = 'https://public.tableau.com/javascripts/api/viz_v1.js';                    
  vizElement.parentNode.insertBefore(scriptElement, vizElement);                
</script>

Based on these comments, I decided to go with the bar chart for my final redesign and abandon the choropleth map--partly because I didn't feel that I had the skills in Tableau to be able to make the choropleth map as readable as I would have liked (e.g. including line callouts to show the small states' abbreviations rather than overlaying them directly on the map). I changed the labels for the bars so that instead of the state names being on the x-axis, each state abbreviation was right at the top (or bottom) of the bar, making it easier to read which bar was associated with which state. I think this improved readability a great deal. I also included a more descriptive title and included a small paragraph underneath to explain the price index and what this metric meant. 

Throughout this process, I tried to stick to the principle that simpler is often better. While the choropleth map was an exciting idea and I have a bias towards map visualizations for any kind of geographic-related data, I realized in getting feedback from peers that the map as I had designed it actually made the information more confusing. The feedback process also reinforced to me the importance of smart color choices. The way my color gradation worked in the choropleth map made it very hard to distinguish between states below the national average, wereas presenting this information in a simple bar chart makes it very easy to compare each state to one another. I did get some feedback that one reader wished I made a more interesting or visually unique visualization, but as she started to walk through potential options including a bubble plot and a scatterplot she actually went back on this thought and said she thought those visualization types would make the data harder to read. There does seem to be somewhat of a trade-off between creating a unique, really visually engaging graphic, versus creating the most readable and universally accessible data visualization. I'm really interested to explore more instances where these principles intersect and to push myself to create really unique and beautiful but informative visuals.
