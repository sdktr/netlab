netlab: a Virtual Networking Labbing Tool
=========================================

*netlab* will help you be more proficient once you decide to drop GUI-based virtual networking labs
and build your labs using CLI and infrastructure-as-code principles.

Using *netlab* you can:

* Describe high-level lab topology in YAML format without worrying about the specific implementation details
* Use the same lab topology with multiple virtualization providers (Virtualbox, KVM/libvirt, Docker containers)
* Create Vagrant- and containerlab configuration files and Ansible inventory from the lab topology
* Configure IP addressing, routing protocols, VLANs, VRFs, and other networking technologies in your lab

Based on your lab topology the :doc:`netlab up<netlab/up>` command will:

* Create IPv4 and IPv6 addressing plan and OSPFv2, OSPFv3, EIGRP, IS-IS, BGP, MPLS/VPN and EVPN routing design
* Prepare all the necessary configuration files to start the lab
* Start the lab using Vagrant or containerlab
* Create additional virtual networking infrastructure needed to support your lab
* Deploy initial configurations (interfaces, IPv4 and IPv6 addresses, usernames...) to your lab devices
* Configure VLANs, VRFs, VXLAN, LLDP, BFD, OSPFv2, OSPFv3, EIGRP, IS-IS, BGP, VRRP, anycast gateways,
  MPLS, BGP-LU, L3VPN (VPNv4 + VPNv6), 6PE, EVPN, SR-MPLS, or SRv6 on your lab devices.
* Start external network management tools specified in lab topology like Graphite or SuzieQ

When the lab is fully configured you could:

* Use the **netlab connect** command to connect to network devices via SSH or **docker exec**
* Use **netlab config** command to deploy custom configuration snippets

Before shutting down your lab with :doc:`netlab down <netlab/down>`, you might want to run the **netlab collect**
command to save the configuration changes you made.

Getting Started
---------------

* Explore the :doc:`supported platforms <platforms>` to figure out whether you could build your desired lab with *netlab*
* Read the :doc:`installation guide <install>`
* Choose the virtualization method you'd like to use to build your lab
* Follow the `instructions in the installation guide <install.html#building-the-lab-environment>`_ to build your lab environment

.. toctree::
   :caption: Installation Guides
   :maxdepth: 2
   :hidden:

   install.md
   platforms.md
..

.. toctree::
   :caption: Using the Tools
   :maxdepth: 2
   :hidden:

   tutorials.md
   topology-overview.md
   cli-overview.md
   example/addressing-tutorial.md
   example/vrf-tutorial.md
   example/external.md
..

.. toctree::
   :caption: Reference Materials
   :maxdepth: 1
   :hidden:

   netlab/cli.md
   topology-reference.md
   modules.md
   module-reference.md
   providers.md
   defaults.md
   outputs/index.md
..

.. toctree::
   :caption: Release Notes
   :maxdepth: 2
   :hidden:

   release.md
   caveats.md
..

.. toctree::
   :caption: Developers
   :maxdepth: 2
   :hidden:

   dev/guidelines.md
   dev/config/index.md
   dev/advanced.md
   roadmap/index.md
..
