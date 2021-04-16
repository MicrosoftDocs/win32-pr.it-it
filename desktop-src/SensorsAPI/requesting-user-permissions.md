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
# <a name="requesting-user-permissions"></a>Richiesta di autorizzazioni utente

Questo argomento descrive come richiedere le autorizzazioni all'utente per usare i sensori. Per informazioni di carattere generale sulle autorizzazioni nell'API dei sensori, vedere [gestione delle autorizzazioni utente](managing-user-permissions.md).

Gli esempi seguenti illustrano alcuni scenari comuni in cui è possibile scegliere di richiedere le autorizzazioni utente.

Il codice di esempio seguente richiede semplicemente le autorizzazioni per tutti i sensori recuperati da Gestione sensori, per tipo, usando una chiamata al metodo asincrona. La piattaforma apre una finestra di dialogo in cui viene richiesto all'utente di abilitare solo i sensori non ancora abilitati. Per determinare se l'utente ha abilitato qualsiasi sensore in questo caso, è necessario gestire l'evento [**ISensorEvents:: OnStateChanged**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onstatechanged) .


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



È possibile scegliere di testare lo stato del sensore in modo sincrono prima di provare a recuperare i dati. Nell'esempio di codice riportato di seguito viene illustrata questa tecnica.


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



Il codice di esempio seguente richiede all'utente le autorizzazioni per il sensore se il tentativo di recuperare un rapporto dati da un determinato sensore ha esito negativo.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager)
</dt> <dt>

[Gestione delle autorizzazioni utente](managing-user-permissions.md)
</dt> </dl>

 

 
