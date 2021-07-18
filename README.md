# Estimating the age of star clusters

This project was done when I was one of the coordinators of Horizon, The Physics and Astronomy Club of IIT Madras

## Long story short
- Go to the SDSS website and get the spectral data of a star cluster or Get the required data using DS9 manually
- Plot the Color magnitude diagram (HR Diagram)
- Employ Isochrone fitting to get the age and metallicity of that star cluster

## Color Magnitude diagram
![HR Diagram or the Color Magnitude diagram](https://github.com/Manaswini1832/Estimating-the-age-of-star-clusters/blob/master/images/hr_diagram.jpg)
- It is a plot of the star/cluster's luminosity/brightness against ‘color’.
- The color of a star tells us about its surface temperature.
- The HR diagram (or CMD) gives us a glimpse of the life cycle of stars.

## Why study the HR diagram ?
- It helps us gain insights into the star’s color, temperature and its luminosity
- It also helps us estimate the age of star clusters

To employ the method of estimation of the age of the star clusters, we first need information about two things : Luminosity and Temperature i.e. Color of the stars.

## Finding the Luminosity
- Absolute magnitudes are the way to go
- Absolute magnitude is defined as the magnitude that a star would have if you saw it from a distance of 10 parsecs (about 32 light-years)
> M = m + 5 - 5log( d )\
> where M = absolute magnitude\
> m = Apparent magnitude\
> d = distance to the object in parsecs

We collected information about the above mentioned apparent magnitudes of stars from the open sourced [SDSS database](https://en.wikipedia.org/wiki/Sloan_Digital_Sky_Survey)

## Filters
- A filter is a screen that blocks out all light except for light with a specific color or a specific wavelength.
- SDSS uses five filters : u, g, r, i, z\
![SDSS filters information](https://github.com/Manaswini1832/Estimating-the-age-of-star-clusters/blob/master/images/sdss_filters.png)
Image taken from the [SDSS website](http://skyserver.sdss.org/dr1/en/proj/advanced/color/sdssfilters.asp)

## How to get the temperature ?
- Color of stars is the way to go
- In astronomy, a star's color is defined as the difference between its magnitudes as seen through two different FILTERS.
- More information available [here](https://tinyurl.com/y52xagj4)

We then collected all the data needed for different star clusters from the SDSS database and plotted their color magnitude diagrams.

## Data collection
We collected data using two methods
1) From the SDSS database using SQL search
2) Manually from DS9

## Collecting data manually from DS9
Following are the screenshots taken while collecting data manually using DS9 using the FITS files obtained from the SDSS website, for different star clusters.\
![DS9 Regions first screenshot](https://github.com/Manaswini1832/Estimating-the-age-of-star-clusters/blob/master/images/ds9_regs1.jpeg)\
![DS9 Regions second screenshot](https://github.com/Manaswini1832/Estimating-the-age-of-star-clusters/blob/master/images/ds9_regs2.jpeg)

## Result of plotting the Color magnitude diagram of the M5 Cluster
![M5 Cluster's color magnitude diagram](https://github.com/Manaswini1832/Estimating-the-age-of-star-clusters/blob/master/images/cmd_m5.png)

## Isochrones
- Helps model our understanding of stellar evolution
- A given isochrone can directly be linked to its initial conditions ( age and metallicity in our case )
- Vary age or metallicity and do ISOCHRONE FITTING
- The one matching our plot gives us the age and metallicity of our star cluster
- Isochrones generated by the [Dartmouth Isochrone generator](http://stellar.dartmouth.edu/models/isolf_new.html) and few lines of Python helped us do isochrone fitting

## Isochrone fitted plot
Following is the isochrone generated by the Dartmouth Isochrone generator that almost resembles the color magnitude diagram obtained for the M5 cluster\
![Isochrone fitted plot of the M5 cluster](https://github.com/Manaswini1832/Estimating-the-age-of-star-clusters/blob/master/images/Isochrone%20fitting.png)

The above isochrone corresponded to an initial age of 10 Gyrs. Therefore the estimated age of the M5 cluster is 10 Gyrs

