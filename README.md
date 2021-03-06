# Moodle Course Builder

[![Build Status][travis-image]][travis-url]

![](https://media.giphy.com/media/bkIgPwdV3Afzq/giphy.gif)

### Moodle Course Backup Building/Modification Tool

This tool was created to allow the editing of a course backup on a local machine for various reasons.

To install this tool:
1. Install Python 3+
2. Add the python bin directory to your run path
3. Install the [openpyxl library](https://openpyxl.readthedocs.io/en/default/) with pip
4. If you are on Mac, remove comment for line 108, and comment out line 111 of objxls.py

To use this tool:
1. Backup a Moodle Course Shell and download the .mbz file
2. Extract the .mbz file using tar, 7zip, or MacOS default archiver (rename the file *.tar or *.zip) to a directory
3. Run "py xmlgenerator"
4. Enter the path to your extracted Moodle Backup
5. Pick option 2 to output the backup into an Excel Spreadsheet
6. The excel file will save into the tool directory
7. Edit the excel file to your liking
8. Run the tool and pick option 1 to import the Excel file into the backup directory
9. Finally archive the backup and import (see archive commands below)
10. You will see the changes you made in the imported backup

Archive Commands:
```sh
tar -czvf backup-moodle2-course-2-tmplt-20170709-1618-nu.mbz ./
```
must be run inside the backup directory where the moodle_backup.xml file is located

In Windows, download [GNU Tools for Windows](https://sourceforge.net/projects/gnuwin32/files/libarchive/2.4.12-1/libarchive-2.4.12-1-setup.exe/download):
```sh
"%programfiles(x86)%\gnuwin32\bin\bsdtar.exe" czvf backup-moodle2-course-2-tmplt-20170709-1618-nu.mbz ./
```

<!-- Markdown link & img dfn's -->
[npm-image]: https://img.shields.io/npm/v/datadog-metrics.svg?style=flat-square
[npm-url]: https://npmjs.org/package/datadog-metrics
[npm-downloads]: https://img.shields.io/npm/dm/datadog-metrics.svg?style=flat-square
[travis-image]: https://img.shields.io/travis/dbader/node-datadog-metrics/master.svg?style=flat-square
[travis-url]: https://travis-ci.org/dbader/node-datadog-metrics
[wiki]: https://github.com/yourname/yourproject/wiki
