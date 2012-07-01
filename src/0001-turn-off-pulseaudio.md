Date: 2012-07-01
Title: Turn off PulseAudio
Tags: linuxaudio

Sometimes it happens that you want to get rid of PulseAudio daemon.
Because of complicated GNOME mechanics, simple `pulseaudio --kill` doesn't
work, as it gets restarted again. So actually you have to use
`pacmd suspend true` and `pacmd suspend false` for this purpose. Pulse daemon
doesn't die, but it suspends all audio and releases the hardware.
More user-friendliness is good, so I wrote
[this little GNOME panel extension](https://extensions.gnome.org/extension/375/turn-off-pulseaudio/).
