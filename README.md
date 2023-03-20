# Mouse_Brain_Heatmap
rmd with the framework to create Mouse brain heatmaps and analyze data generate by Nuti to useable (https://github.com/DaniellaDeWeerd/Nutil-To-Usable).

This code was written using SVGs downloaded from The Allen Brain Atlas http://api.brain-map.org/api/v2/svg_download/100883867?groups=28. Please see their terms of service https://alleninstitute.org/legal/terms-use/ to ensure your use of this code fits both the GNU general pubic license 3 and the Allen Insitutes terms of service.  In very brief and overly simplified terms, if this code is used purely for academic purposes, it may be used freely and changed ad libitum, so long as both the image source and this code are properly cited. 

The analysis method is robust linear regression on rankit transformed outcomes; ties are randomized. This method was chosen as there are often strata with no pathology (true zeros) while another comparative strata has mainly non-zeros. This analysis seeks to answer the question, which regions have more pathology.  An alternative method would be zero-inflated beta regression. This method is very time-consuming, but potentially more powerful. This app does not implement this method, but it may become available in future versions.

Summary brain heatmaps are either the mean or median. At the parent level this is the mean of means or median of medians. For mean display, data are lemon squeezed first, averaged, then back-transformed (https://doi.org/10.1037/1082-989x.11.1.54).
