The Minlog System

    Overview
    Installation
    Mailing List and Contact

Overview

Minlog is an interactive proof system developed by Helmut Schwichtenberg and members of the logic group at the University of Munich.

Minlog is based on first order natural deduction calculus. It is intended to reason about computable functionals, using minimal rather than classical or intuitionistic logic. The main motivation behind Minlog is to exploit the proofs-as-programs paradigm for program development and program verification. Proofs are in fact treated as first class objects which can be normalized. If a formula is existential then its proof can be used for reading off an instance of it, or changed appropriately for program development by proof transformation. To this end Minlog is equipped with tools to extract functional programs directly from proof terms. This also applies to non-constructive proofs, using a refined A-translation. The system is supported by automatic proof search and normalization by evaluation as an efficient term rewriting device.

The latest version of Minlog is available through Git. Cloning the Git repository of Minlog, you get the source code, case studies, and the following documentation:

    Tutorial, a first introduction to Minlog
    Reference Manual, a more thorough description of Minlog

The case studies contain material from the following publications:

    Logic for Gray-code computation, U. Berger, K. Miyamoto, H. Schwichtenberg and H. Tsuiki. (In D. Probst and P. Schuster (eds), Concepts of Proof in Mathematics, Philosophy, and Computer Science, De Gruyter, 2016, pp. 69–110)
    Higman's Lemma and its computational content, H. Schwichtenberg, M. Seisenberger and F. Wiesnet. (In R. Kahle, T. Strahm and T. Studer (eds), Advances in Proof Theory, Birkhäuser, 2016, pp. 353–375)
    Embedding classical in minimal implicational logic, H. Ishihara and H. Schwichtenberg (Final version in Math. Logic Quarterly 63, 2016, pp. 94–101)
    Program extraction in exact real arithmetic, K. Miyamoto and H. Schwichtenberg (MSCS 25, 2015)
    Program extraction from nested definitions, K. Miyamoto, F. Nordvall Forsberg and H. Schwichtenberg (ITP 2013)
    Program extraction from nested definitions, K. Miyamoto, F. Nordvall Forsberg and H. Schwichtenberg (ITP 2013)
    Minlog - A Tool for Program Extraction Supporting Algebras and Coalgebras, U. Berger, K. Miyamoto, M. Seisenberger, and H. Schwichtenberg (CALCO 2011 Volume LNCS 6859, pp. 393–399)
    Minlog, H. Schwichtenberg (The Seventeen Provers of the World, F. Wiedijk, ed., Springer Verlag, 2006, pp. 151–157)
    Program extraction from normalization proofs, U. Berger, S. Berghofer, P. Letouzey, and H. Schwichtenberg (Final version in Studia Logica 82, 2006, pp. 27–51)
    The Warshall Algorithm and Dickson's Lemma: Two Examples of Realistic Program Extraction, U. Berger, H. Schwichtenberg, and M. Seisenberger, Journal of Automated Reasoning 26, 2001, pp. 205–221
    Proof theory at work: Program development in the Minlog system, H. Benl, U. Berger, H. Schwichtenberg, M. Seisenberger, and W. Zuber (Automated Deduction, W. Bibel and P.H. Schmitt, eds., Vol. II, Kluwer 1998)
    Formal correctness proofs of functional programs: Dijkstra's algorithm, a case study, H. Benl, H.Schwichtenberg (Marktoberdorf '97)
    The greatest common divisor: a case study for program extraction from classical proofs, U. Berger and H. Schwichtenberg (Turin '95)

Details of the theory of Minlog are found in the following book by Schwichtenberg and Stanley S. Wainer.

    Proofs and Computations, H. Schwichtenberg and S. Wainer, 2012 (Perspectives in Logic, Association for Symbolic Logic and Cambridge University Press)

Minlog is implemented in Scheme and runs under every Scheme version supporting the Revised5 Report on the Algorithmic Language Scheme. Minlog's favorite dialect is Chez Scheme from Cisco Systems, Inc., which is freely distributed at the address http://www.scheme.com.
Installation
Prerequisite

Minlog runs on Linux, Unix, Mac OS X and Windows. The following software is prerequisite:

    Git

    Follow the official installation procedure suitable to your computer.
    Chez Scheme or an R5RS Scheme interpreter

    Minlog is fully functional with Chez Scheme 9.4 which is available for free at the official page.
    Make sure that the path is set for shell use.
    Emacs

    Emacs is used as the standard user interface of Minlog. Follow the instruction at the official web page to install Emacs.
    pdfLaTeX

    The documentation is provided as LaTeX source code, which should be compiled by the setup script which uses pdflatex. One can skip installing pdfLaTeX if the documentation is not necessary.
    Command Line Tools (only for Mac users)

    The set up script of Minlog runs with the make command. For Mac, it is freely available via Command Line Tools by Apple.

Minlog through Git

You are going to clone http://www.math.lmu.de/~minlogit/git/minlog.git using Git into a directory where you have a write permission.
Using Command Line

You open the command line and move to a directory where you want to have Minlog, then issue the following command:

git clone http://www.math.lmu.de/~minlogit/git/minlog.git

then you will get the Minlog source code in the newly created directory "minlog" at the current directory. We refer to this directory as the Minlog home and also as MINLOG_HOME.

Using Git GUI

You start Git GUI and choose "Clone Existing Repository". In the dialog window, you specify

http://www.math.lmu.de/~minlogit/git/minlog.git

as Source Location and a directory you like to have Minlog as Target Directory. We refer to the Target Directory you gave as the Minlog home and also as MINLOG_HOME.

Setup
Linux/Unix/Mac OS X

Run the make command in the minlog directory.
Windows

You are going to run the setup script, to prepare a shortcut to launch Minlog, and to compile the documentation. Make sure that the path is set for shell use, changing Windows' Path environment variable.

Double click MINLOG_HOME\winsetup.ss. If a Scheme interpreter is not associated, you associate an installed scheme executable, which is typically found at eg. C:\Program Files\Chez Scheme 9.5.4\bin\ta6nt\scheme.exe. Note that the process of executing the script has to have a write permission under MINLOG_HOME.

Open Explorer and go to the "bin" directory of your Emacs installation (Eg. C:\Users\maier\Downloads\emacs-24.5\bin). Right click "runemacs.exe" in the "bin" directory and create a shortcut. Opening the property of it, you see the path to "runemeacs.exe" as the destination of link. In this text box, you add the text ' -l MINLOG_HOME\util\minlog.el --exec (run-minlog)' (without single quotes and replacing MINLOG_HOME by your Minlog home path) at the end of the existing path. For example, the edited text looks like

C:\Users\maier\emacs-24.5\bin\runemacs.exe -l C:\Users\maier\minlog\util\minlog.el --exec (run-minlog)

Browsing the Minlog home using Explorer, you can also copy the correct full path of the Minlog home via the address bar. In case any of the path contains the space character, see Paths containing spaces on Windows.
When you are done, click "OK" to apply the change, and move the shortcut wherever you prefer.

There are two files MINLOG_HOME\doc\tutor.tex and MINLOG_HOME\doc\ref.tex to compile using pdfLaTeX.
Run Minlog

There is a command line script "minlog" in the Minlog home to launch Minlog with Emacs as a user interface.
Windows users can launch Minlog by double clicking the shortcut, which is described in the previous section. Alternatively, Minlog can be launched by Evaluating the following list in a scheme interpreter:

(load "MINLOG_HOME/init.scm")

Troubleshooting
The rootless mode of Mac OS X 10.11 El Capitan

Due to the rootless mode of Mac OS X 10.11, some folders (e.g., /usr/bin) can be non-writable even by using sudo. For example in the installation of Chez Scheme, you can take the following way to complete the installation through the tarball. It is necessary for you to be an administrator of the computer.

cd csv8.4/custom
./configure --installprefix=/usr/local
sudo make install

After the third line, you would be asked to input your password.

Manually running winsetup.ss

Opening a Scheme interpreter, you can manually run winsetup.ss by the folling line:

(load "MINLOG_HOME/winsetup.ss")

where you replace MINLOG_HOME by the actuall path with replacing each backslash "\" by a slash "/". It is a way to check error messages from the Scheme interpreter when winsetup.ss seems to have failed. When you double click winsetup.ss, the window of Chez Scheme closes quite soon, hence it is not easy to check the error message from Chez Scheme. You can avoid this problem by manually running winsetup.ss.

Emacs does not work within a multi window system

In particular on Mac, there can be a pre-installed command-line emacs which prevents Minlog from recognizing the emacs with multi-windows you have newly installed. This is managed by setting an environment variable EMACS to be the path to the executable of the right Emacs. You open or create a file ~/.bash_profile and add the following line:

export EMACS=/usr/local/bin/emacs

where we assume /usr/local/bin/emacs is the right Emacs. You reopen a terminal, then Minlog should start in the multi-window environment. If you only know the icon to launch Emacs, but no file name of the executable, you type the following in the terminal while Emacs is running.

ps xa | grep macs

It shows some lines containing the path to the executable, which typically starts with /Applications/.

It's cumbersome to change the current directory or to type a long path to start Minlog

It is more convenient if you can type just "minlog" in the command line to start it wherever your current directory is. You can take one of the following two options if you use Linux/Unix/Mac OS X.

    You add the following line to your ~/.bash_profile

    export PATH=MINLOG_HOME:$PATH

    where MINLOG_HOME should be replaced by the real path of your minlog. After editing the file, you have to open a new terminal to use the updated .bash_profile.
    You go to (for example) /usr/local/bin and issue the following command.

    ln -s MINLOG_HOME/minlog

    where MINLOG_HOME should be replaced by the real path of your minlog system installed. Make sure that you do not have minlog in the directory (for example) /usr/local/bin before you issue the above command. The reason of having /usr/local/bin here is just because this directory is typically in the environment variable $PATH by default. You can choose anything else suitable with your preference and system.

Paths containing spaces on Windows

The path should be quoted by the double quotation (") in case a path contains a space. For example,

"C:\Program Files\emacs-24.5\bin\runemacs.exe" -l "C:\Program Files\minlog\util\minlog.el" --exec (run-minlog)

Any difference between math.lmu.de and www.mathematik.uni-muenchen.de?

They are pointing the same server.
Further Information

We give further information to work with the source code of Minlog using Git. We assume you are at anywhere under the Minlog home when you issue a git command.
Updating Minlog

New features of Minlog become available as soon as they are ready to be published. In order to update the Minlog source code, issue

git pull

It is recommended to do the setup procedure again.

Beta Version

There are two branches in the repository, master and dev, which stands for development. The former one is the stable version, and the latter is the beta version.

In order to switch to another branch, for example to dev, issue

git checkout dev

It is recommended to do the setup procedure again.

In order to check what the current branch is, issue

git status

Generating Emacs Tags Table

By running the make command at MINLOG_HOME/src the Emacs tags table of Minlog source code can be generated and saved as MINLOG_HOME/src/TAGS. For details see Emacs documentation.
Mailing List and Contact

The development of Minlog can be followed on the Minlog Mailing List. Send an email to

MINLOG-subscribe@lists.mathematik.uni-muenchen.de

in order to join the mailing list.

If you have any problems with the Minlog system or suggestions please feel free to post an email to minlog@mathematik.uni-muenchen.de.

By Kenji Miyamoto
Last update: 29.09.2017 
