===========================================
 Example Code -- Routing Service File Adapter
===========================================

Building C Example
==================
Before compiling or running the example, make sure the environment variable 
NDDSHOME is set to the directory where your version of RTI Connext is installed as explained in the RTI_CoreLibrariesAndUtilities_UsersManual.
Check that the LD_LIBRARY_PATH environment variable is set, as explained in the Link to RTI_Routing_Service_UsersManual
You are supposed to have also installed in your computer the RTI Routing Service Adapter SDK in order to correctly build you adapter

You can find among the file provided an eample makefile,written for a specific architecture (x64Linux2.6gcc4.4.5). The adapter creates a shared library called libfileadapter.so, and copies it to <RTI Rouitng Service Installation Path>/bin/<architecture> in order to not specify the path of the library in the xml configuration file, but just the name.

Before running the example, you should take care of a few parameters inside the xml configuration file, like the path for the source and destination directory, and make sure that the specified folders exist.

Running C Example
=================

If you want to run Routing Service with this adpater, once you have correctly built the adapter, run the routing service specifying where to find the xml configuration file, and the name of the routing_service configuration inside the xml file:

Supposing you are in the RTI_Routing_Service installation directory, run:
./scripts/rtiroutingservice -cfgFile <path for the file file_bridge.xml>/file_bridge.xml -cfgName file_to_file

