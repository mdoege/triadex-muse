## Triadex Muse

Python implementation of the 1971 [Triadex Muse](https://en.wikipedia.org/wiki/Triadex_Muse) by Ed Fredkin and Marvin Minsky

Be careful, this fork of the script sends raw unsigned 8-bit audio samples to standard output, so you need to redirect output to an audio player (or a file)! You can e.g. use the ```play``` command from [SoX](https://sox.sourceforge.net/) to listen to it:

```python3 Muse2.py | play -t raw -b 8 -e unsigned -c 1 -v 1 -r 44100 -q -```

The ```evolve``` parameter (line 257) controls how frequently the Muse slider settings are changed (by randomly picking a slider and setting it to a new value). E.g. if it is set to 10 (default), the settings will change every ten beats. The new settings are also printed to standard error output.

By default, there is a 10% probability that a switch will be moved to the counter section (OFF/ON/Cx), otherwise it will be set to one of the shift register bits (B1–B31). A switch in the counter section will produce a more repetitive sound, while a switch in shift register will cause more random and non-repeating melodies.

The ```sec_max``` parameter (line 263) defines maximum duration of the sound, or use 0 for infinite playback. Limiting duration is especially useful when redirecting audio to a file.

