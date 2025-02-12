| [home page](https://cmustudent.github.io/tswd-portfolio-templates/) | [data viz examples](dataviz-examples) | [critique by design](critique-by-design) | [final project I](final-project-part-one) | [final project II](final-project-part-two) | [final project III](final-project-part-three) |

# Critique and Redesign
_For each step below, you should document your progress as you move forward.  In terms of tone, think of the writeup as though you're keeping journal of your step-by-step process.   You should include any insights you gained from the critique method, and what it led you to think about when considering the redesign.  You should talk about how you moved next to the sketches, and any insights you gleaned from your user feedback.  Document what you changed based on the user feedback in your redesign.  Finally, talk about what your redesigned data visualization shows, why you selected the data visualization you did, and what you attempted to show or do differently._


## Step one: the visualization

What Schools Create the Most Student Loans in the U.S.?

https://howmuch.net/articles/university-with-the-most-student-loan-originations-in-every-state

![cfdd933e5844990cf476406f13b4cce](https://github.com/user-attachments/assets/55aa7cc7-8fa9-4e87-bb94-e954cd4be619)


I like visually busy visualizations because there are so much to work with, also I haven't tryed making heat map yet. This particualr visualization is a perfect combination of two.


## Step two: the critique

The map graph type is good for showing trends. But this visualization is too visually busy, and many interpretations of trends could be drawn. I'm not sure if I should pay attention to the number of public schools shown on the map (large group of color), or the total amount of loans in each school (money amount represented with different color).


## Step three: Sketch a solution

There are three ways of fixing it.

Method 1: keep the map graph, minus the logos of school and their names, and each school's loan amount.
![530d966da7610203b5ef7f433642e2f](https://github.com/user-attachments/assets/2eb2951d-2c28-4588-895d-406b641bf959)


Method 2-1: use bar chart, and group the bars using school types.
![9df5983e77628ae4f9526fe3e59fb67](https://github.com/user-attachments/assets/ced59e45-1ca2-45e0-a29a-1f1b84276b63)


Method 2-2: use bar chart, and group the bars using total loan amount range.
![0e42421e8254f4a7262d067c8a2af87](https://github.com/user-attachments/assets/4e72755b-4c9b-4e6e-8bf0-d7a1d830e515)


## Step four: Test the solution

_Before you conduct your interviews, prepare a simple script.  Use this as a guide and as a way to take notes as you go forward. Come up with your own list of questions you want to ask for the selected visualization. Keep the questions broad so you can get the most value out of your feedback. Then, document answers to your questions here._

Questions to ask (modify these for your own interviews): 

- Can you tell me what you think this is?

- Can you describe to me what this is telling you?

- Is there anything you find surprising or confusing?

- Who do you think is the intended audience for this?

- Is there anything you would change or do differently?

Results: for the map graph
| Question | Interview 1 - classmate from MAM 2 | Interview 2 - classmate from MSPPM|
|----------|-------------|-------------|
|Can you tell me what you think this is?| It shows the distribution and trends of school loans across the state.|I think this graph tells about the loans in the US. There are three color pallets and my eyes need to travel a lot to find the information. It takes time to figure out.|
|Can you describe to me what this is telling you?|There's a lot of pink, which represents public school, on this graph.|I think this graph tells me the loans in each state based on three categories: public, private-nonprofit, proprietary. |
|Who do you think is the intended audience for this?| Based on the jargons, this might be aiming at financial people who are familiar with the terms.|Government agencies, or schools related policy makers.|
|Is there anything you find surprising or confusing?|The terms "Total Loans Originated" and "Proprietary" are confusing. They are jargons that we don't use in daily lifes. Maybe it will be obvious to the targeted audience, but they are not obvious to me.| The grey blocks in the color label (under "$100-299M" and "$500 M and more") are confusing. I try to find them on the graph but what they actually mean is null or N/A.|
|Is there anything you would change or do differently?|I would try to avoid using red/pink and green together. The color conbination might not be color-blind friendly.|I suggest to focus on what you want to tell to audience. Do you want to focus on public school’s loan? Or do you want to compare the public school vs private school?|


Synthesis: 

My redesign draft already exclude the school logos and specific loan amount for each school, yet my interviewee still find it visually busy. Using three color for different school types and four shades for each color representing loan range is still too much visual elements on one graph. Depending on the narrative I want to highlight, it is better to take down a few things.

## Step five: build the solution

I used Datawrapper to create the heat map.

Building on the draf mentioned above, I went a step further and get rid of the four shadings for each loan range. Now the graph only concerns different types of schools. The new title also tells audience clearly what the trend is. I want the narration to highlight the main takeaway in the original article: "Our map clearly demonstrates how the majority of student loans come from public universities."

<div style="min-height:518px" id="datawrapper-vis-iaKdq"><script type="text/javascript" defer src="https://datawrapper.dwcdn.net/iaKdq/embed.js" charset="utf-8" data-target="#datawrapper-vis-iaKdq"></script><noscript><img src="https://datawrapper.dwcdn.net/iaKdq/full.png" alt="" /></noscript></div>




I also used Tableau to creat the two bar charts, each focusing on a different narration.

The first one here has the same narration as the map, which highlights the large amount of public schools. I picked the orange color pallet to represent each loan range.

<div class='tableauPlaceholder' id='viz1739330308173' style='position: relative'><noscript><a href='#'><img alt='When it comes to the most student loans originated in each state, public universities take the cake ' src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Sc&#47;Schoolloan-publicschools&#47;Sheet1&#47;1_rss.png' style='border: none' /></a></noscript><object class='tableauViz'  style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> <param name='embed_code_version' value='3' /> <param name='site_root' value='' /><param name='name' value='Schoolloan-publicschools&#47;Sheet1' /><param name='tabs' value='no' /><param name='toolbar' value='yes' /><param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Sc&#47;Schoolloan-publicschools&#47;Sheet1&#47;1.png' /> <param name='animate_transition' value='yes' /><param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' /><param name='display_overlay' value='yes' /><param name='display_count' value='yes' /><param name='language' value='zh-CN' /><param name='filter' value='publish=yes' /></object></div>                
<script type='text/javascript'>                    
  var divElement = document.getElementById('viz1739330308173');                    
  var vizElement = divElement.getElementsByTagName('object')[0];                    vizElement.style.width='100%';vizElement.style.height=(divElement.offsetWidth*0.75)+'px';                    
  var scriptElement = document.createElement('script');                    
  scriptElement.src = 'https://public.tableau.com/javascripts/api/viz_v1.js';                    
  vizElement.parentNode.insertBefore(scriptElement, vizElement);                
</script>


The second bar chart focuses on the loan range. Since each bar represents school type, I keep the original color pallet of pink, green-blue, and purple.


<div class='tableauPlaceholder' id='viz1739330600699' style='position: relative'><noscript><a href='#'><img alt='The most frequently seen loan range is between $100M - 299M. ' src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Sc&#47;Schoolloan-loanrange&#47;Sheet2&#47;1_rss.png' style='border: none' /></a></noscript><object class='tableauViz'  style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> <param name='embed_code_version' value='3' /> <param name='site_root' value='' /><param name='name' value='Schoolloan-loanrange&#47;Sheet2' /><param name='tabs' value='no' /><param name='toolbar' value='yes' /><param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Sc&#47;Schoolloan-loanrange&#47;Sheet2&#47;1.png' /> <param name='animate_transition' value='yes' /><param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' /><param name='display_overlay' value='yes' /><param name='display_count' value='yes' /><param name='language' value='zh-CN' /><param name='filter' value='publish=yes' /></object></div>                
<script type='text/javascript'>                    
  var divElement = document.getElementById('viz1739330600699');                    
  var vizElement = divElement.getElementsByTagName('object')[0];                    vizElement.style.width='100%';vizElement.style.height=(divElement.offsetWidth*0.75)+'px';                    
  var scriptElement = document.createElement('script');                    
  scriptElement.src = 'https://public.tableau.com/javascripts/api/viz_v1.js';                    
  vizElement.parentNode.insertBefore(scriptElement, vizElement);                
</script>

## References
_List any references you used here._

## AI acknowledgements
_If you used AI to help you complete this assignment (within the parameters of the instruction and course guidelines), detail your use of AI for this assignment here._

I used ChatGPT to 1)collect data and 2) help me navigate Tableau.

Becuase there's no dataset avialble from the website of the original visualization, I uploaded the original heat map to ChatGPT and ask it to collect data from it. The result was an excel form with some mistakes. I then manually clarify the data.

I then ask ChatGPT how to create the drafted graph in Tableau.

<img width="361" alt="image" src="https://github.com/user-attachments/assets/78655a72-e374-4d66-8b42-8401a45071b7" />
