.. _calm_project:

Create a Project in Calm
++++++++++++++++++++++++

Projects are the logical construct that integrate Calm with Nutanix’s native Self-Service Portal (SSP) capabilities, allowing an administrator to assign both infrastructure resources and the roles/permissions of Active Directory users/groups to specific Blueprints and Applications.


#. Click on **Project** in the left hand toolbar .  Click on **Create Project**.

   .. figure:: images/project_list.png

#. Click on **Select Provider**.  Select **Nutanix**.

   .. figure:: images/project_provider.png


#. Click on **Select Clusters & Subnets**

   .. figure:: images/cluster_subnets.png

#. Select the **Rx-Automation-Network**.  Click on **Confirm**

   .. figure:: images/project_network.png

#. Click on **Save & Configure Environment**

   .. figure:: images/project_quota.png

#. Expand the **Linux** section.  Copy the **cloud-init** contents into the **Guest Customization**
  
   .. code-block:: bash
   
    #cloud-config
    users:
    - name: centos
    ssh-authorized-keys:
      - @@{centos_public_key}@@
    sudo: ['ALL=(ALL) NOPASSWD:ALL'] 

   .. note::

#.  Expand the **DISK** section.  Select the disk image as shown.

   .. figure:: images/Env-Disk-Image.png

#.  Expand the **Network Adapter** section.  Select the Network Adapter

   .. figure:: images/Env-Network-Adapter.png

#.  Expand the **Connection** section.  Select the Credential and Address.  Click on Save.

   .. figure:: images/Env-Connection.png


