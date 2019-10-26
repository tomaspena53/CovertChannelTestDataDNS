This project contains sets of files for testing detection of DNSExfiltrator-generated covert channels.

- Text files consisted of small file sizes to test recall of detection method.
  -- File sizes in bytes: 1, 2, 3, 5, 8, 13, 55, 144, 610, 2584, 10496, 28657
- Text files were exfiltrated using multiple settings of DNSExfiltrator (test effect of DNS packet generation process)
  -- DNSExfiltrator maximum trasnmission sizes selected to generate files (bytes): 65, 105, 145, 185, 225, 255 (Default)

File Set 1:
- Files by size containing random characters (used as payload for exfiltration from victim to server).
  -- Text files consisted of small file sizes to test recall of detection method.
     --- Sizes in bytes: 1, 2, 3, 5, 8, 13, 55, 144, 610, 2584, 10496, 28657

File Set 2:
- Files containing domain names from files exfiltrated using DNSExfiltrator. 
  -- Files are in "utf" format to support reading in Python when using the Anaconda Machine Learning distribution on Windows 
  -- Files are labeled as positive samples for deep learning array build
     --- Format:  "/0,1/","/domain name/"
	 --- "0" label is normal/benign
	 --- "1" label is exfiltration-related (sequential in order of packet delivery for each file)

File Set 3:
- Files containing 50% exfiltrated data from File Set 2, plus normal samples pulled from the Cisco/OpenDNS Umbrella Top 1 Million websites list
  -- Files are labeled as positive or negative samples for deep learning array build
     --- Files are in "utf" format to support reading in Python when using the Anaconda Machine Learning distribution on Windows 
     --- Format:  "/0,1/","/domain name/"
	 --- "0" label is normal/benign
	 --- "1" label is exfiltration-related (sequential in order of packet delivery for each file)
