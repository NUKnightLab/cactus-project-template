cactus-project-template
=======================

Basis for creating new Knight Lab-themed documentation or static sites. To use:

Install Cactus
--------------
If you haven't, create a virtual environment for doing cactus projects. While we don't have a lot of experience, it seems you could get away with a single environment for all cactus-based sites.

For now, the core Cactus project hasn't accepted the pull request which supports starting a new cactus project from an alternative source, so you have to plug in Joe's fork.

    mkvirtualenv cactussites
    pip install -e git://github.com/JoeGermuska/Cactus.git#egg=cactus-jlg

You're now ready. Any time you want to start a new "static site," use the following commands:

    cd ~/src (or whereever you keep your git repositories)
    cactus create newsite.knightlab.com --skeleton=https://github.com/NUKnightLab/cactus-project-template/archive/master.zip