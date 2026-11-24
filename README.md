# Castwright: Dramatis Personae

Give every character in a story their own voice. Load a Markdown story, Castwright finds the
characters, assigns each a browser voice (with pitch, rate and volume adjustments), and reads the
story aloud.

## Use it

Live page: https://emptyfishtank-jb.github.io/Castwright/

Open the live page (see below) or `index.html` in Chrome or Edge, then drop in a `.md` file (or click **Load sample story**).
No install, no build, no accounts. Everything runs in the browser with its built-in speech voices.

## Story format

```md
# Chapter 1: The Docking Permit

The airlock hissed open and Captain Vex stepped onto the dock.

**Captain Vex:** You're late.
**Tobb (quietly):** Nobody I'd trust.
```

- `**Name:** line` marks who speaks. Plain `Name: line` also works if the name appears at least twice or is ALL CAPS.
- Lines with no speaker are read by the **Narrator**. `#` headings are read by the Narrator too.
- A bracketed note after the name, like `(quietly)`, is removed from the spoken text.
- Surrounding quote marks are stripped; Markdown formatting is not spoken.

See `samples/sample-story.md`.

## Voices

Each character's voice, pitch, rate and volume are remembered in the browser and can be exported to
a `.json` file and loaded again. Online / "Natural" voices (listed first) usually sound best.

## Versions

Every version is a commit whose message starts with its version number, and each is tagged.
List them with `git tag`, read the history with `git log --oneline`, and pull one up with:

```bash
git checkout v0.1.0      # then open the files; `git checkout main` returns to the latest
```

| Version | What it is |
|---|---|
| v0.1.0 | Audio capture test: can a page hear a browser tab playing Audible? (It could not.) |
| v0.2.0 | Blob pet prototype: a morphing blob with a visualizer mouth, Gemini scene casting, text-to-speech and a per-character voice picker. |
| v1.0.0 | Castwright: load a `.md` story and have each character read in their own adjustable voice. |
| v1.0.1 | The app is now `index.html`, so the GitHub Pages link opens it directly. |

## Layout

- `index.html` is the app.
- `samples/` holds example stories.
- `prototypes/` holds earlier experiments (audio capture test, blob character).

## Ideas for later

- The blob character, morphing to the current speaker.
- Live transcription of audiobook audio, with Gemini casting the scene.
