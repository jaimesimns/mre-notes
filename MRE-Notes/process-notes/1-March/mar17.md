# March 17

Since yesterday did not pan out for me, I'm going to try a different approach. One of Dr. Graham's [blog posts](https://electricarchaeology.ca/2021/03/01/the-dig-we-know-where-the-bodies-are-buried/) involved the sonification of "The Sutton Hoo ship burial," by R. L. S. Bruce-Mitford. He used [Sonic Pi](https://sonic-pi.net/) to make it, using this code:

```with_fx :reverb do
   in_thread do
    loop do
     notes = (ring 20,50,21,50  etc etc: these are the proportions of the different topics for the first topic)
     notes2 = (ring 6, 14, 59 etc etc)
     notes3 etc 
     notes4 etc
     use_synth :piano
     play notes, release: 0.1, amp: rand, pan: rrand(-1, 1)
     play notes2, release: 0.1, amp: rand,pan: rrand(-1, 1)
     play notes etc
     sleep 0.25
    end
   end
 end

with_fx :wobble, phase: 2 do |w|
  with_fx :echo, mix: 0.6 do
    loop do
      sample :drum_heavy_kick
      sample :bass_hit_c, rate: 0.8, amp: 0.4
      sleep 1
    end
  end
end
```

(Again, that belongs to Dr. Graham). Since yesterday was such a failure, I decided to try to copy his methods and see if I could learn what I need from that. So, I'm going to put this into Sonic Pi, and see how that goes. I'm not sure how to remix the midi file in Sonic Pi, but maybe I'll figure that out later.

Dr. Graham also answered my message re: yesterday's failures, and suggested Audacity, Garageband, and LMMS. LMMS I checked out yesterday but struggled to get SoundFonts recognized, but I'm going to try it again with this recommendation. Unfortunately I think Garageband is only for Macs, which I do not have, so Audacity it'll be! Not sure how to remix MIDI files in Audacity, since I've only ever remixed/merged mp3 files, but we'll see how it goes!

### Sonic Pi
So I just finished messing around with SonicPi, and it's great for numerical data! Lots of fun samples to add - I made a choral piece based on random numbers (because I don't have any handily-accessible data right now) using Dr. Graham's outline, and it was pretty cool. A lot of samples are very electronic though - definitely no fiddle, or any other kind of string. Lots of the sounds would be suitable for making a pseudo-sonar for 'tracking' shipwrecks along the Ottawa River though! 

So not really for remixing, but more for creating tracks based on numbers that you could then remix perhaps? Very cool, not for image sonification unless you turn the image into numbers. Which you could, but which doesn't help me with my MIDI file. Onto Audacity!

### Audacity
I've used [Audacity](https://www.audacityteam.org/) before, for a few drag numbers - performing as Hades and Batman, funnily enough. However, I haven't ever used it with MIDI files, and I'm not sure if it'll do what I want it to do. What I *want* to do is turn my MIDI file (sonification of G. B. Greene image) into an Ottawa Valley-style ballad or fiddle reel, such as [Ottawa Valley Reel - Eddy Arsenault](https://www.youtube.com/watch?v=tLUg8aHmpFk). Synths aren't really my thing, and also, I don't think that 'modern' styles are necessary to make people dance - so why not try to use vaguely period-appropriate musicical styles for the sonification instead?

So the MIDI capabilities in Audacity are not great, and don't allow you to change it to other instruments like I want. 

### Virtual Violin/Guitar/Piano 
In messing around with Audacity and how to change its instruments, I did find a [virtual violin](https://virtualpiano.net/?instr=violin) which is pretty cool! You can type a message using your keyboard keys and then play it. There are options for violin, guitar, etc. but they're all fairly unrealistic unfortunately. Also, no fiddle.

### Back to SynthFonts
I'm hoping that if I can change the instrument to a violin/string instrument and then put it in Audacity or something then I can remix it? We'll see. So far I was (once) able to change the VST instrument, but then my notes all disappeared, so that's fun. I was then able to redo changing the VST with the VST pack I downloaded, but it's really not fiddle-like.

Found an online tutorial for FLStudios, so back to there I go.

### FL Studios
I uploaded my midi file and so far I'm playing with changing the instruments. It's easy and right now I have a free trial, though that expires at the end of March and I'm not sure how much it is after. Easy to change instruments though, which is a plus! It's also easy to make patterns, and I've made a good start with making a pattern, following [this tutorial](https://www.youtube.com/watch?v=pDIsEZsalAo). Still not sure how to remix my midi file though!



