# Boolean-Melody-Machine
A generative melody and harmony maker using Boolean logic gates and Euclidean clocks

## Voice envelopes

Each voice has an **ENV** button. Off, the voice plays the original short pluck. On, it opens an envelope row for that voice:

- **Attack**, **Decay**, **Sustain** and **Release** shape the volume of each note.
- **Gate** is how long each note is held before the release starts, so it sets the note length.
- The small graph shows the shape, with a dashed line where the gate ends.

The envelope is saved with patterns, Jam scenes and Discobot projects, and is used in the selection preview, the WAV export, and (as note length) the MIDI export. Patterns saved before this change load with the envelope off.

## Form

The **Form** panel replaces chaining patterns with a chart, the way a modal jazz tune is a lead sheet of sections rather than a list of parts. Press **Follow the chart** and the voices take their key and scale from the chart instead of the ROOT and SCALE selects. The clocks, gates and patterns keep running underneath.

- **Sections A–D.** Each has a root, a scale, a length and a feel. Put them in any order with the + buttons (tap a card to remove it). The form loops. Three charts to start from: *Half-step bridge* (AABA, D Dorian up to E♭ Dorian), *Three colors* (C Lydian, A minor, E Phrygian) and *Open vamp*.
- **Length.** A set number of bars, or a **vamp**: it plays at least and at most so many bars, and in between it moves on when two bar-count clocks meet through AND, OR or XOR (bar clock 3 AND bar clock 5 leaves after bar 15), or by chance each bar. **Cue next section** ends the current section after the next bar.
- **Enter by.** *Hard*: the new key lands on the downbeat. *Pivot*: for the first bar the voices use only the notes the two scales share. *Anticipate*: on the last beat before the section, the voices already quantize to its scale.
- **Key changes and patterns.** Notes a voice is holding in its pattern are moved to the nearest note of each new scale, so a locked phrase keeps its shape through a key change.
- **Feel** works on top of each voice's settings. *Density* moves a voice's logic one step narrower (toward AND) or wider (toward OR) on some bars. *Register* moves every voice down or up an octave. *Color* leans newly drawn notes toward the scale's color tone (the raised 6th in Dorian, the ♯4 in Lydian) or toward the root and fifth.
- **With other apps.** At each new section the key goes out as a Jam Link key change, so a linked Choir follows it. Every bar is also announced on a separate channel for apps that want the whole form; the format is in [FORM-LINK.md](FORM-LINK.md).

The chart is remembered in the browser and saved with patterns, Jam scenes, and Discobot and Mixing Desk projects.

## Jam Link

Press **Link** in this app and in Logic Rhythm, Boolean Melody Machine and Choir (open each in its own tab or window of the same browser) and they share tempo, start/stop, key and mode, and saved scenes, all locked to one beat grid. **Create room** or **Join** with a short code to do the same with people in other places, and hear each other's apps. See [JAM-LINK.md](JAM-LINK.md) for how it works.

Notes for this app: clocks now count in beats, so a tempo change moves every clock together instead of shifting their phase.

## Discobot guest

This app can be a unit in the rack of [Discobot](https://iw978599.github.io/discobot/), a browser sequencer and drum machine. In Discobot choose **Project → Add Guest Instrument** and paste `https://aaronvandorn.github.io/Boolean-Melody-Machine/`. Discobot then starts and stops the app on its beat, sets the tempo, takes its sound into its mixer, and saves its settings with the project. Opened on its own, the app is unchanged. See [JAM-LINK.md](JAM-LINK.md#discobot-guest) for details.
