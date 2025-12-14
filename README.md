Log Archive Tool
Overview

log-archive is a lightweight command-line utility written in Bash that compresses a specified log directory into a timestamped .tar.gz archive. It stores the archive in a dedicated directory and logs the archive date and time for auditing and tracking purposes.

Features

Accepts log directory as a command-line argument

Creates compressed .tar.gz archives

Stores archives in a separate directory

Maintains an archive log with date and time

Simple, dependency-free Bash script

Requirements

Linux or Unix-based system

Bash shell

tar utility (installed by default on most systems)

Usage
log-archive <log-directory>

Example
log-archive /var/log

Output

Archive file format

logs_archive_YYYYMMDD_HHMMSS.tar.gz


Example:

logs_archive_20240816_100648.tar.gz


Archive location

~/log_archives/


Archive log file

~/log_archives/archive.log

Installation

Clone or copy the script:

git clone <repository-url>
cd log-archive


Make the script executable:

chmod +x log-archive


(Optional) Move to a directory in your PATH:

sudo mv log-archive /usr/local/bin/

Logging

Each archive operation is logged in archive.log with the following format:

YYYY-MM-DD HH:MM:SS - Archived <log-directory> to <archive-name>

Error Handling

Exits if no directory argument is provided

Exits if the provided directory does not exist

Stops execution on any command failure

Project Structure
log-archive/
├── log-archive
└── README.md

Use Cases

System log backups

Pre-rotation log archiving

Troubleshooting and audit preparation

Cloud / SRE operational tasks
