DAVS-Toolbox
============

Data Access and Visualization for Sleep Toolbox

#### Overview
The DAVS-Toolbox is a collection of MATLAB scripts and GUIs for accessing and visualizing polysnonmography (PSG) data. Each of the routines include test scripts and test files which allow the user to evaluate performance, verify steps and serve as a brief tutortial for most programmers.

MATLAB script files are available for each of the DAVS-toolbox components.  Click on the component name to access the prefferred download site. Components are posted on the MATLAB file exchange website adn on GITHUB. It is reccomended that the MATLAB website be used to download if available. Links to the GITHUB site for MATLAB deposited routines are also provided for individuals who wish to contribute bug fixes, revisions and extensions. 

### Target Audience
Sleep researchers and engineers apply novel techniques to sleep data.


#### Description

The Data Access and Visualization For Sleep (DAVS) Toolbox is a set of MATLAB scripts and utilities (GUI) that can be used to review and visualize large numbers of sleep studies stored as a European Data Format (EDF)  file and the associated annotations save in an XML format.  The DAVS toolbox includes four components: Data Access, Data Manipulation, Data Visualization, and Data Utilities. 

*Data Access*. The Data Access components include low level files for loading and writing EDF files. The data access functions have been tailored to sleep applications and include support for accessing data by signal and sleep epoch. A class version of the loader includes a checker that compares the EDF header and signal information to original EDF standard, support for identifying EDF files in a folder, and support for plotting signals. The class version of the loader is designed to support GUI development and signal processing applications by providing dependent variables which provide quick access to commonly used signal parameters. For example, the sampling rates for each of the loaded signals can be accessed directly without computing with information from the header and signal information. The EDF write function allows for header, signal information and signal data to be modified in addition to creating new EDF files. Included in the EDF write function is a simple signal generator, which is used to save test data to an EDF file. The annotation loader can be used to access sleep stage and event information stored in an XML file.  The annotation loader can be used to create a Hypnogram or to export events to an excel file.

*Data Manipulation*.  Provides support for de-identifying EDF files and summarizing the contents of EDF files stored in a directory.  The summarizing functionality can be configured to summarize headers, signal labels and to check that expected signals are present in identified files. The data manipulation functions can be used prior to large scale analysis to verify EDF contents.  Alternatively, the functionality can be integrated within analysis pipeline to verify signal content prior to proceeding with an analysis step. 

*Data Visualization*. Signal raster plots can be used to create raster plots from signals stored within an EDF file and annotation event timing can be overlaid on the signals.  The number of signals on a page and the x-axis time scale are pre-configured to settings most commonly used in sleep and circadian applications. Either MATLAB figures can be generated or the collection of figures can be saved to a power point file. HeatMaps can be created from data signals stored with an EDF file and contain similar pre-configured settings for sleep and circadian application as the signal raster plotting program. Single signal heat maps or a panel of heat maps from user selected signals can be created.

*Data Utilities*.  Two utilities with GUIs which use all scripts files in the DAVS toolbox are also provided.  The SignalRasterView utilities can be uses to inspect the contents of and EDF or to check the EDF prior to loading. Signal raster plots can be generated from the same interface. In a second tool, BlockEdfSummarize can be used to generate header and signal content summaries simply by selecting the folder to investigate.  Versions of these tools are provided as MATALB script files, as a MATLAB App and as a Windows compiled tool.

Collectively the script files and data utilities provide significant support for reviewing and preparing a large number of files for analysis. 



#### DAVS Toolbox Content 

Data Access
- [BlockEdfLoad](http://www.mathworks.com/matlabcentral/fileexchange/42784-blockedfload)  [(git)](https://github.com/DennisDean/BlockEdfLoad). An efficient EDF loader that provides several options for accessing header and signal information stored in an EDF file. Specific signals and selected 30 second epochs can be retrieved.
- [BlockEdfLoadClass](http://www.mathworks.com/matlabcentral/fileexchange/45227-blockedfloadclass) [(git)](https://github.com/DennisDean/BlockEdfLoadClass/). Class version of blockEdfLoad. Dependent variables are added that provide quick access to EDF header content. The class includes an EDF checker and support for creating EDF file lists. 
- [BlockEdfWrite](http://www.mathworks.com/matlabcentral/fileexchange/46339-blockedfwrite) [(git)](https://github.com/DennisDean/BlockEdfLoadClass/). An EDF creation function designed to worked in conjunction with BlockEdfLoad and BlockEdfLoadClass. The function can be used to record experimental data and to generate test data.  
- [LoadCompumedicsAnnotationClass](https://github.com/DennisDean/LoadCompumedicsAnnotationsClass). Load sleep stage and event information from a Compumedics file. Generate a hypnogram from stage data.

Data Manipuation
- [BlockEdfDeidentify](http://www.mathworks.com/matlabcentral/fileexchange/46423-blockedfdeidentify) [(git)](https://github/DennisDean/BlockEdfDeidentify/). Function over-writes the subject id and study date fields in the EDF header. 
- [BlockEdfSummarizeClass](https://github.com/DennisDean/BlockEdfSummarizeClass). BlockEdfSummarizeClass can be used to summarize the contents of a folder which contains EDF wiles with the associated annotation file (XML) files. The class is configured to create header and signal summaries, which are written to excel files. An EDF check summary, which compares the EDF content to the EDF specification, can be exported to an EXCEL file.
- [GetMatchedSleepEdfXmlFiles](https://github.com/DennisDean/GetMatchedSleepEdfXmlFiles). Function searches recurrsively within a folder for EDF files. The function assumes EDF files are named as 'prefix'.* and that annotation files are stored in the same folder as the EDF.  The function assumes annotaion files are stores as XML files ('prefix'.XML.edf). Note that the assumed file structure is designed to work with data formats supported by the [National Sleep Research Resource](https:\\sleepdata.org\). 

Data Visualization
- [BlockEdfSignalRasterView](http://www.mathworks.com/matlabcentral/fileexchange/46366-blockedfsignalrasterview) [(git)](https://github.com/DennisDean/BlockEdfSignalRasterView). Creates raster plots from signal data stored within an EDF file. Raster plots are sometimes referred to as waterfall plots. 
- [BlockEdfSignalHeatMapView](http://www.mathworks.com/matlabcentral/fileexchange/46417-blockedfheatmapview) [(git)](https://github.com/DennisDean/BlockEdfSignalRasterView). Creates heatmaps of signal data stored within an EDF file. 

Data Utilities
- [SignalRasterView](http://www.mathworks.com/matlabcentral/fileexchange/46420-blockedfsignalrasterview) [(git)](http://github.com/DennisDean/SignalRasterView). SignalRasterViewFig is a utility for investigating the contents of an EDF file.  The utility (GUI) can be used to compare the EDF contents to the EDF specification, view the EDF headers, to create raster plots of the EDF signals and to create a power point summary of the generated raster plots. 
- [BlockEdfSummarizeFig](https://github.com/DennisDean/BlockEdfSummarizeFig). The simple GUI can be used to summarize and check EDF files stored within a folder.

#### Related links
MATLAB Eile Exchange Submissions:
A list of my MATLAB submissions can be found [here](http://www.mathworks.com/matlabcentral/fileexchange/?term=authorid:113409)


[National Sleep Research Resource](https://sleepdata.org/)
