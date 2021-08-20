---
description: L'API Sensor fornisce notifiche degli eventi tramite interfacce di callback.
ms.assetid: 0c396d54-cb2e-4b07-999f-3f4001db2a02
title: Uso degli eventi dell'API Sensor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ba26e99ef039808ea8c3d6bee9ac8a5b0d6b1a231fb2a4b62c2bb05a2489099
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126501"
---
# <a name="using-sensor-api-events"></a>Uso degli eventi dell'API Sensor

L'API Sensor fornisce notifiche degli eventi tramite interfacce di callback.

Per ricevere notifiche degli eventi, il programma deve implementare le interfacce di callback COM necessarie. Per ricevere eventi dai sensori, è necessario implementare [**ISensorEvents.**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents) Per ricevere eventi dal gestore dei sensori, è necessario implementare [**ISensorManagerEvents.**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanagerevents)

Nell'esempio di codice seguente viene creata una classe che implementa [**ISensorEvents.**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents)


```C++
class CMyEvents : public ISensorEvents
{
public:

    STDMETHODIMP QueryInterface(REFIID iid, void** ppv)
    {
        if (ppv == NULL)
        {
            return E_POINTER;
        }
        if (iid == __uuidof(IUnknown))
        {
            *ppv = static_cast<IUnknown*>(this);
        }
        else if (iid == __uuidof(ISensorEvents))
        {
            *ppv = static_cast<ISensorEvents*>(this);
        }
        else
        {
            *ppv = NULL;
            return E_NOINTERFACE;
        }
        AddRef();
        return S_OK;
    }

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef); 
    }

    STDMETHODIMP_(ULONG) Release()
    {
        ULONG count = InterlockedDecrement(&m_cRef);
        if (count == 0)
        {
            delete this;
            return 0;
        }
        return count;
    }

    //
    // ISensorEvents methods.
    //

    STDMETHODIMP OnEvent(
            ISensor *pSensor,
            REFGUID eventID,
            IPortableDeviceValues *pEventData)
    {
        HRESULT hr = S_OK;

        // Handle custom events here.

        return hr;
    }

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

    STDMETHODIMP OnLeave(
            REFSENSOR_ID sensorID)
    {
        HRESULT hr = S_OK;

        // Peform any housekeeping tasks for the sensor that is leaving.
        // For example, if you have maintained a reference to the sensor,
        // release it now and set the pointer to NULL.

        return hr;
    }

    STDMETHODIMP OnStateChanged(
            ISensor* pSensor,
            SensorState state)
    {
        HRESULT hr = S_OK;

        if(NULL == pSensor)
        {
            return E_INVALIDARG;
        }


        if(state == SENSOR_STATE_READY)
        {
            wprintf_s(L"\nTime sensor is now ready.");
        }
        else if(state == SENSOR_STATE_ACCESS_DENIED)
        {
            wprintf_s(L"\nNo permission for the time sensor.\n");
            wprintf_s(L"Enable the sensor in the control panel.\n");
        }
  

        return hr;
    }

    private:
        long m_cRef;

};

```



Dopo aver implementato l'interfaccia di callback, è possibile fornire a un particolare sensore un puntatore a un'istanza della classe di callback per iniziare a ricevere notifiche degli eventi dal sensore.

Il codice di esempio seguente crea un'istanza della classe di callback e quindi richiede le notifica degli eventi da un sensore.


```C++
CMyEvents* pEventClass = NULL;
ISensorEvents* pMyEvents = NULL;

if(SUCCEEDED(hr))
{
    // Create an instance of the event class.
    pEventClass = new(std::nothrow) CMyEvents();        
}

if(SUCCEEDED(hr))
{
    // Retrieve the pointer to the callback interface.
    hr = pEventClass->QueryInterface(IID_PPV_ARGS(&pMyEvents));
}

if(SUCCEEDED(hr))
{
    // Start receiving events.
    hr = pSensor->SetEventSink(pMyEvents);
} 

```



È possibile scrivere codice simile per ricevere eventi dal gestore dei sensori.

Nell'esempio di codice seguente viene illustrato come arrestare la ricezione di notifiche degli eventi.


```C++
if(SUCCEEDED(hr))
{
    hr = pSensor->SetEventSink(NULL);
}
```



## <a name="requesting-a-report-interval"></a>Richiesta di un intervallo di report

È possibile suggerire un valore per la frequenza con cui l'applicazione riceve gli eventi aggiornati dei dati. Tuttavia, i sensori non sono necessari per fornire eventi in un determinato intervallo. È necessario tenere presente che il valore suggerito potrebbe non corrispondere all'intervallo di report effettivo utilizzato dal sensore per generare eventi. Per conoscere l'intervallo di report effettivo, recuperare il valore della proprietà SENSOR PROPERTY CURRENT REPORT INTERVAL, come descritto in Recupero e impostazione delle proprietà \_ \_ del \_ \_ [sensore.](setting-and-retrieving-sensor-properties.md)

Nell'esempio di codice seguente viene creata una funzione helper che richiede un nuovo valore per la proprietà SENSOR \_ PROPERTY \_ CURRENT REPORT \_ \_ INTERVAL. La funzione accetta un puntatore al sensore per il quale impostare la proprietà e un valore **ULONG** che indica il nuovo intervallo di report da impostare.


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

[Informazioni sugli eventi dell'API Sensor](about-sensor-events.md)
</dt> </dl>

 

 



