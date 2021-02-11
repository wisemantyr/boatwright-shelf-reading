# boatwright-shelf-reading
A shelf reading tool adapted from Georgetown University Libraries for the University of Richmond.

Original tool can be found [here](https://github.com/Georgetown-University-Libraries/AlmaInventory). We used the node version and re-purposed the Export to Google Sheets button to download a CSV directly to local storage.

To use:

1. [Install Docker](https://www.docker.com/products/docker-desktop)
2. Clone or download this repository
3. Create a local.prop file with Alma Bib API key in the main repository directory - see docs from original tool above.
4. Create a docker image using the Dockerfile. We called it `edited_alma_inventory`. This can be done from the command line by traversing to the main repository directory and running the command 

    `docker build -t edited_alma_inventory .`

    If you choose to name the image differently, you will need to edit the docker-compose.yml file with the image name. 

5.  Create and run the container with the command `docker-compose -f docker-compose.yml up -d`
6. Use the app at http://localhost/barcodeReport.html
