# Kontakt Multiscript for Divisimate Templates
Developed with ❤️ by Eric Warren

# About
This KSP script for Kontakt 6+ translates the keyswitch triggers in [Divisimate's Synchron Prime 2.0 template](https://divisimate.com/templates/synchron-prime-2-0) to the default keyswitches used by other sample libraries.

* Cinematic Studio Series
* Spitfire Symphonic Orchestra 2024 edition

# Setup
1. Click on a .nkp file above and download the raw file in the top-right corner.  
   <img width="171" src="https://github.com/user-attachments/assets/84a631a8-af67-4092-bef4-e8cf76fe2574" />

2. Copy the .nkp to _each_ of your Kontakt version's Multiscripts folders.  
K6: Documents/Native Instruments/Kontakt/presets/Multiscripts  
K7: Documents/Native Instruments/Kontakt 7/presets/Multiscripts

3. In Kontakt, load the multiscript by clicking the KSP button, then click Preset > User > DM2 VSP KS Translator.
<img width="657" alt="Screenshot 2024-10-02 at 3 26 08 PM" src="https://github.com/user-attachments/assets/fa3cf539-4943-4d8e-9a2a-d20011b61b82">

4. Select the library for translation, then click the KSP button to close the multiscript.
<img width="366" alt="Screenshot 2024-10-02 at 3 28 21 PM" src="https://github.com/user-attachments/assets/dbb3a3ef-e1dc-4c32-9be8-d8506c174ad0">


# FlexRouter 

*Forked from [jtackaberry/flexrouter](https://github.com/jtackaberry/flexrouter)*


## What is it?

FlexRouter is a highly customizable Kontakt 5 Multiscript designed for managing and unifying keyswitches across instruments from many different developers.

![](https://www.urandom.ca/flexrouter/flexrouter-2.2.0.png)

Some features include:

* support for note, program change, or CC-based keyswitches
 * FlexRouter refers to all these MIDI events as "keyswitches" even though they're not all strictly "keys"
* arbitrary translation between notes, CCs, and program changes
 * one "keyswitch" input event can be translated to *multiple* configurable output events
* can route events to instruments on ports A-D (64 separate channels)
* multiple note-based keyswitches can be activated simultaneously (useful for e.g. layering articulations)
* one keyswitch note/CC/PC can trigger routing to multiple target channels
* note- and CC-based keyswitches can have configurable velocity/value ranges
* one instance of FlexRouter supports 16 rules
* each rule supports up to 128 independently configured keyswitches
* Optional anti-hanging for notes and sustain pedal when jumping between keyswitches
* Optional CC chasing per rule
* probably a few bugs :)


## How do I install it?

Follow these steps:

1. Click this link for the [latest compiled script](https://urandom.ca/flexrouter/latest)
2. Copy the contents to clipboard (usually ctrl-a followed by ctrl-c)
3. In your Kontakt instance, click the KSP button in the toolbar (which look like a parchment scroll in earlier Kontakt versions) to open the multiscript pane
4. Select the desired slot for the script, and click the edit button
5. Paste the clipboard contents into the newly opened text edit area (ctrl-v)
6. Click the Apply button
7. Click the Edit button again to close the text edit area



## What kinds of things can I use it for?

Here are just a few random use-cases that can be solved using FlexRouter:

* Put each articulation patch on different channels (up to 64) and control with keyswitches
  from a single channel
* Route to different patches based on keyswitch velocity
* Assign different instruments on channels 1 through 16, each with multiple patches for articulations, and
  control each instrument independently
* Use UACC to control conventional note-keyswitched libraries
* Use UACC with Spitfire libraries, but cherry-pick certain articulations from
  other libraries on other channels
* Use standard notes on channel 16 to control Spitfire via UACC on channel 1

There's also a [walkthrough video](https://www.youtube.com/watch?v=FddWrEwaNmM) that shows how to implement some of these use-cases.
(Note, the video shows version 1, but all the examples still work with version 2.)


## How do I contribute or make my own customizations?

### Reporting bugs

Create an account on GitHub and [open an issue](https://github.com/jtackaberry/flexrouter/issues).


### Hacking code

First download and install [Sublime Text 3](http://www.sublimetext.com/3), and then download and install the [SublimeKSP](https://github.com/nojanath/SublimeKSP#installation) plugin for ST3.

While you're at it, visit [Nils Liberg's page for the original SublimeKSP](http://nilsliberg.se/ksp/) and click the donate button to buy Nils a coffee for his original work because there's no way I'd have avoided gouging out my eyes at the abomination that is KSP were it not for Nils' KSP extensions.

Clone the FlexRouter repository, and open the KSP scripts under src/ within ST3.

Use SublimeKSP to compile flexrouter.ksp (F5 by default -- see SublimeKSP's README.md for details) and paste the contents of the clipboard (which gets automagically populated by SublimeKSP) into Kontakt as per the installations steps above.

If you want to contribute changes back to FlexRouter, please use the usual GitHub workflow: fork this repository and send me a pull request.  Please don't be offended by scrutiny and nitpicking on any contributed code. :)
