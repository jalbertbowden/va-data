README File for Census 2000 Redistricting Files Delivered via FTP



Note:  Users processing these FTP files in a Windows environment should read carefully the File 
Information section of this document.

  
About the FTP Application

This FTP (File Transfer Protocol) application is intended for experienced users of census 
data, compressed files, and spreadsheet/database software. It provides quick access to data 
users, such as State Data Centers and news media, who need to begin their analysis immediately 
upon data release. Due to the size of the files, the FTP user should have a fast file transfer 
capability. 

Each state directory provides all files available for the identified state. Once uncompressed, the 
data are in a flat ASCII format.  The geographic file is in a fixed-field format; the two data files are 
in comma delimited format. No software is provided. Users of the FTP application need to unzip 
the compressed file after downloading, then import it into the spreadsheet/database software of 
their choice for data analysis and table presentation.

Other Sources of the Data

The Census Bureau releases most Census 2000 data on a state-by-state basis. Tables are available 
in American FactFinder (factfinder.census.gov) upon release of the designated state file. Within 
American FactFinder, individual tables can be downloaded in a text delimited or comma delimited 
format.  

For users without immediate need for the data, CD-ROMs containing the data and access software 
are scheduled for shipping shortly after the state file release.  They can be ordered from the Census 
Bureau?s Customer Services Center at 301-457-4100.  

FTP Directory

The FTP directory is at http://www2.census.gov/census_2000/datasets/  .  When the Census 2000 
redistricting data are added to their respective directories, each state directory has three data files, 
reflecting the three data segments.  See below for more information on the data segments.    
   
File Information

Once uncompressed, these files are in flat ASCII format. The geographic header file (see below) 
contains fixed fields while the data files (File01 and File02, see below), including the geographic 
link fields, are in comma-delimited format.  These files have been constructed in a UNIX 
environment. They use an ASCII linefeed, chr(10), to indicate a new record.

For successful use with many programs running in a Windows environment, these files need to be 
modified to use the ASCII carriage return/linefeed sequence, chr(13) + chr(10) as a record 
terminator. This is an easy step in the UnZIP process using any UnZIP software which offers the 
conversion option.  We tested PKZIP for Windows, version 4.00 following the steps outlined 
below.  This PKZIP shareware can be downloaded from www.pkware.com.  After installing 
PKZIP, do the following:

	--Select the file 

	--Select the Extract option on the tool bar

	--Select the options button at the bottom of the Extract page

		--Under the Miscellaneous section, select the "DOS - convert to CR/LF"
	
The resulting file will meet the ANSI MS-DOS/Windows standard used by Access 97 and other 
MS Windows-based programs.  If the data are being processed in a UNIX environment, they can 
be unzipped using any standard ZIP/UnZIP package.

These FTP data are available as compressed files at the 90% (approximately) file compression 
ratio. We estimate that an average state FTP download (at 56K bps) of the redistricting data will 
take approximately 2 hours. Larger states, of course, will take longer. Our estimate for an FTP 
download for California is approximately 8 hours at the 56K bps speed. If you are using a 
modem/telephone line link to the Internet, we do not recommend using the FTP option.

Segmented Data 

The data in the redistricting files and other Census 2000 summary files are segmented. This is done 
so that individual files will not have more than 255 fields, facilitating exporting into spreadsheet or 
database software. In short, to get the complete data set for the redistricting files, users must 
FTP all three files in the state directory.   

These test files contain:

	Geographic Header file
	File01 (Tables 1 and 2)
	File02 (Tables 3 and 4)

It is easiest to think of the file set as a logical file.  However, this logical file consists of three 
physical files: the geographic header file, file01, and file02. This structure is a change from 
previous decennial census files.    

The explanation below for linking the three redistricting test files requires specific location 
information for the geographic header.  These are located in Chapter 7 of the Technical 
Documentation http://www.census.gov/prod/www/abs/pl94-171.pdf  . A unique logical record 
number (LOGRECNO in the geographic header) is assigned to all files for a specific geographic 
entity; all records for that entity can be linked together across files.  Additional identifying fields 
are also carried over from the geographic header file to the table files.  These are file identification 
(FILEID), state/U.S. abbreviation (STUSAB), characteristic iteration (CHARITER),  characteristic 
iteration file sequence number (CIFSN).  

The geographic header record layout is identical across all electronic data products from Census 
2000.  Since the redistricting data files are quite simple, some of the fields, including some 
geographic header fields that appear in all three files (geographic header, tables 1/2, and tables 3/4) 
are not used.  For example, the character iteration (CHARITER) field is only used in SF2/SF4.  In 
the redistricting data file, it is always coded as 000.

File Record Layout

For a layout of the individual tables for each file, see http://www.census.gov/prod/www/abs/pl94-
171.pdf  .  Select Chapter 6, Summary Table Outlines. 

Estimated File Sizes


State	Geo file			File 1	     	File 2	
		unzip	zip		unzip	zip		unzip	zip	

Alabama	80M	6M		64M	2M		64M	2M

Alaska	11M	.8M		9M	.4M		9M.	3M
	
Arizona	70M	5M		55M	2M		55M	2M

Arkansas	68M	5M		53M	2M		53M	2M

California	234M	16M		186M	12M		186M	13M	

Colorado	68M	5M		54M	3M		54M	3M

Connecticut	26M	2M		20M	2M		20M	2M			

Delaware	9M	.6M		7M	.3M		7M	.3M	

District of 
       Columbia	3M	.2M		2M	.2M		2M	.2M

Florida	155M	10M		123M	6M		123M	6M

Georgia	100M	7M		79M	4M		79M	4M

Hawaii	10M	.6M		7M	.6M		7M	.6M

Idaho	40M	3M		31M	.9M		31M	.9M

Illinois	190M	13M		151M	6M		151M	6M

Indiana	100M	7M		78M	3M		78M	3M

Iowa	79M	6M		62M	2M		62M	2M

Kansas	80M	6M		64M	2M		64M	2M		

Kentucky	53M	4M		42M	2M		42M	2M

Louisiana	71M	5M		56M	2M		56M	2M

Maine	25M	2M		19M	.6M		19M	.6M

Maryland	41M	3M		32M	2M		32M	2M	

Massachusetts	53M	4M		42M	3M		42M	3M

Michigan	125M	9M		98M	5M		98M	5M

Minnesota	95M	7M		75M	3M		75M	3M
	
Mississippi	65M	5M		50M	2M		50M	2M

Missouri	115M	8M		90M	3M		90M	3M
	
Montana	41M	3M		32M	.8M		32M	.8M

Nebraska	62M	5M		50M	2M		50M	2M

Nevada	30M	2M		25M	1M		25M	1M

New     
    Hampshire	15M	1M		12M	.5M		12M	.5M

New Jersey	75M	5M		60M	4M		60M	4M

New Mexico	60M	4M		50M	2M		50M	2M

New York	162M	11M		130M	7M		130M	7M

North Carolina	110M	8M		90M	4M		90M	4M

North Dakota	39M	3M		30M	.6M		30M	.6M

Ohio	125M	9M		100M	5M		100M	5M		

Oklahoma	81M	6M		64M	3M		64M	3M

Oregon	66M	5M		51M	2M		51M	2M

Pennsylvania	160M	12M		125M	5M		125M	5M

Rhode Island	10M	.7M		8M	.4M		8M	.4M

South Carolina	68M	5M		53M	2M		53M	2M

South Dakota	37M	3M		30M	.7M		30M	.7M

Tennessee	85M	6M		68M	3M		68M	3M

Texas	310M	22M		245M	11M		245M	11M

Utah	37M	3M		30M	1M		30M	1M		

Vermont	11M	.8M		9M	.3M		9M	.3M

Virginia	70M	5M		55M	3M		55M	3M

Washington	92M	6M		73M	4M		73M	4M

West Virginia	40M	3M		32M	1M		32M	1M		

Wisconsin	90M	7M		70M	3M		70M	3M

Wyoming 	30M	2M		23M	.5M		23M	.5M

Puerto Rico	33M	2M		27M	1M		27M	1M
 

 
 
