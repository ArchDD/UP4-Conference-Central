# Conference Central
An App Engine application developed for users to create and register for conferences.

## Table of contents

- [Software Requirements](#Software Requirements)
- [Creators](#creators)
- [Copyright and license](#copyright-and-license)

## Software Requirements & API information

- Python 2.7.10

- Google App Engine

- Google Cloud Endpoints API

## Setup Instructions

### App Engine Deployment

1. Update the value of `application` in `app.yaml` to the app ID you
   have registered in the App Engine admin console and would like to use to host
   your instance of this sample.
1. Update the values at the top of `settings.py` to
   reflect the respective client IDs you have registered in the
   [Developer Console][4].
1. Update the value of CLIENT_ID in `static/js/app.js` to the Web client ID
1. (Optional) Mark the configuration files as unchanged as follows:
   `$ git update-index --assume-unchanged app.yaml settings.py static/js/app.js`
1. Run the app with the devserver using `dev_appserver.py DIR`, and ensure it's running by visiting your local server's address (by default [localhost:8080][5].)
1. (Optional) Generate your client library(ies) with [the endpoints tool][6].
1. Deploy your application.

### API Explorer Testing
1. Access API explorer via '/apis-explorer' at end of URL
2. Select conference API service
3. Execute the endpoint methods with relevant fields

## Creators

**Dillon Keith Diep**


## Copyright and license

The code released was created for educational purposes, copyright and license subject to Udacity's provided source code - no other enforcements otherwise.
