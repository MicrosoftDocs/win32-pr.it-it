---
description: Usare gli elementi di programmazione dell'alimentazione del dispositivo per gestire il modo in cui i dispositivi vengono eseguiti mentre il sistema è in stato di sospensione.
ms.assetid: 44479f5d-2e92-4802-a633-3e0bb7d61e94
title: Uso dell'API per la potenza del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cabd7a54efc0979360a863dc9c0cf16d69d8d22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529100"
---
# <a name="using-the-device-power-api"></a>Uso dell'API per la potenza del dispositivo

Usare gli elementi di programmazione dell'alimentazione del dispositivo per gestire il modo in cui i dispositivi vengono eseguiti mentre il sistema è in stato di sospensione.

## <a name="opening-and-closing-the-device-list"></a>Apertura e chiusura dell'elenco dei dispositivi

L'apertura e la chiusura dell'elenco dei dispositivi sono un processo oneroso in termini di tempo di CPU. Le funzioni [**DevicePowerOpen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) e [**DevicePowerClose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) che eseguono questa operazione sono necessarie solo se l'applicazione deve eseguire una query sull'elenco di dispositivi più volte.

Se viene chiamato [**DevicePowerOpen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) , è necessario chiamare [**DevicePowerClose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) quando vengono completate le query dell'elenco dispositivi. [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) e [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) non chiuderanno l'elenco dei dispositivi se è stato aperto in modo esplicito da **DevicePowerOpen**.

## <a name="enumerating-devices"></a>Enumerazione dei dispositivi

La funzione [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) rileva se l'elenco dei dispositivi è aperto e, in caso contrario, lo apre. **DevicePowerEnumDevices** enumera i dispositivi in base ai criteri di ricerca specificati. Se l'elenco dei dispositivi è stato aperto dalla funzione, viene chiuso prima che la funzione restituisca.

## <a name="enabling-and-disabling-a-device-from-waking-the-system"></a>Abilitazione e disabilitazione di un dispositivo dal sistema

La funzione [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) , simile a [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices), rileva se l'elenco dei dispositivi è aperto e, in caso contrario, lo apre. **DevicePowerSetDeviceState** imposta quindi i criteri specificati per il dispositivo specificato. Se l'elenco dei dispositivi è stato aperto dalla funzione, viene chiuso prima che la funzione restituisca.

## <a name="example-code"></a>Codice di esempio

L'esempio seguente illustra l'uso dell'API per la potenza del dispositivo.


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



In questo esempio l'elenco dei dispositivi viene aperto una volta e chiuso una volta. Se le funzioni [**DevicePowerOpen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) e [**DevicePowerClose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) non sono state chiamate, l'elenco dei dispositivi verrebbe aperto e chiuso da ogni chiamata a [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) e [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate). Con **DevicePowerOpen** e **DevicePowerClose** è stata salvata l'apertura dell'elenco dei dispositivi due volte non necessarie.

 

 



