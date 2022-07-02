This is an adaptation of the Swerty keylayout for Danish:
https://johanegustafsson.net/projects/swerty/

Installation instructions: Dwerty for Linux

Add the contents of se.txt to the end of the file /usr/share/X11/xkb/symbols/dk.
Then look up the following section in the file /usr/share/X11/xkb/rules/evdev.xml:

    <layout>
      <configItem>
        <name>dk</name>
        ....

Add the following variant block after the line <variantList>:

        <variant>
          <configItem>
            <name>dwerty</name>
            <description>Dwerty</description>
          </configItem>
        </variant>

Finally, after the line "! variant" in the file /usr/share/X11/xkb/rules/evdev.lst add the following line:
  dwerty          dk: Dwerty

Now Dwerty should show up as one of the alternative keyboard layouts for Danish 
