# Conference Central
An App Engine application developed for users to create and register for conferences.

## Table of contents
- [Design Choices](#Design Choices)
- [Software Requirements](#Software Requirements)
- [Creators](#creators)
- [Copyright and license](#copyright-and-license)

## Design Choices

The Session class is modelled similarly to the existing Conference class for consistency, with the required properties from specification and the session name being a requirement. It is designed to be simple and more lenient to match the abstract nature of Conference Central. The SessionForm class includes all properties of the Session class to prevent data loss, when creating a session the form is passed alongside with a websafeConferenceKey in the request container to define the new session and associate it with a conference ancestor.

Speakers of sessions are set as string properties. This was chosen over using profiles as the speakers themselves may not have registered on the app. The speaker field is also intended to be versatile, as there could be multiple speakers or corner cases that may lead to unusual input values (unidentifiable speaker or multiple aliases)

## Additional Queries

### getProfileByEmail
This query checks whether a profile associated with the email address provided. It would be useful for users who are searching for other members they may know using email or an API service that automatically scans through an authed user's friendlist and retrieving emails to search.

### getNextConference
This query uses the current time to establish the next conference to be held and returns that conference to the user. A user may be interested in the next conference to be held, and the query synergises well with the announcement feature where both indicate shortly upcoming events.

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
