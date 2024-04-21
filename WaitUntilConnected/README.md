/******************************************************************************
 * 
 * WaitUntilConnected version 0.2
 * 
 * Short:
 * WaitUntilConnected is a simple SANA2 tool.
 * It waits until the SANA2 device is CONNECTED and is intended
 * to be used with the RoadShow TCP/IP stack, but not exclusive.
 * 
 * Written by Philippe CARPENTIER, 2024.
 * Compiled with SAS/C 6.58 for AmigaOS/M68K.
 * Freely distributed for non-commercial purposes.
 * 
 * Arguments:
 * DEVICE: The SANA2 device name (full path).
 * UNIT:   The SANA2 device unit number.
 * DELAY:  Extra delay (in ticks, 50 per second).
 * 
 * Defaults:
 * DEVICE="DEVS:Networks/wifipi.device"
 * UNIT=0
 * DELAY=25
 * 
 * Syntax:
 * C:WaitUntilConnected ?
 * C:WaitUntilConnected DEVICE="DEVS:Networks/wifipi.device" UNIT=0
 * C:WaitUntilConnected DEVICE="DEVS:Networks/wifipi.device" UNIT=0 DELAY=50
 * C:Version FULL C:WaitUntilConnected
 * 
 * Example:
 * Run <>NIL: C:WirelessManager DEVICE="wifipi.device" UNIT=0 CONFIG="ENVARC:Sys/Wireless.prefs"
 * C:WaitUntilConnected DEVICE="DEVS:Networks/wifipi.device" UNIT=0 DELAY=100
 * Run >NIL: NetLogViewer CX_POPUP=NO
 * C:AddNetInterface DEVS:NetInterfaces/WiFiPi
 * 
 ******************************************************************************/