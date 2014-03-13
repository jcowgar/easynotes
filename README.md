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

You can also cause Easy Notes to not print the note name in some notes. For example, maybe your
student has had adequate time to learn F, G and A. You can turn those off. All other pitches
such as D, E, f, and f' will still display their note name but F, G and A will not.

    %%ps [ (D) (E) (F) ] easynotes_hide

You can also reset the hide list for other songs.

    %%ps easynotes_showall

Limitations
-----------

* Does not support ``breve`` or ``longa`` notes. This generally is not a problem 
  since any student just learning the music staff (thus using easy notes)
  is probably not going to run into such notes.
* Only supports treble, bass and alto clefs at this time.
