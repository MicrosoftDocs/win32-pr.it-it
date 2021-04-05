---
description: L'API del sensore fornisce notifiche degli eventi tramite interfacce di callback.
ms.assetid: 0c396d54-cb2e-4b07-999f-3f4001db2a02
title: Uso degli eventi dell'API del sensore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a54fcb14138c1b20470a2b716e5cce86235c3102
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967870"
---
# <a name="using-sensor-api-events"></a><span data-ttu-id="afa19-103">Uso degli eventi dell'API del sensore</span><span class="sxs-lookup"><span data-stu-id="afa19-103">Using Sensor API Events</span></span>

<span data-ttu-id="afa19-104">L'API del sensore fornisce notifiche degli eventi tramite interfacce di callback.</span><span class="sxs-lookup"><span data-stu-id="afa19-104">The Sensor API provides event notifications through callback interfaces.</span></span>

<span data-ttu-id="afa19-105">Per ricevere l'evento notifica, il programma deve implementare le interfacce di callback COM richieste.</span><span class="sxs-lookup"><span data-stu-id="afa19-105">To receive event notfications, your program must implement the required COM callback interfaces.</span></span> <span data-ttu-id="afa19-106">Per ricevere gli eventi dai sensori, è necessario implementare [**ISensorEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents).</span><span class="sxs-lookup"><span data-stu-id="afa19-106">To receive events from sensors, you must implement [**ISensorEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents).</span></span> <span data-ttu-id="afa19-107">Per ricevere gli eventi da Gestione sensori, è necessario implementare [**ISensorManagerEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanagerevents).</span><span class="sxs-lookup"><span data-stu-id="afa19-107">To receive events from the sensor manager, you must implement [**ISensorManagerEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanagerevents).</span></span>

<span data-ttu-id="afa19-108">Il codice di esempio seguente crea una classe che implementa [**ISensorEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents).</span><span class="sxs-lookup"><span data-stu-id="afa19-108">The following example code creates a class that implements [**ISensorEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents).</span></span>


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



<span data-ttu-id="afa19-109">Dopo l'implementazione dell'interfaccia di callback, è possibile fornire un sensore particolare con un puntatore a un'istanza della classe di callback per iniziare a ricevere notifiche di eventi dal sensore.</span><span class="sxs-lookup"><span data-stu-id="afa19-109">After implementing the callback interface, you can provide a particular sensor with a pointer to an instance of your callback class to start receiving event notifications from the sensor.</span></span>

<span data-ttu-id="afa19-110">Il codice di esempio seguente crea un'istanza della classe di callback e quindi richiede l'evento notifiche da un sensore.</span><span class="sxs-lookup"><span data-stu-id="afa19-110">The following example code creates an instance of the callback class, and then requests event notifcations from a sensor.</span></span>


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



<span data-ttu-id="afa19-111">È possibile scrivere codice simile per ricevere eventi da Gestione sensori.</span><span class="sxs-lookup"><span data-stu-id="afa19-111">You can write similar code to receive events from the sensor manager.</span></span>

<span data-ttu-id="afa19-112">Nell'esempio di codice seguente viene illustrato come arrestare la ricezione delle notifiche degli eventi.</span><span class="sxs-lookup"><span data-stu-id="afa19-112">The following example code shows how to stop receiving event notifications.</span></span>


```C++
if(SUCCEEDED(hr))
{
    hr = pSensor->SetEventSink(NULL);
}
```



## <a name="requesting-a-report-interval"></a><span data-ttu-id="afa19-113">Richiesta di un intervallo di report</span><span class="sxs-lookup"><span data-stu-id="afa19-113">Requesting a Report Interval</span></span>

<span data-ttu-id="afa19-114">È possibile suggerire un valore per la frequenza con cui Applicaton riceve gli eventi di aggiornamento dei dati.</span><span class="sxs-lookup"><span data-stu-id="afa19-114">You can suggest a value for how frequently your applicaton receives data-updated events.</span></span> <span data-ttu-id="afa19-115">Tuttavia, non è necessario che i sensori forniscano eventi a un determinato intervallo.</span><span class="sxs-lookup"><span data-stu-id="afa19-115">However, sensors are not required to provide events at any particular interval.</span></span> <span data-ttu-id="afa19-116">È necessario tenere presente che il valore suggerito potrebbe non corrispondere all'intervallo di report effettivo usato dal sensore per generare eventi.</span><span class="sxs-lookup"><span data-stu-id="afa19-116">You should be aware that your suggested value might not match the actual report interval the sensor uses to raise events.</span></span> <span data-ttu-id="afa19-117">Per individuare l'intervallo effettivo del report, recuperare il valore della \_ Proprietà Sensor \_ Current \_ report \_ Interval, come descritto in [recupero e impostazione delle proprietà del sensore](setting-and-retrieving-sensor-properties.md).</span><span class="sxs-lookup"><span data-stu-id="afa19-117">To know the actual report interval, retrieve the value for the SENSOR\_PROPERTY\_CURRENT\_REPORT\_INTERVAL property, as described in [Retrieving and Setting Sensor Properties](setting-and-retrieving-sensor-properties.md).</span></span>

<span data-ttu-id="afa19-118">Nell'esempio di codice seguente viene creata una funzione di supporto che richiede un nuovo valore per \_ la \_ \_ Proprietà Sensor \_ intervallo report corrente.</span><span class="sxs-lookup"><span data-stu-id="afa19-118">The following example code creates a helper function that requests a new value for the SENSOR\_PROPERTY\_CURRENT\_REPORT\_INTERVAL property.</span></span> <span data-ttu-id="afa19-119">La funzione accetta un puntatore al sensore per il quale impostare la proprietà e un valore **ULONG** che indica il nuovo intervallo del report da impostare.</span><span class="sxs-lookup"><span data-stu-id="afa19-119">The function takes a pointer to the sensor for which to set the property, and a **ULONG** value that indicates the new report interval to be set.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="afa19-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="afa19-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="afa19-121">Informazioni sugli eventi dell'API del sensore</span><span class="sxs-lookup"><span data-stu-id="afa19-121">About Sensor API Events</span></span>](about-sensor-events.md)
</dt> </dl>

 

 



