# Hotel Lobby AI — real input → output demos

Three **unretouched** examples: the exact input image(s) we uploaded, and the exact clip that came back.
No cherry-picking beyond "these three worked on the first try" — these are the samples we show on the site.

> Generated with [Hotel Lobby AI](https://hotellobbyai.top/) — two photos → a cinematic duet clip, in the browser.
> Free tier: <https://hotellobbyai.top/> · Examples page: <https://hotellobbyai.top/hotel-lobby-ai-examples.html>

---

## 1. Two separate photos → one duet clip  (`demos/duo-two-photos/`)

The main use case: two people photographed separately, placed on one stage.

| File | Role |
|---|---|
| [`input-left.png`](demos/duo-two-photos/input-left.png) | first performer (photo 1) |
| [`input-right.png`](demos/duo-two-photos/input-right.png) | second performer (photo 2) |
| [`output.mp4`](demos/duo-two-photos/output.mp4) | the generated clip (10 s) |

**What the output demonstrates**
- both subjects read as standing in the *same* room, with one shared light direction;
- a slow push-in rather than a hard cut;
- warm practicals + slight bloom (the "orange studio stage" look).

**Input requirements that made it work** (the part people underestimate):
- both photos shot from roughly the same camera height;
- same lighting direction (both lit from the front);
- faces clearly visible, no other people in frame;
- similar clothing brightness between the two photos.

**How to reproduce:** upload the two files above at <https://hotellobbyai.top/>, pick the orange studio
stage, keep motion low–medium, render 4–10 s.

---

## 2. Single couple photo → short clip  (`demos/couple/`)

| File | Role |
|---|---|
| [`input.jpg`](demos/couple/input.jpg) | the source photo |
| [`output.mp4`](demos/couple/output.mp4) | generated clip |

Shows the single-photo path: the subject stays recognisable while the frame gets gentle motion and a
cinematic grade. Useful for testing how much motion a single still can take before artefacts appear.

---

## 3. Single pets photo → short clip  (`demos/pets/`)

| File | Role |
|---|---|
| [`input.jpg`](demos/pets/input.jpg) | the source photo |
| [`output.mp4`](demos/pets/output.mp4) | generated clip |

Fur and whiskers are the classic failure case for image-to-video models — this sample is included
because it is a *hard* input, not a flattering one.

---

## Honest notes

- These are **early samples**: the exact seed / prompt strings were not recorded per clip. What you see in
  the output (stage, framing, motion) is the preset that was used.
- No retouching, no frame interpolation, no post-processing: the `.mp4` files are the model output.
- Durations currently available: **4–15 s (H3)** and **4–30 s (Seedance)**.

## Related

- Prompt/parameter cookbook: <https://github.com/mcfly-tt/hotel-lobby-ai-prompts>
- Model-agnostic AI video recipes: <https://github.com/mcfly-tt/awesome-ai-video-prompts>

## License

The demo media in this repository is released under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) —
you may reuse it with attribution to <https://hotellobbyai.top/>.
