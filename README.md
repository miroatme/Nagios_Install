#################################################
#						#
#						#
#	Nagios Install Script Readme		#
#						#
#		Created By Kevin K.		#
#		EMAIL: KevinK@linux.com		#
#						#
#################################################
#
#-------------------------------------------------------------------------------
##This program is free software: you can redistribute it and/or modify
##it under the terms of the GNU General Public License as published by
##the Free Software Foundation, either version 3 of the License, or
##(at your option) any later version.
##
##This program is distributed in the hope that it will be useful,
##but WITHOUT ANY WARRANTY; without even the implied warranty of
##MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
##GNU General Public License for more details.
##
##You should have received a copy of the GNU General Public License
##along with this program.  If not, see <http://www.gnu.org/licenses/>.
##-------------------------------------------------------------------------------

This script will download the latest tarballs, extract them, compile each,
and install the Nagios monitoring program. 
You will need to have a few things before this will work correctly. 
INSTALL: 
make
php
httpd
gcc
glibc
glibc-common
gd
gd-devel
openssl-devel
xinted

Create the user ( and possiblely group) that you will be 
running the program with. 
DEFAULT: nagios ( for user and group)
DEFAULT: nagiosadmin ( for website)

For this you will need to have a list of the latest tarballs 
links for the script to download. This can be done from the Nagios site
or from you own hosts. 
Each link needs to be on different lines, as to conform with the download. 

Example:
http://www.example.com/path/to/nagios-3.1.24.tar.gz
http://www.sample.com/this/is/nagios-plugins-1.4.1.tar.gz
http://www.example.com/dir/is/nrpe.tar.gz

The same pattern can be said for the OPTIONS file. 
OPTIONS file is for what you would use when calling './configure'
This file is needed for the basics of:
nagios admin/gui user
nagios process user

The format is:
--with-nagios-user=[USERNAME]
--with-nagios-group=[GROUPNAME]
--with-command-user=[PROCusername]
--with-command-group=[PROCGROUP]

There are many options that you can use. Please feel free to take
a look at the Nagios Documentation for details and decriptions. 

This files is not needed if you want to 
go with the default of:
nagiosadmin (for the GUI)
nagios (for process)



TODO
Add manual imput for configure options -m | --manual)
Fix portablity issues
and much much more...
