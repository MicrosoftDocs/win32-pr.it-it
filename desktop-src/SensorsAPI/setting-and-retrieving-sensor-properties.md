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
# <a name="retrieving-and-setting-sensor-properties"></a><span data-ttu-id="d97e1-104">Recupero e impostazione delle proprietà dei sensori</span><span class="sxs-lookup"><span data-stu-id="d97e1-104">Retrieving and Setting Sensor Properties</span></span>

<span data-ttu-id="d97e1-105">In questo argomento viene descritto come recuperare e impostare i valori per le proprietà del sensore.</span><span class="sxs-lookup"><span data-stu-id="d97e1-105">This topic describes how to retrieve and set values for sensor properties.</span></span> <span data-ttu-id="d97e1-106">L'interfaccia [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) fornisce i metodi per impostare e recuperare i valori per le proprietà del sensore.</span><span class="sxs-lookup"><span data-stu-id="d97e1-106">The [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) interface provides the methods to set and retrieve values for sensor properties.</span></span>

## <a name="retrieving-sensor-properties"></a><span data-ttu-id="d97e1-107">Recupero delle proprietà dei sensori</span><span class="sxs-lookup"><span data-stu-id="d97e1-107">Retrieving Sensor Properties</span></span>

<span data-ttu-id="d97e1-108">È possibile recuperare alcuni valori di proprietà da un sensore prima che l'utente lo abbia abilitato.</span><span class="sxs-lookup"><span data-stu-id="d97e1-108">You can retrieve some property values from a sensor before the user has enabled it.</span></span> <span data-ttu-id="d97e1-109">Informazioni come il nome del produttore o il modello del sensore possono essere utili per decidere se il programma può usare il sensore.</span><span class="sxs-lookup"><span data-stu-id="d97e1-109">Information such as the manufacturer's name or the model of the sensor can help you to decide whether your program can use the sensor.</span></span>

<span data-ttu-id="d97e1-110">È possibile scegliere di recuperare un singolo valore di proprietà o di recuperare una raccolta di valori di proprietà insieme.</span><span class="sxs-lookup"><span data-stu-id="d97e1-110">You can choose to retrieve a single property value, or to retrieve a collection of property values together.</span></span> <span data-ttu-id="d97e1-111">Per recuperare un singolo valore, chiamare [**ISensor:: GetProperty**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getproperty).</span><span class="sxs-lookup"><span data-stu-id="d97e1-111">To retrieve single value, call [**ISensor::GetProperty**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getproperty).</span></span> <span data-ttu-id="d97e1-112">Per recuperare una raccolta di valori, chiamare [**ISensor:: GetProperties**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getproperties).</span><span class="sxs-lookup"><span data-stu-id="d97e1-112">To retrieve a collection of values, call [**ISensor::GetProperties**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getproperties).</span></span> <span data-ttu-id="d97e1-113">È possibile recuperare tutte le proprietà per un sensore passando **null** tramite il primo parametro a **ISensor:: GetProperties**.</span><span class="sxs-lookup"><span data-stu-id="d97e1-113">You can retrieve all properties for a sensor by passing **NULL** through the first parameter to **ISensor::GetProperties**.</span></span>

<span data-ttu-id="d97e1-114">Nell'esempio di codice seguente viene creata una funzione di supporto che stampa il valore di una singola proprietà.</span><span class="sxs-lookup"><span data-stu-id="d97e1-114">The following example code creates a helper function that prints the value of a single property.</span></span> <span data-ttu-id="d97e1-115">La funzione riceve un puntatore al sensore dal quale recuperare il valore e una chiave di proprietà che contiene la proprietà da stampare.</span><span class="sxs-lookup"><span data-stu-id="d97e1-115">The function receives a pointer to the sensor from which to retrieve the value and a property key that contains the property to print.</span></span> <span data-ttu-id="d97e1-116">La funzione è in grado di stampare valori per numeri, stringhe e **GUID**, ma non per altri tipi più complessi.</span><span class="sxs-lookup"><span data-stu-id="d97e1-116">The function can print values for numbers, strings, and **GUID** s, but not other, more complex types.</span></span>


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



<span data-ttu-id="d97e1-117">Nell'esempio di codice seguente viene creata una funzione che recupera e stampa una raccolta di proprietà.</span><span class="sxs-lookup"><span data-stu-id="d97e1-117">The following example code creates a function that retrieves and prints a collection of properties.</span></span> <span data-ttu-id="d97e1-118">Il set di proprietà da stampare viene definito dalla matrice denominata SensorProperties.</span><span class="sxs-lookup"><span data-stu-id="d97e1-118">The set of properties to print is defined by the array named SensorProperties.</span></span>


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



## <a name="setting-sensor-properties"></a><span data-ttu-id="d97e1-119">Impostazione delle proprietà del sensore</span><span class="sxs-lookup"><span data-stu-id="d97e1-119">Setting Sensor Properties</span></span>

<span data-ttu-id="d97e1-120">Prima di poter impostare i valori delle proprietà per un sensore, l'utente deve abilitare il sensore.</span><span class="sxs-lookup"><span data-stu-id="d97e1-120">Before you can set property values for a sensor, the user must enable the sensor.</span></span> <span data-ttu-id="d97e1-121">Inoltre, non tutte le proprietà del sensore possono essere impostate.</span><span class="sxs-lookup"><span data-stu-id="d97e1-121">Also, not all sensor properties can be set.</span></span>

<span data-ttu-id="d97e1-122">Per impostare uno o più valori per le proprietà, chiamare [**ISensor:: seproperties**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-setproperties).</span><span class="sxs-lookup"><span data-stu-id="d97e1-122">To set one or more values for properties, call [**ISensor::SetProperties**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-setproperties).</span></span> <span data-ttu-id="d97e1-123">Questo metodo viene fornito con un puntatore [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) che contiene la raccolta di proprietà da impostare e i relativi valori associati.</span><span class="sxs-lookup"><span data-stu-id="d97e1-123">You provide this method with an [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) pointer that contains the collection of properties to set, and their associated values.</span></span> <span data-ttu-id="d97e1-124">Il metodo restituisce un'interfaccia [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) corrispondente che può contenere codici di errore per le proprietà che non è stato possibile impostare.</span><span class="sxs-lookup"><span data-stu-id="d97e1-124">The method returns a corresponding [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) interface that may contain error codes for properties that could not be set.</span></span>

<span data-ttu-id="d97e1-125">Nell'esempio di codice seguente viene creata una funzione di supporto che imposta un nuovo valore per \_ la \_ \_ Proprietà Sensor \_ intervallo report corrente.</span><span class="sxs-lookup"><span data-stu-id="d97e1-125">The following example code creates a helper function that sets a new value for the SENSOR\_PROPERTY\_CURRENT\_REPORT\_INTERVAL property.</span></span> <span data-ttu-id="d97e1-126">La funzione accetta un puntatore al sensore per il quale impostare la proprietà e un valore **ULONG** che indica il nuovo intervallo del report da impostare.</span><span class="sxs-lookup"><span data-stu-id="d97e1-126">The function takes a pointer to the sensor for which to set the property, and a **ULONG** value that indicates the new report interval to be set.</span></span> <span data-ttu-id="d97e1-127">Si noti che l'impostazione di un valore per questa particolare proprietà non garantisce che il sensore accetterà il valore specificato.</span><span class="sxs-lookup"><span data-stu-id="d97e1-127">(Note that setting a value for this particular property does not guarantee that the sensor will accept the specified value.</span></span> <span data-ttu-id="d97e1-128">Per informazioni sul funzionamento di questa proprietà, vedere [**proprietà del sensore**](sensor-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="d97e1-128">See [**Sensor Properties**](sensor-properties.md) for information about how this property works.)</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="d97e1-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d97e1-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d97e1-130">**Proprietà del sensore**</span><span class="sxs-lookup"><span data-stu-id="d97e1-130">**Sensor Properties**</span></span>](sensor-properties.md)
</dt> </dl>

 

 
