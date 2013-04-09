django-dosiero
==============

Simple Django app to allow administrators to upload and manage media files,
for use with flatpages or another simple CMS, for example.

Requirements
------------

Django 1.4.x. Other versions may work but have not been tested.


Usage
-----

Copy the dosiero directory to your project, or put it on your PYTHONPATH.
Add 'dosiero' to your INSTALLED_APPS and run syncdb. You will have a new
app in your admin that users with administrative rights can use to upload
files and link to from elsewhere.

Configuration
-------------

You can set the following configuration variables in your settings.py:

* DOSIERO_UPLOAD_TO is the subdirectory of the media folder that files will be
uploaded too (i.e., the upload_to argument to FileField). Default: 'dosiero'.

* If DOSIERO_BACKUP_DIR is defined, then deleted files will be renamed to 
include a hash of the file contents and moved to this directory, instead
of being outright deleted, so you can keep backup copies of all files.
This should be a full path to the directory.


