C----------------------------------------------------------------------------------
C  			          additive rhythm                
C----------------------------------------------------------------------------------
C
C  This Pure Data patch creates "generative music" using the following abstractions.
C  
C  1.) It creates an additive rhythm where the rests between notes randomly generated.
C  2.) It uses a harmonic series as the scale for the notes.
C  3.) It uses Acreil's filter bank abstraction (fbank~) to randomly filter the melody.
C
C  It is writed in vanilla Pure Data using pd 0.50.0
C
C  Please see https://youtu.be/xxxxxxxxxxxxx for an example of the use of this
C  Pure Data patch.
C
C----------------------------------------------------------------------------------
C  Requirements:   Pure Data <https://puredata.info/downloads/pure-data>
C----------------------------------------------------------------------------------
C
Usage:  The file additveRhythm.pd is the parent patch which contains the 
        rest of the modules.

              Explanation of the primary patches:
midiClockOut: Generates bangs in sync at a particular bpm rate.  It need not be
              connected to a synthesizer.
addRhythm:    This patch creates an additive rhythm of one measure of 16th notes.
              The rhythm changes randomly approximately every two measures.
judySynth~:   Sends out an amplitude enveloped note according to the rhythm.
fbank~:       Acreil's bandpass filter bank. Here, the bandpass frequency is changed
              randomly every 1/16th note.

Contributing: Any contributions to this project are welcome.

Acknowledgements: I'd like to thank Acreil for sharing his Pure Data patches.
