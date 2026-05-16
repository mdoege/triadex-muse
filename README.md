## Triadex Muse

Python implementation of the 1971 [Triadex Muse](https://en.wikipedia.org/wiki/Triadex_Muse) by Ed Fredkin and Marvin Minsky

Be careful, this fork of the script sends raw unsigned 8-bit audio samples to standard output, so you need to redirect output to an audio player (or a file)! You can e.g. use the ```play``` command from [SoX](https://sox.sourceforge.net/) to listen to it:

```python3 Muse2.py | play -t raw -b 8 -e unsigned -c 1 -v 1 -r 44100 -q -```

The sec_max variable in the script defines maximum duration of the sound, or use 0 for infinite playback. Limiting duration is especially useful when redirecting audio to a file.

