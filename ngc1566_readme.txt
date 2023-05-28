# Final catalogue produced by the pipeline
# Photometry is in Vega system, using ZP from the STScI webpage
# Galactic ext from NED and aperture correction is included. Distance modulus used 31.28 mag (18.0 Mpc) from http://edd.ifa.hawaii.edu. This distance is different from the one listed in Calzetti et al 2015. Catalogues with the latter distance are available on request. Please ask Angela.
# When 66.666 appears in a photometry column, it means the source was not located
# within the field of view of that frame.
# When 99.999 appears in a photometry column, it means the source was not detected,
# i.e., the flux was negative or extremely small.
# When 44.444 appears in a photometry column (only present in the CI-based catalog),
# it means the source was detected, but the CI-based aperture correction was undefined.
# The photometry in the avgapcor catalog uses average aperture corrections 
# calculated from isolated clusters in the field. The photometry in the CI-based
# catalog uses aperture corrections calculated from a CI-aperture correction 
# relation derived from artificial clusters. The number of filters in which each
# source is detected may be different between the two catalogs because CI-based 
# aperture corrections are occasionally unreliable for certain filters.
# Photometry performed at aperture radius of 4 px and sky at 7 px and 1 px wide.
# Cardelli extinction law applied to derive cluster properties.
# SED fitting algorithm described in Adamo et al 2010 (MNRAS, 407, 870). Error analysis described in Adamo et al 2012 (MNARS, 426, 1185). Models used are Yggdrasil models (Kroupa IMF, nebular continuum+emission line with covering factor =0.5, metallicity Z=0.02, PadAGB isocrones) see Adamo et al 2017 (ApJ, 841, 131).

Order of the columns
1. source id
2. x coordinates in the ref frame (image aligned and registered, these coordinates are the same in each filter)
3. y coordinates in the ref frame (image aligned and registered, these coordinates are the same in each filter)
4. RA coordinates in the ref frame (image aligned and registered, these coordinates are the same in each filter)
5. DEC coordinates in the ref frame (image aligned and registered, these coordinates are the same in each filter)
6. final total mag in WFC3/F275W
7. final photometric error in WFC3/F275W
8. final total mag in  WFC3/F336W
9. final photometric error in WFC3/F336W
10. final total mag in WFC3/F435W
11. final photometric error in ACS/F435W
12. final total mag in WFC3/F555W
13. final photometric error in ACS/F555W
14. final total mag in WFC3/F814W
15. final photometric error in ACS/F814W
16. CI=mag(1px)-mag(3px) measured in the F555W. This catalogue contains only sources with CI>=1.35.
17. best age in yr
18. max age in yr (within 68 % confidence level)
19. min age in yr (within 68 % confidence level)
20. best mass in solar masses
21. max mass in solar masses (within 68 % confidence level)
22. min mass in solar masses (within 68 % confidence level)
23. best E(B-V)
24. max E(B-V) (within 68 % confidence level)
25. min E(B-V) (within 68 % confidence level)
26. chi2 fit residual in F275W, if positive the flux observed at that wavelenght is higher then predicted by the best fitted model (and viceversa)
27. chi2 fit residual in F336W, if positive the flux observed at that wavelenght is higher then predicted by the best fitted model (and viceversa)
28. chi2 fit residual in F435W, if positive the flux observed at that wavelenght is higher then predicted by the best fitted model (and viceversa)
29. chi2 fit residual in F555W, if positive the flux observed at that wavelenght is higher then predicted by the best fitted model (and viceversa)
30. chi2 fit residual in F814W, if positive the flux observed at that wavelenght is higher then predicted by the best fitted model (and viceversa)
31. reduced chi2
32. Q probability is a measurement of the quality of the fit; if close to 1 fit is good, if close to 0 the fit outputs are not well constrained. See numerical recipies
33. Number of filter. Sources with UBVI or UV-BVI detection have Nflt=4; sources with detection in UV-UBVI have Nflt=5. The remining sources have Nflt=0. The SED fit has been done only on sources with Nflt>=4
34. Final morphological flag. The classification contained in this column is the one that should be used to perform the cluster analysis. It has been derived in a hybrid way. A fraction has been visually inspected by 3 humans, a fraction only by ML, a fraction by one humans which has revised the ML classification. The flag in column 35 will provide the source of the classification. Only clusters with Nflt>=4, CI>=1.35 and m_555<=-6.0  mag have been morphologically classified. Please, notice that the aperture correction applied to the V band before the magnitude cut is dependent of the CI measured in this filter. Those sources which did not pass the cut have assigned here a morphological flag which corresponds to class=0. Class=1, symmetric, compact cluster.  Class=2, concentrated object with some degree of asymmetry, possible color gradient.  Class=3, multiple peak system, diffuse, could be spurious nearby stars along the line of sight.  Class=4, spurious detection (foreground/background sources, single bright stars, artifacts).
35. Method of visual inspection. Flag 0, the source has been classified only by the ML approach; flag 1 is for sources which have been classified by the ML and then verified by 1 human; flag 3 is for sources which have been visually classified both by 3 humans and by the ML; flag 4 the sources have been first classified by 3 humans, then by the ML, and again verified by 1 human. If a source has flag 3 or 4 the human classification listed in column 36 has been preferred to the ones given in column 37 and 38. If a source has flag 1 then the classification given in column 38 has been preferred above the ML one. If a source has flag 0 then only ML classification is available and can be used. A flag 6 indicates a post-reclassification of sources that had originally assigned class 4. These sources have been selected to satisfy the following conditions CI <= 1.8, V-I <= 1.8 mag and  23.28 > V > 18.0 mag. At difference of the classification in column 39 we add here an extra requirement on the luminosity being brighter than -8 mag (i.e. V<23.28 mag)
36. Final morphological class of the source after visual inspection of 3 humans (mode value). The classification is the same as before (0,1,2,3,4).
37. Final morphological class of the source using the machine learning (ML) approach. The classification is the same as before (0,1,2,3,4).
38. Final morphological classification assigned by 1 human who has verified the ML classification. The classification is the same as before (0,1,2,3,4).
39. Final morphological post-reclassification by 1 human of sources that had originally assigned class 4. These sources have been selected to satisfy the following conditions CI <= 1.8, V-I <= 1.8 mag and V > 18.0 mag.
