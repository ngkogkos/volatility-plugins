# volatility-plugins
Plugins for the Volatility framework

# facebook_extractor
## Setup
Simply clone the repository locally and copy the facebook_extractor.py inside the "/volatility/volatility/plugins/" path.

## Usage
The facebook_extractor.py contains 3 Volatility plugins:
- facebookgrabinfo
- facebookcontacts
- facebookmessages

For each plugin you can view its available options with:
$ python vol.py "facebook-plugin" -h

Usually you would want to run facebookcontacts firstly, in order to get some contact IDs and the owner's ID. Then you can grab the owner's information and also look up for messages of him with some other contact.

Example:
![Example Usage](http://i.imgur.com/w5DUBSV.png)

## Notes

- The oid argument is not necessary because the plugin should find the owner's ID automatically. However, there is a possibility that 2 different users logged in their account prior to capturing the RAM dump. Hence, the code won't decide for the correct ID but let you know about that and then you would have to supply it with the --oid parameter.
