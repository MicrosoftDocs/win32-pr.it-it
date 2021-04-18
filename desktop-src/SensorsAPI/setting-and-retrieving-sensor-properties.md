---
description: In questo argomento viene descritto come recuperare e impostare i valori per le proprietà del sensore. L'interfaccia ISensor fornisce i metodi per impostare e recuperare i valori per le proprietà del sensore.
ms.assetid: 7d10e5b4-bae7-4564-84eb-75c6a2eeef8f
title: Recupero e impostazione delle proprietà dei sensori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78f64bf0e253f47ae2d8cd1f4945f3b87aa3406b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314667"
---
# <a name="retrieving-and-setting-sensor-properties"></a>Recupero e impostazione delle proprietà dei sensori

In questo argomento viene descritto come recuperare e impostare i valori per le proprietà del sensore. L'interfaccia [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) fornisce i metodi per impostare e recuperare i valori per le proprietà del sensore.

## <a name="retrieving-sensor-properties"></a>Recupero delle proprietà dei sensori

È possibile recuperare alcuni valori di proprietà da un sensore prima che l'utente lo abbia abilitato. Informazioni come il nome del produttore o il modello del sensore possono essere utili per decidere se il programma può usare il sensore.

È possibile scegliere di recuperare un singolo valore di proprietà o di recuperare una raccolta di valori di proprietà insieme. Per recuperare un singolo valore, chiamare [**ISensor:: GetProperty**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getproperty). Per recuperare una raccolta di valori, chiamare [**ISensor:: GetProperties**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getproperties). È possibile recuperare tutte le proprietà per un sensore passando **null** tramite il primo parametro a **ISensor:: GetProperties**.

Nell'esempio di codice seguente viene creata una funzione di supporto che stampa il valore di una singola proprietà. La funzione riceve un puntatore al sensore dal quale recuperare il valore e una chiave di proprietà che contiene la proprietà da stampare. La funzione è in grado di stampare valori per numeri, stringhe e **GUID**, ma non per altri tipi più complessi.


```C++
HRESULT PrintSensorProperty(ISensor* pSensor, REFPROPERTYKEY pk)
{
    assert(pSensor);

    HRESULT hr = S_OK;

    PROPVARIANT pv = {};

    hr = pSensor->GetProperty(pk, &pv);

    if(SUCCEEDED(hr))
    {
        if(pv.vt == VT_UI4)  // Number
        {
            wprintf_s(L"\nSensor integer value: %u\n", pv.ulVal);
        }
        else if(pv.vt == VT_LPWSTR)  // String
        {
            wprintf_s(L"\nSensor string value: %s\n", pv.pwszVal);
        }
        else if(pv.vt == VT_CLSID)  // GUID
        {
            int iRet = 0;

            // Convert the GUID to a string.
            OLECHAR wszGuid[39] = {}; // Buffer for string.
            iRet = ::StringFromGUID2(*(pv.puuid), wszGuid, 39);

            assert(39 == iRet); // Count of characters returned for GUID.

            wprintf_s(L"\nSensor GUID value: %s\n", wszGuid);
        }
        else  // Interface or vector
        {
            wprintf_s(L"\nSensor property is a compound type. Unable to print value.");
        }
    }

    PropVariantClear(&pv);

    return hr;    
}
```



Nell'esempio di codice seguente viene creata una funzione che recupera e stampa una raccolta di proprietà. Il set di proprietà da stampare viene definito dalla matrice denominata SensorProperties.


```C++
HRESULT PrintSensorProperties(ISensor* pSensor)
{
    assert(pSensor);

    HRESULT hr = S_OK;

    DWORD cVals = 0; // Count of returned properties.
    IPortableDeviceKeyCollection* pKeys = NULL; // Input
    IPortableDeviceValues* pValues = NULL;  // Output

    // Properties to print.
    const PROPERTYKEY SensorProperties[] =
    {
        SENSOR_PROPERTY_MANUFACTURER,
        SENSOR_PROPERTY_SERIAL_NUMBER,
        SENSOR_PROPERTY_DESCRIPTION,
        SENSOR_PROPERTY_FRIENDLY_NAME
    };

    // CoCreate a key collection to store property keys.
    hr = CoCreateInstance(CLSID_PortableDeviceKeyCollection, 
                                NULL, 
                                CLSCTX_INPROC_SERVER,                                 
                                IID_PPV_ARGS(&pKeys));

    if(SUCCEEDED(hr))
    {
        // Add the properties to the key collection.
        for (DWORD dwIndex = 0; dwIndex < ARRAYSIZE(SensorProperties); dwIndex++)
        {
            hr = pKeys->Add(SensorProperties[dwIndex]);

            if(FAILED(hr))
            {
                // Unexpected.
                // This example returns the failed HRESULT.
                // You may choose to ignore failures, here.
                break;
            }
        }
    }

    if(SUCCEEDED(hr))
    {
        // Retrieve the properties from the sensor.
        hr = pSensor->GetProperties(pKeys, &pValues);
    }

    if(SUCCEEDED(hr))
    {
        // Get the number of values returned.        
        hr = pValues->GetCount(&cVals);
    }

    if(SUCCEEDED(hr))
    {
        PROPERTYKEY pk; // Keys
        PROPVARIANT pv = {}; // Values

        // Loop through the values;
        for (DWORD i = 0; i < cVals; i++)
        {
            // Get the value at the current index.
            hr = pValues->GetAt(i, &pk, &pv);

            if(SUCCEEDED(hr))
            { 
                // Find and print the property.
                if(IsEqualPropertyKey(pk, SENSOR_PROPERTY_MANUFACTURER))
                {
                    wprintf_s(L"\nManufacturer: %s\n", pv.pwszVal);
                }
                else if(IsEqualPropertyKey(pk, SENSOR_PROPERTY_SERIAL_NUMBER))
                {
                    wprintf_s(L"Serial number: %s\n", pv.pwszVal);
                }
                else if(IsEqualPropertyKey(pk, SENSOR_PROPERTY_FRIENDLY_NAME))
                {
                    wprintf_s(L"Friendly name: %s\n", pv.pwszVal);
                }
                else if(IsEqualPropertyKey(pk, SENSOR_PROPERTY_DESCRIPTION))
                {
                    wprintf_s(L"Description: %s\n", pv.pwszVal);
                }
            }

            PropVariantClear(&pv);
        } // end i loop        
    }

    SafeRelease(&pKeys);
    SafeRelease(&pValues);

    return hr;
};
```



## <a name="setting-sensor-properties"></a>Impostazione delle proprietà del sensore

Prima di poter impostare i valori delle proprietà per un sensore, l'utente deve abilitare il sensore. Inoltre, non tutte le proprietà del sensore possono essere impostate.

Per impostare uno o più valori per le proprietà, chiamare [**ISensor:: seproperties**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-setproperties). Questo metodo viene fornito con un puntatore [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) che contiene la raccolta di proprietà da impostare e i relativi valori associati. Il metodo restituisce un'interfaccia [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) corrispondente che può contenere codici di errore per le proprietà che non è stato possibile impostare.

Nell'esempio di codice seguente viene creata una funzione di supporto che imposta un nuovo valore per \_ la \_ \_ Proprietà Sensor \_ intervallo report corrente. La funzione accetta un puntatore al sensore per il quale impostare la proprietà e un valore **ULONG** che indica il nuovo intervallo del report da impostare. Si noti che l'impostazione di un valore per questa particolare proprietà non garantisce che il sensore accetterà il valore specificato. Per informazioni sul funzionamento di questa proprietà, vedere [**proprietà del sensore**](sensor-properties.md) .


```C++
HRESULT SetCurrentReportInterval(ISensor* pSensor, ULONG ulNewInterval)
{
    assert(pSensor);

    HRESULT hr = S_OK;

    IPortableDeviceValues* pPropsToSet = NULL; // Input
    IPortableDeviceValues* pPropsReturn = NULL; // Output

    // Create the input object.
    hr = CoCreateInstance(__uuidof(PortableDeviceValues),
                            NULL,
                            CLSCTX_INPROC_SERVER,                           
                            IID_PPV_ARGS(&pPropsToSet));

    if(SUCCEEDED(hr))
    {
        // Add the current report interval property.
        hr = pPropsToSet->SetUnsignedIntegerValue(SENSOR_PROPERTY_CURRENT_REPORT_INTERVAL, ulNewInterval);
    }

    if(SUCCEEDED(hr))
    {
        // Only setting a single property, here.
        hr = pSensor->SetProperties(pPropsToSet, &pPropsReturn);
    }

    // Test for failure.
    if(hr == S_FALSE)
    {
        HRESULT hrError = S_OK;
      
        // Check results for failure.
        hr = pPropsReturn->GetErrorValue(SENSOR_PROPERTY_CURRENT_REPORT_INTERVAL, &hrError);

        if(SUCCEEDED(hr))
        {
            // Print an error message.
            wprintf_s(L"\nSetting current report interval failed with error 0x%X\n", hrError);

            // Return the error code.
            hr = hrError;
        }
    }
    else if(hr == E_ACCESSDENIED)
    {
        // No permission. Take appropriate action.
    }

    SafeRelease(&pPropsToSet);
    SafeRelease(&pPropsReturn);
   
    return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Proprietà del sensore**](sensor-properties.md)
</dt> </dl>

 

 
