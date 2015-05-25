Avestan Keyboard ReadMe

By Pim Rietbroek
MAY 21, 2015

COPYRIGHT
Copyright  2015  Pim Rietbroek.
Copying and distribution of this “Avestan Keyboard ReadMe” file, with or without modification, are permitted in any medium without royalty provided the copyright notice and this notice are preserved.  This file is offered as-is, without any warranty.

LICENSING
The Avestan keyboard for OS X, version 1.0, is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with this program.  If not, see <http://www.gnu.org/licenses/>.

WHAT IS THE AVESTAN KEYBOARD?
The Avestan Keyboard for OS X version 1.0 is a piece of free software intended for all those who wish to input text in the Avestan script on a computer running OS X. Such text will be encoded according to the internationally accepted Unicode Standard.

INSTALLATION AND ACTIVATION

The file called “Avestan.bundle” should be put in one of the following folders (if it doesn’t exist, create it):

/Library/Keyboard Layouts	(making the keyboard available to all users on the machine)

~/Library/Keyboard Layouts	(making the keyboard available to the user only)

/Network/Library/Keyboard Layouts	(making the keyboard available to all users on the network)

You need to log out and log in again for the keyboard layout to show up in the list in the Input Sources tab of the Keyboard preference pane of System Preferences [OS X 10.10.x “Yosemite”]. The keyboard can now be activated, something that needs to be done only once.

1. Open System Preferences.
2. Click on “Keyboard”.
3. In the Keyboard pane, click on the “Input Sources” tab.
4. In Input Sources, the left-hand list shows the installed keyboard layouts. (It may be only one, when you have activated no others.) Near the bottom (right), checkmark “Show Input menu in menu bar”: this will help you choose amongst the installed keyboards.
5. Also in Input Sources, below the left-hand list, click on the “+” button to choose the keyboard you wish to add. In the pop-up list, click on “Avestan (Avestan)”: the right-hand pane will probably just show you one choice, “Avestan”, with the Faravahar symbol next to it. Click that item to select it, and click the “Add” button.
6. You can quit System Preferences: you are done! “Avestan” is now an option in your Keyboard menu, which is shown in the menu bar in the right-hand half. (The Keyboard menu is frequently called the “flag menu”, because many keyboards have a flag icon associated with it.)

For more detailed information, please consult the Avestan Keyboard User Guide.

USE

In the Keyboard menu found towards the right of the menu bar in OS X – sometimes called the “flag menu” – the Avestan keyboard is symbolised by a picture of the “Faravahar” (see: http://en.wikipedia.org/wiki/Faravahar).

FOR OTHER DEVELOPERS: DESIGN CONSIDERATIONS

I have been on the lookout for Avestan resources for some time, on and off. In the spring of 2015 I stumbled across Ernst Tremel’s diligent efforts to get an Avestan keyboard working on Ubuntu <http://www.skytower.org/~ernstjtremel/index.htm> (he has also provided the world with the “Ahuramazda” Avestan font). Simos Xenitellis actually compiled the Ubuntu keyboard on the basis of information provided by Ernst Tremel <http://simos.info/blog/archives/1134>. AFAIK, his is the first working Avestan keyboard ever created and published.

I considered making an Avestan keyboard for OS X because there is a piece of very user-friendly software to make your own keyboard for OS X called “Ukelele” <http://scripts.sil.org/ukelele>, and I thought I should use Mr. Tremel’s keyboard layout as a model, or at least as a starting point. (The way to increase the availability of texts in the Avestan script is to make input as easy as possible, so I thought all major operating systems should at least afford the user an input method. I can only hope that someone will do the same for the Windows platform.)

I studied his keyboard layout and found a few key mappings less helpful because they pointed to Private Use Area codes. It is quite understandable that he included them because in his own “Ahuramazda” font the Avestan ligatures are present at PUA code points, and he obviously wanted to give users access to these ligatures whether the OpenType GSUB would be understood by the user’s application at the rendering stage or not. But an Avestan keyboard which can be used with _any_ properly-encoded Unicode Avestan font should, IMO, not give prominence to PUA encodings: any other font containing Avestan could just as well have the Avestan ligatures at completely different PUA code points. So in a universally useful Avestan keyboard, PUA encoding should be avoided. Therefore I decided to drop the Avestan ligature PUA key mappings.