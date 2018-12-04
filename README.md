# Dance Organizer
This program is intended to help with the placement of dancers in Higher Grounds.
The intended use is to export the results of a Google survey into a CSV file, and feed the CSV
file into this program. Changing the survey will likely cause this program to become outdated, and 
require updates from me or someone else similarly qualified.

## Instructions for Use
1.  Go to the 'Releases' tab on this page, and download the latest release.
2.  Unzip this release into a folder somewhere.
3.  Go to your survey's Google Sheet with the survey output, and export it as a CSV
4.  Move the CSV from the last step into the folder you created in step 3, and rename it `input.csv`.
5.  Doubleclick the .exe file in that folder. There may be warnings about unknown software or admin
rights. Grant it whatever it wants.
6.  The program will run, and display some messages in a command line. You may normally ignore these.
It will then generate several files, which contain the dance organization results. These will
be `.csv` files, which can be uploaded back into Excel or Google Sheets for viewing/distribution.
7.  Enjoy a free Saturday!

## Algorithm
Any acceptable dance arrangement must satisfy the following:
1.  Every dance must have an acceptable number of participants
2.  Every dancer must be in an acceptable number of dances
3.  Dancers shouldn't have dances in the wrong styles, be in dances they don't want, or dances
which are the wrong skill level.

I therefore proceed with the following process:
1.  Move through the whole primacy-sorted list and try to give each dancer at least one of her (apologies for the sexism)
requests. 
2.  Give each dancer as many requests as possible, in order of primacy.
3.  Put each dancer in their minimum number of desired dances, respecting style and skill guidelines.
4.  Give each dance its minimum number of dancers, respecting style and skill guidelines.
5.  Complain if there are still dances or dancers without acceptable assignments.

### Dancer Information
The above algorithm implies the need to collect the following information about each dancer:
* Name
* Year
* Skill Rating (currently dealing with this as a number but could really be any conditional system)
* Dance Styles

Accordingly, we will also need the following information about each dance:
* Name
* Style
* Max Dancers
* Min Dancers
* Preferred Number of Dancers
* Skill Distribution (how many dancers of each skill band)

I will include an example Google Sheet with these fields filled in there can be no confusion as to the structure.
