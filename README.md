# dda2003-assignment-4-solved
**TO GET THIS SOLUTION VISIT:** [DDA2003 Assignment 4 Solved](https://www.ankitcodinghub.com/product/dda-2003-mds-6112-assignment-4-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;115884&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;DDA2003 Assignment 4 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
1 Description

Figure 1: The visual result of assignment 4.

This assignment aims to help students get familiar with animated highdimensional data visualization using D3.

In this assignment, you are asked to produce the following visualization results.

• Given a high-dimensional data set in a .json file, visualize the data using a Sankey diagram, as shown in Figure 1.

• Visualize two categories into different shapes.

• Using stacked bar charts to visualize and show the statics, as shown in Figure 1 at the right part.

(a) (b)

Figure 2: Animation of high-dimensional data visualization.

• Create an animation. Two frames are shown in Figure 2

For the complete animation, please refer to the provided video.

2 Requirement

• Access data.

• Stack probabilities.

• Create person.

• Visualize paths.

• Visualize persons.

• Add color and filter.

• Visualize bars.

• Update numbers.

Online Resources The following online resources will be helpful in finishing this assignment.

• SVG in D3

• Scale in D3

• Selection in D3

• Timer in D3

3 Instruction

3.1 Access variables

Figure 3 shows the data we used in this assignment. Each object represents a possible starting point, specified by a sex and a socioeconomic status (ses). The object also has the percentage of people in that starting group that attained (at most) various degrees. Here, you need to define the data accessor, data category, and data range for education and socioeconomic status. The sex variable has been defined in the .js file. You are asked to define the remaining two variables.

Figure 3: The high-dimensional data.

3.2 Stack probabilities

Since we need to create several people per second, we want our generatePerson() function to be as simple as possible. Given their sex and socioeconomic status, we know the probability of a person falling into one of our education “buckets”. Since these probabilities sum up to 100%, we can stack these probabilities and use a random number to assign a person to a bucket. Here we take the probabilities for females who grew up in a low-income household as an example.

We can take these probabilities and stack them on top of each other so that each level instead represents the probability that a person achieves that level or lower. The highest level (Bachelor’s and up), will get the number 1 because there is a 100% chance that a person achieved that level or lower.

When we have these stacked probabilities, we can choose a random number between 0 and 1, which we will locate on the number line. For example, if we choose the number 0.32, this person will be placed in the Some Postsecondary education bucket, sketched in Figure 4(a).

In this part, you need to generate an empty stackedProbabilities object to populate. You will loop over each of the starting points in the data set, generating the status key and instantiating a stackedProbability number. Next, you loop over each of the education buckets (in order), adding the current probability to the stacked probability, then returning the current sum. Note that you need to add an additional check – if we are looking at the last education bucket, we will return 1 instead of the running sum. This will help account for rounding errors, where the sum is 0.99 and does not completely add up to 1. The output of stackedProbabilities is shown in Figure 4(b).

(a) probability diagram (b) probability object structure

Figure 4: Illustration of stacking probabilities.

3.3 Create person

In this part, you are asked to put the stacked probabilities to use and create a generatePerson() function. Here we want this function to return an object with a sex, ses, and education. If we peek at the bottom of the chart.js file, we wil see a few utility functions that will help us with some dirty work. For example, there is a getRandomValue() function that takes an array of values and returns a random value. The procedure is as follows:

• Generate a statusKey and grab the matching stacked probabilities. • Generate a random number using Math.random() and use d3.bisect() to find the index where that number will “fit” in the probabilities array.

Figure 5: Output of generatePerson() function

Figure 5 shows an output of generatePerson function.

3.4 Draw path

Next, you will create a scale that will convert from a socioeconomic id to a y-position. We want these paths to be evenly spaced between the bounds, but to still fit inside. You can achieve this by padding the scale’s domain, making it span [−1,3] instead of [0,2]. This way, the real socioeconomic status ids will fit inside the bounds.

(a) y scale left (b) y-scale right

Figure 6: Y scale diagram.

You will also want the scale’s domain to be backwards: [3,−1] instead of [−1,3] because we want the highest y position (closer to the bottom) to correspond to the lowest id. An example is shown in Figure 6.

You will need to create that six-item array for each permutation of starting and ending ids. Map over each of the starting ids and also each of the ending ids, creating that six-item array for each loop. Pass the result to LinkOptions (using d3.merge()), which will flatten these into one array.

Finally, the output of linkOptions is shown in Figure 8. Note that you need to add an interpolator function to line generator to smooth the paths.

(i.e., .curve(d3.curveMonotonX)).

(a) Path example (b) Path parts diagram

Figure 7: Example path.

3.5 Visualize persons

In this part, you need to create a function called updateMarkers() that will draw people. You will use d3.timer() to update the position of people. d3.timer()’s first parameter is a callback function that it will call until the timer is stopped (which we can do the timer’s .stop() method). The callback function will have access to one parameter: how many milliseconds have elapsed since the timer started. Then you need to add a new person to the people array every time updateMarkers() runs.

3.6 Add color and filter

Figure 8: Output of linkOptions.

linear scale that interpolates between two colors – by setting the domain to an array of the sesIds, then you will get three unique, equally-spaced colors. One interpolator that can be used is d3.interpolateHcl.

To address this, you need to give each person a unique id when we create them. Each time we call generatePerson(), we will increment the currentPersonId variable that we’ll use as an id. This way, each person’s id will be distinct.

3.7 Visualize bars

3.8 Update numbers

4 Evaluation

In total, there are 100 points in this assignment. A detailed evaluation is provided here.

1. Access education attributes and socioeconomic status. (5 pts)

2. Stack probabilities. (10 pts)

3. Create person. (5 pts)

4. Visualize path. (15 pts)

5. Visualize persons. (20 pts)

6. Add color and filter. (20 pts)

7. Visualize bars. (10 pts)

8. Update numbers (10 pts)

9. Submission (5pts). Please compress your code and a readme file (optional) into a zip file and submit the zip file to Black Board. The readme file can include descriptions that help the grader run the interface successfully.
