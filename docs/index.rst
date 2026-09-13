LwUTIL |version| documentation
==============================

Welcome to the documentation for version |version|.

LwUTIL is a lightweight utility library that collects small helper macros and functions
for value comparisons, bit manipulation, endian-aware serialization and a few common
algorithms, commonly hand-written again and again in day-to-day C/C++ development.

.. image:: static/images/logo.svg
    :align: center

.. rst-class:: center
.. rst-class:: index_links

    :ref:`download_library` :ref:`getting_started` `Open Github <https://github.com/MaJerle/lwutil>`_ `Donate <https://paypal.me/tilz0R>`_

Features
^^^^^^^^

* Written in C (C11), compatible with ``stdint.h`` data types
* Get the minimum or maximum of two values, constrain a value to a range, or map it between two ranges
* Get the absolute value of a signed input
* Silence "unused variable" compiler warnings
* Dereference and assign through a pointer, but only when it is not ``NULL``
* Compute the number of elements in a statically allocated array, with ``LWUTIL_ASZ`` as a short alias
* Store and load ``16-bit`` and ``32-bit`` values to and from a byte buffer, in little- or big-endian format

  * Pointer-advancing extended variants are available for sequential (de)serialization

* Set, clear, toggle or check bits against a bit mask
* Convert ``8/16/32-bit`` values to their hexadecimal ASCII representation
* Encode and decode ``32-bit`` values in variable-length integer (``varint``) format
* Check whether a time period has elapsed against a rolling time reference, useful for non-blocking periodic tasks
* Calculate a rolling (sliding-window) linear regression slope over fixed-step sample data, with helpers to query window capacity/count and reset it
* Assert an expression at compile time
* No dynamic memory allocation
* User friendly MIT license

Requirements
^^^^^^^^^^^^

* C compiler
* Negligible flash and RAM footprint - only the functions you actually call get linked

Contribute
^^^^^^^^^^

Fresh contributions are always welcome. Simple instructions to proceed:

#. Fork Github repository
#. Respect `C style & coding rules <https://github.com/MaJerle/c-code-style>`_ used by the library
#. Create a pull request to ``develop`` branch with new features or bug fixes

Alternatively you may:

#. Report a bug
#. Ask for a feature request

License
^^^^^^^

.. literalinclude:: ../LICENSE

Table of contents
^^^^^^^^^^^^^^^^^

.. toctree::
    :maxdepth: 2
    :caption: Contents

    self
    get-started/index
    user-manual/index
    api-reference/index
    changelog/index
    authors/index

.. toctree::
    :maxdepth: 2
    :caption: Other projects
    :hidden:

    LwBTN - Button manager <https://github.com/MaJerle/lwbtn>
    LwDTC - DateTimeCron <https://github.com/MaJerle/lwdtc>
    LwESP - ESP-AT library <https://github.com/MaJerle/lwesp>
    LwEVT - Event manager <https://github.com/MaJerle/lwevt>
    LwGPS - GPS NMEA parser <https://github.com/MaJerle/lwgps>
    LwCELL - Cellular modem host AT library <https://github.com/MaJerle/lwcell>
    LwJSON - JSON parser <https://github.com/MaJerle/lwjson>
    LwMEM - Memory manager <https://github.com/MaJerle/lwmem>
    LwOW - OneWire with UART <https://github.com/MaJerle/lwow>
    LwPKT - Packet protocol <https://github.com/MaJerle/lwpkt>
    LwPRINTF - Printf <https://github.com/MaJerle/lwprintf>
    LwRB - Ring buffer <https://github.com/MaJerle/lwrb>
    LwSHELL - Shell <https://github.com/MaJerle/lwshell>
    LwUTIL - Utility functions <https://github.com/MaJerle/lwutil>
    LwWDG - RTOS task watchdog <https://github.com/MaJerle/lwwdg>