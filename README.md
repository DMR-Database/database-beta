<p align="center">
<a href="https://github.com/BM-Database" target="_blank"><img src="img/BM-logo2.gif" width="360"></a>
<br>
<img src="img/BM-beta.jpg" width="300">
<br>
</p>
<hr>

<h1>DMR user database BETA has 158673 entries.
</h1>
<hr>
<h2 id="english">DMR user database <b>BETA</b> for Ailunce, Anytone, Tytera and Pi-Star :)</h2>
DMR user database BETA are unverified "up to date" database files wich are automatically created every 30 minutes. This means that after our normal <a href="https://github.com/bm-database/database">updates</a>, new dmr users who register, will be automatically added here to the databases, but they are not verified yet by us and the data might not be complete. If you always need to be up to date, even if the display might not show all the information for the newest users, then these files are what you need.
<br>
<hr>
<b>Statistics about DMR user database BETA vs verified version (updated when new users are added)
<br>
<br>
</b>
<ul>
<li>Anytone BETA Database has 158674 entries<br>
<li>Anytone verified Database has 158499 entries<br><br>
<li>Ailunce HD1 BETA Database has 158673 entries<br>
<li>Ailunce HD1 verified Database has 158498 entries<br><br>
<li>Tytera MD-2017 BETA Database has 100000 entries<br>
<li>Tytera MD-2017 verified Database has 100000 entries<br><br>
<li>Tytera MD-380 and 390 BETA Database has 158909 entries<br>
<li>Tytera MD-380 and 390 verified Database has 158734 entries<br><br>
<li>Pi-Star BETA Database has 158675 entries<br>
<li>Pi-Star original Database has 157111 entries<br><br>
<li>Pi-Star SSH Helper Database has 158674 entries<br>
</ul>
<hr>
<b>Why is there a difference in the count of entries?</b><br>
<br><ul><li>BETA version is more "up to date" then the verified version.
<br><li>Anytone Database has a leading header.
<br><li>Ailunce HD1 Database has no leading header and represence the actual user count.
<br><li>Tytera MD-2017 Database can only handle 100k users (the first 100k users are put into the database).
<br><li>Tytera MD380/390 Database has leading header and 237 extra TG contacts.
<br><li>Pi-Star database has two leading headers.
<br><li><a href="https://github.com/wa1gov/Pistar-SSH-Helper">Pi-Star SSH Helper</a> Database has one leading header.</li>
</ul>
<hr>
<b>Add our database to your Pi-Star?</b><br>
<br>
If you want to add our Database support to your Pi-Star, just follow this howto.
<br>Execute the following commands in a ssh session with your Pi-Star.
<ul><li>rpi-rw
<li>sudo nano /usr/local/sbin/HostFilesUpdate.sh 
</ul></li>
<br><br>Find the line:
<ul><li>curl --fail -o ${DMRIDFILE} -s http://www.pistar.uk/downloads/DMRIds.dat
</li></ul>
<br>and place a # in front of it
<ul><li>#curl --fail -o ${DMRIDFILE} -s http://www.pistar.uk/downloads/DMRIds.dat
</li></ul>
<br>add the following line under it 
<ul><li>
curl --fail -o ${DMRIDFILE} -s https://raw.githubusercontent.com/DMR-Database/database-beta/master/DMRIds.dat
</ul></li>
<br>it should looke like this now:
<ul>
#curl --fail -o ${DMRIDFILE} -s http://www.pistar.uk/downloads/DMRIds.dat
<br>curl --fail -o ${DMRIDFILE} -s https://raw.githubusercontent.com/DMR-Database/database-beta/master/DMRIds.dat
</ul>
Then press ctrl-x to exit, confirm with y to save and press enter to use the chosen filename.
<br><br>
Then execute sudo pistar-update or sudo HostFilesUpdate.sh and enjoy all callsigns on the display and webinterface.
<br>
We hope that Pi-Star will add this in the future.
<hr>
<b>Download latest DMR user database BETA for Ailunce, Anytone and Tytera
</b>
<ul>
<br>
<li>
<a href="https://raw.githubusercontent.com/DMR-Database/database-beta/master/userhd.csv">BETA Database for Ailunce HD1</a>
</li>
<li>
<a href="https://raw.githubusercontent.com/DMR-Database/database-beta/master/userat.csv">BETA Database for Anytone</a>
</li>
<li>
<a href="https://github.com/DMR-Database/database-beta/raw/master/user.bin">BETA Database for Tytera MD380 & MD390</a>
</li>
<li>
<a href="https://raw.githubusercontent.com/DMR-Database/database-beta/master/usermd2017.csv">BETA Database for Tytera MD-2017</a>
</li>
</ul>
<br>
For MD380-MD390 : If you edit the database by yourself do not forget to fill in the number of characters on the first line. Preview at the bottom of Notepad tab. Example Length: 4,275,525 Enter this number on the first line without commas thus 4275525.
