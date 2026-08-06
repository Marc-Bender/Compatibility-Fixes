# Compatibility-Fixes

##3DConnexion SpaceMouse Legacy driver Fix for Win11


This targets Win11 25H2 26200.8894 and newer (and possibly a few versions before that -- this is the version that i did this to)

w/ Windows ADK for Win10 1809 i build a SDB where the 3DConnexion driver executable is targeted to run with "FaultTolerantHeap" enabled
as this is (as per copilots interpretation of the eventlogs) the culprit.

The generated SDB is also attached here 

install it with cmd.exe and then 
sdbinst.exe \<path to sdbfile\>
