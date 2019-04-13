scales4orac
===========

The objective of this project is to create a Pure Data "note effect" for *[Orac](https://github.com/TheTechnobear/Orac)*. The effect transforms an input "white key" note into the corresponding note of a specified scale. The note is then handed over to the next module in the *Orac* chain, e.g. a synthesizer, that will play the new note.

For example, by chaining in this order *U-scales* (the obvious name displayed in *Orac* for *scales4orac*) and the [*S-rhodey* synthesizer in Orac 1.x](https://github.com/TheTechnobear/Orac/tree/master/Organelle/orac/modules/S-rhodey) running on an Organelle, after specifying C3 as the root note of a minor scale in *scales4orac* , pressing the 3rd white key on an Organelle would play an Eb3 instead (the 3rd note in the C3 major scale). In the same way most Pure Data modules do, the settings would enable to further transpose the output, e.g. +12 semitones for 1 octave higher.

Note that I am not a trained musician, so a lot of what I write could be incorrect. **Learning the actual music theory and practicing on a conventional keyboard is actually more important than using anything like this hack!!!** But I came to music late in my life and this is a nice shortcut. Moreover, it gives me a great excuse to learn Pure Data.

## Specifications

The following is the target behaviour I would like to achieve from the effect running on an Organelle.

To set the desired scale, the user must press Aux + the required root note, then release Aux. The Aux button's led starts blinking, and the user has 3 seconds to press any of the black keys. Doing so will "store" the scale in the black key. If any scale was already stored in the key, it will be overwritten. After storing a new scale, the scale is also selected for performing. By default, all black keys are set to a C3 major scale... that is like saying that each white key plays itself.

Then, to perform, the user presses the black keys to switch scale as necessary, and plays using the white keys only.

## Project status

At the moment, the code is far from being suitable to be used in Orac, and it is not much more than a few tests going in the general direction described above. However, it doesn't feel like I am that distant from the final objective, I'm learning fast!

The code was written using [Purr Data](https://github.com/agraef/purr-data) 2.8.1 on macOS - that is a Pure Data 0.48 interpreter (0.49 is the latest version of the language at the moment of writing). However, I'm learning Pure Data from [Dr Rafael Hernandez' YouTube video tutorials](https://www.youtube.com/playlist?list=PL12DC9A161D8DC5DC) that must be a few years old, so it is unlikely I am using any cutting edge feature of the language.

## Credits
Of course, I must thank [Critter & Guitari](https://www.critterandguitari.com/) for risking their a**es making a business out of building Organelles (I hope it's working out for you guys :-) ), and the amazing community writing software for the device, with [TheTechnobear](https://github.com/TheTechnobear) at the top of the list, for writing *Orac*. A great thanks also goes to Dr Rafael Hernandez for his training videos, that are freely available [on his YouTube page](https://www.youtube.com/user/cheetomoskeeto/featured).
