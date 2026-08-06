# Compatibility-Fixes

## 3DConnexion SpaceMouse Legacy driver Fix for Win11


This targets Win11 25H2 26200.8894 and newer (and possibly a few versions before that -- this is the version that i did this to)

w/ Windows ADK for Win10 1809 i build a SDB where the 3DConnexion driver executable is targeted to run with "FaultTolerantHeap" enabled
as this is (as per copilots interpretation of the eventlogs) the culprit.

The generated SDB is also attached here 

install it with cmd.exe and then 
sdbinst.exe \<path to sdbfile\>

## CompatibilityTelemetryRunner get nuked... 

So this Microsoft First Party "tool" (or abomination there of) is penetrantly running really often thereby packing up CPU very badly and it just generally does not serve any purpose for me. 

It also resurrects itself after being killed in Taskmanager (usually 2 times per day) and after being deleted from the harddrive (you need a seperate linux installation to do that; takes a while for it to come back). 

My "fix" for now is to do a Compatibility shim with the terminateEXE fix applied targeting that executable. 
