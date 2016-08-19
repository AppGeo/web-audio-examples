## Web Audio Examples

### additive.html
* Additive Synthesis, in which complex tones can be created by a
  stack of sine oscillators running at whole number multiples
  (harmonics) of a fundamental frequency.
* Only useful for explaining theory.  Running a sufficient number
  of oscillators for most audio applications would be too
  computationally expense.  Approaches such as subtractive and FM
  synthesis are much more efficient.

### button.html
* Demonstrates how to load small audio samples and associate them
  with user interface events.
* Adds a popping aluminum can sound to a button's _mousedown_ and
  _mouseup_ events.
* Also provides alternative code (commented out) that demonstrates the
  use of an audio sprite.

### envelope.html
* Demonstrates how to modulate the initial volume and harmonics of a
  note to simulate the attack and decay dynamics of a real musical
  instrument.
* Shows how to schedule events on the _AudioContext_ timeline.

### fm.html
* FM Synthesis, which generates complex tones via frequency
  modulation, quickly varying the frequency of one oscillator with
  another.
* Also Vibrato, a slow oscillation in frequency that adds richness to
  a tone.
* Shows how the output from one _AudioNode_ can be fed into an
  _AudioParam_ of another _AudioNode_, causing its value to vary over
  time.

### formant.html
* Emulates a male singing a set of vowel sounds.
* Demonstrates how a set of bandpass filters can model the human vocal
  tract.
* Vowel formants are defined as parallel arrays of frequencies, Q-values
  (which define the width of bandpass) and amplitudes.
* A slider smoothly transitions from one vowel to the next.

### hearing.html
* A simple hearing test. Generates a sine wave with a frequency
  that can be set between 20 Hz and 20,000 Hz, the range of human
  hearing.
* Demonstrates that humans perceive frequency logarithmically.

### keyboard.html
* The same audio processing chain as _envelope.html_ except with
  a musical keyboard rendered in HTML instead of a frequency slider.
* A note can be sustained by dragging off the key before the _mouseup_
  event.  Click on that key to cancel the note.
* Shows how to convert a MIDI note number to an oscillator frequency.

### loop.html
* Loads various audio loops and demonstrates the effect of high pass
  and low pass filters.
* Can switch the visualization between frequency bars and a
  spectrogram.

### microphone.html
* Visualizes the input from the microphone as frequency bars or a
  spectrogram.

### noise.html
* Generates various types of noise:
  * White - Equal power across all frequencies.
  * Pink - Power decreases as frequency increases, favoring lower
    frequencies.  This noise sounds more balanced and natural to
    human hearing.
  * Brown - Favors lower frequencies even more strongly than pink
    noise.
* Demonstrates the use of _ScriptProcessorNode_.

### subtractive.html
* Subtractive Synthesis, in which the output from an oscillator with
  high frequency harmonic content (square, triangle and sawtooth
  waves) is modified using filters to create complex tones.
