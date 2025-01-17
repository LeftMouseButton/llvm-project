.. _configure:
..
   Do not edit this file directly. CMake will auto generate it.
   If the changes are intended, add this file to your commit.

==========================
Configure Options
==========================

Below is the full set of options one can use to configure the libc build.
An option can be given an explicit value on the CMake command line using
the following syntax:

.. code-block:: sh

  $> cmake <other build options> -D<libc config option name>=<option value> <more options>

For example:

.. code-block:: sh

  $> cmake <other build options> -DLIBC_CONF_PRINTF_DISABLE_FLOAT=ON <more options>

See the main ``config/config.json``, and the platform and architecture specific
overrides in ``config/<platform>/config.json`` and ``config/<platform>/<arch>/config.json,``
to learn about the defaults for your platform and target.

* **"printf" options**
    - ``LIBC_CONF_PRINTF_DISABLE_FLOAT``: Disable printing floating point values in printf and friends.
    - ``LIBC_CONF_PRINTF_DISABLE_INDEX_MODE``: Disable index mode in the printf format string.
    - ``LIBC_CONF_PRINTF_DISABLE_WRITE_INT``: Disable handling of %n in printf format string.
    - ``LIBC_CONF_PRINTF_FLOAT_TO_STR_USE_MEGA_LONG_DOUBLE_TABLE``: Use large table for better printf long double performance.
