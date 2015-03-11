Fabla - OpenAV Productions
==========================
Official page: http://openavproductions.com/fabla

This is my fork of LV2 drum sampler plugin Fabla.

Here's how it differs from the original:
 - Clicked pads play the sample at a MIDI velocity of 70 (upstream is 120)
 - There is zero enforced attack (upstream adds 2ms attack to your samples to compensate for DC offset)
   Note that this means you will get a nasty pop/click if your sample doesn't begin at zero!
   But on the flipside, your samples will not get at all colored (noticeable with some kicks/hats)


![screenshot](https://raw.github.com/harryhaaren/openAV-Fabla/master/gui/fabla.png "Fabla 1.3 Screenshot")

Dependencies
------------
```
ntk  (git clone git://git.tuxfamily.org/gitroot/non/fltk.git ntk)
cairo
cairomm-1.0
sndfile
lv2
```

Install
-------
Once deps are satisfied, building and installing into ~/.lv2/ is easy,
just run CMake as usual:
```
mkdir build
cd build
cmake ..
make
make install
```

Running
-------
After the `Install` step Ardour3, QTractor, and any other LV2 host should
automatically find Fabla, and be able to use it.

If you have the JALV LV2 host installed, the "run.sh" script can be used to
launch Fabla as a standalone JACK client:
```
$ ./run.sh
```

Contact
-------
If you have a particular question, email me!
```
harryhaaren@gmail.com
```

Cheers, -Harry
