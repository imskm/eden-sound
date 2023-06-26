# List devices

```console
aplay -l
```

Create virtual device using PulseAudio tool

```console
# pacmd load-module module-null-sink sink_name=Virtual_Sink sink_properties=device.description=Virtual_Sink


# This worked
# NOTE(muktar): Creating / loading module `module-combine-sink` worked but `module-null-sink` did not.
# How I figured it out: I created virtual audio device using KDE's sound settings and checked the value
# of that audio divice using `pacmd` command and `list-sinks`
pacmd load-module module-combine-sink sink_name=Virtual_Sink sink_properties=device.description=Virtual_Sink

# module-combine-sink
```
