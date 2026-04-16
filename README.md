# PhD-Seeker 🎓

PhD Seeker is a python web scraper to search for fully funded doctorate positions, advertised on well-known academic position websites.

If nowadays you are actively seeking a PhD position to pursue your studies, you must have realized that the process of searching for relevant vacancies is not straight forward. Visiting a large number of position advertising websites and encountering irrelevant commercials are two of the most common problems.

Simply modify the keywords and you will receive a CSV/XLSX file containing the last two pages from the most popular advertisers.

# Sources 📚
- [www.scholarshipdb.net](http://www.scholarshipdb.net  "www.scholarshipdb.net")
- [www.findaphd.com](http://www.findaphd.com "www.findaphd.com")


# Next Goals 🎯
- [ ] Expanding the academic position advertising source
- [ ] Adding databases of different universities
- [ ] Finding and removing overlapped positions
- [ ] Adding LinkedIn search to get informed directly from university professors
- [X] Getting the keywords from command line instead of hard-coding the source
- [X] Fetching pages simultaneously
- [X] Checking the availability of the new updates of `phdseeker` and notifying the user
- [ ] GUI support

Installation
==============

## PyPi

**phdseeker** is available on [PyPi](http://pypi.python.org/pypi/phdseeker):

    $ pip install phdseeker

## Git

You can get latest stable changes from github server:

    $ git clone https://github.com/archna1212/PHD-OPENINGS.git
    $ cd PhD-Seeker
    $ python setup.py install

## Zip, Tarball

You can download the latest tarball.

### *nix

Get the latest tarball & install:

    $ wget -O phdseeker-master.tar.gz https://github.com/archna1212/PHD-OPENINGS/archive/master.tar.gz
    $ tar xvzf phdseeker-master.tar.gz && cd PhD-Seeker-main
    $ python setup.py install

### Windows

#### Downloading Archive

Download latest zip archive.

https://github.com/Aghababaei/PhD-Seeker/archive/master.zip

Decompress it, and run the following command in root directory of `PhD-Seeker`

    $ python setup.py install

#### Adding Python to Windows environmental variables

Prior to running codes, make sure that Python has been already added to environmental variables as a `PATH`, otherwise:

1. Right-click This PC and going to Properties.
2. Click on the Advanced system settings in the menu on the left.
3. Click on the Environment Variables button o​n the bottom right.
4. In the System variables section, select the Path variable and click on Edit. The next screen will show all the directories that are currently a part of the PATH variable.
5. Click on New and entering Python’s install directory.


#### Requirements
**phdseeker**  is relied on several great python packages.
If you want to just run the code by calling the script, you need to install its dependencies, in advance.
```
pip install -r requirements.txt
```

# Usage
```
phdseeker

Usage:
    phdseeker -h
    phdseeker -V
    phdseeker [-k <keywords> -c <countries> --maxpage=<n> --output=<filetype(s)> -v]

options:
    -h --help                       Show this screen.
    -V --version                    Output version information, and repositories' list and exit.
    -v --verbose                    Show the found positions on the terminal.
    -k <keywords>, --keywords=<keywords>    Declare desired keywords to seek. [default: Computer Science, Machine Learning, Deep Learning]
    -c <countries>, --countries=<countries>    Filter by countries.
    -o <filetype(s)>, --output=<filetype(s)>     Set the output type csv/xlsx/both [default: both]
    --maxpage=<n>                   Maximum number of pages to fetch. [default: 10]
```
### usage example
```
$ phdseeker -k 'Computer Science, Machine Learning' --maxpage=1 -v

Searching for the Keywords 'Computer Science, Machine Learning' in up to 1 page.
========================================::[ scholarshipdb ]::========================================
                                       >> 704 positions found <<
===========================================::[ findaphd ]::==========================================
                                        >> 72 positions found <<

>>>> 776 positions have been found in total.
Specifically, 21 records of them have been saved in the following files:
PhD_Positions_2022-08-08[Computer Science, Machine Learning].csv saved!
PhD_Positions_2022-08-08[Computer Science, Machine Learning].xlsx saved!
Elapsed time is 3.87
┏━━━━━━━━━━━━━━━━━━━┳━━━━━━━━━━━━━━━━━━━━┳━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┓
┃ Country           ┃ Date               ┃ Title                                                    ┃
┡━━━━━━━━━━━━━━━━━━━╇━━━━━━━━━━━━━━━━━━━━╇━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┩
│ 1 Belgium         │                    │ Application of machine learning to screen hyperspectral  │
│                   │                    │ data for important soil and plant properties             │
│ 2 China           │                    │ PhD student (m/f/d) in the field of engineering,         │
│                   │                    │ computer science, technical software development,        │
│                   │                    │ mathematics, physics, data engineering or similar        │
│ 3 China           │                    │ SFI Centre for Research Training in Machine Learning     │
│ 4 Cyprus          │                    │ SFI Centre for Research Training in Machine Learning     │
│ 5 Denmark         │ about 1 hour ago   │ PhD Position in Computational Genetics and Machine       │
│                   │                    │ Learning: analysis of multi-omics biological data in     │
│                   │                    │ novel populations of Brachypodium                        │
│ 6 Denmark         │ about 18 hours ago │ PhD Stipend in Human-in-the-loop Data Mining and Deep    │
│                   │                    │ Learning on Graph Data (16-22068)                        │
│ 7 Germany         │                    │ Discovery of new materials for applications on glass     │
│                   │                    │ using Deep Machine Learning and Data Analytics           │
│ 8 Germany         │                    │ Novel techniques for neuromorphic reservoir computing    │
│ 9 Netherlands     │ 8 days ago         │ PhD Candidate: Graph Neural Networks for Electricity and │
│                   │                    │ Gas Networks                                             │
│ 10 Norway         │ 3 months ago       │ PhD Research Fellow in Informatics - Knowledge           │
│                   │                    │ Representation and Machine Learning                      │
│ 11 Poland         │                    │ The Constitutive Law Establishment of Advanced High      │
│                   │                    │ Strength Steel based on Machine Learning                 │
│ 12 Spain          │ 14 days ago        │ CALL 41-2022-1 Researcher in the Sustainable Artificial  │
│                   │                    │ Intelligence (SAI) research unit                         │
│ 13 Suriname       │ 8 days ago         │ PhD "In silico prediction of antibiotic resistance"      │
│                   │                    │ (M/F)                                                    │
│ 14 Sweden         │ about 12 hours ago │ PhD student in Computational Science and Engineering     │
│                   │                    │ with focus on Optimization for Federated Machine         │
│                   │                    │ Learning                                                 │
│ 15 Switzerland    │ about 2 months ago │ PhD position in the field of Machine Learning            │
│                   │                    │ (Graph-based High-dimensional generative models) with    │
│                   │                    │ application to Medical Data Analysis at the Department   │
│                   │                    │ of Computer Science                                      │
│ 16 United Kingdom │ about 20 hours ago │ Research Assistant                                       │
│ 17 United Kingdom │ 3 days ago         │ PhD Studentship: Implementation of Machine Learning at   │
│                   │                    │ the Edge                                                 │
│ 18 United Kingdom │                    │ Machine Learning Meets Sequential Monte Carlo Methods    │
│ 19 United Kingdom │                    │ PhD Studentship in Computer Science                      │
│ 20 United Kingdom │                    │ SFI Centre for Research Training in Machine Learning     │
│ 21 United Kingdom │                    │ Scholarship for the PhD in Medical Sciences in the       │
│                   │                    │ fields of Neuroscience and Biomedical Engineering for    │
│                   │                    │ the PhD Research Project ‘Development of a closed-loop   │
│                   │                    │ controller for automatic administration of anaesthetic   │
│                   │                    │ and analgesic agents during surgery using machine        │
│                   │                    │ learning methods’                                        │
└───────────────────┴────────────────────┴──────────────────────────────────────────────────────────┘
│                  Out of 776 found Ph.D. positions, 21 have been fetched in 1 page                 │
└───────────────────────────────────────────────────────────────────────────────────────────────────┘
```


