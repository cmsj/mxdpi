The syntax is:

<pre>mxdpi <dpi level> <hidraw device></pre>

<tt><dpi level></tt> should be an integer in {0,...,14}. Higher integers correspond to higher dpi settings.

<tt><hidraw device></tt> is the hidraw device that corresponds to your mouse. This should usually be <tt>/dev/hidraw< X >"</tt>, where <tt>< X ></tt> is an integer. You can find the right device name by executing

<pre>cat /sys/class/hidraw/hidraw< X >/device/uevent</pre>

for all integers <tt>< X ></tt> for which this file exists.