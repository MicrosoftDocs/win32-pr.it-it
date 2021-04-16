---
description: Questo argomento descrive come richiedere le autorizzazioni all'utente per usare i sensori. Per informazioni di carattere generale sulle autorizzazioni nell'API dei sensori, vedere Gestione delle autorizzazioni utente.
ms.assetid: e43ad497-86f1-4804-a67a-0aeb56b80d7f
title: Richiesta di autorizzazioni utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41e103426388d2db49bb5a8fb01d3370207ec49b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525656"
---
# <a name="requesting-user-permissions"></a><span data-ttu-id="88e9e-104">Richiesta di autorizzazioni utente</span><span class="sxs-lookup"><span data-stu-id="88e9e-104">Requesting User Permissions</span></span>

<span data-ttu-id="88e9e-105">Questo argomento descrive come richiedere le autorizzazioni all'utente per usare i sensori.</span><span class="sxs-lookup"><span data-stu-id="88e9e-105">This topic describes how to request permissions from the user to use sensors.</span></span> <span data-ttu-id="88e9e-106">Per informazioni di carattere generale sulle autorizzazioni nell'API dei sensori, vedere [gestione delle autorizzazioni utente](managing-user-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="88e9e-106">For background information about permissions in the Sensor API, see [Managing User Permissions](managing-user-permissions.md).</span></span>

<span data-ttu-id="88e9e-107">Gli esempi seguenti illustrano alcuni scenari comuni in cui è possibile scegliere di richiedere le autorizzazioni utente.</span><span class="sxs-lookup"><span data-stu-id="88e9e-107">The following examples illustrate some of the common scenarious where you can choose to request user permissions.</span></span>

<span data-ttu-id="88e9e-108">Il codice di esempio seguente richiede semplicemente le autorizzazioni per tutti i sensori recuperati da Gestione sensori, per tipo, usando una chiamata al metodo asincrona.</span><span class="sxs-lookup"><span data-stu-id="88e9e-108">The following example code simply requests permissions for all sensors retrieved from the sensor manager, by type, using an asynchronous method call.</span></span> <span data-ttu-id="88e9e-109">La piattaforma apre una finestra di dialogo in cui viene richiesto all'utente di abilitare solo i sensori non ancora abilitati.</span><span class="sxs-lookup"><span data-stu-id="88e9e-109">The platform will open a dialog box to prompt the user only to enable sensors that are not already enabled.</span></span> <span data-ttu-id="88e9e-110">Per determinare se l'utente ha abilitato qualsiasi sensore in questo caso, è necessario gestire l'evento [**ISensorEvents:: OnStateChanged**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onstatechanged) .</span><span class="sxs-lookup"><span data-stu-id="88e9e-110">To determine whether the user enabled any sensors in this case, you must handle the [**ISensorEvents::OnStateChanged**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onstatechanged) event.</span></span>


```C++
// Get the sensor collection.
hr = pSensorManager->GetSensorsByType(SAMPLE_SENSOR_TYPE_TIME, &pSensorColl);

if(SUCCEEDED(hr))
{
    // Request permissions for all sensors
    // in the collection.
    hr = pSensorManager->RequestPermissions(0, pSensorColl, FALSE);
}

```



<span data-ttu-id="88e9e-111">È possibile scegliere di testare lo stato del sensore in modo sincrono prima di provare a recuperare i dati.</span><span class="sxs-lookup"><span data-stu-id="88e9e-111">You can choose to test the sensor state synchronously before attempting to retrieve data.</span></span> <span data-ttu-id="88e9e-112">Nell'esempio di codice riportato di seguito viene illustrata questa tecnica.</span><span class="sxs-lookup"><span data-stu-id="88e9e-112">The following example code demonstrates this technique.</span></span>


```C++
if(SUCCEEDED(hr))
{
   // Check the current sensor state.
   SensorState state = SENSOR_STATE_NOT_AVAILABLE;

   hr = pSensor->GetState(&state);

   if(SUCCEEDED(hr))
   {
       if(state == SENSOR_STATE_ACCESS_DENIED)
       {
           wprintf_s(L"\nSensor not enabled, requesting permissions...\n");
           hr = pSensorManager->RequestPermissions(0, pSensorColl, TRUE);

           if(hr == HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED) ||
              hr == HRESULT_FROM_WIN32(ERROR_CANCELLED)) 
           {
               wprintf_s(L"\nYou have previously denied access to this sensor.\n");
               wprintf_s(L"Please use the Location and Other Sensors control panel\n");
               wprintf_s(L"to enable the WDK Time Sensor and run this program again.\n");
           }
       }
   }
}

if(SUCCEEDED(hr))
{
    // Get the data report.
    hr = pSensor->GetData(&pReport);
}
```



<span data-ttu-id="88e9e-113">Il codice di esempio seguente richiede all'utente le autorizzazioni per il sensore se il tentativo di recuperare un rapporto dati da un determinato sensore ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="88e9e-113">The following example code prompts the user for sensor permissions if an attempt to retrieve a data report from a particular sensor fails.</span></span>


```C++
if(SUCCEEDED(hr))
{
    // Get the data report.
    hr = pSensor->GetData(&pReport);

    if(E_ACCESSDENIED == hr)
    {
       wprintf_s(L"\nSensor not enabled, requesting permissions...\n");
       hr = pSensorManager->RequestPermissions(0, pSensorColl, TRUE);

       if(hr == HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED) ||
          hr == HRESULT_FROM_WIN32(ERROR_CANCELLED)) 
       {
           wprintf_s(L"\nYou have previously denied access to this sensor.\n");
           wprintf_s(L"Please use the Location and Other Sensors control panel\n");
           wprintf_s(L"to enable the WDK Time Sensor and run this program again.\n");
       }
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="88e9e-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="88e9e-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88e9e-115">**ISensorManager**</span><span class="sxs-lookup"><span data-stu-id="88e9e-115">**ISensorManager**</span></span>](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager)
</dt> <dt>

[<span data-ttu-id="88e9e-116">Gestione delle autorizzazioni utente</span><span class="sxs-lookup"><span data-stu-id="88e9e-116">Managing User Permissions</span></span>](managing-user-permissions.md)
</dt> </dl>

 

 
