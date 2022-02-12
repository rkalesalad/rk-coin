Rkcoin integration/staging tree                                                              
================================
<p align="center">
  <img src="your_relative_path_here" width="128" title="hover text">
  <img src="https://drive.google.com/uc?export=view&id=1HHf5UcRDp1b5If_NdkXX-JyPAZ6DcRxj" width="128" alt="accessibility text">
</p>
Copyright (c) 2009-2014 Bitcoin Developers

Copyright (c) 2011-2014 Litecoin Developers

Copyright (c) 2022 RK coin Developers

What is Rkcoin?
----------------

Rkcoin is a lite version of Bitcoin using scrypt as a proof-of-work algorithm.
 - 2 minute block targets
 - subsidy halves in 420k blocks (~4 years)
 - ~42 million total coins
 - 25 coins per block




Development process
-------------------

Developers work in their own trees, then submit pull requests when they think
their feature or bug fix is ready.

If it is a simple/trivial/non-controversial change, then one of the Rkcoin
development team members simply pulls it.

If it is a *more complicated or potentially controversial* change, then the patch
submitter will be asked to start a discussion with the devs and community.

The patch will be accepted if there is broad consensus that it is a good thing.
Developers should expect to rework and resubmit patches if the code doesn't
match the project's coding conventions (see `doc/coding.txt`) or are
controversial.

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable. [Tags](https://github.com/rkcoin-project/rkcoin/tags) are created
regularly to indicate new official, stable release versions of Rkcoin.

Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test. Please be patient and help out, and
remember this is a security-critical project where any mistake might cost people
lots of money.

### Automated Testing

Developers are strongly encouraged to write unit tests for new code, and to
submit new unit tests for old code.

Unit tests for the core code are in `src/test/`. To compile and run them:

    cd src; make -f makefile.unix test

Unit tests for the GUI code are in `src/qt/test/`. To compile and run them:

    qmake BITCOIN_QT_TEST=1 -o Makefile.test bitcoin-qt.pro
    make -f Makefile.test
    ./rkcoin-qt_test
    
Additionally, commands to operate and use coin once loaded consist of 

    cd desktop/rkcoin 
    qmake
    make
    ./rkcoin-qt
    ./rkcoin-qt -testnet
