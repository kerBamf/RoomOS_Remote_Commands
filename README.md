#RoomOS Remote Command Utility

A simple utility for sending XML commands to Cisco RoomOS devices

###Dependencies

####Packages
python-dotenv
openpyxl
requests

####Environment Variables
This app uses python-dotenv, so you will need to include a .env with the following variables:
PASSWORD - base64 encoded password for the codecs you intend to access
FILENAME - Name of the xlsx file containing your list of codecs

####File Structure
This utility parses excel(.xlsx) files for retrieving codec IPs and XML files for codec commands
Codec excel files should be located in a directory codec_lists, with IPs listed in the third column
XML files should be stored in a directory called XML_Files
Both directories should be added to your .gitignore file to prevent commit conflicts as files are added and removed

###How To Use
1. Add an excel sheet with a list of IPs to your codec_lists directory and update your .env accordingly
2. Add any necessary xml command files to your XML_Files directory
3. Run send_command.py - When prompted, enter the filename of the xml you wish to send
