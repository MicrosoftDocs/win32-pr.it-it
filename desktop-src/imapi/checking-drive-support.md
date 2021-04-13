---
title: Verifica del supporto delle unità
description: Nell'esempio seguente vengono esaminate le caratteristiche del dispositivo del disco indipendenti dai supporti inseriti nel dispositivo.
ms.assetid: 2d7e5ff9-7f1b-4bc1-bbc8-5e7eab45cdb0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49173ab8070821a03028106080dedc21925b088c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396891"
---
# <a name="checking-drive-support"></a>Verifica del supporto delle unità

Nell'esempio seguente vengono esaminate le caratteristiche del dispositivo del disco indipendenti dai supporti inseriti nel dispositivo. In particolare, vengono recuperati gli elenchi di funzionalità supportate, i profili supportati e le pagine in modalità supportata, nonché le impostazioni e il profilo correnti della funzionalità.


```VB
' This script examines the burn device characteristics such as 
' product ID, product revision level, feature set, and profiles. 

' Copyright (C) Microsoft Corp. 2006

Option Explicit

' Constants
const IMAPI_FEATURE_PAGE_TYPE_DVD_DASH_WRITE = 47

WScript.Quit(Main)

Function Main
    Dim Index                ' Index to recording drive.
    Dim Recorder             ' Recorder object
    Dim Path                 ' Directory of files to burn
    Dim Stream               ' Data stream for burning device
    
    Index = 1                ' Second drive on the system

    ' Create a DiscMaster2 object to connect to CD/DVD drives.
    Dim g_DiscMaster
    Set g_DiscMaster = WScript.CreateObject("IMAPI2.MsftDiscMaster2")

    ' Create a DiscRecorder object for the specified burning device.
    Dim uniqueId
    set recorder = WScript.CreateObject("IMAPI2.MsftDiscRecorder2")
    uniqueId = g_DiscMaster.Item(Index)
    recorder.InitializeDiscRecorder( uniqueId )

    ' *** - Formatting to display recorder info
    WScript.Echo "--------------------------------------------------"
    Wscript.Echo " ActiveRecorderId: " & recorder.ActiveDiscRecorder
    Wscript.Echo "        Vendor Id: " & recorder.VendorId
    Wscript.Echo "       Product Id: " & recorder.ProductId
    Wscript.Echo " Product Revision: " & recorder.ProductRevision
    Wscript.Echo "       VolumeName: " & recorder.VolumeName
    Wscript.Echo "   Can Load Media: " & recorder.DeviceCanLoadMedia
    Wscript.Echo "    Device Number: " & recorder.LegacyDeviceNumber

    Dim mountPoint
    For Each mountPoint In recorder.VolumePathNames
        WScript.Echo "      Mount Point: " & mountPoint
    Next

    WScript.Echo "Supported Features"  'in _IMAPI_FEATURE_PAGE_TYPE 
    Dim supportedFeature
    For Each supportedFeature  in recorder.SupportedFeaturePages
        if supportedFeature = _
            IMAPI_FEATURE_PAGE_TYPE_DVD_DASH_WRITE then
                WScript.Echo "    Feature: " & supportedFeature & _
                    "  Drive supports DVD-RW."
        else
                     WScript.Echo "    Feature: " & supportedFeature
        end if
    Next
    
    WScript.Echo "Current Features"    'in _IMAPI_FEATURE_PAGE_TYPE
    Dim currentFeature
    For Each currentFeature  in recorder.CurrentFeaturePages
        WScript.Echo "    Feature: " & currentFeature
    Next
    
    WScript.Echo "Supported Profiles"  'in _IMAPI_PROFILE_TYPE
    Dim supportedProfile
    For Each supportedProfile  in recorder.SupportedProfiles
        WScript.Echo "    Profile: " & supportedProfile
    Next

    WScript.Echo "Current Profiles"    'in _IMAPI_PROFILE_TYPE
    Dim currentProfile
    For Each currentProfile    in recorder.CurrentProfiles
        WScript.Echo "    Profile: " & currentProfile
    Next
    
    WScript.Echo "Supported Mode Pages"  'in  _IMAPI_MODE_PAGE_TYPE
    Dim supportedModePage       
    For Each supportedModePage in recorder.SupportedModePages
        WScript.Echo "    Mode Page: " & supportedModePage
    Next

    WScript.Echo
    WScript.Echo "----- Finished content -----"
    Main = 0
End Function
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di IMAPi](using-imapi.md)
</dt> <dt>

[**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2)
</dt> <dt>

[**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2)
</dt> <dt>

[**tipo di \_ pagina della funzionalità IMAPI \_ \_**](/windows/desktop/api/imapi2/ne-imapi2-imapi_feature_page_type)
</dt> <dt>

[**tipo di \_ pagina modalità IMAPI \_ \_**](/windows/desktop/api/imapi2/ne-imapi2-imapi_mode_page_type)
</dt> <dt>

[**tipo di \_ profilo IMAPI \_**](/windows/desktop/api/imapi2/ne-imapi2-imapi_profile_type)
</dt> </dl>

 

 




