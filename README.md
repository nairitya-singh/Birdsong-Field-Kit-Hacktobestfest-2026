# Birdsong — Field Kit

A phone-friendly birding companion built around Google's open YAMNet audio event classifier. Record a short sound, run inference in the browser, and get a broad bird-call suggestion. Audio stays on-device; observation notes use localStorage.

## Run it

Serve this folder from localhost or HTTPS (microphone access requires a secure context), for example `node server.mjs`. Open the app online once so TensorFlow.js and the model assets can be cached. Tap **Start listening** for a six-second recording or choose an audio file. Verify offline operation on the target browser before heading out.

## Model and limits

YAMNet is a general AudioSet sound-event model, not a species classifier. Results are broad labels such as bird vocalization or chirping and can be wrong in wind or overlapping sound. First setup needs internet; cached assets enable repeat offline use.

## Stack

Vanilla JS/CSS/HTML, TensorFlow.js, open YAMNet, service-worker app shell, local observation history. The existing arcade game remains in `game.js`; the field kit is now the main experience.
