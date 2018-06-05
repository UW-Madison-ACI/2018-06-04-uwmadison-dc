---
layout: workshop      # DON'T CHANGE THIS.
carpentry: "dc"    # what kind of Carpentry (must be either "lc" or "dc" or "swc")
venue: "3218 Sewell Social Sciences Building"        # brief name of host site without address (e.g., "Euphoric State University")
address: "Social Science Computing Cooperative, 4226 William H Sewell Social Sciences Building, 1180 Observatory Dr, Madison, WI 53706"      # full street address of workshop (e.g., "Room A, 123 Forth Street, Blimingen, Euphoria")
country: "us"      # lowercase two-letter ISO country code such as "fr" (see https://en.wikipedia.org/wiki/ISO_3166-1)
language: "en"     # lowercase two-letter ISO language code such as "fr" (see https://en.wikipedia.org/wiki/ISO_639-1)
latlng: "43.0764116,-89.4052577"       # decimal latitude and longitude of workshop venue (e.g., "41.7901128,-87.6007318" - use http://www.latlong.net/)
humandate: "Jun 4-5, 2018"    # human-readable dates for the workshop (e.g., "Feb 17-18, 2020")
humantime: "8:30am - 4:30pm"    # human-readable times for the workshop (e.g., "9:00 am - 4:30 pm")
startdate: 2018-06-04      # machine-readable start date for the workshop in YYYY-MM-DD format like 2015-01-01
enddate: 2018-06-05        # machine-readable end date for the workshop in YYYY-MM-DD format like 2015-01-02
instructor: ["Lauren Michael", "Michelle Craft","Dorothea Salo", "Maria Kamenetsky", "Karl Broman"] # boxed, comma-separated list of instructors' names as strings, like ["Kay McNulty", "Betty Jennings", "Betty Snyder"]
helper: ["Trisha Adamus", "Christina Koch"]     # boxed, comma-separated list of helpers' names, like ["Marlyn Wescoff", "Fran Bilas", "Ruth Lichterman"]
email: ["ContactACI@lists.wisc.edu"]    # boxed, comma-separated list of contact email addresses for the host, lead instructor, or whoever else is handling questions, like ["marlyn.wescoff@example.org", "fran.bilas@example.org", "ruth.lichterman@example.org"]
collaborative_notes: "http://pad.software-carpentry.org/2018-06-04-uwmadison-dc"            # optional: URL for the workshop collaborative notes, e.g. an Etherpad or Google Docs document
eventbrite: "45449830667"          # optional: alphanumeric key for Eventbrite registration, e.g., "1234567890AB" (if Eventbrite is being used)
---

<!-- run "make workshop-check" to check things -->

Registration is required and will be available just below, starting at
5:00pm on Wednesday, 9 May 2018.
Make sure to read all details below before registering and to choose appropriately between UW-Madison's
[Data Carpentry](https://uw-madison-aci.github.io/2018-06-04-uwmadison-dc/) and
[Software Carpentry](https://uw-madison-aci.github.io/2018-06-06-uwmadison-swc/) workshops.

{% if page.eventbrite %}
<iframe
  src="https://www.eventbrite.com/tickets-external?eid={{page.eventbrite}}&ref=etckt"
  frameborder="0"
  width="100%"
  height="206px"
  scrolling="auto">
</iframe>
{% endif %}


## General Information

[Data Carpentry](http://datacarpentry.org) workshops are for any researcher
who has data they want to analyze, and no prior computational experience is required.
This hands-on workshop teaches basic concepts, skills and tools for working more
effectively with data.

We will cover data organization in spreadsheets, OpenRefine, SQL for
data management, and R for data analysis and visualization.

For researchers who have already been programming and seek to expand their capabilities, our
UW-Madison [Software Carpentry workshop (Jun 6-7)](https://uw-madison-aci.github.io/2018-06-06-uwmadison-swc) will likely be more appropriate.
These two workshops are NOT intended to be taken back-to-back, and you can learn about
future workshops at UW-Madison by joining the [mailing list](http://wisc.us9.list-manage.com/subscribe?u=c3aae71670855b66d79d170b8&id=6d65510fb6)
of UW-Madison's [Advanced Computing Initiative](http://aci.wisc.edu/).

**Who:**
  The course is aimed at UW-Madison-affiliated graduate students, staff, and other researchers.


{% if page.latlng %}
<p id="where">
  <strong>Where:</strong>
  {{page.address}}.
  Get directions with
  <a href="//www.openstreetmap.org/?mlat={{page.latlng | replace:',','&mlon='}}&zoom=16">OpenStreetMap</a>
  or
  <a href="//maps.google.com/maps?q={{page.latlng}}">Google Maps</a>.
</p>
{% endif %}

{% if page.humandate %}
<p id="when">
  <strong>When:</strong>
  {{page.humandate}}.
  {% include workshop_calendar.html %}
</p>
{% endif %}

<p>
  <strong>Requirements:</strong> Participants should plan to attend BOTH days of the workshop and bring a
  laptop with a Mac, Linux, or Windows operating sytem (not a tablet, Chromebook, etc.) that they have
  administrative privileges on. They should have a few specific software packages installed (listed
  <a href="#setup">below</a>). They are also required to abide by
  Data Carpentry's
  <a href="{{site.dc_site}}/code-of-conduct/">Code of Conduct</a>.
</p>

{% comment %}
  ACCESSIBILITY

  Modify the block below if there are any barriers to accessibility or
  special instructions.
{% endcomment %}
<p id="accessibility">
  <strong>Accessibility:</strong> We are committed to making this workshop
  accessible to everybody.
  The workshop organizers have checked that:
</p>
<ul>
  <li>The room is wheelchair / scooter accessible.</li>
  <li>Accessible restrooms are available.</li>
</ul>
<p>
  Materials will be provided in advance of the workshop and
  large-print handouts are available if needed by notifying the
  organizers in advance.  If we can help making learning easier for
  you (e.g. sign-language interpreters, lactation facilities) please
  get in touch (using contact details below) and we will
  attempt to provide them.
</p>

{% comment %}
  CONTACT EMAIL ADDRESS

  Display the contact email address set in the configuration file.
{% endcomment %}
<p id="contact">
  <strong>Contact</strong>:
  Please email
  {% if page.email %}
    {% for email in page.email %}
      {% if forloop.last and page.email.size > 1 %}
        or
      {% else %}
        {% unless forloop.first %}
        ,
        {% endunless %}
      {% endif %}
      <a href='mailto:{{email}}'>{{email}}</a>
    {% endfor %}
  {% else %}
    to-be-announced
  {% endif %}
  for more information.
</p>

<hr/>

{% comment %}
 SURVEYS - DO NOT EDIT SURVEY LINKS
{% endcomment %}
<h2 id="surveys">Surveys</h2>

{% if page.carpentry == "swc" %}
<p>Please be sure to complete these surveys before and after the workshop.</p>
<p><a href="{{ site.swc_pre_survey }}{{ site.github.project_title }}">Pre-workshop Survey</a></p>
<p><a href="{{ site.swc_post_survey }}{{ site.github.project_title }}">Post-workshop Survey</a></p>
{% elsif page.carpentry == "dc" %}
  <p>Please be sure to complete these surveys before and after the workshop.</p>
<p><a href="{{ site.dc_pre_survey }}{{ site.github.project_title }}">Pre-workshop Survey</a></p>
<p><a href="{{ site.dc_post_survey }}{{ site.github.project_title }}">Post-workshop Survey</a></p>
{% elsif page.carpentry == "lc" %}
<p>Ask your instructor about pre- and post-workshop Survey details.</p>
{% endif %}

<hr/>


<h2 id="schedule">Preliminary schedule</h2>

<h3>Day 1</h3>
<table class="table table-striped">
<tr> <td>8:30 - 9:00</td>  <td>Installation Help</td> </tr>
<tr> <td>9:00 - 9:10</td>  <td><a href="2018-06-04_DC_intro.pdf">Introduction</a></td> </tr>
<tr><td>9:10 - 10:30</td> <td><a href="https://lmichael107.github.io/spreadsheet-ecology-lesson/">Data Organization in Spreadsheets</a></td></tr>
<tr><td>10:30 - 10:45</td> <td>Break</td></tr>
<tr><td>10:45 - 12:00 </td> <td><a href="http://www.datacarpentry.org/OpenRefine-ecology-lesson/">Data Cleaning with OpenRefine</a></td></tr>
<tr><td>12:00 - 1:00</td> <td>Lunch Break</td></tr>
<tr><td>1:00 - 2:15</td> <td><a href="http://www.datacarpentry.org/sql-ecology-lesson/">Data Management with SQL</a></td></tr>
<tr><td>2:15 - 2:30</td> <td>Coffee</td></tr>
<tr><td>2:30 - 4:00</td> <td><a href="http://www.datacarpentry.org/sql-ecology-lesson/">Data Management with SQL</a></td></tr>
</table>


<h3>Day 2</h3>
<table class="table table-striped">
<tr> <td>8:30 - 9:00</td>  <td>Installation Help</td> </tr>
<tr><td>9:00 - 9:15</td> <td>Day 2 intro</td></tr>
<tr><td>9:15 - 10:30</td> <td>Intro to R</td></tr>
<tr><td>10:30 - 10:45</td> <td>Break</td></tr>
<tr><td>10:45 - 12:00</td> <td>Data manipulation with dplyr</td></tr>
<tr><td>12:00 - 1:00</td> <td>Lunch Break</td></tr>
<tr><td>1:00 - 2:30</td> <td>Data Visualization with ggplot2 </td></tr>
<tr><td>2:30 - 2:45</td> <td>Coffee</td></tr>
<tr><td>2:45 - 3:15</td> <td>Reproducible reports with R Markdown </td></tr>
<tr><td>3:15 - 4:00</td> <td>Capstone project </td></tr>
<tr><td>4:00 - 4:15</td> <td>Wrap up and fill out the post-workshop survey (see below)</td></tr>
</table>




{% if page.collaborative_notes %}
<p id="collaborative_notes">
  We will use this <a href="{{page.collaborative_notes}}">collaborative document</a> for chatting, taking notes, and sharing URLs and bits of code.
</p>
{% endif %}

<hr/>


<h2 id="setup">Setup</h2>

To participate in a Data Carpentry workshop,
you will need working copies of the software described below.
Please make sure to install everything and try opening it to make sure it works
_before_ the start of your workshop. If you run into any problems,
please feel free to email the instructor or arrive early to your workshop on
the first day.

Participants should bring and use their own laptops to insure the proper setup of
tools for an efficient workflow once you leave the workshop.

This workshop will be using the software outlined in the install instructions below.
Please see the section for your operating system for those directions.

<h3 id="windows">Windows</h3>

Please go through all the installation steps below and make sure that
you not only installed them, but start them up to make sure they're working.
If you have any problems, don't hesitate to email the instructors to
ask for help, or arrive early on the first day of the workshop to
get help.

- **A spreadsheet program**

  For this workshop you will need a spreadsheet program. Many people already have
  Microsoft Excel installed, and if you do, you're set!

  If you need a spreadsheet
  program, there are a few other options, like OpenOffice and LibreOffice. Install
  instructions for LibreOffice, which is free and open source, are here.

  - **Download the Installer**

    Install LibreOffice by going to the [installation
    page](https://www.libreoffice.org/download/libreoffice-fresh/).
    The version for Windows should automatically be selected.
    Click on the button below "Main Installer" **Download Version
    x.y.z**. You will go to a page that asks about a donation,
    but you don't need to make one. Your download should begin
    automatically.

  - **Install LibreOffice**

    Once the installer is downloaded, double click on it and it should install.

  - To use LibreOffice, double click on the icon and it will open.

- **OpenRefine**

  OpenRefine (previously Google Refine) is a tool for data cleaning
  that runs through a web browser, and any browser -
  Safari, Firefox, Chrome, Explorer - should work fine.
  You will need to download OpenRefine and install it,
  and when you open it, it will run through the browser, but you don't need
  an internet connection, and the data will all be stored on your computer.

  - Go to the OpenRefine [download page](http://openrefine.org/download.html)

  - Click on _Windows kit_ to download the install file

  - To use it, unzip, and double-click on openrefine.exe (if you're having issues
    with openrefine.exe try refine.bat instead)

  - OpenRefine will then open in your web browser.

  - If it doesn't open automatically, open a web broswer after
    you've started the program and go to the URL
    <http://localhost:3333> and you should see OpenRefine.

- **R**

  In the workshop, we will use RStudio. RStudio is a nice interface to the
  programming language R. To use RStudio, you need to install both R and RStudio.

  - Download R from [here](http://cran.r-project.org/bin/windows/base/release.htm)

  - Run the .exe file that was just downloaded

  - Go to the [RStudio Download page](http://www.rstudio.com/ide/download/desktop)

  - Under _Installers_ select **RStudio 0.98.1103 - Windows XP/Vista/7/8**

  - Double click the file to install it

  - Once it's installed, open RStudio to make sure it works and you don't get any error messages.


- **SQLite**

  For this workshop we're going to use DB Browser for SQLite.

  - Download the Windows.exe installer from the
    [the DB Browser for SQLite website](http://sqlitebrowser.org/).

  - Open the downloaded file and follow the instructions to install to your computer.




---

<h3 id="mac">Mac</h3>

Please go through all the installation steps below and make sure that
you not only installed them, but start them up to make sure they're working.
If you have any problems, don't hesitate to email the instructors to
ask for help, or arrive early on the first day of the workshop to
get help.

- **A spreadsheet program**

  For this workshop you will need a spreadsheet program. Many people already have
  Microsoft Excel installed, and if you do, you're set!

  If you need a spreadsheet
  program, there are a few other options, like OpenOffice and LibreOffice. Install
  instructions for LibreOffice, which is free and open source, are here.

  - **Download the Installer**

    Install LibreOffice by going to the [installation page](https://www.libreoffice.org/download/libreoffice-fresh/). The version for Mac
    should automatically be selected. Click on the button below "Main Installer" **Download Version x.y.z**. You
    will go to a page that asks about a donation, but you don't need to make one.
    Your download should begin automatically.

  - **Install LibreOffice**

    Once the installer is downloaded, double click on it and it should install.

  - To use LibreOffice, double click on the icon and it will open.

- **OpenRefine**

  OpenRefine (previously Google Refine) is a tool for data cleaning
  that runs through a web browser, and any browser -
  Safari, Firefox, Chrome, Explorer - should work fine.
  You will need to download Google Refine and install it,
  and when you open it, it will run through the browser, but you don't need
  an internet connection, and the data will all be stored on your computer.

  - Go to the OpenRefine [download page](http://openrefine.org/download.html)

  - Click on _Mac kit_ to download the install file

  - Open the downloaded .dmg file

  - Drag the icon in to the Applications folder

  - Double click on the icon and Google Refine will then open in your web browser.

  - If it doesn't open automatically, open a web broswer after you've started the program and go to the URL <http://localhost:3333> and you should see OpenRefine.

- **R**

  In the workshop, we will use RStudio. RStudio is a nice interface to the
  programming language R. To use RStudio, you need to install both R and RStudio.

  - Go to [CRAN](http://cran.r-project.org) and click on _Download R for (Mac) OS X_

  - Select the .pkg file for the version of OS X that you have and the file
    will download.

  - Double click on the file that was downloaded and R will install

  - Go to the [RStudio Download page](http://www.rstudio.com/ide/download/desktop)

  - Under _Installers_ select **RStudio x.yy.zzz - Mac OS X 10.6+ (64-bit)** to download it.

  - Once it's downloaded, double click the file to install it

  - Once it's installed, open RStudio to make sure it works and you don't get any error messages.


- **SQLite**

  For this workshop we're going to use DB Browser for SQLite.

  - Download the Mac .dmg installer from the
    [the DB Browser for SQLite website](http://sqlitebrowser.org/).

  - Open the downloaded file and follow the instructions to install to your computer.




---

<h3 id="linux">Linux</h3>

Please go through all the installation steps below and make sure that
you not only installed them, but start them up to make sure they're working.
If you have any problems, don't hesitate to email the instructors to
ask for help, or arrive early on the first day of the workshop to
get help.

- **A spreadsheet program**

  For this workshop you will need a spreadsheet program. LibreOffice comes
  preinstalled with several Linux distributions. If you don't already have it, use
  your package manager to install it: (e.g., `sudo apt-get install
  libreoffice` for Ubuntu and other Debian-based distributions).


- **OpenRefine**

  OpenRefine (previously Google Refine) is a tool for data cleaning that runs
  through a web browser, and any browser - Safari, Firefox, Chrome, Explorer -
  should work fine.  You will need to download Google Refine and install it, and
  when you open it, it will run through the browser, but you don't need an
  internet connection, and the data will all be stored on your computer.

  - Go to the OpenRefine [download page](http://openrefine.org/download.html)

  - Click on _Linux kit_ to download the install file

  - Download and extract

  - Type `./refine` in your terminal and Google Refine will then
    open in your web browser.

  - If it doesn't open automatically, open a web broswer after you've started
    the program and go to the URL <http://localhost:3333> and you should
    see OpenRefine.


- **R**

  In the workshop, we will use RStudio. RStudio is a nice interface to the
  programming language R. To use RStudio, you need to install both R and RStudio.

  - Follow the instructions for your distribution
    from [CRAN](https://cloud.r-project.org/bin/linux/). For most distributions, you
    can use your package manager (e.g. for Debian/Ubuntu run `sudo
    apt-get install r-base`, and for Fedora run `sudo yum install
    R`) but make sure that you have at least R 3.2.2 (as pre-packaged
    versions might be out of date).

  - To install RStudio, go to
    the [RStudio Download page](http://www.rstudio.com/ide/download/desktop)

  - Under _Installers_ select the version for your distribution.

  - Once it's downloaded, double click the file to install it (or `sudo dpkg
    -i rstudio-x.yy.zzz-amd64.deb` at the terminal).

  - Once it's installed, open RStudio to make sure it works and you don't get any error messages.


- **SQLite**

  For this workshop we're going to use DB Browser for SQLite.

  - Download the appropriate installer from the
    [the DB Browser for SQLite website](http://sqlitebrowser.org/).

  - Open the downloaded file and follow the instructions to install to your computer.

---
