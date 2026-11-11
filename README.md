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

## Sources and thanks

Most of the hymns come from the **[Open Hymnal Project](https://openhymnal.org)**,
maintained by Brian J. Dumont with many contributors, who has spent years
carefully typesetting public-domain hymns from historic hymnals so that anyone
can use them. Each hymn here names the hymnal it was taken from and links back
to the project.

They were converted with `cecilia library import openhymnal`, which:

- takes only hymns the Open Hymnal marks as public domain;
- also checks that the tune and the harmony are free **worldwide**: their
  composers died more than 70 years ago (the Open Hymnal checks US law only,
  so a few settings, such as Vaughan Williams's, are left out for now and
  become free in later years);
- leaves out tunes already in this library, and hymns whose shape a Cecilia
  score can't show faithfully;
- was checked note for note against the Open Hymnal's own MIDI recordings.

Only the music is used; the words are not included.
