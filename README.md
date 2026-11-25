# Automated File & Folder Cleanup

A Python automation script designed to remove files and directories older than 30 days from a specified directory (`pics`), helping automate storage maintenance.

## Features

- Recursively traverses directories and subdirectories.
- Checks file and folder timestamps against a predefined threshold.
- Deletes qualifying files and directories.
- Tracks and reports deletion counts.
- Checks whether the target path exists.

## Tech Stack

- **Python 3**
- `os` — Directory traversal, file metadata and file deletion.
- `shutil` — Recursive directory deletion.
- `time` — Timestamp calculation and age comparison.

## How It Works

1. Calculates the cutoff timestamp for 30 days.
2. Traverses the target directory using `os.walk()`.
3. Retrieves metadata change timestamps using `os.stat()`.
4. Deletes files and folders that meet the age condition.
5. Displays the total deletion counts.

## Usage

Configure the target directory and age threshold:

    path = "pics"
    days = 30

Run the script:

    python3 code.py

## Applications

- Automated storage management
- Temporary file cleanup
- Log file maintenance
- Directory housekeeping

## Warning

Deletion is permanent. Test using a disposable directory.
Deleting an old folder also deletes its newer contents.
The current implementation requires improvements to error
handling, directory traversal and deletion counting.
