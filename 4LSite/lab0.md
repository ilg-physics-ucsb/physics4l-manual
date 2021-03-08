# Lab 0: Learning to use Phyphox


:::Materials 
- Your phone with the Phyphox App installed
  - See instructions in Part I
- A magnet
- Ruler
- Steel screw
:::

# The Phyphox App


:::RFigure Phyphox s
![The Phyphox Phone App in the iOS store](imgs/Lab0/phyphox.png)
:::

In this intro lab, we will learn how to use the Phyphox app to acquire data that we will later analyze. You can download the app from their [website](https://Phyphox.org/) or find it in the iOS/Google Play store. 

Phyphox allows you to use the sensors in your phone to measure quantities such as frequency, acceleration, and magnetic field strength. It also includes some additional modules with special functionality, such as acoustic stopwatches. Data can be exported in many common formats for quantitative analysis. Additionally, Phyphox on the phone can be controlled remotely from your desktop as long as they are on the same Wi-Fi network.

You are encouraged to play with Phyphox, explore its capabilities and the experiment ideas on the website, and take creative license with your investigations throughout the course. The instructions provided in each lab can be seen as a &ldquo;minimum&rdquo; requirement &ndash; the features of Phyphox go far beyond these suggestions. For example, you can try your hand at coding and making your own sensors by using the Phyphox API.

# Experiments
## 1. Overview
We will get familiar with the Phyphox app by investigating the external magnetic field of a magnet with your phone&rsquo;s magnetometer.
However, we actually need to know where the magnetometer even is! [Fi](#Fi-typical-phone) shows an image of a &ldquo;typical&rdquo; phone with a multitude of sensors. Unfortunately, this layout varies among device brands, models and even *versions* as increasingly innovative integrated circuit boards are manufactured.

::: LFigure typical-phone xs
![A Typical Phone with a vast array of sensors](imgs/Lab0/typicalphone.png)
:::

If we do not know the exact location of the magnetometer, it is difficult to make sense of magnetic field readings, whose strength varies with measurement distance. Our first task is, then, to find the location of the magnetometer on our phones. Since you will need to know this location for future labs, feel free to mark it with, for example, a small piece of tape.

After we find the exact location of the magnetometer, we will explore how Phyphox allows us to take *calibrated* and *uncalibrated* data, and which type to use in our experiments. Lastly, remember to subtract the background noise from the measurements before you move on to the data analysis.

:::Note
For  experiments, be mindful of the environment you are working in! An appropriate location may be a room with minimal electronic devices, or on top of a wooden/nonmetallic table. Be sure to remove any magnets and metals from the experiment area to minimize external fields.
:::







## 2. Get to know your magnetometer

::: Materials
- Your phone with Phyphox
- A magnet
- Steel screw
:::

Since we know that the field of a magnet is strongest near its poles, we will run a magnetized object around the phone to pinpoint where the reading is highest. It’s never in the center of the device, so you can’t make an accurate measurement just by moving a magnetic source toward or away from the face of your phone.  Usually, the magnetometer is located somewhere at the edge of the phone, and its exact location depends on the brand and model.

As mentioned in the note above, metallic objects around your phone may affect the reading you get. Nearby metal and magnets may make it difficult to pinpoint the magnetometer location, and are likely to interfere with future experiments that require quantitative data.

::: Question
Why would metal interfere with the calculation of magnetic field?
:::


You are now ready to begin [Ex](#Ex-mag-locate). Click on the arrow to expand the instructions.

:::::: Exercise mag-locate
Instructions for labs in this course will be in &ldquo;exercise&rdquo; boxes such as this one, with numbered steps to help you navigate the procedure. The easiest way to complete these labs successfully is to tackle each step in order, taking observational notes on each numbered step so that you have a record of what you&rsquo;ve done for your final write-up.

We will now describe the process you will  use to find the location of the magnetometer:
1. Find a steel screw (or another small object that can be magnetized, like a paperclip) and a magnet, and magnetize the screw by rubbing it with the permanent magnet.
2. Remove the magnet from your experiment area.
3. Move the tip across the surface of your phone until you get a strong reading as it reaches the magnetometer.

:::Note
 The magnetometer in your phone is extremely sensitive because it is designed to be used as a compass. It can easily resolve 50 µT, but it also saturates at few mT.  If you are using a neodymium magnet, it might easily saturate the sensor because of its strong fields. Make sure that the magnet is either weak enough or far enough from the sensor, that the field strength stays below 2 mT. Just check that if the magnet gets closer the readings can still increase.
:::

::::::

 
Now that we have found the location of the magnetometer, the next step is to gain a working knowledge of its features. On Phyphox, you can see that the magnetometer has a *calibrated* and *uncalibrated* mode. Think about which mode you should use for the purpose of measuring the magnetic field strength of a magnet.

::: Question
Define calibration in the context of a physics experiment. List a few reasons why calibration of all measuring devices is critical to *any* physics experiment.
:::
 
Since the magnetometer is very sensitive, any kind of unwanted magnetization will affect your measurements. Unfortunately, your phone is full of things that create magnetic fields and that can be easily magnetized. This is why the magnetometer is usually at the edge &ndash; to isolate it as much as possible. 

If your phone is exposed to a strong magnetic field, part of your device&rsquo;s integrated circuit might become magnetized, leaving your compass pointing in the wrong direction. Nearly every phone has some strategy to calibrate the magnetometer under these circumstances. You might trigger this when measuring the strength of a magnetic field. For your phone to make sure that the compass is working, it will automatically subtract the component from the external field to get calibrated data. This could be a problem if you try to measure a higher magnetic field on purpose.

:::::: Exercise 
Now make a magnetometer measurement by putting the magnet somewhere around your phone. Make sure the absolute field strength is 100 µT or more. Then you can rotate the phone about every axis while measuring, and if your phone applies a calibration to the reading, at some point the readings will suddenly drop (usually to around 50 µT, sometimes less). 

During calibration, the magnetometer uses the Earth&rsquo;s magnetic field in conjunction with its gyroscope to determine the relative orientation of its sensors. Since the $x$, $y$ and $z$ directions are mutually orthogonal, it analyzes how rotation along each of these axes affects the sensor measurement, to determine how these axes are aligned relative to the device. 
::: Question
For a phone that applies active calibration, why do you expect to see the change in readings?
:::
Therefore, for the purpose of measuring the *raw* strength of a magnetic field, you should switch to the *uncalibrated* magnetometer. 
::::::



## 3. Measure the direction and strength of a magnetic field with Phyphox

::: Materials
- Your phone with Phyphox
- A magnet
:::

####


<br>

In [Ex](#Ex-strengthanddirection), the magnet will provide an external magnetic field. Our first task is to characterize the magnet by measuring the *direction* of this field. Later, we will take care of the background noise to measure the *magnitude*.

:::::: Exercise strengthanddirection
First, let&rsquo;s identify the axes and directions of your magnetometer:
####

**Axis Determination Steps**
1. Open Phyphox and go to the "magnetometer" module.  You can see that there are three plots, representing $B_x$,  $B_y$ and $B_z$.
2. Identify which direction is geographic north in your room.
3. Rotate your phone so each of the three primary axes (short, medium, long) of your phone is aligned with geographic north [fn] Don&rsquo;t be alarmed if there are other nonzero components when your phone is facing geographic north! The magnetic field at a particular location actually fluctuates in inclination and direction a little. If you want to know precisely where the magnetic field points, you can look it up at on [NOAA](https://www.ngdc.noaa.gov/geomag/calculators/magcalc.shtml)[/fn]. 
4. Take note of which axis has the highest absolute reading &ndash; this specifies the axis of the magnetometer aligned with north.
####

:::Figure magnor s
![Hyperphysics: The magnetic north pole is the geographic south pole!](imgs/Lab0/magneticnorth.png)
####
Hyperphysics: The magnetic north pole is the geographic south pole!
:::

**Direction Determination Steps**
1. The $z$ direction of your magnetometer likely runs out of the face of your phone, so we will first test the sign of this axis.
2. Rotate your phone so that the back of it is facing geographic north.
3. If the reading is negative, the axis is defined so that the positive direction points *out of your phone screen*. You can understand this by imagining an arrow pointing from geographic south to geographic north.
4. Repeat for the remaining axes.



Now let&rsquo;s measure the direction of magnetic field from the  magnet.

**Measurement steps:**
1. Put your phone on the table, open the Phyphox app and go to “magnetometer.”
2. Start recording. You should see some random fluctuations on the plot. 
3. Hold the magnet above the magnetomer, with one flat side facing up. Move it up and down above the magnetometer.
4.  Now flip the magnet over, and repeat the motion.
5.  Stop recording to view the collected data. 

::: Question
1. Identify the axis name and sign in [Fi](#Fi-phonaxes) for your phone.
2. Why does $B_z$ change when you move the magnet vertically?
3. Describe the change you observed in the plot after you flipped the magnet, and give a possible explanation.

:::

::: Figure phonaxes m
![Label your axes, including sign](imgs/phoneaxes.png)
:::


By observing how $B_z$ changes with the vertical motion of the magnet, you should be able to identify the direction of the magnetic field. Mark one side with “⨂” to indicate that the magnetic field is going into that side, and the other side with “⨀” to indicate that the field is coming out of this side. You will use these magnets for other labs this quarter.

::: Question
 Explain how you determined the magnet&rsquo;s polarity from your data, *i.e.*, how you decided which sides represent the magnet&rsquo;s north (⨀) and south (⨂) poles. 
:::


::::::

## 4. Measure the field around a magnetic source
:::Materials
- Your phone
- A magnet
- Ruler
- Steel screw
:::




In [Ex](#Ex-strengthanddirection), we asked you to identify the poles of your permanent magnet and make some qualitative observations about how field strength behaves as you move the magnet above the magnetometer. 
:::RFigure bar_magnet xs
  ![The magnetic field of a bar magnet has the characteristic of a &lsquo;dipole,&rsquo; in that its strength falls off more slowly in the direction perpendicular to its polarized axis, than along its axis. From far away, the behavior looks similar to that of a monopole](imgs/Lab0/BarMagnetFieldFRONT.png)
:::
We will now make a more quantitative measurement of the field surrounding the magnet. Unlike electric charges, magnetic charges do not exist as &ldquo;monopoles&rdquo; with a spherically symmetric magnetic-field, in our universe [fn] At least as far as we know! See [Wikipedia](https://en.wikipedia.org/wiki/Magnetic_monopole#Searches_for_magnetic_monopoles)[/fn]; the poles must always come in equal and opposite pairs, and the surrounding field is therefore changed. 



Permanent magnets themselves are made of ~$10^{24}$ tiny atomic dipoles, and hence their measurable fields are actually the sum of all of these individual contributions. The size and geometry of a magnet, therefore, ultimately determine the character of its field.

Measurements of disk and bar-like magnets from close (but not *too* close) distances reveal that the field is approximately dipolar itself, as shown in [Fi](#Fi-bar_magnet). However, despite the &ldquo;dipole&rdquo; (and higher order, *e.g.* &ldquo;quadrupole&rdquo;) contributions to the field from the magnet&rsquo;s shape, along the axis that runs through the poles of a magnet, the field behaves much like a &ldquo;monopole&rdquo;&ndash; similar to the electric field of a single electric charge. In this experiment, we will investigate how the magnetic field along the axis running through the center of your neodymium magnet disk behaves as a function of distance.

::: Question

1. Theoretically, how might the strength of the magnetic field (along your magnet&rsquo;s $z$-axis) depend on distance from the source? Your answer should be written as a proportionality, $B(r)\propto...$.  (You don&rsquo;t need to specify the proportionality constant.)

2. Devise a quick experiment that could verify this, and sketch a plot of the expected result. 

3.  Based on the relationship between strength and distance proposed in (a), say that you doubled the distance from $r$ to $2 r$.  How would this change the resulting field strength?
:::


:::::: Exercise
As your final exercise in getting familiar with the magnetometer, you will attempt to verify your prediction quantitatively.

It should be emphasized that since we are using the uncalibrated magnetometer, you have to **subtract the background** from the measurements. The background includes Earth&rsquo;s magnetic field and local fields from nearby electronic devices and metals.

:::Note
 Be careful! Do not to move or rotate your phone between data aquisitions, because this would change the background contribution.
:::

####

**Magnetic Force and Distance steps:**
1. Mark 0.0 cm, 0.5 cm, 1.0 cm, 2.0 cm, and 4.0 cm on a piece of paper. Align the edge of your phone nearest to the magnetometer with the 0 cm mark
2. Start a measurement without the magnet (place the magnet far from your work area) and record the values. 
3. Magnetize a steel screw and align it with the 0.5 cm mark.
4. Record about 1 second of data and stop.
5. Double the distance to 1 cm, 2 cm, 4 cm, and record 1 second of data each.
6. Export the data. For each measurement made above, calculate the average of the 1-second interval, and record the average field strength and the distance of the measurement in a table.
:::Figure
![Example set up for measuring magnetic strength vs. distance](imgs/Lab0/setup.png)
:::

:::Question 
For each doubling, calculate the ratio of the magnetic field $B(2r)/B(r).$ You should have three ratios for 4 data points.

1. Do the ratios match your expectations from Question 6c? 

2. Do some ratios match better than others?

3. Propose an explanation for part (b). Consider things such as the nature of the magnetic field (Should the measurement be more accurate closer to or farther from the device?), as well as experimental corrections like the exact location of the magnetometer (Is it exactly at where you labeled? What effect might an offset have on your data?).
:::
::::::
# Write-up

###  **@fa-hand-o-right@  Instructions :**
 #### **1. Answer all questions clearly, showing your work where appropriate.**
 #### **2. Starting on a seperate page:** 
  - Write a short summary (~1 page, single spaced) describing the important concepts of the lab, what you did, and any important observations. 
  - In this summary, be sure to **summarize your results** and **reasons why you believe your data are precise and accurate**. If you do not think your data are accurate, explain why, and how this could be fixed in a future lab.

 #### **3. Additional Information:**
 - You should attach images of your plots,  data, and setup.  Doing so may allow you to regain partial or full credit even if your experiment fails.
 

:::Summary

<iframe id="contentframe" height="500px" width="100%" src="https://gauchospace.ucsb.edu/courses/mod/lti/launch.php?id=5682337&triggerview=0" allow="microphone https://coursekit.google.com; camera https://coursekit.google.com; geolocation https://coursekit.google.com; midi https://coursekit.google.com; encrypted-media https://coursekit.google.com; autoplay https://coursekit.google.com" allowfullscreen="1" style="height: 500px;"></iframe>

:::



# Feedback

Any feedback you choose to give will be used to improve labs this quarter!
::: Hider Open Feedback Form
<iframe src="https://docs.google.com/forms/d/e/1FAIpQLSfAhZHIlwtGnfv3XMpzTs043ZUjluKyanJWl-hFrU9KCgvswQ/viewform?embedded=true" width="100%" height="1000" frameborder="0" marginheight="0" marginwidth="0">Loading…</iframe>
:::

<br>
<br>
<br>
<br>