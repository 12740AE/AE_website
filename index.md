# Welcome to Smart Dorm/Home Security 

<p align="center">
  <img src="./image/first_pic.jpeg" width="350">
</p>

**Video link:**  

**Progress report link:** [Progress Report](https://12740ae.github.io/progress-report/)


## 1. Introduction


### 1.1 Motivation

Dorm rooms and college shared-living spaces are unfortunately common settings for theft. They usually have minimal security, if any, but college students store a plethora valuables here: laptop, phone, passport/SS card, cash, electronics, gaming platforms, just to name a few. Sometimes a simple door lock is not enough to deter the average thief- and what if the thief is a cohabitant? Burglary incidents vary between colleges, but in some cases, victims can be as common at 13% of the student population[1]. Consumer Report even provides reviews on dorm insurance, and homeowners policies can also be extended to children on a college campus. Improving dorm room/living space security and oversight is important and a key step to prevent the ubiquitous issue of thievery. 


### 1.2 Goals

We are interested in using sensors to help us learn about the security of our living spaces by providing remote ways to monitor our front doors. 
Our objective is to achieve the following with sensors:
  1.)Record the time and date when the door is opened and closed for review at a later time
  2.)Provide visual feedback when the door has been completely and successfully locked
It will be important to maintain a record of time/date so if there is an intruder, a user can specify the time and date of when the crime took place. Additionally, individuals who live together can compare the timestamps to identify if there is an intruder by verifying the timestamps with their own knowledge of when they enter/exited the space. 
Additionally, many students agree that it would give them peace of mind to see that the door is indeed locked as they leave the property. Sometimes, we can even forget to lock the door. By providing a visual feedback such as an LED light to signify that the door is locked, a person standing several feet away can verify that they did indeed lock the door. 

## 2. Methodology

### 2.1 Phenomena of Interest

**Acceleration**

*Physical Principles*

With the accelerometer, we are measuring acceleration, or change in velocity of an object. Acceleration, in physics, is a vector quality and has a direction and magnitude as a result. Change in either the direction or magnitude will result in positive or negative acceleration. 

Acceleration is measured in g or G, which is equal to about 32.2 feet per second[2]. The g provides a measure of stress that a body would experience if it was accelerated at so many times the Earth’s gravitational pull. To give a frame of reference, the average playground swing can produce about 2g, or two times the earth’s gravitational force at the bottom of the swing path. In our scenario, closing a door leisurely or even slamming it would produce around the same amount of g at the edge of the door where the moment arm (from the door hinge as the pivot point) is the greatest, and so are the forces acting on the door. 

*Signal Characteristics and Static/Dynamic Behavior*

Acceleration is found mainly as gravity or the result of a net force. Acceleration from gravity is a (fairly- since gravity technically varies at different times and places) static physical property that all items exhibit when there isn’t a normal force to neutralize the Earth’s gravitational pull. Static acceleration as gravity can be used to measure if an object of interest is stationary but tilting. Dynamic acceleration is observed when a net force is applied to an object, causing time-varying change in direction or velocity, such as in the case of the object in motion or experiencing vibrations.

**Infrared Radiation**

*Physical Principles*

Infrared or IR is a kind of radiation emitted by almost all objects, and is emitted as heat energy. It’s part of the electromagnetic (EM)  spectrum, which also includes gamma-rays, x-rays, UV radiation and visible light[3]. EM radiation is created by electric and magnetic oscillation fields perpendicular to each other as well as charged particles traveling in space[4]. 

*Signal Characteristics and Static/Dynamic Behaviors*

IR frequencies range between 3 GHz and up to 400 THz, and wavelengths between 1000 micrometers and 760 nanometers for each complete cycle. The unit of measurement is most commonly the wavelength, in micrometers. IR radiation emitted by humans is steadily within .75 to 1000 micrometer and averages at 12 micrometers, all of which are values around the median of the IR spectrum. For warm-blooded animals, including humans, the main form of IR radiation produced would be in the form of thermal radiation[5].

IR radiation is a fairly dynamic phenomena. IR as heat and less obvious forms of radiation are found in everything from household heating appliances such as toasters to communication signals between the TV and its remote controller. In perfectly insulated environments, it is possible to maintain a level of IR radiation so it may behave statically, however, this is an idealized situation that is seldom found in the natural world.

**Visible Light**

*Physical Principles*

Visible light is also part of the electromagnetic spectrum, at higher frequencies that IR radiation discussed previously. As shown in Figure 1, the wavelengths for visible light range between 400 -700 nm, and the most common measurement for visible light is its wavelength, in nanometers. All waves in the electromagnetic spectrum travel as the speed of light, commonly known as coefficient c.  

<p align="center">
  <img src="./image/new1.png" width="500">
</p>

<p align="center">
 Figure 1: Diagram showing the entire electromagnetic spectrum[6]
</p>

*Signal Characteristics and Static/Dynamic Behaviors*

Light has natural and artificial sources, including the Sun, fluorescent lamps, incandescent bulbs, LEDs and so on. Most light sources use the at least some part of the full spectrum of visible light but may be skewed towards particular wavelengths of light (Figure 2). Natural light does contain the full spectrum.

<p align="center">
  <img src="./image/new2.png" width="500">
</p>

<p align="center">
Figure 2 : Emission spectrum analysis showing intensity of each wavelength in visible light spectrum for natural light (left), and incandescent light (right)[7]
</p>

The average spectra observed may be different as a result from the skewed/favoring behavior of different light sources. When light is emitted at a wavelength, the signal characteristics (wavelength, amplitude, frequency, speed) are static, unless the positioning of the light source or the light source itself is modified. 

Another characteristic of visible light is light intensity. Light is measured with respect to direction and strength. Luminous flux is the “total amount of light emitted in all directions by a light source”, and is measured in lumens. Luminous intensity is also called luminance, and described by the strength of the light visible to the human eye. Luminance is measured in candela or lumens/steridian to represent intensity of the light through a unit area of the light source’s surface (i.e. the light bulb surface). Illuminance on the other hand, is measured in lux and describes the amount of light being projected/reflected onto a given surface area (such as is the case in indirect light)[9].

**Distance**

*Physical Principles*

Physical distance can use an array of measurements that provide some approximation of the space between at least two entities. It most commonly has units in feet-inches and meters.

*Signal Characteristics and Static/Dynamic Behaviors*

Distance can be dynamic if the position of any entities are moved; differential distance, or distance that changes with respective to time is derived as velocity. If no work is done in a system, the distance between entities is usually static. 

**Force**

*Physical Principles*

Force is the “push or pull upon an object resulting from the object’s interaction with another object”[10]. The unit of force is the Newton, which is equal to 1 kg-m/s2, representing the relationship of force as the driving entity behind a 1 kg mass accelerating at 1 m/s2. From modern kinematics, force is presented as a vector quality with a magnitude and direction. 

*Signal Characteristics and Static/Dynamic Behaviors*

Dynamic and static forces are represented in physical systems as bodies in motion or still. For example, a ball rolling along a plank exerts gravitational force (weight) across the length of the plank, so the load varies over time.

 A static load is constant over time, such as a ball sitting still at the end of the plank. Under static, unchanging force, a body can only respond by being displaced, while dynamic forces acting on a body can change the body’s displacement, velocity, and acceleration (these are time varying)[11].

## Sensors Used

**Accelerometer**

**Model: ADXL 335**

*Physical Principles*

The accelerometer used has small capacitive plates within the chip, creating a differential capacitor. Differential capacitance is described mathematically as follows:

 <img src="./image/new22.png" width="500"> Equation1



## 5. Reference
Ada, Lady. “PIR Motion Sensor.” Adafruit Learning System, [learn.adafruit.com/pir-passive-infrared-proximity-motion-sensor/how-pirs-work](learn.adafruit.com/pir-passive-infrared-proximity-motion-sensor/how-pirs-work)

Adafruit. “BISS0001 Micro Power PIR Motion Detector IC.” Adafruit Learn, cdn-learn.adafruit.com/assets/assets/000/010/133/original/BISS0001.pdf.

Analog Devices. Accelerometer Specifications - Quick Definitions. www.analog.com/en/products/landing-pages/001/accelerometer-specifications-definitions.html.

Analog Devices. “Small, Low Power, 3-Axis ±3 g Accelerometer Datasheet.” ADXL 335, 2010, www.analog.com/media/en/technical-documentation/data-sheets/ADXL335.pdf.

“Arduino HC-SR501 Motion Sensor Tutorial.” Henry's Bench, 10 Feb. 2018, henrysbench.capnfatz.com/henrys-bench/arduino-sensors-and-input/arduino-hc-sr501-motion-sensor-tutorial/.

Bicycle Helmet Safety Institute. “What's a g?” What Is a g? Acceleration?, Feb. 2019, www.helmets.org/g.htm.

Brookshire, Bethany. “Scientists Say: Infrared.” Science News for Students, Aug. 2018, www.sciencenewsforstudents.org/blog/scientists-say/scientists-say-infrared.

Burnett, Roderick. “Understanding How Ultrasonic Sensors Work.” MaxBotix Inc., Publisher Name MaxBotix Inc.Publisher Logo, 16 Sept. 2019, www.maxbotix.com/articles/how-ultrasonic-sensors-work.htm.

ELEC Freaks. Ultrasonic Ranging Module HC - SR04. Mouser Electronics, 2019, www.mouser.com/datasheet/2/813/HCSR04-1022824.pdf.

ElectronicsTutorial. “Introduction to Capacitors, Capacitance and Charge.” Basic Electronics Tutorials, 15 Sept. 2018, www.electronics-tutorials.ws/capacitor/cap_1.html.

EO Edmund Optics. “Optical Filters: Edmund Optics.” Edmund Optics Worldwide, www.edmundoptics.com/resources/application-notes/optics/optical-filters/.

Ibrahim, Syed. “Static and Dynamic Forces.” Research Gate, Research Gate, Aug. 2014, www.researchgate.net/publication/311807851_Static_and_dynamic_forces.

Interlink Electronics. “Force Sensitive Resistor Integration Guide and Evaluation Parts Catalog.” 400 Series Evaluation Parts , cdn-learn.adafruit.com/assets/assets/000/010/126/original/fsrguide.pdf.

Konica Minolta. “Luminance vs. Illuminance.” Konica Minolta Sensing Americas, 2019, sensing.konicaminolta.us/blog/luminance-vs-illuminance/.

Last Minute Engineers. “How HC-SR501 PIR Sensor Works & How To Interface It With Arduino.” Last Minute Engineers, Last Minute Engineers, 7 Dec. 2018, lastminuteengineers.com/pir-sensor-arduino-tutorial/.

LEC Expert. “Units of Light.” LEC, Nov. 2015, www.lec-expert.com/topics/units-of-light.

Lee Shuk-Ming, Olivia. “Radiation Emitted by Human Body - Thermal Radiation.” Radiation, Sept. 2010, www.hko.gov.hk/education/edu02rga/radiation/radiation_02-e.htm.

Libretexts. “Electromagnetic Radiation.” Chemistry LibreTexts, Libretexts, 5 June 2019, [https://chem.libretexts.org/Bookshelves/Physical_and_Theoretical_Chemistry_Textbook_Maps/Supplemental_Modules_(Physical_and_Theoretical_Chemistry)/Spectroscopy/Fundamentals_of_Spectroscopy/Electromagnetic_Radiation](https://chem.libretexts.org/Bookshelves/Physical_and_Theoretical_Chemistry_Textbook_Maps/Supplemental_Modules_(Physical_and_Theoretical_Chemistry)/Spectroscopy/Fundamentals_of_Spectroscopy/Electromagnetic_Radiation)

Luna Optoelectronics. “CDS Photoconductive Photocells.” Lunainc.com, 2016, [https://media.digikey.com/pdf/Data%20Sheets/Photonic%20Detetectors%20Inc%20PDFs/PDV-P9003.pdf](https://media.digikey.com/pdf/Data%20Sheets/Photonic%20Detetectors%20Inc%20PDFs/PDV-P9003.pdf)

Navarro-Cia, Miguel. “Pyroelectric-Sensor-a-Sketch-of-the-Pyroelectric-Sensor-with-an-Integrated-Resonant.” Research Gate, Feb. 2016, www.researchgate.net/figure/Pyroelectric-sensor-a-Sketch-of-the-pyroelectric-sensor-with-an-integrated-resonant_fig3_294873294.

Orzel, Chad. “Football Physics: Putting G-Forces In Perspective.” Forbes, Forbes Magazine, 9 Nov. 2015, www.forbes.com/sites/chadorzel/2015/11/08/football-physics-putting-g-forces-in-perspective/#40fc0a41766e.

Pan, A., and X. Zhu. “Photoconductivity.” Photoconductivity - an Overview | ScienceDirect Topics, 2015, www.sciencedirect.com/topics/chemistry/photoconductivity.

Pederson, Tracy. “What Is Infrared?” LiveScience, Purch, 2019, www.livescience.com/50260-infrared-radiation.html.

The Physics Classroom. “The Meaning of Force.” The Physics Classroom, 2019, www.physicsclassroom.com/class/newtlaws/Lesson-2/The-Meaning-of-Force.

Pujol, Rémy. “Journey into the World of Hearing - Specialists.” Cochlea- Hearing Ranges, 6 June 2018, www.cochlea.org/en/hear/human-auditory-range.

“Pyroelectricity.” ScienceDaily, ScienceDaily, www.sciencedaily.com/terms/pyroelectricity.htm.

Radford, Max, and Francis Riemensperger. “The Electromagnetic Spectrum.” Mini Physics, 22 May 2016, www.miniphysics.com/electromagnetic-spectrum_25.html.

Smith, Daniel. “Calculating the Emission Spectra from Common Light Sources.” COMSOL Multiphysics, Jan. 2016, www.comsol.com/blogs/calculating-the-emission-spectra-from-common-light-sources/.

