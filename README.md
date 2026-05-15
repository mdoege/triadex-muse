## Triadex Muse

Python implementation of the 1971 [Triadex Muse](https://en.wikipedia.org/wiki/Triadex_Muse) by Ed Fredkin and Marvin Minsky

This fork uses the [SoX](https://sox.sourceforge.net/) play command (instead of pyo) for sound output by piping raw 8-bit unsigned samples into it:

```python3 Muse2.py | play -t raw -b 8 -e unsigned -c 1 -v 1 -r 44100 -q -```

The sec_max variable defines maximum duration of the sound, or 0 for infinite playback.
