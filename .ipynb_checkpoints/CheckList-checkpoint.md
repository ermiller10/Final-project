1. Import data using pandas
https://data.usgs.gov/datacatalog/data/USGS:60bfb8a4d34e86b938916d6f
    My data from the Tampa Bay cores looks really weird and non-functional
    figure out how to use Panda's read_csv function. I can't tell if the assignment example had already loaded the csv data from USGS somewhere directly onto the computer
    Should I just upload the csv data directly to computer and go from there? wouldn't the file have to be somewhere in the jupyter notebook? Is this why the URL function is useful?
    Is the url that I included actually a url to the data or just the abstract? just the abstract. When I searched the url from assignment it just began downloading a file to my computer. I want this
    "If we right click CSV (data) and select Copy link address, we’ll find the URL that will directly download the CSV data onto our machine. This URL is quite long, but it can be reduced down to the following URL. We can use requests to read a CSV file from a URL."
    
I found the download link in my downloads and copied this. Is this specific to where the file was saved and will this only work on my computer?

1. has been done!

2. Would be interpreting my data and understanding what each recorded variable represents.Is there more than just the abstract available? I need a key for the table headers. Included in the abstract there was...




Definitions come from metadata. Does emily want a link to this in the notebook?


Depth_mid= A numeric identifier of the interval mid-point depth below the sediment interface in centimeters

DBD= Dry Bulk Density: A numeric identifier of the sediment dry bulk density in grams per cubic centimeter (g/cm3). 

210Pb = A numeric identifier of the sediment total lead-210 activity in decays per minute per gram (dpm/g). Measured at 46.5 kiloelectronvolt (KeV) on a planar gamma counter. Blank/empty cells indicate the measurement was not done. The value 0.00 is given to analyzed samples found to be below detection; see gamma analysis process step for detection limits of radioisotopes

210Pb_e = A numeric identifier of the measurement error in sediment total lead-210 activity in decays per minute per gram (dpm/g). Blank/empty cells indicate the measurement was not done. The value 0.00 is given to analyzed samples found to be below detection

226Ra = A numeric identifier of the sediment total radium-226 activity in decays per minute per gram (dpm/g). Measured at 352 kiloelectronvolt (KeV) on a planar gamma counter. Blank/empty cells indicate the measurement was not done. The value 0.00 is given to analyzed samples found to be below detection; see gamma analysis process step for detection limits of radioisotopes

226Ra_e = A numeric identifier of the measurement error in sediment total radium-226 activity in decays per minute per gram (dpm/g). Blank/empty cells indicate the measurement was not done. The value 0.00 is given to analyzed samples found to be below detection

210Pbex = A numeric identifier of the sediment excess lead-210 activity in decays per minute per gram (dpm/g). Calculated as the difference between total lead-210 and total radium-226 activities. Blank/empty cells indicate the measurement was not done

210Pbex_e A numeric identifier of the propagated measurement error in sediment excess lead-210 activity in decays per minute per gram (dpm/g). Blank/empty cells indicate the measurement was not done

137Cs = A numeric identifier of the sediment total cesium-137 activity in decays per minute per gram (dpm/g). Measured at 662 kiloelectronvolt (KeV) on a planar gamma counter. Blank/empty cells indicate the measurement was not done. The value 0.00 is given to analyzed samples found to be below detection; see gamma analysis process step for detection limits of radioisotopes

7Be = A numeric identifier of the total sediment beryllium-7 activity in decays per minute per gram (dpm/g). Measured at 477 kiloelectronvolt (KeV) on a well gamma counter. The value 0.00 is given to analyzed samples found to be below detection; see gamma analysis process step for detection limits of radioisotopes.

7Be_e = A numeric identifier of the measurement error in sediment total beryllium-7 activity in decays per minute per gram (dpm/g). Blank/empty cells indicate the measurement was not done. The value 0.00 is given to analyzed samples found to be below detection

wtC = Total amount of organic carbon by weight percent in soil. Sediments in this sample set were placed in a acid fuming desiccator to remove inorganic carbon prior to analysis. Blank/empty cells indicate the measurement was not done. Refer to the attribute accuracy and process step sections for further details

wtN= Total amount of organic nitrogen by weight percent in soil. Sediments in this sample set were placed in a acid fuming desiccator to remove inorganics prior to analysis. Blank/empty cells indicate the measurement was not done. Refer to the attribute accuracy and process step sections for further details

Age = A numeric identifier for the age in years from the collection date of the core interval based on the Continuous Rate of Supply lead-210 age model. Blank/empty cells indicate the measurement was not done

Age_e = A numeric identifier for the age model uncertainty in years of the core interval based on the Continuous Rate of Supply lead-210 age model. Error is propagated through the model. Blank/empty cells indicate the measurement was not done.

VAR = Vertical Accretion Rate: A numeric identifier for the vertical accretion rate of the sediment in millimeters per year (mm/y). Calculated as the difference in interval midpoint divided by the difference in ages of those adjacent sediment intervals

MAR = Mass Accumulation Rate: A numeric identifier for the mass accumulation rate of the sediment in grams per square meter per year (g/m2/y). Calculated by multiplying dry bulk density times vertical accretion rate

CAR = Carbon Accumulation Rate: A numeric identifier for the carbon mass accumulation rate of the sediment in grams of carbon per square meter per year (gC/m2/y). Calculated by multiplying the average mass accumulations rate for the combined depth interval of the elemental sample times weight percent carbon

year = The year corresponding to the soil horizon based on the Continuous Rate of Supply (CRS) lead-210 age model. Calculated as collection date minus age of sediment at each depth interval. Year is not calculated for deeper sections that are beyond the limits of the CRS model
LOI = Loss On Ignition is the amount of material lost when sediment is burned in a muffle furnace for 4 hours at 450 degrees Celsius. Percent LOI is an operationally defined proxy estimate for the amount of organic matter (and organic carbon) content

Should I relabel these or include a key in my notebook?

3. Cherry-picking data
MAR, CAR, and VAR
Mass accumulation rate, carbon accumulation rate, and vertical accretion rate all seem relatively straight forward
What do I want to plot these against?
year? not so straighforward
year= The year corresponding to the soil horizon based on the Continuous Rate of Supply (CRS) lead-210 age model. Calculated as collection date minus age of sediment at each depth interval. Year is not calculated for deeper sections that are beyond the limits of the CRS model

You could try plotting this and seeing what it looks like

What else could I compare MAR, CAR, and VAR
