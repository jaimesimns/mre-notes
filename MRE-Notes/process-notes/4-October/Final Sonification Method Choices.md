# Sonification Method
### Final Choices
[[process-notes]]

==DECISION==
I am going to use MIDItime, as I don't intend to rely on synthetic instruments. Instead, I want to create my own 'instruments' through the use of samplers to express the noise icons that I desire. This way, I can turn bird noises into an instrument by mapping them by pitch, or saw noises, or remix the Ottawa Valley Reel to better express the meaning behind my data.

==OPTIONS==
1. Sonic pi - works best with percentage or short data sets; also more of a synth feel - the Dig example
2. MIDItime - best for time series data; very complicated - the programming historian
3. Daniel Ruten

"In [the lesson](https://programminghistorian.org/lessons/sonification), Graham provides an introduction to the theory of data sonification, before detailing some of the sonification methods and resources that are available to historians. In particular, he discusses some methods to convert historical data into MIDI notation that can then be mapped to instrumentation. Some of these tools, such as [Musicalgorithms](http://www.musicalgorithms.org/3.2/) and the [MIDITime package for Python](https://pypi.python.org/pypi/miditime), were particularly designed with time-series/quantitative data in mind. But Graham also provides an example of the potential of MIDITime to analyze historical texts, as he uses it to sonify topic modelling data from John Adams’ diaries. By [mapping the resultant MIDI data to different instruments in Garageband](https://www.youtube.com/watch?v=ikqRXtI3JeA&feature=youtu.be), he offers us a means to hear the relative occurrence of different topics in the diaries over a 50-year period. Being able to listen to the relations between these different concepts over time this way provided a very unique and intriguing representation of a textual narrative. As Graham emphasizes, the choices one makes regarding how to represent data sonically in this fashion reveal the ways in which we privilege, condense and transform information as historians." (Daniel Ruten)

"The key difference is that instead of using conventional instruments, I planned to assign the MIDI data to samplers. (A [sampler](https://goo.gl/1nfuuo) is a kind of digital instrument that plays back any audio file that is loaded into it.) From there, each sampler would be loaded with a Text-to-Speech audio file of its corresponding word. The MIDI notation would then tell each sampler when to trigger its spoken word, corresponding to the occurrences of the word in the text. When all of this is combined, then, we would be able to hear the linear frequency of multiple spoken words over time in a text in a sort of sonic word cloud, thus quickly getting a sense of both shifting patterns of common word usage as well as the relations between the usage of different words over time." (Daniel Ruten, https://programminghistorian.org/posts/sonic-word-clouds)
- he used Ableton Live and its built in samplers
- more detailed version https://danielruten.wordpress.com/2017/04/15/sonic-word-clouds-an-experiment-with-data-sonification-part-i-introduction/
"As an example, he shows how he converted topic modeling data from the entries of John Adam’s diaries into MIDI notation, which he then mapped to different instruments in Garageband. As Graham emphasizes, the choices of how to represent data through sound in this fashion are revealing of how we organize, privilege, reduce and transform information as historians. [3] However, the end result of this representation is not immediately intelligible to the listener; one may decide to, say, represent a topic concerning war in a text with the sound of piercing trumpets, but a listener has no means to truly understand the representation on its own without a separate guide. Therefore, this particular kind of sonification seems more useful as a kind of reflective process than as a practical method of textual representation or analysis."

Part 2: https://danielruten.wordpress.com/2017/04/15/sonic-word-cloud-project-part-2-the-python-script/

MIDItime
- every note need time, pitch, velocity (volume), and duration
- time is most important bc it is when notes are played in relation to one another
- pitch can be 60 (Middle C)
- velocity 127 (the max)
- duration (200 beats? depends on how long you want it to go)
- need to turn the data into lists of MIDI notes that the MIDITime module could process.
- - need to produce audio to later load into a sampler and map the MIDI data to these samplers

Part 3: https://danielruten.wordpress.com/2017/04/15/sonic-word-cloud-project-part-3-bringing-it-all-together-in-ableton/
- used Ableton but could also use LMMS
- requires samplers
- first: load all sampler tracks needed
- second: load the mp3s into the samplers, and rename as appropriate
- next: bring in corresponding midi track(s)


Part 4: https://danielruten.wordpress.com/2017/04/15/sonic-word-cloud-project-part-4-conclusions/

install MIDItime
https://pypi.org/project/miditime/