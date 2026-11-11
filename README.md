# Cecilia Library

Shared music and organ setups for [Cecilia](https://github.com/garethcheyne/cecilia),
the free organ recorder and player.

- **`music/`**: hymns and voluntaries any Cecilia can play, on any organ.
  Cecilia stores pieces by *what* the organist did ("Great Principal 8′ on"),
  not raw MIDI, so music shared from one church plays on another's organ.
- **`organs/`**: organ setups (which MIDI message each stop, keyboard and pedal
  uses), so the next church with the same model doesn't have to teach Cecilia
  every stop again.

Cecilia reads the catalogue at
`https://garethcheyne.github.io/cecilia-library/index.json`, which is rebuilt
whenever something is added here.

## Using it

In Cecilia, open **Library → Community** to add music, or **Organs → Find your
organ** to use a shared setup. Nothing in this repo needs to be downloaded by
hand.

## Sharing

See [CONTRIBUTING.md](CONTRIBUTING.md). In short: only share music you're
allowed to (public domain, or your own work under an open licence), and say
how far an organ setup has been tested.

## Licences

Every file states its own licence:

- **Music** carries a `licence`: `public-domain`, `CC0-1.0`, `CC-BY-4.0` or
  `CC-BY-SA-4.0`.
- **Organ setups** are factual MIDI mappings shared as
  [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/): anyone may
  use them for anything.
