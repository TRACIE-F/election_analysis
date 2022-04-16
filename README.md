# Colorado Election Analysis #

## Overview of Election Audit ##
The purpose of this audit is to determine the results of an election in Colorado. The results determined are total votes, voter turnout by county, largest county turnout, candidate results, and election winner. With proper adjustments, this code is re-usable for other elections.

## Election-Audit Results ##

 * In this election, 369,711 total votes were cast in all of Jefferson, Denver, and Arapahoe county.
![total_votes](https://github.com/TRACIE-F/election_analysis/blob/main/Resources/Total_votes.png)

* The voter county turnout breaks down as follows:
    * **Jefferson County** accounted for **10.5%** of the total votes with **38,855** votes.
    * **Denver County** accounted for **82.8%** of the total votes with **306,055** votes.
    * **Arapahoe County** accounted for **6.7%** of the total votes with **24,801** votes.
![county_votes](https://github.com/TRACIE-F/election_analysis/blob/main/Resources/County_votes.png)

* By a significant margin, **Denver County** had the highest voter turnout
![largest_county_turnout](https://github.com/TRACIE-F/election_analysis/blob/main/Resources/Largest_county_turnout.png)

 * The candidate vote totals break dwon as follows:
   * **Charles Casper Stockham** won **23%** of the total votes with **85,213** votes.
   * **Diana Degettte** won **73.8%** of the total votes with **272,892** votes.
   * **Raymon Anthony Doane** won **3.1%** of the total votes with **11,606** votes.
![candidate_results](https://github.com/TRACIE-F/election_analysis/blob/main/Resources/candidate_results.png)

 * The winner is **Diana Degettte** with **73.8%** of the total votes with **272,892** votes.
![the_winner_is](https://github.com/TRACIE-F/election_analysis/blob/main/Resources/the_winner_is.png)

## Election-Audit Summary ##
In a summary statement, provide a business proposal to the election commission on how this script can be used—with some modifications—for any election. Give at least two examples of how this script can be modified to be used for other elections.

**Code Modifications**
The structure of the election analysis code allows for re-use with relatively simple modifications. The code is set up to:
 * Connect to a .csv file with the election data
 * Filter through the candidates and counties to count the number of votes for both
 * Calculate the percentages for voter turnout per county and for candidates
 * Print the results for the total votes, county turnout, largest voter turnout, candidate results, and overall winner to a .txt file

To utilize the code again for a different election:

 * Maintain the same file structure
   * It is vital for the code to maintain these folder structures:
      * A main folder (name is flexible) containing the Python code
      * A sub-folder (Resources) containing the election results .csv file
      * A sub-folder (Analysis) to hold the .txt file created by the code
 ![folder_structure](https://github.com/TRACIE-F/election_analysis/blob/main/Resources/file_structure.png)
 
 * Importing the .csv
   *  In line 9 of the Python code, we import the election data. If the folder structure matches the instructions above, simply adjust the name of the file to match your uploaded .csv. If the new .csv is named *Disctrict123_election_results* the updated code should read `file_to_load = os.path.join("Resources","District123_election_results.csv")`
![Code_change_1](https://github.com/TRACIE-F/election_analysis/blob/main/Resources/Code_change_1.png)

 * Structure your data or adjust the code
   * To ensure the code pulls the appropriate data, one of two things must happen:
      * Adjust your data to ensure the candidate's name is in column C and the county's name is in column B OR
      * Alter the code in row 48 and 51 to match the new .csv structure. For example, if a new .csv has the candidate name in column D and county name in column A, row 48 of the code should be altered to read `candidate_name = row[3]` and row 51 of the code should be altered to read `county_name = row[0]`
![Code_change_3](https://github.com/TRACIE-F/election_analysis/blob/main/Resources/Code_change_3.png)
