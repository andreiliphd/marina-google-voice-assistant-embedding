# Marina
============

Simple to use embedding of Google Voice Assistant.

---

## Features
- Test Google Voice Assistant
- Good manual

---

## Setup
Clone this repo:

```
https://github.com/andreiliphd/marina-google-voice-assistant-embedding.git
```
I had problems with official Google documentation. That's why I decided to provide additional screenshots to make life easier.

Official Google documentation can be found at [Google Assistant SDK](https://developers.google.com/assistant/sdk/guides/service/python/embed/config-dev-project-and-account?hardware=other) page.

You can start with official Google documentation and if something need clarification look at this page for more details.

1. Go to [Actions on Google](https://console.actions.google.com/). Add a new project. Provide a name of project and tune language and country settings.
![Add new project](https://github.com/andreiliphd/marina-google-voice-assistant-embedding/raw/master/screenshots/new_project.png)
2. Enable [Google Voice Assistant API](https://console.developers.google.com/apis/api/embeddedassistant.googleapis.com/overview).
![Enable API](https://github.com/andreiliphd/marina-google-voice-assistant-embedding/raw/master/screenshots/enable_api.png)
3. Fill in form in [OAth consent screen](https://console.developers.google.com/apis/credentials/consent).
![OAth consent screen](https://github.com/andreiliphd/marina-google-voice-assistant-embedding/raw/master/screenshots/oauth_creation.png)
4. Register your model(device).
![Device registration](https://github.com/andreiliphd/marina-google-voice-assistant-embedding/raw/master/screenshots/device_registration.png). Don't forget to download key file.
5. Install libraries. Google Voice Assistant works perfectly inside Anaconda environment.
```
sudo apt-get update
sudo apt-get install python3-dev
sudo apt-get install portaudio19-dev libffi-dev libssl-dev
pip install --upgrade google-assistant-sdk[samples]
pip install --upgrade google-auth-oauthlib[tool]
```
6. Install OAth key that you generated in step 4.
```
google-oauthlib-tool --scope https://www.googleapis.com/auth/assistant-sdk-prototype \
      --save --headless --client-secrets /path/to/client_secret_client-id.json
```
7. Install packages that this repositary depends on.
```
conda install -c conda-forge python-sounddevice
pip install SoundFile
```
The rest of the packages usually installed inside Anaconda environment.

---


## Usage

Just run cells.


---

## License
Free
