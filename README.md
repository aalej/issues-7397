# Repro for issue 7397

## Versions

firebase-tools: v.13.12.0<br>
node: v20.12.2<br>
python: 3.12.4<br>
platform: macOS Sonoma 14.5

## Setup

1. Run `cd functions`
1. Run `python3.12 -m venv venv`
1. Run `. "/Users/<path>functions/venv/bin/activate" && python3.12 -m pip install -r requirements.txt`

## Steps to reproduce

1. Run `firebase emulators:start --project demo-project`
1. On a separate terminal, run `curl http://127.0.0.1:5001/demo-project/us-central1/addmessage?text=Hello%20World`

```
$ curl http://127.0.0.1:5001/demo-project/us-central1/addmessage?text=Hello%20World
curl http://127.0.0.1:5001/demo-project/us-central1/addmessage?text=Hello%20World
Message with ID v2J4bALHd0VyD2RLctWM added.
```
