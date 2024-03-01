# Transkribus API Test
```Testing the Transkribus API```

The aim of this repo is to keep track of my attempts to learn how to interface with the API for Transkribus using primarily Python.

This attempt is first to learn how to interact with API, then to interact with Transkribus


## What is Transkribus

[Transkribus](https://readcoop.eu/transkribus/) is an AI platform which has a focus on [OCR](https://en.wikipedia.org/wiki/Optical_character_recognition) tasks.

It describes itself in the followig manner:
> Transkribus is an **AI-powered** platform for **text recognition**, **transcription** and **searching of historical documents** – from any place, any time, and in any language.

<p><a href="https://readcoop.eu/transkribus/?wvideo=l3bbnzyqnk"><img src="https://embed-ssl.wistia.com/deliveries/b09c4ff5451185d3d651b8e723b5463412d8fca5.jpg?image_play_button_size=2x&amp;image_crop_resized=960x540&amp;image_play_button=1&amp;image_play_button_color=193060e0" style="width: 400px; height: 225px;" width="400" height="225"></a></p><p><a href="https://readcoop.eu/transkribus/?wvideo=l3bbnzyqnk">Transkribus | AI powered Handwritten Text Recognition</a></p>


## What is their API

Their [API documentation](https://readcoop.eu/transkribus/docu/rest-api/) is a set of Restful methods to facilitate communication between the Transkribus application and the server. It can be summarised in the following manner:

- **Login and Authentication**:
  The user has to POST their credentials to the login method and include the Session-ID in subsequent requests.

- **Collections and Documents**:
  The user can access, list, and retrieve the collections and documents they have rights to via GET requests.

- **Jobs and Processing Tasks**:
  The user can start, monitor, cancel, and query the details and errors of various processing tasks, such as document creation, layout analysis, HTR, OCR, etc., via POST and GET requests.

- **Search and Recognition**:
  The user can perform full-text search and OCR recognition on documents and pages via GET and POST requests.


## Goal

Our intitial goal will be to do the following:
- Authenticate
- Upload an image
- Kick off a transcription job (you can do that through the web interface)
- Download the completed text transcription of the image


