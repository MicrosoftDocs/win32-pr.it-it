---
description: Usare gli elementi di programmazione Alimentazione del dispositivo per gestire le prestazioni dei dispositivi mentre il sistema è in stato di sospensione.
ms.assetid: 44479f5d-2e92-4802-a633-3e0bb7d61e94
title: Uso dell'API Power Device
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1aff8239c1cd0ffc8d5e8abaf0133a9ca42bb3a01a5b6fc2acef7850929a8484
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032771"
---
# <a name="using-the-device-power-api"></a>Uso dell'API Power Device

Usare gli elementi di programmazione Alimentazione del dispositivo per gestire le prestazioni dei dispositivi mentre il sistema è in stato di sospensione.

## <a name="opening-and-closing-the-device-list"></a>Apertura e chiusura dell'elenco dei dispositivi

L'apertura e la chiusura dell'elenco di dispositivi è un processo disperso in termini di tempo di CPU. Le [**funzioni DevicePowerOpen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) e [**DevicePowerClose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) sono necessarie solo se l'applicazione deve eseguire più query sull'elenco dei dispositivi.

Se [**viene chiamato DevicePowerOpen,**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) è necessario [**chiamare DevicePowerClose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) al termine delle query dell'elenco di dispositivi. [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) e [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) non chiudono l'elenco di dispositivi se è stato aperto in modo esplicito **da DevicePowerOpen.**

## <a name="enumerating-devices"></a>Enumerazione dei dispositivi

La [**funzione DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) rileva se l'elenco dei dispositivi è aperto e, in caso contrario, lo apre. **DevicePowerEnumDevices enumera** i dispositivi in base ai criteri di ricerca specificati. Se l'elenco di dispositivi è stato aperto dalla funzione, viene chiuso prima che la funzione venga restituita.

## <a name="enabling-and-disabling-a-device-from-waking-the-system"></a>Abilitazione e disabilitazione di un dispositivo per la disattivazione del sistema

La [**funzione DevicePowerSetDeviceState,**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) simile a [**DevicePowerEnumDevices,**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices)rileva se l'elenco di dispositivi è aperto e, in caso contrario, lo apre. **DevicePowerSetDeviceState** imposta quindi i criteri specificati per il dispositivo specificato. Se l'elenco di dispositivi è stato aperto dalla funzione, viene chiuso prima che la funzione venga restituita.

## <a name="example-code"></a>Codice di esempio

L'esempio seguente illustra l'uso dell'API Power Device.


```C++
#define _WIN32_WINNT 0x0600
#include <Windows.h>
#include <PowrProf.h>
#include <stdio.h>
#include <tchar.h>

#pragma comment(lib, "PowrProf.lib")

int __cdecl main()
{
 // Define and initialize our return variables.
 LPWSTR  pRetBuf = NULL;
 ULONG bufSize = MAX_PATH * sizeof(WCHAR);
 ULONG uIndex = 0;
 BOOLEAN bRet = FALSE;

 // Open the device list, querying all devices
 if (!DevicePowerOpen(0)) 
  {
   printf("ERROR: The device database failed to initialize.\n");
   return FALSE;
  }

 // Enumerate the device list, searching for devices that support 
 // waking from either the S1 or S2 sleep state and are currently 
 // present in the system, and not devices that have drivers 
 // installed but are not currently attached to the system, such as 
 // in a laptop docking station.

 pRetBuf = (LPWSTR)LocalAlloc(LPTR, bufSize);

 while (NULL != pRetBuf && 
        0 != (bRet = DevicePowerEnumDevices(uIndex,
           DEVICEPOWER_FILTER_DEVICES_PRESENT,
           PDCAP_WAKE_FROM_S1_SUPPORTED|PDCAP_WAKE_FROM_S2_SUPPORTED,
           (PBYTE)pRetBuf,
           &bufSize)))
  {
   printf("Device name: %S\n", pRetBuf);

   // For the devices we found that have support for waking from 
   // S1 and S2 sleep states, disable them from waking the system.
   bRet = (0 != DevicePowerSetDeviceState((LPCWSTR)pRetBuf, 
                                  DEVICEPOWER_CLEAR_WAKEENABLED, 
                                  NULL));

   if (0 != bRet) 
    {
     printf("Warning: Failed to set device state.\n");
    }
   uIndex++;
  }

 // Close the device list.
 DevicePowerClose();
 if (pRetBuf!= NULL) LocalFree(pRetBuf);
 pRetBuf = NULL;

 return TRUE;
}
```



In questo esempio l'elenco dei dispositivi viene aperto una sola volta e chiuso una volta. Se le [**funzioni DevicePowerOpen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) e [**DevicePowerClose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) non sono state chiamate, l'elenco dei dispositivi sarebbe stato aperto e chiuso da ogni chiamata a [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) e [**DevicePowerSetDeviceState.**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) Con **DevicePowerOpen e** **DevicePowerClose** è stato salvato due volte l'apertura dell'elenco dei dispositivi.

 

 



