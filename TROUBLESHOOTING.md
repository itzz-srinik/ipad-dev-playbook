# Troubleshooting

## "Traceback (most recent call last)"
This is how Python shows an error report. It is not a crash.
Read the last line. That is the real reason.

## ModuleNotFoundError after installing a package
A newer version of the library may have renamed things. Pin the
older version:

    pip install "package-name<2"

Then put the same pin in requirements.txt so others get it too.

## "Could not open requirements file: No such file or directory"
The terminal is in a different folder or the file was not saved.
Run ls to list files. If it is missing, create it from the terminal:

    printf "package-one\npackage-two\n" > requirements.txt

## "Commit operation was cancelled due to empty commit message"
Type a message in the box above the Commit button first.

## A random cache file shows up in Source Control
Create a .gitignore file containing:

    __pycache__/
    *.pyc

## The terminal is stuck on a running server
Open a new terminal with the + button and keep working there.

## Running out of free Codespace hours
Stop the Codespace when done: click the blue button at the bottom
left and choose Stop Current Codespace. Closing the tab does not
stop it right away.

## Safety
Never paste auth tokens or secrets from the terminal into public
places such as issues, READMEs, or screenshots.

