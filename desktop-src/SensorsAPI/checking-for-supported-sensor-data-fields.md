---
description: In questo argomento viene descritto come verificare che un sensore possa fornire un determinato set di campi dati.
ms.assetid: 918ba4a3-d2ac-47ee-ba29-f7ddf67ffbc5
title: Verifica dei campi dati dei sensori supportati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cfd9cf42d1008ec1bb0e2785ec5113c5a817105
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316621"
---
# <a name="checking-for-supported-sensor-data-fields"></a><span data-ttu-id="c665d-103">Verifica dei campi dati dei sensori supportati</span><span class="sxs-lookup"><span data-stu-id="c665d-103">Checking for Supported Sensor Data Fields</span></span>

<span data-ttu-id="c665d-104">In questo argomento viene descritto come verificare che un sensore possa fornire un determinato set di campi dati.</span><span class="sxs-lookup"><span data-stu-id="c665d-104">This topic describes how to verify that a sensor can provide a particular set of data fields.</span></span>

<span data-ttu-id="c665d-105">Dopo aver recuperato un oggetto sensore, è possibile chiamare [**ISensor:: GetSupportedDataFields**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getsupporteddatafields) per determinare se il sensore è in grado di fornire i dati necessari.</span><span class="sxs-lookup"><span data-stu-id="c665d-105">After you have retrieved a sensor object, you can call [**ISensor::GetSupportedDataFields**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getsupporteddatafields) to determine whether the sensor can provide the data you need.</span></span>

<span data-ttu-id="c665d-106">Il codice di esempio seguente crea una funzione di supporto che verifica se il sensore può fornire tutti e tre i campi dati di esempio.</span><span class="sxs-lookup"><span data-stu-id="c665d-106">The following example code creates a helper function that tests whether the sensor can provide all three of the sample data fields.</span></span> <span data-ttu-id="c665d-107">La funzione accetta un puntatore a un sensore come input e restituisce un valore booleano, dove **true** indica che il sensore può fornire tutti i campi dati richiesti.</span><span class="sxs-lookup"><span data-stu-id="c665d-107">The function takes a pointer to a sensor as its input and returns a Boolean value, where **TRUE** indicates that the sensor can provide all the data fields required.</span></span>


```C++
BOOL CheckForSupportedDataFields(ISensor* pSensor)
{
    assert(pSensor);

    HRESULT hr = S_OK;
    DWORD cKeys = 0; // Key count.
    BOOL bRet = FALSE;

    IPortableDeviceKeyCollection* pKeys = NULL; // Output

    // CoCreate a key collection to store property keys.
    hr = CoCreateInstance(CLSID_PortableDeviceKeyCollection, 
                                NULL, 
                                CLSCTX_INPROC_SERVER, 
                                IID_PPV_ARGS(&pKeys));

    if(SUCCEEDED(hr))
    {
        hr = pSensor->GetSupportedDataFields(&pKeys);
    }

    if(SUCCEEDED(hr))
    {
        hr = pKeys->GetCount(&cKeys);
    }

    if(SUCCEEDED(hr))
    {
        PROPERTYKEY pk;
        BOOL bHour, bMinute, bSecond = FALSE;

        for (DWORD i = 0; i < cKeys; i++)
        {
            hr = pKeys->GetAt(i, &pk);

            if(SUCCEEDED(hr))
            {
                // Test for the data fields.
                if(IsEqualPropertyKey(pk, SAMPLE_SENSOR_DATA_TYPE_HOUR))
                {
                    bHour = TRUE;
                }
                else if(IsEqualPropertyKey(pk, SAMPLE_SENSOR_DATA_TYPE_MINUTE))
                {
                    bMinute = TRUE;
                }
                else if(IsEqualPropertyKey(pk, SAMPLE_SENSOR_DATA_TYPE_SECOND))
                {
                    bSecond = TRUE;
                }
            }
        }

        // Compute the return value.
        // If all three properties were found,
        // bRet will resolve to TRUE.
        bRet = bHour && bMinute && bSecond;
    }

    SafeRelease(&pKeys);

    return bRet;
}
```



## <a name="related-topics"></a><span data-ttu-id="c665d-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c665d-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c665d-109">**ISensorDataReport**</span><span class="sxs-lookup"><span data-stu-id="c665d-109">**ISensorDataReport**</span></span>](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport)
</dt> </dl>

 

 
