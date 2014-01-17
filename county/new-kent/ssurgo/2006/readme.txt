The export contains the following soil survey area (SSA) data:

SSA Symbol:             VA127
SSA Name:               New Kent County, Virginia
SSA Version:            4
SSA Version Est.:       6/2/2006 1:28:24 PM
Tabular Data Version:   4
Tabular Version Est.:   6/2/2006 1:28:24 PM
Spatial Data Version:   1
Spatial Version Est.:   7/28/2004 9:05:00 AM
Spatial Format:         ArcView Shapefile
Coordinate System:      UTM Zone 18, Northern Hemisphere (NAD 83)


The export also contains the following MS Access SSURGO template 
database:

Template DB Name:       soildb_VA_2002.mdb
Template DB Version:    30
Template DB State:      VA
MS Access Version:      Access 2002


When soil data is exported from the Soil Data Mart, the end result is
always a single zip file, regardless of what export options were
selected.  The format of an export file name is: soil_ssasymbol.zip,
where ssasymbol is the symbol of the corresponding soil survey area.
An export from the Soil Data Mart always contains data for one and only
one soil survey area.

A survey area symbol is a five character string where the first two 
characters are a U.S. state or territory postal code, and the last three 
characters are digits that represent the soil survey area within the 
corresponding state or territory.

The export file can be unzipped using WinZip or an equivalent
application.  When an export file is unzipped, the following directory
hierarchy is produced in the directory to which the export file was
unzipped:

soil_ssasymbol
    tabular
    spatial

where ssasymbol is the symbol of the corresponding soil survey area.

The top level directory contains the following files:

soil_metadata_ssasymbol.txt - Federal Geographic Data Committee (FGDC)
metadata in plain ASCII format.

soil_metadata_ssasymbol.xml - the same FGDC metadata in XML format.

README.txt - this file

The root directory will also contain a zipped, empty MS Access SSURGO
template database, if one was requested as part of the download.  The
non-extension part of the zipped template database file name varies,
but if one was included, it will be the only file in the top level
directory with an extension of "zip".

Directory "tabular" contains any tabular data that was requested.

Directory "spatial" contains any spatial data that was requested.

It is possible to request tabular data without including the
corresponding spatial data, and vice versa.

Tabular data is provided as a set of ASCII delimited files.  Each file
corresponds to table in the SSURGO 2.2 data model.  The tabular data
isn't particularly useful until it has been imported into an MS Access
SSURGO template database.  If a template database was not included in
the export file, you can download one from the following URL:

http://soildatamart.nrcs.usda.gov/templates.aspx

For information about importing tabular data into a template database,
or information about the capabilities of the template database in
general, do the following:

1.  Open the MS Access SSURGO template database in the appropriate
version of MS Access.

2.  Click the Reports tab of the Database Window.  The Database Window
may be behind a form titled "SSURGO Import" or "Soil Reports".

3.  Either double-click the report titled "How to Understand and Use
this Database", or select this report and then click "Preview".

4.  After the Report Viewer window is displayed, either click the
printer icon or select "Print" from the File menu.  You can also
browse this report using the Preview window.

The format in which spatial data is provided depends on the spatial
format option that was selected when the download was requested.
Spatial data is available in the following formats:

ArcView Shape File
ArcInfo Coverage
ArcInfo Interchange

Spatial data files use a naming convention that depends on the
corresponding spatial format.

For spatial data in ArcView Shape File format, the following file name
prefixes are used:

soilsa_a - soil survey area boundary polygons
soilmu_a - map unit boundary polygons
soilmu_l - line map units
soilmu_p - point map units
soilsf_l - line spot features
soilsf_p - point spot features
soilsf_t - spot feature descriptions

For spatial data in ArcInfo Coverage or ArcInfo Interchange format, the
following file name prefixes are used:

ssa_a - soil survey area boundary polygons
smu_a - map unit boundary polygons
smu_l - line map units
smu_p - point map units
ssf_l - line spot features
ssf_p - point spot features
ssf_t - spot feature descriptions

Spatial data always includes survey area and map unit boundary
polygons, but all other feature classes are optional.

Data exported from the Soil Data Mart is in SSURGO 2.2 format.
Additional information about the SSURGO 2.2 data model can be obtained
from the SSURGO Metadata reports in the MS Access SSURGO template
database, or from the Soil Data Mart website at:

http://soildatamart.nrcs.usda.gov/ssurgometadata.aspx

Questions should be directed to the National Soil Information System
(NASIS) Hotline.  The NASIS Hotline, which resides at the USDA NRCS
National Soil Survey Center in Lincoln Nebraska, is staffed from 8:00
AM to 4:30 PM Central Time.

(402) 437-5378 - Steve Speidel
(402) 437-5379 - Tammy Cheever

e-mail:  hotline@lin.usda.gov


