# aawk
Linux awk short command 

This script will shorten your awk filtering commands. 

Ex. If you want to filter all dates from below log file

time=t1 date=d1 rule=in
time=t2 date=d3 rule=out
rule=r3 date=sd3 run=no

Long awk command is	: awk -F"date=" '{print $2}' your.log | cut -f1 -d" "
Output you will get	: 	d1
						d3
						sd3

This script will shorten your awk command. Using the aawk.py you can use the same command by: python3 aawk.py "date=" " " your.log 

If you copy this aawk.py to your /usr/bin file and add a alias you can further shorten the command : aawk "date=" " " your.log

Requirenment: python3

How to run :

1) Download the aawk.py
2) Copy the aawk.py file

sudo cp aawk.py /etc

3) Add alias to run the aawk.py 

	Open the .bashrc file

	vi ~/.bashrc


	Add new alias

	alias aawk='python3 /etc/aawk.py'
