Application Role

The application role deploys the website.

The website is:

index.html

The application package is:

my-website.tar.gz

------------------------------------------------

What Is a Tarball?

A tarball is an archive containing one or more files.

Example:

index.html
style.css
images/

can be packaged into:

my-website.tar.gz

.tar.gz means:

tar = archive files together
gzip = compress the archive

------------------------------------------------

Create the Tarball

From the project root:

mkdir -p /tmp/my-website

Copy the website:

cp roles/app/files/index.html /tmp/my-website/

Create the archive:

tar -czf roles/app/files/my-website.tar.gz -C /tmp/my-website .

Check:

ls -lh roles/app/files/

Expected output:

index.html
my-website.tar.gz

----------------------------------------------------

App Deployment Flow

my-website.tar.gz
       │
       │ copy
       ↓
/tmp/my-website.tar.gz
       │
       │ unarchive
       ↓
/var/www/html/
       │
       ↓
index.html
       │
       ↓
     Nginx
       │
       ↓
    Browser
