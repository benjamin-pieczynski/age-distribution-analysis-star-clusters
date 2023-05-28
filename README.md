# age-distribution-analysis-star-clusters
Star Cluster Age Distribution notebook for analysis of spiral structure in galaxies. This project makes use of the Legacy Extragalactic UV Survey data found here https://archive.stsci.edu/prepds/legus/dataproducts-public.html. You can learn more about the LEGUS project here https://legus.stsci.edu/.

# About this project
This project was a revisitation to my undergraduate research studying the mechnaism of spiral structure in galaxies using star cluster age distributions relative to the apparant spiral arms. During a graduate level galaxies class we were given a final project of our own choosing to showcase what we learned in the course. The code available here was the result of this project. Essentially this project assigns star clusters to a spiral arm / structure to examine the age distribution. This can be used to study mechanisms of spiral formation such as wave-density theory. The summary of my findings for NGC1566 can be found in analysis_summary.

# How to use
Most of the instruction is readily available within the code, but here is a general list of how to implement your own version of the project.
1) Download a spitzer 3.6 micron fits imagine of your target (I recommend NED - NASA/IPAC Extragalactic Database)
2) Download cluster catalogs from the target LEGUS galaxy here https://archive.stsci.edu/prepds/legus/dataproducts-public.html
3) Follow the code and replace NGC1566 where needed
4) Adjust the xlim and ylim parameters to beter fit the galaxy image
5) Determine age ranges of clusters and adjust label names accordingly
6) Use DS9 to locate the correct pixel location of the 3.6 micron peaks
7) Map the arms in the image. This has a learning curve as each parameter adjusts the arm shape differently. Not all galaxies will have the same amount of arms or arm segments so function calls will need to be added or removed.
8) Find the pixel scale for the image and a cited distance to the target, VERY IMPORTANT! Usually you can find these in the hearer of your fits file (HDU). 

   example:
   
            hdul = fits.open('NGC_1566_3.6.fits')  # open a FITS file
            
            hdr = hdul[0].header  # the primary HDU header
            
            hdr
            
            ...
            
            / TARGET AND POINTING INFORMATION
            
            ...
            
            PXSCAL1 =    -1.22334117768332 / [arcsec/pix] Scale for axis 1 at CRPIX1,CRPIX2 
            
            PXSCAL2 =     1.22328355209902 / [arcsec/pix] Scale for axis 2 at CRPIX1,CRPIX2
            
            
9) cluster_DATA contains the arms and clusters assigned to each arm. The rest of the code is a data analysis template, so users could develope their own methods to view the information in this table. The plots included in this project can be adjusted to the users desire, but require careful adjustments to each plotting function.

# Dependancies
numpy

matplotlib

astropy

pandas

csv

tablulate

# Disclaimer
As always there could be areas where I may have made subtle mistakes with direct consequences to my results. I ask that you approach any findings with caution. While the results agreed with other papers on NGC6946 it does not mean my approach was free of mistakes (my primary field is not extragalactic astronomy).

# Aknowledgement
This project made use of star cluster data from the LEGUS collaboration.

LEGUS citation:

Lee, J.~C., Calzetti, D., Adamo, A., et al. 2014, aas
