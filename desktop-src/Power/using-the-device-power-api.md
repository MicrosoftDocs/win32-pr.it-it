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
# <a name="using-the-device-power-api"></a><span data-ttu-id="4fd62-103">Uso dell'API per la potenza del dispositivo</span><span class="sxs-lookup"><span data-stu-id="4fd62-103">Using the Device Power API</span></span>

<span data-ttu-id="4fd62-104">Usare gli elementi di programmazione dell'alimentazione del dispositivo per gestire il modo in cui i dispositivi vengono eseguiti mentre il sistema è in stato di sospensione.</span><span class="sxs-lookup"><span data-stu-id="4fd62-104">Use the Device Power programming elements to manage the way devices perform while the system is in a sleep state.</span></span>

## <a name="opening-and-closing-the-device-list"></a><span data-ttu-id="4fd62-105">Apertura e chiusura dell'elenco dei dispositivi</span><span class="sxs-lookup"><span data-stu-id="4fd62-105">Opening and closing the device list</span></span>

<span data-ttu-id="4fd62-106">L'apertura e la chiusura dell'elenco dei dispositivi sono un processo oneroso in termini di tempo di CPU.</span><span class="sxs-lookup"><span data-stu-id="4fd62-106">Opening and closing the device list is a costly process in terms of CPU time.</span></span> <span data-ttu-id="4fd62-107">Le funzioni [**DevicePowerOpen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) e [**DevicePowerClose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) che eseguono questa operazione sono necessarie solo se l'applicazione deve eseguire una query sull'elenco di dispositivi più volte.</span><span class="sxs-lookup"><span data-stu-id="4fd62-107">The [**DevicePowerOpen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) and [**DevicePowerClose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) functions that do this are only necessary if the application needs to query the device list multiple times.</span></span>

<span data-ttu-id="4fd62-108">Se viene chiamato [**DevicePowerOpen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) , è necessario chiamare [**DevicePowerClose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) quando vengono completate le query dell'elenco dispositivi.</span><span class="sxs-lookup"><span data-stu-id="4fd62-108">If [**DevicePowerOpen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) is called, [**DevicePowerClose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) must be called when device-list queries are complete.</span></span> <span data-ttu-id="4fd62-109">[**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) e [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) non chiuderanno l'elenco dei dispositivi se è stato aperto in modo esplicito da **DevicePowerOpen**.</span><span class="sxs-lookup"><span data-stu-id="4fd62-109">[**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) and [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) will not close the device list if it has been explicitly opened by **DevicePowerOpen**.</span></span>

## <a name="enumerating-devices"></a><span data-ttu-id="4fd62-110">Enumerazione dei dispositivi</span><span class="sxs-lookup"><span data-stu-id="4fd62-110">Enumerating devices</span></span>

<span data-ttu-id="4fd62-111">La funzione [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) rileva se l'elenco dei dispositivi è aperto e, in caso contrario, lo apre.</span><span class="sxs-lookup"><span data-stu-id="4fd62-111">The [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) function detects whether the device list is open, and if not, opens it.</span></span> <span data-ttu-id="4fd62-112">**DevicePowerEnumDevices** enumera i dispositivi in base ai criteri di ricerca specificati.</span><span class="sxs-lookup"><span data-stu-id="4fd62-112">**DevicePowerEnumDevices** enumerates the devices based on the specified search criteria.</span></span> <span data-ttu-id="4fd62-113">Se l'elenco dei dispositivi è stato aperto dalla funzione, viene chiuso prima che la funzione restituisca.</span><span class="sxs-lookup"><span data-stu-id="4fd62-113">If the device list was opened by the function, it is closed before the function returns.</span></span>

## <a name="enabling-and-disabling-a-device-from-waking-the-system"></a><span data-ttu-id="4fd62-114">Abilitazione e disabilitazione di un dispositivo dal sistema</span><span class="sxs-lookup"><span data-stu-id="4fd62-114">Enabling and disabling a device from waking the system</span></span>

<span data-ttu-id="4fd62-115">La funzione [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) , simile a [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices), rileva se l'elenco dei dispositivi è aperto e, in caso contrario, lo apre.</span><span class="sxs-lookup"><span data-stu-id="4fd62-115">The [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) function, similar to [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices), detects whether the device list is open, and if not, opens it.</span></span> <span data-ttu-id="4fd62-116">**DevicePowerSetDeviceState** imposta quindi i criteri specificati per il dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="4fd62-116">**DevicePowerSetDeviceState** then sets the specified criteria for the specified device.</span></span> <span data-ttu-id="4fd62-117">Se l'elenco dei dispositivi è stato aperto dalla funzione, viene chiuso prima che la funzione restituisca.</span><span class="sxs-lookup"><span data-stu-id="4fd62-117">If the device list was opened by the function, it is closed before the function returns.</span></span>

## <a name="example-code"></a><span data-ttu-id="4fd62-118">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="4fd62-118">Example Code</span></span>

<span data-ttu-id="4fd62-119">L'esempio seguente illustra l'uso dell'API per la potenza del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4fd62-119">The following example demonstrates the use of the Device Power API.</span></span>


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



<span data-ttu-id="4fd62-120">In questo esempio l'elenco dei dispositivi viene aperto una volta e chiuso una volta.</span><span class="sxs-lookup"><span data-stu-id="4fd62-120">In this example the device list is opened once, and closed once.</span></span> <span data-ttu-id="4fd62-121">Se le funzioni [**DevicePowerOpen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) e [**DevicePowerClose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) non sono state chiamate, l'elenco dei dispositivi verrebbe aperto e chiuso da ogni chiamata a [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) e [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate).</span><span class="sxs-lookup"><span data-stu-id="4fd62-121">If the [**DevicePowerOpen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) and [**DevicePowerClose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) functions were not called, the device list would have been opened and closed by each call to [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) and [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate).</span></span> <span data-ttu-id="4fd62-122">Con **DevicePowerOpen** e **DevicePowerClose** è stata salvata l'apertura dell'elenco dei dispositivi due volte non necessarie.</span><span class="sxs-lookup"><span data-stu-id="4fd62-122">By using **DevicePowerOpen** and **DevicePowerClose** we saved opening the device list two unnecessary times.</span></span>

 

 



