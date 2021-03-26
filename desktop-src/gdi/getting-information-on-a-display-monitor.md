---
description: Nell'esempio di codice seguente viene illustrato come utilizzare EnumDisplayDevices per ottenere informazioni su un monitor di visualizzazione.
ms.assetid: 8c2420de-292f-481e-b06b-54cc174a8faf
title: Recupero di informazioni su un monitor di visualizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e8b120563e9ceed2e87d66e5bb79790a0f7c771
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993989"
---
# <a name="getting-information-on-a-display-monitor"></a>Recupero di informazioni su un monitor di visualizzazione

Nell'esempio di codice seguente viene illustrato come utilizzare [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) per ottenere informazioni su un monitor di visualizzazione.


```C++
BOOL GetDisplayMonitorInfo(int nDeviceIndex, LPSTR lpszMonitorInfo)
{
    FARPROC EnumDisplayDevices;
    HINSTANCE  hInstUser32;
    DISPLAY_DEVICE DispDev; 
    char szSaveDeviceName[33];  // 32 + 1 for the null-terminator 
    BOOL bRet = TRUE;
        HRESULT hr;
    
    hInstUser32 = LoadLibrary("c:\\windows\User32.DLL");
    if (!hInstUser32) return FALSE;  
    
    // Get the address of the EnumDisplayDevices function 
    EnumDisplayDevices = (FARPROC)GetProcAddress(hInstUser32,"EnumDisplayDevicesA");
    if (!EnumDisplayDevices) {
        FreeLibrary(hInstUser32);
        return FALSE;
    }

    ZeroMemory(&DispDev, sizeof(DispDev));
    DispDev.cb = sizeof(DispDev); 
    
    // After the first call to EnumDisplayDevices,  
    // DispDev.DeviceString is the adapter name 
    if (EnumDisplayDevices(NULL, nDeviceIndex, &DispDev, 0)) 
        {  
                hr = StringCchCopy(szSaveDeviceName, 33, DispDev.DeviceName);
                if (FAILED(hr))
                {
                // TODO: write error handler 
                }
        
        // After second call, DispDev.DeviceString is the  
        // monitor name for that device  
        EnumDisplayDevices(szSaveDeviceName, 0, &DispDev, 0);   
        
                // In the following, lpszMonitorInfo must be 128 + 1 for  
                // the null-terminator. 
                hr = StringCchCopy(lpszMonitorInfo, 129, DispDev.DeviceString);
                if (FAILED(hr))
                {
                // TODO: write error handler 
                }
                
    } else    {
        bRet = FALSE;
    }

    FreeLibrary(hInstUser32);

    return bRet;
}
```



 

 



