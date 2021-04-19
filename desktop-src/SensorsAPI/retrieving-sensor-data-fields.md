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
# <a name="retrieving-sensor-data-values"></a><span data-ttu-id="a8a47-103">Recupero dei valori dei dati del sensore</span><span class="sxs-lookup"><span data-stu-id="a8a47-103">Retrieving Sensor Data Values</span></span>

<span data-ttu-id="a8a47-104">Questo argomento descrive come recuperare dati da un sensore, in modo sincrono e asincrono.</span><span class="sxs-lookup"><span data-stu-id="a8a47-104">This topic describes how to retrieve data from a sensor, synchronously and asynchronously.</span></span>

## <a name="retrieving-data-synchronously"></a><span data-ttu-id="a8a47-105">Recupero dei dati in modo sincrono</span><span class="sxs-lookup"><span data-stu-id="a8a47-105">Retrieving Data Synchronously</span></span>

<span data-ttu-id="a8a47-106">È possibile recuperare i dati del sensore in modo sincrono chiamando [**ISensor:: GetData**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getdata).</span><span class="sxs-lookup"><span data-stu-id="a8a47-106">You can retrieve sensor data synchronously by calling [**ISensor::GetData**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getdata).</span></span>

<span data-ttu-id="a8a47-107">Nell'esempio di codice seguente viene recuperato un report dei dati del sensore, quindi vengono recuperati tre singoli valori di campo dati.</span><span class="sxs-lookup"><span data-stu-id="a8a47-107">The following example code retrieves a sensor data report, and then retrieves three individual data field values.</span></span> <span data-ttu-id="a8a47-108">Il sensore di esempio fornisce dati personalizzati sull'ora locale corrente in campi di dati di ora, minuti e secondi.</span><span class="sxs-lookup"><span data-stu-id="a8a47-108">The sample sensor provides custom data about the current local time in hour, minute, and second data fields.</span></span> <span data-ttu-id="a8a47-109">La variabile denominata pSensor contiene un puntatore a [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) che rappresenta il sensore che fornisce i dati.</span><span class="sxs-lookup"><span data-stu-id="a8a47-109">The variable named pSensor contains a pointer to [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) that represents the sensor that supplies the data.</span></span>


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



## <a name="retrieving-data-asynchronously"></a><span data-ttu-id="a8a47-110">Recupero dei dati in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="a8a47-110">Retrieving Data Asynchronously</span></span>

<span data-ttu-id="a8a47-111">È possibile ricevere i dati del sensore in modo asincrono eseguendo la registrazione per ricevere l'evento [**ISensorEvents:: OnDataUpdated**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) .</span><span class="sxs-lookup"><span data-stu-id="a8a47-111">You can receive sensor data asynchronously by registering to receive the [**ISensorEvents::OnDataUpdated**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) event.</span></span> <span data-ttu-id="a8a47-112">Per informazioni su come ricevere i callback degli eventi del sensore, vedere [uso degli eventi dell'API del sensore](using-sensor-api-events.md).</span><span class="sxs-lookup"><span data-stu-id="a8a47-112">To understand how to receive sensor event callbacks, see [Using Sensor API Events](using-sensor-api-events.md).</span></span>

<span data-ttu-id="a8a47-113">Nell'esempio di codice seguente viene illustrata un'implementazione di [**ISensorEvents:: OnDataUpdated**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) che recupera i valori dei dati dal rapporto dati fornito dall'evento.</span><span class="sxs-lookup"><span data-stu-id="a8a47-113">The following example code shows an implementation of [**ISensorEvents::OnDataUpdated**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) that retrieves data values from the data report provided by the event.</span></span> <span data-ttu-id="a8a47-114">Il sensore di esempio fornisce dati personalizzati sull'ora locale corrente in campi di dati di ora, minuti e secondi.</span><span class="sxs-lookup"><span data-stu-id="a8a47-114">The sample sensor provides custom data about the current local time in hour, minute, and second data fields.</span></span>


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



 

 
