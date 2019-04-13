scales4orac
===========

The objective of this project is to create a Pure Data "note effect" for *[orac](https://github.com/TheTechnobear/Orac)*. The effect transforms an input "white key" note into the corresponding note of a specified scale. The note is then handed over to the next module in the orac chain, e.g. a synthesizer, that will play the new note.

For example, by chaining in this order *U-scales* (the obvious name displayed in *orac* for *scales4orac*) and the [*S-rhodey* synthesizer in orac 1.x](https://github.com/TheTechnobear/Orac/tree/master/Organelle/orac/modules/S-rhodey) running on an Organelle, after specifying C3 as the root note of a minor scale in *scales4orac* , pressing the 3rd white key on an Organelle would play an Eb3 instead (the 3rd note in the C3 major scale). In the same way most Pure Data modules do, the settings would enable to further transpose the output, e.g. +12 semitones for 1 octave higher.

Note that I am not a trained musician, so a lot of what I write could be incorrect. **Learning the actual music theory and practicing on a conventional keyboard is actually more important than using anything like this hack!!!** But I came to music late in my life and this is a nice shortcut. Moreover, it gives me a great excuse to learn Pure Data.

The code was written using Purr Data 2.8.1 - that is a Pure Data 0.48 interpreter (0.49 is the latest at the moment of writing). However, I'm learning Pure Data from [Dr Rafael Hernandez' YouTube video tutorials](https://www.youtube.com/playlist?list=PL4B9054632F465780) that must be a few years old, so it is unlikely I am using any cutting edge feature of the language.

##Specifications

The following is the target behaviour I would like to achieve from the effect running on an Organelle.

To set the desired scale, the user must press Aux + the required root note, then release Aux. The Aux button's led starts blinking, and the user has 3 seconds to press any of the black keys. Doing so will "store" the scale in the black key. If any scale was already stored in the key, it will be overwritten. After storing a new scale, the scale is also selected for performing. By default, all black keys are set to a C3 major scale... that is like saying that each white key plays itself.

Then, to perform, the user presses the black keys to switch scale as necessary, and plays using the white keys only.
