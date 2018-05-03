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
