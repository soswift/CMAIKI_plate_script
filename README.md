 Sean Swift 20181211
 how to use make_plate_map.r

# List of inputs

Must include:
-i	= Input, i.e. your barcodes that you scanned using your phone. Scan by columns starting at A1 ( A1-H1, A2-H2, etc.)
		This should be exported as a .csv file

-m	= Metadata, i.e. "CMAIKI_Sample_Collection" spreadsheet, downloaded as a .csv file. The barcodes will be matched to this file, so make sure it is the most up to date version.

Optional: 

-o		= output, if you want to specify the filename of the output (this might not work, probably don't use)

-p		= pdf output, if you want to specify the filename of the pdf plate map (which may be broken)

--nopdf		= disable pdf output. 
--textwrap 	= set which character to wrap text, not really that importan unless you want a pretty pdf map


# What to enter into the command line

 1. Move your input and metadata files into the folder
 i.e. download "CMAIKI_Sample_Collection" as a csv and move it to Desktop/R/CMAIKI_plate_script/
 then download the barcode .csv from your phone and move it to Desktop/R/CMAIKI_plate_script/

 2. Open terminal

 3. Change the directory so that you are in the CMAIKI_plate_script folder

 cd Desktop/R/CMAIKI_plate_script/

 4. Run make_plate_map.r with input (-i) as barcode .csv and metadata (-m) as the CMAIKI_Sample_Collection spreadsheet.

 note: these must be in the same folder as make_plate_map.r, or you will need to specify which folder they are in
(e.g. /home/sean/Desktop/R/CMAIKI_plate_script/plate3_20181203/METADATA_C- MAIKI_Sample_Collection_All_Samples_20181203.csv).

./make_plate_map.r -i "INPUT_cmaikibarcodes_Plate3.csv" -m "METADATA_C-MAIKI_Sample_Collection_All_Samples_20181203.csv"

 Ignore the warning, but make sure there are no ERROR messages, because this means things didn't work. 
 Go back and check your spreadsheets to make sure they don't have duplicate entries or missing information.
