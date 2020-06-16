.. _lcm:

-----------------------
Lifecycle Manager (LCM)
-----------------------

What is LCM?
++++++++++++

- LCM aims to enable administrators to take inventory of the firmware and software in their Nutanix environment and perform updates in a simple, cluster-aware, fashion.
- LCM is an industry-unique solution - providing the same 1-click operational upgrade simplicity for 7 (and growing) different hardware vendor appliances running Nutanix software.
- LCM just offers a management layer that will allow users to deploy firmware upgrades simply without having to worry about upgrade paths or conflicts between versions. Customers should not require a manual to upgrade their environment - LCM aims to solve this at scale.
- Once a customer performs an Inventory of their cluster, all the firmware is downloaded and staged. From there, users can deploy the updates with as much or as little granularity as they desire. You can either select individual entities for upgrade or do the entire cluster at once (subject to what the actual component being upgraded allows).
- A Dark Site LCM version is available

.. note::

   For detailed information about LCM, please refer to the `Life Cycle Manager Guide v2.2 <https://portal.nutanix.com/page/documents/details/?targetId=Life-Cycle-Manager-Guide-v22%3ALife-Cycle-Manager-Guide-v22>`_

Performing Inventory with LCM
+++++++++++++++++++++++++++++

.. note::

   Some entities are local to Prism Central, such as Calm, Epsilon, and Karbon. To manage these entities, you must log on to **Prism Central**.

   Other entities, such as component firmware, are local to Prism Element. To manage these entities, you must log on to **Prism Element**.

#. From the drop-down menu, select **LCM**.

#. In the LCM sidebar, select **Inventory**.

#. To take an inventory, click **Perform Inventory**.

   - If you do not have auto-update enabled, and a new version of the LCM framework is available, LCM shows the following warning message:

   .. figure:: images/3.png
       :align: center
       :scale: 50%

#. To enable auto-inventory, click **Settings** and select the **Enable LCM Auto Inventory** checkbox in the dialog box that appears.

#. Click **OK**.

   .. figure:: images/4.png
       :align: center

      Use the Focus button to switch between a general display and a component-by-component display.

Performing Updates with the Life Cycle Manager
++++++++++++++++++++++++++++++++++++++++++++++

#. From the drop-down menu, select **LCM**.

#. In the LCM sidebar, under *Updates*, select **Software** or **Firmware**.

#. Select the updates you want to perform.

   - Select the checkbox for the node you want to update, or select All to update the entire cluster.
   - Select the components you want to update. When you select a node, LCM selects the checkboxes for all updateable components by default. Clear the checkbox of any component you do not want to update.

#. Click **NCC Check**.  In the dialog box that appears, specify which prechecks you want LCM to run before updating.

#. Click **Run**.

#. When the prechecks are complete, click **Update**.

#. Review the selected updates and click **Apply Updates**. LCM updates the selected components.

   .. figure:: images/5.png

   .. figure:: images/6.png

   .. figure:: images/7.png

   .. figure:: images/8.png

#. You may wish to run the **Performing Inventory with LCM** steps upon completion to identify any available updates to the cluster.