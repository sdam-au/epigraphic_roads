# Script accessing workflow in Python (internal SDAM project):

## Online scenario

The workflow is designed so we can access the dataset via API, tranform it into JSON and then save it in the SDAM project repository in Sciencedata.dk. If we are unable to access the Sciencedata.dk, please contact us at sdam.cas@list.au.dk. A separate Python package ```sddk``` was created specifically for this purpose, see https://github.com/sdam-au/sddk. If you want to save the dataset in your preferred location, scripts need to be modified.

1. Go to Google Colab & sign in with your Google email account. 
2. Create a new notebook, select Github tab.
3. Paste in the URL of the notebook on Github (choose from dropdown menu, if you are using the same email account for Github and for Google).
4. Ingest and save to your own Goodle drive into Google Colab folder (it may be done automatically).
5. Google Colab includes all basic libraries but requires an install of unusual libraries once per session.
6. Committing any changes back to Github has to be further tested.

## Offline scenario

1. Download scripts from Github and run locally in Jupyter Notebook, but check the dependencies and libraries. 
2. The documentation needs further tests and elaboration.