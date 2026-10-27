# Fingerlight Bench

A two-phone finger transillumination experiment that runs in a single web page.

Two phones sandwich a fingertip. They take turns lighting the finger with their flashlights while both cameras record. Each phone keeps time by watching the other phone's light, so no network connection is needed between them. Each phone measures two light paths:

- **Through the finger**: the other phone's light, transmitted through the finger to this camera.
- **Bounced back**: this phone's own light, reflected from the tissue on its side.

For each path the page shows the pulse waveform, pulse rate, red and green AC/DC (the pulsing share of the signal) and a raw red-to-green ratio. Every frame can be saved as CSV.

> **Research prototype.** This is not a medical device and gives no medical readings. The red-to-green ratio is not blood oxygen.

## Try it

Open the GitHub Pages link for this repository in Chrome on Android. Camera access needs HTTPS (or `localhost`), so opening the file directly from storage will not work.

The page starts with a simulation, so you can see how it behaves before using real phones.

## Setting up two phones

1. Open the page on both phones. Choose **Leader** on one and **Follower** on the other, with the same slot length.
2. Leader: press **Start camera**, accept the camera prompt, then lay it screen down so the camera bar faces up.
3. Place the fingertip pad over the leader's main camera, with the rest of the finger over its flashlight.
4. Follower: press **Start camera**, then lower it onto the finger with its main camera over the middle of the nail. Support it at the ends so its weight does not press on the finger.
5. Dim the room, rest the forearm at heart height, keep still, and ignore the first 20–30 seconds.

Start with **Solo** mode on one phone to find a finger position that gives a steady pulse.

## Known limits

- Flashlight control from the browser works in Chrome on Android. iPhones can record but not light.
- Phone cameras filter out most near-infrared light, so the page works with visible red and green.
- Manual exposure is used where the camera allows it; otherwise brightness levels drift.

## Licence

MIT. See [LICENSE](LICENSE).
