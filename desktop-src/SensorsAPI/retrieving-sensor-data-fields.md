---
description: Questo argomento descrive come recuperare dati da un sensore, in modo sincrono e asincrono.
ms.assetid: 4ae80816-5e53-4ed1-9300-4b38c22d65e2
title: Recupero dei valori dei dati del sensore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4642f120e549cd77b1b37610037092facf2ead1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306361"
---
# <a name="retrieving-sensor-data-values"></a>Recupero dei valori dei dati del sensore

Questo argomento descrive come recuperare dati da un sensore, in modo sincrono e asincrono.

## <a name="retrieving-data-synchronously"></a>Recupero dei dati in modo sincrono

È possibile recuperare i dati del sensore in modo sincrono chiamando [**ISensor:: GetData**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getdata).

Nell'esempio di codice seguente viene recuperato un report dei dati del sensore, quindi vengono recuperati tre singoli valori di campo dati. Il sensore di esempio fornisce dati personalizzati sull'ora locale corrente in campi di dati di ora, minuti e secondi. La variabile denominata pSensor contiene un puntatore a [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) che rappresenta il sensore che fornisce i dati.


```C++
if(SUCCEEDED(hr))
{
    // Get the data report.
    hr = pSensor->GetData(&pReport);
}
  
if(SUCCEEDED(hr))
{
    PROPVARIANT var = {};

    hr = pReport->GetSensorValue(SAMPLE_SENSOR_DATA_TYPE_HOUR, &var);

    if(SUCCEEDED(hr))
    {
        if(var.vt == VT_UI4)
        {
            // Get the hour value.
            ulHour = var.ulVal;                
        }
    }

    PropVariantClear(&var);

    hr = pReport->GetSensorValue(SAMPLE_SENSOR_DATA_TYPE_MINUTE, &var);

    if(SUCCEEDED(hr))
    {
        if(var.vt == VT_UI4)
        {
            // Get the hour value.
            ulMinute = var.ulVal;
        }
    }

    PropVariantClear(&var);

    hr = pReport->GetSensorValue(SAMPLE_SENSOR_DATA_TYPE_SECOND, &var);

    if(SUCCEEDED(hr))
    {
        if(var.vt == VT_UI4)
        {
            // Get the hour value.
            ulSecond = var.ulVal;
        }
    }

    PropVariantClear(&var);        

    if(SUCCEEDED(hr))
    {
        // Print the local time to the console window.
        wprintf_s(L"\nCurrent local time is: \n");
        wprintf_s(L"%02d:%02d:%02d (synchronous)\n\n", ulHour, ulMinute, ulSecond);
    }

```



## <a name="retrieving-data-asynchronously"></a>Recupero dei dati in modo asincrono

È possibile ricevere i dati del sensore in modo asincrono eseguendo la registrazione per ricevere l'evento [**ISensorEvents:: OnDataUpdated**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) . Per informazioni su come ricevere i callback degli eventi del sensore, vedere [uso degli eventi dell'API del sensore](using-sensor-api-events.md).

Nell'esempio di codice seguente viene illustrata un'implementazione di [**ISensorEvents:: OnDataUpdated**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) che recupera i valori dei dati dal rapporto dati fornito dall'evento. Il sensore di esempio fornisce dati personalizzati sull'ora locale corrente in campi di dati di ora, minuti e secondi.


```C++
STDMETHODIMP OnDataUpdated(
        ISensor *pSensor,
        ISensorDataReport *pNewData)
{
    HRESULT hr = S_OK;

    if(NULL == pNewData ||
       NULL == pSensor)
    {
        return E_INVALIDARG;
    }

    ULONG ulHour = 0;
    ULONG ulMinute = 0;
    ULONG ulSecond = 0;

    PROPVARIANT var = {};

    hr = pNewData->GetSensorValue(SAMPLE_SENSOR_DATA_TYPE_HOUR, &var);

    if(SUCCEEDED(hr))
    {
        if(var.vt == VT_UI4)
        {
            // Get the hour value.
            ulHour = var.ulVal;                
        }
    }

    PropVariantClear(&var);

    if(SUCCEEDED(hr))
    {
        hr = pNewData->GetSensorValue(SAMPLE_SENSOR_DATA_TYPE_MINUTE, &var);
    }

    if(SUCCEEDED(hr))
    {
        if(var.vt == VT_UI4)
        {
            // Get the hour value.
            ulMinute = var.ulVal;
        }
    }

    PropVariantClear(&var);

    if(SUCCEEDED(hr))
    {
        hr = pNewData->GetSensorValue(SAMPLE_SENSOR_DATA_TYPE_SECOND, &var);
    }

    if(SUCCEEDED(hr))
    {
        if(var.vt == VT_UI4)
        {
            // Get the hour value.
            ulSecond = var.ulVal;
        }
    }

    PropVariantClear(&var);

    if(SUCCEEDED(hr))
    {
        // Print
        wprintf_s(L"Current local time is: \n");
        wprintf_s(L"%02d:%02d:%02d (asynchronous)\n", ulHour, ulMinute, ulSecond);
    }

    return hr;
}
```



 

 
