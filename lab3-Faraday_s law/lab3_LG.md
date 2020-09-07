# Lab 3: Faraday&rsquo;s Law
---
### All Materials needed:
-  iOLab
- Neodymium magnet
- Long wire
- Hook and spring
- Ruler

### Learning Objectives:
-  Faraday&rsquo;s Law
-  Lenz&rsquo;s Law
-  Basic Concepts in Error Analysis
---
# Part I: Induction and the Electromotive Force

Now that we have completed two projects focusing on the physics of moving charges -- their behavior in external magnetic fields and the magnetic fields they themselves generate -- we now move on to talk about moving *magnets*.

As you may have learned by now, similarly to the way a moving charge (and, hence, a changing electric field) can generate a magnetic field, a changing magnetic field also induces an electric field. This electric field, like any, has the ability to do *work* (&#9733 see footnote) . Specifically, we will be interested in how it can do work to generate current in a wire. In this lab, we will investigate the current induced in a loop of wire in the vicinity of a moving magnetic source.


The equation that describes the creation of an electric field by a changing magnetic field is Faraday’s Law. It states that if any open surface experiences a time-varying magnetic *flux*, then a net voltage (or emf) exists around the perimeter of that surface. Here, flux refers to the net magnitude and direction of magnetic field lines penetrating the area enclosed by a loop of wire, or 

::: Figure:Equation
$$
\Phi_B= \vec B \cdot \vec A
$$
:::



For a coil with a loop of area $A$, Faraday’s Law predicts that the emf measured around the perimeter is

::: Figure:Equation
$$
V_{coil} =  V_{loop} = - \frac{d \Phi_B}{dt}
$$
:::

Note that the cause of Faraday’s Law is some **time-varying **external magnetic field. 

:::Figure:Simulation
`<iframe src="https://kapawlak.github.io/PhDemoJS/Apps/Faradays_Law/Faradays_Law.html" width= "100%" height="750" style="border:none;"> </iframe>`
:::
<!-- Stated below
Lenz&rsquo;s Law states that the established current flow in the loop will be in a direction such that the magnetic field generated by this current opposes the change in the magnetic flux from the external field.
-->

In which direction does the current flow in such a situation? The question is addressed by Lenz&rsquo;s law, which states that the magnetic field generated by the current flow (recall the previous lab experiment) will point in the direction *opposite* to the change  in the magnetic flux  from the external field -- the electron motion attempts to generate a $B$ field that &ldquo;cancels out&rdquo; the change in flux, so that the total field in the region is $\vec B =0$.

:::Question
Try to describe what would happen if, instead, the current generated a magnetic field that aligned with the external flux, recalling that a current itself generates a magnetic field. Which laws of physics would might this ultimately break? 
:::

For a coil with $N$ loops in series, the area increases to $NA$, so Faraday’s Law predicts that the emf measured around the perimeter is:

::: Figure:Equation
$$
V_{coil} = N V_{loop} = - N\frac{d \Phi_B}{dt}
$$
:::
The effect of these loops is essentially to amplify the emf by a factor of $N$. In this experiment we will have a coil with 4-5 loops, with which we will be able to measure earth&rsquo;s magnetic field.

####

 (&#9733) Footnote: Magnetic fields themselves cannot do work, but when energy is expended (e.g. by pushing a magnet) to cause a change of magnetic field or flux in some region, the resulting electric field can do work. 
# Part II: Experiments

This lab will involve the study of Faraday’s Law and Lenz’s Law acting upon a coil, which we  create by winding a wire around the iOLab device. We will measure Lenz’s Law by moving a magnet suddenly toward or away from the coil, and observing the direction of current. We will measure Faraday’s Law by spinning the iOLab in the earth’s magnetic field, and measuring the voltage as a function of rotational velocity.
## 1. Prelab Setup 

### Materials needed:
- iOLab
- Neodymium magnet
- Long wire
- Hook and spring

### Time to Complete:
- 1 minute reading 
- 10 minutes setup and data
- 5 minutes questions

Before starting the exercises, as always, make sure your iOLab is calibrated! The experiment in this lab requires us to construct a series of loops, which we will do by conveniently wrapping our enameled wire around the iOLab in the exercise below.

:::Exercise
We will wind the coil around with the two ends inserted into the “G+” and “G-” inputs of the iOLab. These should be inserted such that if the current in the loop moves counterclockwise, it will flow into G+ making a positive signal, and vice versa. This configuration is used to ensure that the iOLab coordinate system is consistent with the right-hand rule.

iOLab setup:
1. Ensure that you have calibrated your device, and that you have removed as much enamel as possible from the tips of your wire.
2.  Plug one end of the wire into “G+.”
3.  Extend the wire to the side and secure it with tape, so that you can continue the winding process.  
4.  Wrap the wire in the clockwise direction for 4 or 5 turns (write down how many somewhere). Try to keep the winding orderly, like a coil, and as tight as possible.
5.  Finishing by plugging the remaining end into “G-.” 
6.  Use tape as necessary to secure the wire.

:::Figure:Figure
![](imgs/iOwrap.jpg)
:::
:::
####
To verify that the coil is working as expected and capable of taking data, follow the verification steps in Exercise 2 below:
####
:::Exercise
Verification:
1. Identify the South pole of your magnet.
2. Open the iOLab software and select the &ldquo;High Gain&rdquo; sensor.
3.  Hit &ldquo;record.&rdquo; 
4.  With the south pole of the magnet facing the loop, move the magnet towards the center of your loop very quickly.
5.  You should see the measurement jump in the plot.
6.  Make sure this jump (positive or negative) is consistent with Lenz's law -- otherwise, check the direction of your winding.

:::Question:
a. In which direction does the voltage jump? 

b. A positive voltage jump means that current is flowing from G- to G+. Based on the direction of your wire winding, is the current flowing clockwise or counter-clockwise?

c. Now consider the orientation of your magnet, where the south pole should have been facing your loop. Does your observation of the current direction match Lenz&rsquo;s law?
:::
:::

## 2. Measuring Earth&rsquo;s Magnetic Field by Faraday’s Law 

### Materials needed:
-  iOLab wrapped with Long wire
- Spring
- Ruler

### Time to Complete:
- 10 minutes reading 
- 10 minutes data
- 10 minutes questions

We will now use the iOLab coil to measure the horizontal component of Earth&rsquo;s magnetic field by using Faraday's Law.

:::Note
The discussion below is a bit more &ldquo;mathy&rdquo; than that in previous labs, but the procedure is actually quite simple. Don&rsquo;t be intimidated! You are all very capable of working through this, or else I would not include it. :-)
:::

######
We want to use the Earth’s magnetic field to generate an induced emf. An emf will be induced if flux is changing, but unlike the local field generated by a tiny magnet, Earth&rsquo;s field is *constant* over large areas, so we will need to be clever about our experimental setup.

####

Recall that flux is $\Phi_B= \vec B\cdot \vec A$, meaning that it depends on the *angle* between the direction of the magnetic field and the plane of the loop. This implies that *rotating* the loop should result in a change of flux! Say we changed the angle of the loop as a function of time; the resulting expression would be:

:::Figure:Equation
$$
\Phi_B(t)=\vec B \cdot \vec A=BA \cos(\theta(t))
$$

:::
Let&rsquo;s use the equation for the EMF now and try to calculate the voltage over time by taking the derivative of the above by using the chain rule:

:::Figure:Equation
$$
V_{coil}(t)=-N BA \;  \frac{d}{dt}  \cos(\theta(t))\\
=-N BA \;  \sin(\theta(t)) (\frac{d}{dt}  \theta (t))\\
=-N BA \; \omega(t)  \sin(\theta(t)) 
$$
:::
where $\omega(t)=\dot \theta(t)$ is the angular velocity of the loop. This equation might look scary or unfamiliar, and that&rsquo;s O.K. -- we are about to simplify things. Since $\sin(\theta)$ is a function that is always between $-1$ and $1$, we can choose to consider only data points for angles that maximize or minimize this value. We call this the *envelope* of the function since it represents the highest and lowest possible values. 

####

Replacing the $\sin$ term with $\pm 1$ gives us a simple linear equation for $V_{coil}$ v.s. $\omega$,

:::Figure:Equation
$$
V_{coil}(t)=\mp N BA \; \omega(t)
$$
when 
$$
 \sin(\theta(t)) = \pm 1
$$
:::

Let&rsquo;s be more concrete about this now: A controlled way of changing the angle of the loop is to hang the iOLab from from a spring and twist it so that it oscillates left and right. As we let the iOLab oscillate, a plot of $V_{coil}$ v.s. $\omega$ will trace out a complicated function that fills in a shape that looks like a bow tie, whose upper and lower edges are given by Equation 6 with slope $NBA$.:





:::Figure:Simulation
`<iframe src="https://kapawlak.github.io/PhDemoJS/Apps/Faradays_Law_osc/Faradays_Law_osc.html" width= "100%" height="750" style="border:none;"> </iframe>`
:::







:::Question
Say you know :
1. the area, $A$ of your loops
2. the number of loops $N$ of your coil, and
3. the slope, S, of the envelope $V_{coil}= S \omega$ from your data.
 
Write down the expression for $B$ in terms of $A, N$ and $S$ (Hint: Look at Equation 6). 


You will need this equation to calculate Earth&rsquo;s magnetic field based on your data in the next exercise. If you don&rsquo;t understand this question, come back to it after completing the next exercise.
:::

::: Exercise
The iOLab&rsquo;s Gyroscope and High Gain sensor will gather the data. Make sure that the magnets from previous labs are moved far away from the experimental area.

**Collecting data**:
1. Hang the iOLab device from the spring at the edge of the table. For example, you could attach the spring to a binder clip on a textbook. Any way to keep the iOLab hanging securely will work. *Please do this over a carpeted area or bed so you don&rsquo;t damage your device if you accidentally drop it.*
2. Let it rest for a while until its orientation is relatively still. 
3. Open the software, go to “chart mode,” and select “Gyroscope” and “High Gain” from the “sensors” column.
4.  Note the orientation of the device and rotate it for three full revolutions. 
5.  Start recording and let go of the iOLab. 
:::Figure:Figure
![](imgs/spin.gif)
:::
6.  Let the device rotate for at least five cycles. You should see that the gyroscope $y$ component is oscillating and the high gain is making small peaks on the plot. 

:::Figure:Figure
![](imgs/plotgif.gif)
:::

7.  Now switch to “parametric plot mode,” and change gyroscope to “$\omega_y$.”
8.  The plot should be gyroscope vs. high gain. Highlight all data, and you should see a bow tie shape on the plot.
 ![](imgs/lab3.png)
9.  Using the “zoom” mode, record the coordinates of at least 8 extrema on one straight line along the edge of the bow. By symmetry, you can choose either the increasing line or the decreasing line.  These measurements correspond to the maximum voltage during rotation. Note that the $x$-axis has units of radians/second (rad/s) and the $y$-axis has units of millivolts (mV). 

10. To get the area of the coil, simply use a ruler to measure the $x$ and $y$ dimensions of the iOLab. 

After completing these steps, you should have all values needed to calculate the slope (and hence the magnetic field) from Faraday’s Law.

::: Question
(a) Enter the coordinates of your extrema from part 9 into a spreadsheet and calculate the slope, with units and reasonable sig. figs.

(b) Use the expression you derived in Question 3 to calculate $B$ with appropriate units. 
:::

:::

## 3. A first look at error analysis
### Time to Complete:
- 10-20 minutes reading 
- 15-30 minutes questions


The measurement you made in Exercise 2 should reflect the Earth&rsquo;s magnetic field, but there are many factors that can influence the quality of your data. In this section, we will introduce you to some basic error analysis that will help you determine the quality (accuracy and precision) of your data. At the end of this section I have an example of my own error analysis to guide you through the process!

### Part 1: Comparison to an Accepted Value
A fundamental step of experimental work (in any STEM field) is comparing your measured value to some accepted value. Here we will compare the $B$ measured in Exercise 2 to the value in the NOAA database.

:::Question:
(a) Visit [NOAA&rsquo;s website](https://www.ngdc.noaa.gov/geomag/calculators/magcalc.shtml#igrfwmm) and look up the magnitude of the horizontal magnetic field at your current location. Record this value in units of $\mu T$. 
![](imgs/noaa.png)
####
(b) Calculate the *discrepancy* with your measurement: 
$$
discrepancy = | accepted\, value - your\, value|
$$

(c) What is the sign of your discrepancy? I.e., is your value higher or lower than the accepted value? 

:::

### Part 2: Estimating uncertainty
It is very unlikely that your result perfectly matches the value in the NOAA database -- in fact, most experiments never give values that are right &ldquo;on the nose&rdquo; because of uncertainty . In reality, we care only that our measurement is *reasonably* close. &ldquo;Reasonably&rdquo; means within our expected margin of error -- whether that be not having an exactly precise value for our loop area, or our slope being slightly off.

We will now crudely estimate our uncertainty. While more advanced lab courses will later introduce you to formal error analysis, we will stick to a simpler approach that addresses the important concepts.

:::Question:
For this question we will assume that the *slope* of your line is likely correct, and that any error is related to your area measurement.

(a)  Based on how accurately you were able to measure the dimensions of the iOLab, estimate how much you could have possibly *overestimated* or *underestimated* the area of the coil, and call this value $\delta A$. 

(b) Write your area as $Area= (A \pm \delta A)$m$^2$. For example, if  I measured an area of $104$ cm$^2$ and was not very confident in this, and so I set $\delta A= 3$ cm$^2$, I would write
$$
Area = (1.04 \pm  0.03) \times  10^{-2} {m}^2
$$

(c) Return to your equation $B = S/ NA$ and calculate the uncertainty bounds on your measurement by plugging in $A - \delta A$ and then $A +\delta A$. Write your result as $B_{h}= (B \pm \delta B)$ as before.
:::


### Part 3: Accepted Value v.s. Error Bounds
You&rsquo;ve now calculated the error bounds on your result considering the uncertainty in your area measurement. Your final task is to determine if your measurement is *reasonably* close.


:::Question:
 From the results of questions 5 and 6, is your discrepancy less than your $|\delta B|$? In other words, does the accepted value fall within the range of values given by $B \pm \delta B$?
:::
If the answer to the first part of Question 7 is, &ldquo;No,&rdquo; and therefore, to the second part is, &ldquo;Yes,&rdquo; congratulations! More than likely, this will not be the case. Here are some tips for understanding your result:

- If the accepted value comes close to these bounds, say within $(B \pm 2\delta B)$ you can likely consider your experiment a success. 

- If the accepted value is very far from your bounds, you likely have either made a math/units mistake, or have a large source of *systematic* error that is affecting your results. Some examples of this could be objects or walls that are distorting or blocking the magnetic field where you are working (would this lead to a larger or smaller B value?), or your having forgotten to put away magnets.

:::Question:
 If your result is not consistent with the accepted value, even with error bounds, propose a reason why. Make sure your explanation makes sense!
:::


### Part 4: An example
This section is optional to read: here I am just recounting my own experience with this lab and my error analysis. 

In a first attempt at this lab I measured the following values: 
- $A =0.00975$ m$^2$
- $S =5.4\times 10^{-7}$ V$\cdot$ s
- $N= 5$

This resulted in a Magnetic field strength of $B = 11.1 \mu$ T. Using NOAA&rsquo;s website, I found that the horizontal $B$ field at my location was $24 \mu$T, such that my discrepancy was $13 \mu$T -- more than double my measurement!
####

Going back, I proceeded to calculate my error bounds on $A$. I assumed my accuracy  (using a poorly marked meter stick) was about $\delta A=1$cm$^2$. I then calculated the magnetic field for the upper and lower bounds on my Area and found:
$$
B = (11.1 \pm 0.1 ) \mu T
$$

The comparison between my value and NOAA&rsquo;s value was still *way off*. Because my value was *less than* the accepted one, and I was fairly confident in my values for S and N, I reasoned that the $B$ field in the room must be much weaker than outside.

I went back and repeated the experiment outside (you are not required to do this, of course, as long as you give an explanation of your discrepancy), and indeed: Broida hall, with its thick walls and metal beams, was screening the strength of the magnetic field! My new slope came out to $1.1 \times 10^{-6}$ V$\cdot$ s, giving me $B = (22.6 \pm 0.3 )\mu$T. 

####
The accepted value is not in these bounds, but it is **significantly** closer.  The remaining error, I reasoned, was probably due to the buildings and specific geography of my location, slight miscalibration of the gyroscope, or some slight wobbling of my iOLab since I was holding it with my hand, exposed to the wind.


## Part III: Write-up
 - For Part I, give a short summary of Faraday&rsquo;s Law, and describe what magnetic flux is.
 - For Part II, write a short paragraph describing the procedure taken and any important observations for each Exercise. Be sure to summarize your results, and reasons why you believe your data are precise and accurate. If you do not think your data are accurate, explain why, and how it could be fixed in a future lab.
 - You are encouraged to attach images of your plots,  data, and setup -- doing so may allow you to regain partial or full credit even if your experiment fails.
 - At the end of your write-up, please include the answers to all questions, clearly numbered. Show your work if applicable.