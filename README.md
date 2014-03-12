Easy Notes format for abcm2ps
=============================

Easy Notes is a format file for abcm2ps that shows the note name inside of
the actual note head. This is used to teach music to new students.

![Example of Easy Notes Output](http://jeremy.cowgar.com/easynotes.png "Example of Easy Notes Output")

To use Easy Notes, add to your ``.abc`` file:

    %%format easynote.fmt
    %%ps easynotes_on

You can also issue a:

    %%ps easynotes_off

to return back to normal note heads.

It is also advisable to use ``%%scale 1.2`` or larger to make the letters in the note heads
large enough to be readable at a normal distance.

Limitations
-----------

* Does not support ``breve`` or ``longa`` notes. This generally is not a problem 
  since any student just learning the music staff (thus using easy notes)
  is probably not going to run into such notes.
* Does not yet support the bass clef.

Future
------

* Support the idea of an ignore list for notes. For example, once you have taught
  your student C, D and E and they have had sufficient time to learn to sight read
  those notes, you could add C, D and E to the Easy Notes ignore list. This would
  cause those notes to not show the note name in the head, but other notes would.
* Support the bass clef.
* Make half and whole notes more noticable.