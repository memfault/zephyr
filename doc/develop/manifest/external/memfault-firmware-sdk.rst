.. _external_module_memfault_firmware_sdk:

memfault-firmware-sdk
#####################

Introduction
************

`memfault-firmware-sdk`_ provides embedded developers with built-in remote debugging, performance
monitoring, and OTA update capabilities for MCU-based devices. It automatically captures crash
reports, logs, and stack traces from devices in the field, making it easier to diagnose issues
without physical access. The SDK also collects lightweight performance metrics such as memory usage,
battery life, connectivity, and firmware stability to track fleet reliability over time.

The SDK communicates with the `Memfault`_ platform, which aggregates this data so teams can
prioritize and resolve issues faster. In addition, the SDK supports over-the-air firmware updates,
enabling controlled rollouts and remote deployment of new releases.

Usage with Zephyr
*****************

To pull in ``memfault-firmware-sdk`` as a Zephyr :ref:`module <modules>`, add it as a West project
in the :file:`west.yaml` file with the following content and run :command:`west update`:

.. code-block:: yaml

   manifest:
     remotes:
       # Add the Memfault GitHub repo
       - name: memfault
         url-base: https://github.com/memfault
     projects:
       # Add the Memfault SDK
       - name: memfault-firmware-sdk
         path: modules/lib/memfault-firmware-sdk
         revision: master
         remote: memfault

For more detailed instructions and API documentation, refer to the
`memfault-firmware-sdk documentation`_ as well as the provided `memfault-firmware-sdk examples`_.

Reference
*********

.. _memfault-firmware-sdk introduction:
    https://docs.memfault.com/docs/mcu/introduction

.. _memfault-firmware-sdk Zephyr guide:
   https://docs.memfault.com/docs/mcu/zephyr-guide

.. _memfault-firmware-sdk examples:
   https://github.com/memfault/memfault-firmware-sdk/tree/master/examples

.. _Memfault:
   https://memfault.com/
