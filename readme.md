# Electrohydrodynamic Inkjet High Speed Profile Dataset
This dataset is a collection of post-processed high-speed videos of ink jet formation in an Electrohydrodynamic Inkjet Printer. Image analysis was used to extract the z-axis profile of an ink column's diameter during jet formation and collapse.

An EHDIJ uses electric signal applied at the printer tip to drive droplet formation and attract ink to the grounded substrate. The electrical and fluid behavior at the tip of an EHDIJ printer is dynamic, transient, and not fully understood. Manufacturing outcomes of EHD printing are closely tied to the interplay of tip, electrical signal, substrate, and ink properties. Understanding these droplet dynamics is key to producing high-resolution and consistent output from the EHD printer. Advances in this technology could enable EHD additive printed patterns with features sizes far smaller (micron and below) than other current additive technologies, possibly enabling novel energy, electronics, optical, and biomedical applications.


## Contents
This prelimenary dataset comprises eight jetting events. Summary measurements, full time vs. z profiles, and figures are provided for each original video.

### ./summary.csv
Contains a summary of metrics extracted from each of the eight videos. Length measurements are in centimeters and time units in seconds unless otherwise specified. Some fields, such as jet_duration, may have multiple values if multiple events are recorded in the video. In such cases, the field will contain an ordered list of measurements.

> import pandas as pd

> df = pd.read_csv('./summary.csv', index_col=None)

### ./cache/
Contains time traces of each jet event. Each column is measurements at a constant pixel height, and each row is the profile of the printer tip and ink at one time frame from the video.

> df = pd.read_csv('./summary.csv', index_col=0)

The first column is the time in seconds from the start of the video. (Source videos were all taken at 8500 fps.) With this import command, the dataframe index will be the time stamp.

Units are pixels of ink column width. An estimate of pixel size can be found in the summary statistics for each video.

### ./figures/
Contains a collection of automatically-generated traces and examples from the creation of the database. For each source video, this includes a frame showing the mirror plane detection used to isolate the ink column, time profiles of drop height and velocity priort to jetting, and jet thickness over time during jetting. 



## Credits
No additional publications are available at this time in support of this data. It is provided with thanks to SEMI-FlexTech and the Army Research Lab.

#### Corresponding Author:
Oliver Nakano-Baker ^  [onb@uw.edu]

#### Contributors:
Liangkui Jiang *

Xuipeng Jiang *

J. Devin MacKenzie ^

Shan Jiang *

Hantang Qin *

______

^ University of Washington Materials Science and Engineering

\* Iowa State University Industrial and Manufacturing Systems Engineering
