# Sharing with the Cecilia Library

Thank you! Everything here is checked automatically, then reviewed by a person
before it's added.

## Music

**What may be shared**

- ✅ Tunes and harmonisations in the **public domain**: in most countries,
  anything whose composer and arranger died more than 70 years ago, e.g.
  Monk's EVENTIDE, Dykes' NICAEA.
- ✅ **Your own** arrangements, compositions or recordings, under `CC0-1.0`,
  `CC-BY-4.0` or `CC-BY-SA-4.0`.
- ✅ Your recording of a public-domain piece, if the person playing agrees.
- ❌ Modern hymns, worship songs and arrangements still under copyright (most
  CCLI-licensed music), even if your church is licensed to play them.
  A church licence doesn't allow publishing.
- ❌ Arrangements copied from a recent hymn book, even of an old tune: the
  arrangement may be copyrighted. Write your own, or use one known to be
  public domain.

**How**

- From Cecilia: **Library → ⋮ → Share** saves a file with personal details
  removed and asks for the licence.
- Scores (`*.score.json`, the format of Cecilia's built-in hymns) are best
  for hymns: they're exact, show as clean notation and are easy to correct.
  Put them in `music/hymns/` or `music/voluntaries/`.
- Fill in `licence`, `source` (the book or edition you worked from) and a few
  `tags` (`hymn`, `evening`, `funeral`, `advent`…).
- Name the file after its `id`, e.g. `eventide.score.json` with
  `"id": "eventide"`.

## Organ setups

- From Cecilia: **Organs → your organ → Share** saves `<id>.organ.json` and
  `<id>.meta.json`. Put both in `organs/<maker>/`.
- In the `.meta.json`, describe the organ so others can tell whether it's
  theirs: `maker`, `model`, `years` and any `notes`, e.g. "set MIDI to mode
  B first".
- Be honest about `confidence`:
  - `template`: worked out from a manual; not tried on an organ.
  - `learned`: every stop captured with *Learn every stop* on a real organ.
  - `verified`: learned, and a recording played back correctly on it.
- Leave out the church's name unless you'd like it known.

## Checks

Every pull request runs `cecilia library check`, which makes sure that:

- every file loads, and each piece plays on Cecilia's built-in organs with
  every note on a keyboard;
- every piece has an allowed licence;
- no two items share an id;
- organ setups have a description, and organs whose stops only toggle have
  a general cancel message.

To run the same check locally, with the Cecilia source checked out beside this
repo:

```sh
cargo run --manifest-path ../cecilia/server/Cargo.toml -p organ-server -- library check .
```
