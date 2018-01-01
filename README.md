Colman Keyboard Layout for MacOS
======

The Colman layout is a keyboard layout designed to be efficient and ergonomic. It follows the philosophy of the Workman layout while establishing better numerical characteristics comparable to the Colemak layout.

Designed by ? and posted to https://colmanlayout.wordpress.com/

## Installation

 * Copy Colman.bundle to a Keyboard Layouts directory:
   * Copying the bundle to /Library/Keyboard Layouts/ requires administrator rights to the computer, but will allow the layout system-wide, including the OS X login screen. To enable input options on the login window, check the option in System Preferences / Users & Groups / Login Options / Show Input menu in login window.
	* ~/Library/Keyboard Layouts/ needs less access and is specific to just the user’s account it is saved to.
 * Log out of OS X and log back in.
 * Open System Preferences, click on the Language & Text icon, and in the Input Menu tab enable the Colman layout.
 * Make sure that the Show input menu in menu bar box is also checked.
 * To switch quickly between layouts you can press Command+Space or Command+Option+Space. Note, this hotkey combination conflicts with the default settings for showing Spotlight. Check your settings in System Preferences, Keyboard, Keyboard Shortcuts tab, Spotlight against Keyboard & Text Input.

## Tools

Remap the caps lock key to delete or forward delete with PCKeyboardHack:
http://pqrs.org/macosx/keyremap4macbook/pckeyboardhack.html

Remap any other key with KeyRemap4MacBook:
http://pqrs.org/macosx/keyremap4macbook/

Ukelele to create the layout:
http://scripts.sil.org/cms/scripts/page.php?site_id=nrsi&id=ukelele

iConvert Icons to make the NO menu icon:
http://iconverticons.com/

## Original Linux proposal

You need to edit five files with administrative privilege

Add the following to the end of /usr/share/X11/xkb/symbols/us (GNU/Linux)or /usr/local/share/X11/xkb/symbols/us (FreeBSD)

    // Colman Keyboard Layout symbols for xkb on X.Org Server 7.x
    partial alphanumeric_keys
    xkb_symbols "colman" {
    name[Group1]= "English (Colman)";
    include "us(basic)"
    include "us(basic)"
    // Alphanumeric section
    key <AD01> {  [   q,  Q   ] };
    key <AD02> {  [   l,  L   ] };
    key <AD03> {  [   r,  R   ] };
    key <AD04> {  [   w,  W   ] };
    key <AD05> {  [   b,  B   ] };
    key <AD06> {  [   j,  J   ] };
    key <AD07> {  [   m,  M   ] };
    key <AD08> {  [   u,  U   ] };
    key <AD09> {  [   y,  Y   ] };
    key <AD10> {  [   semicolon,  colon   ] };

    key <AC01> {  [   a,  A   ] };
    key <AC02> {  [   n,  N   ] };
    key <AC03> {  [   h,  H   ] };
    key <AC04> {  [   s,  S   ] };
    key <AC05> {  [   f,  F   ] };
    key <AC06> {  [   p,  P   ] };
    key <AC07> {  [   t,  T   ] };
    key <AC08> {  [   e,  E   ] };
    key <AC09> {  [   o,  O   ] };
    key <AC10> {  [   i,  I   ] };

    key <AB01> {  [   z,  Z   ] };
    key <AB02> {  [   x,  X   ] };
    key <AB03> {  [   v,  V   ] };
    key <AB04> {  [   c,  C   ] };
    key <AB05> {  [   k,  K   ] };
    key <AB06> {  [   g,  G   ] };
    key <AB07> {  [   d,  D   ] };
    // End alphanumeric section

    key <CAPS> { [    BackSpace,       BackSpace] };

    include "level3(ralt_switch)"
    };

Open /usr/share/X11/xkb/rules/evdev.lst and /usr/share/X11/xkb/rules/base.lst (GNU/Linux)or /usr/local/share/X11/xkb/rules/evdev.lst and /usr/local/share/X11/xkb/rules/base.lst (FreeBSD) find the line

    colemak         us: English (Colemak)

(under !variant) and add the following line after it.

    colman          us: English (Colman)

Open /usr/share/X11/xkb/rules/evdev.xml and  /usr/share/X11/xkb/rules/base.xml (GNU/Linux)or /usr/local/share/X11/xkb/rules/evdev.xml and  /usr/local/share/X11/xkb/rules/base.xml(FreeBSD), and find the lines

    <variant>
    <configItem>
    <name>colemak</name>
    <description>English (Colemak)</description>
    </configItem>
    </variant>

and add the following lines after them.

    <variant>
    <configItem>
    <name>colman</name>
    <description>English (Colman)</description>
    </configItem>
    </variant>
