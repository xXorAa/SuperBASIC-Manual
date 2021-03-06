..  _wm-block:

WM\_BLOCK
=========

+----------+-------------------------------------------------------------------+
| Syntax   |  WM\_BLOCK [#channel,] width, height, x, y, palette\_index        |
+----------+-------------------------------------------------------------------+
| Location |  SMSQ/E  >= 3.00                                                  |
+----------+-------------------------------------------------------------------+

Newer Window Managers maintain a table of colour settings for programs to use
as “standard colours”. This is called the *System Palette*, also known as a
‘colour theme’. Four system palette tables, or themes, are supplied with the
operating system.

The list is sorted by *usage* rather than *colour* and includes colour values
to be used for display items such as window background, border, loose items and
so on. The items are referenced by a 4-digit hex number (16-bit value) as per
the list under the entry for :ref:`wm-ink`, or the decimal number equivalent.
These numbers should not be used in standard :ref:`ink`, :ref:`paper` and :ref:`border` statements –
they are not colour values, merely an index to an entry in a list of colour
values. They should be used with the WM_x equivalent commands, which will look
up the colour values to be used for the item numbers in the list.

WM\_BLOCK draws a block in the channel indicated using the colour for the
specified item number from the system palette.

**Example**

::

    WM_BLOCK #1,100, 40, 0, 0, $201

Draws a block 100 pixels wide and 40 pixels high to #1 in the current system
palette's window background colour.

**CROSS-REFERENCE**

See :ref:`wm-ink`,
:ref:`wm-paper`,
:ref:`wm-border`,
:ref:`wm-strip`.

