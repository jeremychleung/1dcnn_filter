<!-- # 1D-CNN Temporal Filter for Atmospheric and Climate Research -->
1D-CNN Temporal Filter for Atmospheric and Climate Research
=====
<!-- [![DOI](https://zenodo.org/badge/698311843.svg)](https://zenodo.org/badge/latestdoi/698311843)<br /> -->
This repository contains sample codes of constructing a one-dimensional convolutional neural network (1D-CNN) temporal filter. We intended to create this code (and 1D-CNN filter) for analyzing data of meteorology, climate, atmospheric and oceanic sciences, etc., but the filter could be applied to other kinds of data theoretically.
<br /> <br />

**About the 1D-CNN temporal filter**
-----
- Traditional, widely used temporal filters, such as FFT ans Lanczos filter, relies on a certain number of neighboring data points to calculate the output value of each point. Thus, there will be loss of data at the very beginning and the end of the filtered output, depending on the length of window applied. Due to the same reason, the filter may be unable to work properly if missing values exist in the input time series, and will result in no valid output values near missing values (see https://www.ncl.ucar.edu/Applications/filter.shtml).
- Incomplete (or discontinuous) time series is a common and unavoidable issue in meteorological data, especially for in-situ observations.
- The 1D-CNN temperoal filter, which is designed to consists of a combination of convolutional and subtraction layers, may address the above issue(s).
- The convolutional layer serves as lowpass filters of different cut-off frequencies or periods. The subtraction layer is used to remove any unwanted signals.
- The combination of subtractive and convolutional layers acts as a high-pass filter by removing the low-pass filtered signal generated by the convolutional layer.
- One could build a highpass, bandpass, or lowpass filter by employing different combinations of convolutional and subtraction layers.
- Please refer to [Yu et al. (2024, under review)](https://) and [Stan and Mantripragada (2023)](https://journals.ametsoc.org/view/journals/aies/2/4/AIES-D-22-0079.1.xml) for more detail about the calculation procedure and the theory behind it. A Tensorflow version was also provided by [Stan and Mantripragada (2023)]([https://journals.ametsoc.org/view/journals/aies/2/4/AIES-D-22-0079.1.xml](https://github.com/cristianastan2/AIES-Deep-Learning-Filter)).
 <br /> 
 
<!--
**Files**
-----
- Training code
  - Location: [code/??.csv](https://github.com/jeremychleung/1DCNN_Filter)
- Sample input data
  - Location: [input/??.csv](https://github.com/jeremychleung/1DCNN_Filter)
  - Description: This is a sample input data file, which is provided by the Hong Kong Observatory.
- Sample output data
  - Location: [output/??.csv](https://github.com/jeremychleung/1DCNN_Filter)
  - Description: This is the output data generated by the provided sample code and data. 
<br />
-->

**Citation and references**
-----
If you use the 1D-CNN temporal filter in a publication or for any other purposes, please cite 
- Yu D., Leung J.C.H., Kong H., Chan P., Fong C., Zhang B. A 1D convolutional neural network (1D-CNN) temporal filter for atmospheric variables: A case study on intraseasonal signal detection based on Hong Kong Observatory station data. (under review). <!-- https://doi.org/10.1007/s00382-022-06142-2 -->
- Stan, C., & Mantripragada, R. S. S. (2023). A deep learning filter for the intraseasonal variability of the tropics. Artificial Intelligence for the Earth Systems, 2(4), e220079. 
<!-- - Zenodo archive: https://doi.org/10.5281/zenodo.8410597 -->
<br /> 

<!-- **References** 
-----
- Ye G., Leung J.C.H., Dong W., Xu J., Li W., Qian W., Zhang B. A Reanalysis-Based Global Tropical Cyclone Tracks Dataset for the Twentieth Century. Scientific Data (under review). <!-- https://doi.org/10.1007/s00382-022-06142-2 -->
<!-- - Leung, J.CH., Qian, W. Monitoring the Madden–Julian oscillation with geopotential height. Clim Dyn 49, 1981–2006 (2017). https://doi.org/10.1007/s00382-016-3431-x -->
<!-- - Wheeler, M.C., Hendon, H.H. An All-Season Real-Time Multivariate MJO Index: Development of an Index for Monitoring and Prediction. Mon Weather Rev 132:1917–1932 (2004). https://journals.ametsoc.org/view/journals/mwre/132/8/1520-0493_2004_132_1917_aarmmi_2.0.co_2.xml -->
<!-- <br /> -->


**Contact**
-----
If you have any questions about the data, feel free to contact Dr. Jeremy Leung (chleung@pku.edu.cn or liangzx@gd121.cn) and Dr. Hoiio Kong (hikong@cityu.edu.mo)
<br /> 
