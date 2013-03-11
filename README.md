cactus-project-template
=======================

Basis for creating new Knight Lab-themed documentation or static sites. To use:

Install Cactus
--------------
If you haven't, create a virtual environment for doing cactus projects. While we don't have a lot of experience, it seems you could get away with a single environment for all cactus-based sites.

For now, the core Cactus project hasn't accepted the pull request which supports starting a new cactus project from an alternative source, so you have to plug in Joe's fork.

    mkvirtualenv cactussites
    pip install -e git://github.com/JoeGermuska/Cactus.git#egg=cactus-jlg

You're now ready. See below for guidance on starting a new site.


Start a new site
----------------
In a terminal:
    workon cactussites
    cd ~/src (or whereever you keep your git repositories)
    cactus create newsite.knightlab.com --skeleton=https://github.com/NUKnightLab/cactus-project-template/archive/master.zip
    cd newsite.knightlab.com
    cactus serve
    
You're now looking at your site. Have fun!

Add your new site to GitHub
---------------------------
First, create the git repository where the site will live.
* Go to https://github.com/new
* Choose "NUKnightLab" from the "owner" menu
* For the repository name, use the fully-qualified domain name of the site (e.g. newsite.knightlab.com)
* Check "Public"
* Uncheck "Initialize this repository with a README"

In a terminal:
    cd ~/src/newsite.knightlab.com
    git add *
    git commit -m "initial"
    git remote add origin git@github.com:NUKnightLab/newsite.knightlab.com.git
    git push -u origin master
