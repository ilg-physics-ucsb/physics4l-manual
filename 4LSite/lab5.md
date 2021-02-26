# Lab 5: Planck's Constant 

::: Materials
- Red, Blue, Green, Yellow LEDs
- Power Block
- Breadboard and Wires
- Potentiometer
- 220 $\Omega$ resistor (or 2 100$\Omega$ resistors)
- Multimeter
:::


# Light, Photons, and Planck's Constant 

By now you've learned that light is, fundamentally, electromagnetic radiation: mathematically, it is wave a solution to Maxwell's equations that features oscillating electric and magnetic fields that propagate through space. This classical picture of light if useful for many applications of optics, and provides an accurate description that is testable (as you have seen in the previous microwave lab). As you are nearing the completion of your introductory physics education, we now shift to looking beyond the classical behavior of physics and delving into the *quantum*.

The nature of light, as physicists learned in 1905, is not actually classical at the microscopic level. As it turns out, quantum mechanics dictates that energy is quantized, and hence that light has a *particle* nature. We call these particles that carry electromagnetic energy **photons**.


:::RFigure ledp m
![In the photoelectric effect, electrons can be ejected from a conductor if the incident light is above some threshold frequency corresponding to the *binding energy* of the electron in the valence orbital. If the frequency is less than this threshold, ejection will not occur regardless of the light's *intensity*.](../imgs/Lab5/pee.png)

In the photoelectric effect, electrons can be ejected from a conductor if the incident light is above some threshold frequency corresponding to the *binding energy* of the electron in the valence orbital. If the frequency is less than this threshold, ejection will not occur regardless of the light's *intensity*.
:::
In 1905, Einstein published a seminal paper explaining the *Photoelectric Effect* using the notion of photons, and soon earning him his first Nobel Prize. The Photoelectric Effect is the observation that electrons are ejected from some materials (typically metals) when light is shone on its surface; however, the rate the electrons are ejected from the metal is not entirely proportional to the *intensity*, or the amount of light, as you might expect -- electrons seemed to only respond to light above a certain cut off frequency. This cut-off frequency is the the frequency at which a photon carries energy *equal to or grather than* the binding energy between the electron and the nucleus of the atom. 

This discovery inevitably led to the development of Quantum Theory, and the notion of photons as the quantum mechanical carriers of electromagnetic energy.  Planck's constant gives the proportionality between frequency and energy for photons in the Planck-Einstein Relation:
:::Equation per
$$
E= h \nu
$$
:::

## LEDs

The determination of Planck's constant was fairly difficult in the early 20th century: it was first laboriously calculated by Planck in an elaborate *black body radiation* experiment, which requires deep knowledge of statistical physics and laboratory technique. Today, luckily, we can measure it quite easily due to advances in solid-state circuitry and the invention of the light-emitting diode (LED)

:::LFigure ledp l
![](../imgs/Lab5/ledp.jpg)
####
A cartoon of electrons subjected to a voltage, forcing them across the gap where they emit a photon
:::
LEDs are specially manufactured semiconductor devices which basically accomplish the photoelectric effect in reverse. An LED contains layers of two different semiconductor materials with special energy levels that are "doped". While the theory of semiconductors is far beyond the scope of this course, and is better treated in a solid-state physics class, we will briefly sketch the fundamental process that leads to photon emission below.



At small voltages, the boundary of the materials in the LED acts similar to a capacitor: electrons are not able to flow between the layers freely, and accumulate on the surface. Unlike capacitors, however, once the voltage is increased beyond a threshold, electrons gain enough energy to "jump" across the material boundary. After the electron crosses this "gap", it has extra energy that dissipated by producing a photon of a specific frequency. The frequency of the photon is determined by the kinds of materials and chemical treatments the semiconductor is subjected to. 

We can associate the threshold voltage needed to cause electrons to "jump the gap" with the gap energy as:

:::Equation led
$$
E_{gap} = e V_{th}
$$
:::

Despite the complicated things that happen on a microscopic level, indeed the simple, naive, form of [Eq](#Eq-led) is actually true to a decent level of precision! We can then combine this relation with [Eq](#Eq-per) to obtain the functional equation

:::Equation ledper
$$
e V_{th} = h \nu
$$
:::

[Eq](#Eq-ledper) has two unknowns: $\nu$ and $V_{th}$. Luckily, we can measure the peak wavelength of the LED light for each provided component,  meaning that if then measure $V_{th}$, we can determine Planck's constant as:

:::Equation planck
$$
 h = \frac{e V_{th} \lambda}{c}
$$
:::


For the LEDs supplied in the RexQualis kit, the following Table shows the wavelength of the dominant peaks and its error:
:::Table
| Color|$\lambda$ (nm) | $\delta \lambda$ (nm)|
| ------| ------| ------ |
| Red  | 625| $\pm$ 5 |
|Yellow|592| $\pm$ 3 |
|Green |517| $\pm$ 3 |
|Blue |465| $\pm$ 5 |
:::

If you do not have these LEDs, it is acceptable to use these values and make a note in your analysis of the results. 

# Using an LED to measure $h$




::: Materials
- Red, Blue, Green, Yellow LEDs
- Power Block
- Breadboard and Wires
- Potentiometer
- 220 $\Omega$ resistor (or 2 100$\Omega$ resistors)
- Multimeter
:::

In this part of the lab, we will set up the basic experiment which will allow us to measure $V_{th}$ for each of the LEDs. Since our power block does not allow us to modulate the voltage through the LED, we will use the 10k trim pot as a **voltage divider**, allowing us to interpolate between a continuous range of voltages using the analogue dial. The trim pot will be connected in series with a **current limiting** resistor to ensure that we do not blow out the LEDs, which can handle a maximum current of $30$ mA.

::::::Question
The potentiometer in your kit is a variable-range resistor. The resistance between lead 1 and 3 is always approximately $10$ k$\Omega$. As you turn the dial, the resistance between leads 1 and 2 ranges from approximately $0 \Omega$ and $10$ k$\Omega$

:::Figure vrr xl
![A variable resistor functions like two resistors in series whose values always adds up to the total resistance. Adjusting the wiper only affects the resistance between leads 1 and 2](../imgs/Lab5/vrr.jpg)

A variable resistor functions like two resistors in series whose values always adds up to the total resistance. Adjusting the wiper only affects the resistance between leads 1 and 2
:::

In [Ex](#Ex-led), we will use the potentiometer as a voltage divider by connecting 1 to 3.3V, 3 to ground, and 2 to a $220 \Omega$ resistor attached to the load.

:::Figure cd m
![](../imgs/Lab5/planckexp.png)
:::
 
 1. As a function of resistance between 1 and 2, $R_{1}$, the total resistance of the potentiometer $R_{tot}= 10$ k $\Omega$, and the current-limiting resistor $R_L= 220 \Omega$ calculate the voltage across the LED. 

 2. What are the maximum and minimum voltages obtainable and what $R_{1}$ corresponds to them?

 3. What value of $R_{in}$ would produce 1.5V across the LED?

::::::

::::::Exercise led
In this exercise, you will construct a circuit to observe the turn on voltage of various LEDs.

:::Figure circuit m
![Example of a wrapped coil with the final loop tucked to keep it tidy](../imgs/Lab5/SimpleSetup.jpg)
:::
**Setup:**
1. Using [Fi](#Fi-circuit) as a guide, connect lead 1 of your potentiometer to the positive rail and lead 3 to the negative rail. Used in this fashion, your potentiometer acts as a **voltage divider**.
2. Connect your $220 \Omega$ resistor in series with lead 2 of the potentiometer. 
3. Place your colored LEDs in different rows, with their negative end in the negative rail.  
4. Connect your multimeter to the negative rail and the  $220 \Omega$ resistor row, and turn it on in Voltage mode
5. Run a jumper wire from your $220 \Omega$ resistor to one of the LEDs 
6. Turn on your power block and rotate the potentiometer dial until you see the LED just barely lit
7. Record the value of the voltage across the LED in a table like the one below
:::Table
 
| Color|$\lambda$ | $\nu$ |$V_{th}$|
| ------| ------| ------ |------| 
|@fa-pencil@       |        |         |        |
|@fa-pencil@     |        |         |        |

:::
8. Repeat for all LED colors.

::::::
::::::Question
1. Present your table of data, with an additional column showing the calculated value of $h$ for each LED
:::Table
 
| Color|$\lambda$ | $\nu$ |$V_{th}$|$h$|
| ------| ------| ------ |------|------| 
|@fa-pencil@       |        |         |        |       |
|@fa-pencil@     |        |         |        |       |

:::
2. Are your calculated values higher or lower than the accepted value of $h$?
3. Comment on why you think your values are higher or lower.
::::::

# Improving the measurement of $h$




::: Materials
- Red, Blue, Green, Yellow LEDs
- Power Block
- Breadboard and Wires
- Potentiometer
- 220 $\Omega$ resistor (or 2 100$\Omega$ resistors)
- Multimeter
:::



::::::Exercise led2
We will refine the measurement of $h$ by performing the measurement multiple times, and identifying the value of $h$ from a linear relationship.

**Steps:**
1. Repeat the steps of [Ex](#Ex-led), but take **5** measurements for each LED color, resetting the potentiometer to 0V between each trial.
2. Calculate the **average** turn on voltage, $\bar V_{th}$ for 5 trials, as well as the **standard deviation**, $\delta V_{th}$  . 
3. Record these values in a table like the one below

:::Table
 
| Color|$\lambda$ | $\nu$ | $\bar V_{th}$| $\delta V_{th}$ |
| ------| ------| ------ |------| ------| 
|@fa-pencil@       |        |         |        |        |
|@fa-pencil@     |        |         |        |        |

:::
8. Repeat for all LED colors.

::::::

::::::Question
1. Present your table of data, with two additional columns showing the calculated value of $\bar h$ for each LED, and the standard deviation of $h$. 
    :::Table
    | Color|$\lambda$ | $\nu$ | $\bar V_{th}$| $\delta V_{th}$ |$\bar h$| $\delta h$ |
    | ------| ------| ------ |------| ------| ------| ------| 
    |@fa-pencil@       |        |         |        |        |       |        |
    |@fa-pencil@     |        |         |        |        |       |        |

    :::
    The standard deviation of a product $A=XY$ is calculated as
    $$
    \frac{\delta A}{A} = \sqrt{ \Big(\frac{\delta X}{X}\Big)^2 + \Big(\frac{\delta Y}{Y}\Big)^2}
    $$
2. Make a single scatter plot containing 
    - $\bar V_{th}$ v.s. $\nu$, 
    - $(\bar V_{th} + \delta V_{th})$ v.s. $\nu$ 
    - $(\bar V_{th} - \delta V_{th})$ v.s. $\nu$. 

    The later two plots are effectively showing the *error bars* on your first plot. You may use google sheets to do this.
3. From the equation relating $V_{th}$ and $\nu$, what is the significance of the slope of this plot? Calculate the accepted theoretical value
3. Find the value of the slope for the line of best fit for $\bar V_{th}$ v.s. $\nu$. How does it compare to the accepted value you calculated?  
4. What value of $h$ does your slope indicate? 
5. Does your line of best fit intercept the origin? Explain what this means and provide some reasons for the observation.
6. Is the calculation of $h$ from your slope more accurate than the individual measurements? Why do you think this is?
::::::


:::Question

1. Which source of uncertainty, $\delta V_{th}$ or $\delta \lambda$, do you think influences the *precision* of your results more? Explain.
2. Which do you think influences your *accuracy* more? Explain.
:::



# Write Up

###  **@fa-hand-o-right@  Instructions :**
 #### **1. Answer all questions clearly, showing your work where appropriate.**
 #### **2. Starting on a seperate page:** 
  - Write a short summary (~ 1 page, single spaced) describing Planck's constant, how you tested it, and any important observations.
  - In these summaries, be sure to **summarize your results** and **reasons why you believe your data are precise and accurate**. If you do not think your data are accurate, explain why, and how this could be fixed in a future lab.

 #### **3. Additional Information:**
 - You should attach images of your plots,  data, and setup.  Doing so may allow you to regain partial or full credit even if your experiment fails.


::::::Summary
  :::Hider Lab Submission
  <iframe id="contentframe" width="100%" src="https://gauchospace.ucsb.edu/courses/mod/lti/launch.php?id=6277672&forceview=0" allow="microphone https://coursekit.google.com; camera https://coursekit.google.com; geolocation https://coursekit.google.com; midi https://coursekit.google.com; encrypted-media https://coursekit.google.com;" allowfullscreen="1" style="height: 500px;"></iframe>
 :::
::::::

# Feedback

Any feedback you choose to give will be used to improve labs this quarter! Feedback is not required on all questions. If you&rsquo;d like just to leave some comments, scroll to the bottom of the form.
::: Hider Open Feedback Form
<iframe src="https://docs.google.com/forms/d/e/1FAIpQLSfwRMJCLOQqad_xstc9veot0WyzSmMH3XCGxQ_918RWt0KvgA/viewform?embedded=true" width="100%" height="1000" frameborder="0" marginheight="0" marginwidth="0">Loading…</iframe>
:::
