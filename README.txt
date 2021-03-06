=== Scale Workshop ===

== Contributors ==
* Sevish
* Scott Thompson


== Description ==

Scale Workshop is a tool that allows you to create microtonal tunings within your web browser. Your created tunings can be exported and downloaded to your device in the various formats. These tuning files can be loaded into some synthesizers, allowing you to play microtonal music with them.


== Frequently Asked Questions ==

= Is this a replacement for Scala/LMSO? =

No, those pieces of software are much more sophisticated. The goal of this project is *quick* input/generation/generation of tuning data within the web browser. It's just a simple tool you can use conveniently.


= How do I enter tuning data? =

Tuning data should be entered in to the text area labeled 'Tuning Data'. Add each note on its own new line. Cents and ratios are both supported.
* To specify a ratio, simply write it in the format e.g. 3/2.
* To specify an interval in cents, include a . in the line e.g. 701.9 or 1200.

No need to enter 0. or 1/1 on the first line as your scale is automatically assumed to contain this interval.

The interval on the final line is assumed to be your interval of equivalence (i.e. your octave or pseudo-octave).

Don't add any other weird data to a line. Don't try to mix decimals with ratios (e.g. 2/1.5). Scale Workshop will try to gracefully ignore any rubbish that you put in, but it's very possible that weird stuff will happen.


= Can I copy and paste the contents of a Scala file (.scl) directly into the Tuning Data field? =

Scala files contain non-tuning related comments at the top of the file, so Scale Workshop will throw an error if you try to paste them in directly. Instead you can use the 'Load .scl' function, which automatically removes those comments for you. Or you can paste the Scala file but remove the comments manually.


= Can I play and hear my scales in the browser? =

Not yet. But I am considering it for a future version. It would be useful right?


= Are non-octave based scales supported? =

Yeah.


= How do I make my own keyboard mapping? =

Keyboard mappings are not supported. You can still export a Scala keyboard mapping file (.kbm) but it will assume a linear mapping.
However you can always use duplicate lines in your tuning in order to skip any keys that you don't want to include.


= When I export a tuning, I get a weird filename, why? =

Exporting a file with the correct filename is not supported in Safari (iOS and macOS). You can try to use Firefox, Chrome or Opera instead.


= Can you add a new feature to Scale Workshop? =

Probably! Just contact the author and make a request.
http://sevish.com/contact


= I found a bug =

Please contact the author with as much info as possible about the issue and how to reproduce it.
http://sevish.com/contact


== Changelog ==

= 0.7.0 =
* Scale modifiers added: 'stretch', 'random variance', 'mode'
* Users can now input 'n\m' to specify n steps out of m-EDO
* When generating a rank-2 temperament, display the scale sizes which are MOS
* Improve UI for user input, using custom modals instead of JS prompts
* Code refactored to reduce the amount of duplication
* Code is now split up over various js files so it's easier to navigate
* Change logo/favicon to square shape

= 0.6 =
* Generate rank-2 temperaments

= 0.5 =
* Fix incorrect base frequency when exporting TUN format and NI Kontakt format
* Export Scala .kbm format

= 0.4 =
* All dependencies (Bootstrap, jQuery etc.) now included in scaleworkshop directory
* Import Scala .scl format
* Export Scala .scl format
* Export AnaMark TUN format
* Export Native Instruments Kontakt script format
* Export Max/MSP coll format

= 0.3 =
* Generate equal-tempered tuning
* Generate harmonic series segment tuning
* Generate subharmonic series segment tuning

= 0.2 =
* Allow tuning data input to be parsed into a frequency table

= 0.1 =
* Initial version


== Roadmap ==

= 0.7.1 =
* More scale modifiers? E.g. 'quantize to BPM', 'sort ascending', 'octave reduce'

= 1.0 =
* Stable

= 2.0 =
* Built-in synth using web audio API, allowing you to play and hear your scales in the browser


== License ==

Copyright (c) 2017 Sean Archibald

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
