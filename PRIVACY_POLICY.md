# Privacy Policy — Humm

_Last updated: 2026-05-12_

Humm is an Android app that turns a short ambient-audio sample into a 0–100 "vibe" score and a generative visual. This policy explains what the app does — and, more importantly, what it does **not** do — with your data.

## What we collect

**Nothing.** Humm does not collect, store, or transmit any personal data.

Specifically:

- We do not ask for an account, email, phone number, or any other identifier.
- We do not use analytics, crash reporting, advertising SDKs, or any other third-party telemetry.
- We do not collect device identifiers, advertising IDs, IP addresses, or location.

## What the microphone is used for

Humm requests the `RECORD_AUDIO` permission so that, when you tap **Listen**, it can capture roughly four seconds of audio from the device microphone.

That recording:

1. Lives only in the device's volatile RAM (the running process memory) for the duration of the analysis.
2. Is fed to the on-device Rust audio engine, which extracts four anonymous acoustic statistics: average loudness, transient density, spectral centroid (brightness), and spectral entropy (chaos).
3. Is discarded immediately after analysis. The raw audio is never written to internal or external storage, never copied to a clipboard, and never transmitted anywhere.

The microphone is only active while the foreground Listen action is running. Humm has no background service.

## What leaves your device

Nothing leaves your device automatically. The app does not have the Android `INTERNET` permission — the permission is explicitly removed from the app manifest, so the operating system blocks any attempt by the app or its dependencies to open a network socket.

If you tap the **Share** or **Add to Insta Story** button, Android's standard share sheet is invoked with an image of your aura and score that the app renders locally. At that point, what you do with the image (post it, send it to a friend, save it) is between you and the destination app — Humm itself never sees that content again.

## Children's privacy

Humm is rated for ages 13+. We do not knowingly collect any information from anyone, so we do not knowingly collect information from children either.

## Permissions used

| Permission        | Why                                                                                       |
| ----------------- | ----------------------------------------------------------------------------------------- |
| `RECORD_AUDIO`    | Capture the 4-second analysis buffer (foreground only, RAM only, discarded immediately).  |


## Changes to this policy

If the data practices ever change (they won't unless we add explicit features that require it), this document and the in-app description will be updated and the version number bumped.

## Contact

For any privacy questions, file an issue on the Humm GitHub repository.
