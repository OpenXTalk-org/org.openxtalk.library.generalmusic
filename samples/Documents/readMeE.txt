
OpenXTalk General Music Library 'playSentence' features

OpenXTalk General Music Library includes a modified version of UDI's MakeSMF/PlayPMD script library,
Which is compatible with UxPlayMIDI, an XCMD that works with HyperCard/OS7-9 and SuperCard/OS7-9. 
This expands on the HyperTalk 'playSentence' text based musical notation syntax.
MakeSMF PlayPMD has handlers to play notes and convert playSentence to a standard MIDI file.
OXT General Music Library includes modifications to try to locate a MIDI playback engine, first checking for
OXT AVMIDIPlayer library (Apple only) or OXT FluidSynth library (cross-platform), then if they are not found
it will attempt to fall back to any other available MIDI Players such as MCI MIDI (Windows),
Quicktime MIDI Play (Windows or MacOS X 10.7 Lion and earlier), or command-line players (TMidity).
This offers functionality almost the same as UxPlayMIDI to  MetaCard/RuntimeRevolution/LiveCode and OpenXTalk 


Grammar of Score:

Please refer to "pmd2E.doc" in detail. The basis is the playSentence of HyperTalk, but it is expanded so that multi-part, chord and some effects are usable. 
This grammar is known as playSentence Musical (MIDI) Data, or "PMD" for convenience (melody format of a certain cellular phone is unrelated).
A '.PMD' file is simply a text file that a score which conforms to PMD grammar is stored in, allowing for a sequence to be edited with any text editor.

Difference with UxPlayMIDI:

Bend (%) and Portamento (&) are ignored.
makeSMF can use up to 16 parts while UxplayMIDI can use max 32 parts.
makeSMF sets 96 with Acoustic (Z) on, UxPlayMIDI sets 127
makeSMF sets 64 with Pedal (H) on, UxPlayMIDI sets 127
makeSMF read a Tempo command(T) from only 1st part. It influences all parts,
UxPlayMIDI reads each part T-command and influence to each part.

NOTE: 'Convert from SMF..' button reads a SMF ( Standard Midi File ) and try to make an PMD score. 
It read only a basic amount of pitch and step-time (gate-time). This function is incomplete, but is usable in input assistance.


System environment
Instrument patch numbers are based on the Roland's General Standard soundbank found in Apple's CoreAudio (as well as QuickTIme Music Instruments) and is also part of Microsoft Windows(XP+).
A GM/GS sound bank is necessary to for playback. OXT GM Library will try to load the Roland bank or FluidSynth's default GM sound font automatically.

All 'makeSMF'/'playPMD' scripts are the same as 1.3. The versions 1.3.1, 1.3.2 and 1.3.3 have other revised scripts.
These stacks are free to use. All scripts and music data is a public domain. 
You copy these freely and can change it. 

'makeSMF'/'playPMD' scripts original author:
UDI  2004.02
eudio@chabashira.co.jp
http://member.nifty.ne.jp/UDI/


OpenXTalk General Music Library: 
OXT GM Lib contains additionally handlers for converting MIDI values, scanning for SoundFonts in common locations, reading information such as patch names from SoundFonts/DLS files, etc.
OXT GM Lib also includes the SoundFont HyperSounds.sf2 originally from Rebecca G. Bettencourt with three instrument sound samples from the HyperCard era, including the classic 'Boing'