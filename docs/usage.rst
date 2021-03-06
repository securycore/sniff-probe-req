=====
Usage
=====

Enabling the monitor mode
-------------------------

The `sniff-probe-req` script must be used with a wireless interface in monitor mode.

With `ifconfig` and `iwconfig`
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

::

    sudo ifconfig <wireless interface> down
    sudo iwconfig <wireless interface> mode monitor
    sudo ifconfig <wireless interface> up

For example:

::

    sudo ifconfig wlan0 down
    sudo iwconfig wlan0 mode monitor
    sudo ifconfig wlan0 up

With `airmon-ng` from aircrack-ng
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

To kill all the interfering processes:

::

    sudo airmon-ng check kill

To enable the monitor mode:

::

    sudo airmon-ng start <wireless interface>

For example:

::

    sudo airmon-ng start wlan0

Example of use
--------------

::

    sudo sniff-probe-req -i wlan0

Here is a sample output:

.. image:: _static/img/sniff_probe_req_output_example.png
