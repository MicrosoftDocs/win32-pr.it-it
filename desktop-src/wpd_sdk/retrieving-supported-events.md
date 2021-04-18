---
description: Recupero degli eventi del servizio supportati
ms.assetid: 1bf3aa08-7ffc-417f-a67e-9eee042337b9
title: Recupero degli eventi del servizio supportati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f515b65b8ed062c346777224a64539f5229a704a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317224"
---
# <a name="retrieving-supported-service-events"></a><span data-ttu-id="f153d-103">Recupero degli eventi del servizio supportati</span><span class="sxs-lookup"><span data-stu-id="f153d-103">Retrieving Supported Service Events</span></span>

<span data-ttu-id="f153d-104">L'applicazione WpdServicesApiSample include codice che illustra in che modo un'applicazione può recuperare gli eventi supportati da un determinato servizio Contatti chiamando metodi sulle interfacce seguenti.</span><span class="sxs-lookup"><span data-stu-id="f153d-104">The WpdServicesApiSample application includes code that demonstrates how an application can retrieve the events supported by a given Contacts service by calling methods on the following interfaces.</span></span>



|                                                                                      |                                                                                                       |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f153d-105">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="f153d-105">Interface</span></span>                                                                            | <span data-ttu-id="f153d-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f153d-106">Description</span></span>                                                                                           |
| [<span data-ttu-id="f153d-107">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="f153d-107">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                             | <span data-ttu-id="f153d-108">Utilizzato per recuperare l'interfaccia **IPortableDeviceServiceCapabilities** per accedere agli eventi supportati.</span><span class="sxs-lookup"><span data-stu-id="f153d-108">Used to retrieve the **IPortableDeviceServiceCapabilities** interface to access the supported events.</span></span> |
| [<span data-ttu-id="f153d-109">**IPortableDeviceServiceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="f153d-109">**IPortableDeviceServiceCapabilities**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)     | <span data-ttu-id="f153d-110">Fornisce l'accesso agli eventi e agli attributi di evento supportati.</span><span class="sxs-lookup"><span data-stu-id="f153d-110">Provides access to the supported events and event attributes.</span></span>                                         |
| [<span data-ttu-id="f153d-111">**IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="f153d-111">**IPortableDevicePropVariantCollection**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="f153d-112">Contiene l'elenco degli eventi supportati.</span><span class="sxs-lookup"><span data-stu-id="f153d-112">Contains the list of supported events.</span></span>                                                                |
| [<span data-ttu-id="f153d-113">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="f153d-113">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)                               | <span data-ttu-id="f153d-114">Contiene gli attributi per un determinato evento.</span><span class="sxs-lookup"><span data-stu-id="f153d-114">Contains the attributes for a given event.</span></span>                                                            |



 

<span data-ttu-id="f153d-115">Quando l'utente sceglie l'opzione "4" nella riga di comando, l'applicazione richiama il metodo **ListSupportedEvents** trovato nel modulo ServiceCapabilities. cpp.</span><span class="sxs-lookup"><span data-stu-id="f153d-115">When the user chooses option "4" at the command line, the application invokes the **ListSupportedEvents** method that is found in the ServiceCapabilities.cpp module.</span></span>

<span data-ttu-id="f153d-116">Si noti che prima di recuperare l'elenco di eventi, l'applicazione di esempio apre un servizio contatti in un dispositivo connesso.</span><span class="sxs-lookup"><span data-stu-id="f153d-116">Note that prior to retrieving the list of events, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="f153d-117">In WPD, un evento viene descritto in base al nome, alle opzioni e ai parametri.</span><span class="sxs-lookup"><span data-stu-id="f153d-117">In WPD, an event is described by its name, options, and parameters.</span></span> <span data-ttu-id="f153d-118">Il nome dell'evento è una stringa descrittiva di script, ad esempio, "MyCustomEvent".</span><span class="sxs-lookup"><span data-stu-id="f153d-118">The event name is a script-friendly string, for example, "MyCustomEvent".</span></span> <span data-ttu-id="f153d-119">Le opzioni evento indicano se un determinato evento viene trasmesso a tutti i client e se tale evento supporta AutoPlay.</span><span class="sxs-lookup"><span data-stu-id="f153d-119">The event options indicate whether a given event is broadcast to all clients and whether that event supports autoplay.</span></span> <span data-ttu-id="f153d-120">Gli attributi dei parametri dell'evento includono PROPERTYKEY e VARTYPE di un determinato parametro.</span><span class="sxs-lookup"><span data-stu-id="f153d-120">The event parameter attributes includes a given parameter's PROPERTYKEY and VARTYPE.</span></span>

<span data-ttu-id="f153d-121">Quattro metodi del modulo ServiceCapabilities. cpp supportano il recupero di eventi supportati per il servizio contatti specificato: **ListSupportedEvents**, **DisplayEvent**, **DisplayEventOptions** e **DisplayEventParameters**.</span><span class="sxs-lookup"><span data-stu-id="f153d-121">Four methods in the ServiceCapabilities.cpp module support the retrieval of supported events for the given Contacts service: **ListSupportedEvents**, **DisplayEvent**, **DisplayEventOptions**, and **DisplayEventParameters**.</span></span> <span data-ttu-id="f153d-122">Il metodo **ListSupportedEvents** recupera un conteggio degli eventi supportati e l'identificatore GUID per ogni evento.</span><span class="sxs-lookup"><span data-stu-id="f153d-122">The **ListSupportedEvents** method retrieves a count of supported events and the GUID identifier for each event.</span></span> <span data-ttu-id="f153d-123">Il metodo **DisplayEvent** Visualizza il nome o il GUID dell'evento, quindi chiama **DisplayEventOptions** e **DisplayEventParameters** per visualizzare i dati relativi agli eventi.</span><span class="sxs-lookup"><span data-stu-id="f153d-123">The **DisplayEvent** method displays the event name or GUID, and then calls **DisplayEventOptions** and **DisplayEventParameters** to display the event-related data.</span></span>

<span data-ttu-id="f153d-124">Il metodo **ListSupportedEvents** richiama il metodo [**IPortableDeviceService:: capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) per recuperare un'interfaccia [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) .</span><span class="sxs-lookup"><span data-stu-id="f153d-124">The **ListSupportedEvents** method invokes the [**IPortableDeviceService::Capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) method to retrieve an [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) interface.</span></span> <span data-ttu-id="f153d-125">Utilizzando questa interfaccia, vengono recuperati gli eventi supportati chiamando il metodo [**IPortableDeviceServiceCapabilities:: GetSupportedEvents**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedevents) .</span><span class="sxs-lookup"><span data-stu-id="f153d-125">Using this interface, it retrieves the supported events by calling the [**IPortableDeviceServiceCapabilities::GetSupportedEvents**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedevents) method.</span></span> <span data-ttu-id="f153d-126">Il metodo **GetSupportedEvents** recupera i GUID per ogni evento supportato dal servizio e copia tali GUID in un oggetto [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="f153d-126">The **GetSupportedEvents** method retrieves the GUIDs for each event supported by the service and copies those GUIDs into an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object.</span></span>

<span data-ttu-id="f153d-127">Il codice seguente illustra il recupero degli eventi del servizio supportati.</span><span class="sxs-lookup"><span data-stu-id="f153d-127">The following code illustrates retrieving supported service events.</span></span>


```C++
// List all supported events on the service
void ListSupportedEvents(
    IPortableDeviceService* pService)
{
    HRESULT hr          = S_OK;
    DWORD   dwNumEvents = 0;
    CComPtr<IPortableDeviceServiceCapabilities>     pCapabilities;
    CComPtr<IPortableDevicePropVariantCollection>   pEvents;

    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceServiceCapabilities interface from the IPortableDeviceService interface to
    // access the service capabilities-specific methods.
    hr = pService->Capabilities(&pCapabilities);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceServiceCapabilities from IPortableDeviceService, hr = 0x%lx\n",hr);
    }

    // Get all events supported by the service.
    if (SUCCEEDED(hr))
    {
        hr = pCapabilities->GetSupportedEvents(&pEvents);
        if (FAILED(hr))
        {
            printf("! Failed to get supported events from the service, hr = 0x%lx\n",hr);
        }
    }

    // Get the number of supported events found on the service.
    if (SUCCEEDED(hr))
    {
        hr = pEvents->GetCount(&dwNumEvents);
        if (FAILED(hr))
        {
            printf("! Failed to get number of supported events, hr = 0x%lx\n",hr);
        }
    }

    printf("\n%d Supported Events Found on the service\n\n", dwNumEvents);

    // Loop through each event and display it
    if (SUCCEEDED(hr))
    {
        for (DWORD dwIndex = 0; dwIndex < dwNumEvents; dwIndex++)
        {
            PROPVARIANT pv = {0};
            PropVariantInit(&pv);
            hr = pEvents->GetAt(dwIndex, &pv);

            if (SUCCEEDED(hr))
            {
                // We have an event.  It is assumed that
                // events are returned as VT_CLSID VarTypes.
                if (pv.puuid != NULL)
                {
                    DisplayEvent(pCapabilities, *pv.puuid);
                    printf("\n");
                }
            }

            PropVariantClear(&pv);
        }
    }
}
```



<span data-ttu-id="f153d-128">Dopo che il metodo **ListSupportedEvents** recupera i GUID che rappresentano ogni evento supportato dal servizio specificato, richiama il metodo **DisplayEvent** per recuperare i dati specifici dell'evento.</span><span class="sxs-lookup"><span data-stu-id="f153d-128">After the **ListSupportedEvents** method retrieves the GUIDs representing each event supported by the given service, it invokes the **DisplayEvent** method to retrieve event-specific data.</span></span> <span data-ttu-id="f153d-129">Questi dati includono il nome dell'evento, le relative opzioni (broadcast o AutoPlay), i GUID di parametro, i tipi di parametro e così via.</span><span class="sxs-lookup"><span data-stu-id="f153d-129">This data includes the event name, its options (broadcast or autoplay), parameter GUIDs, parameter types, and so on.</span></span>

<span data-ttu-id="f153d-130">Il metodo **DisplayEvent** richiama il metodo [**IPortableDeviceServiceCapabilities:: GetEventAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes) per recuperare una raccolta di attributi per l'evento specificato.</span><span class="sxs-lookup"><span data-stu-id="f153d-130">The **DisplayEvent** method invokes the [**IPortableDeviceServiceCapabilities::GetEventAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes) method to retrieve a collection of attributes for the given event.</span></span> <span data-ttu-id="f153d-131">Chiama quindi il metodo [**IPortableDeviceValues:: GetStringValue**](iportabledevicevalues-getstringvalue.md) e richiede che il driver restituisca un nome descrittivo per l'evento specificato.</span><span class="sxs-lookup"><span data-stu-id="f153d-131">It then calls the [**IPortableDeviceValues::GetStringValue**](iportabledevicevalues-getstringvalue.md) method and requests that the driver return a user-friendly name for the given event.</span></span> <span data-ttu-id="f153d-132">**DisplayEvent** chiama quindi [**IPortableDeviceValues:: GetIPortableDeviceValuesValue**](iportabledevicevalues-getiportabledevicevaluesvalue.md) per recuperare le opzioni dell'evento.</span><span class="sxs-lookup"><span data-stu-id="f153d-132">Next, **DisplayEvent** calls the [**IPortableDeviceValues::GetIPortableDeviceValuesValue**](iportabledevicevalues-getiportabledevicevaluesvalue.md) to retrieve the event options.</span></span> <span data-ttu-id="f153d-133">Infine, DisplayEvent chiama [**IPortableDeviceValues:: GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md) per recuperare l'elenco dei parametri dell'evento.</span><span class="sxs-lookup"><span data-stu-id="f153d-133">Finally, DisplayEvent calls the [**IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md) to retrieve the list of event parameters.</span></span> <span data-ttu-id="f153d-134">Passa i dati restituiti da questi metodi alle funzioni di supporto **DisplayEventOptions** e **DisplayEventParameters** , che eseguono il rendering delle opzioni e delle informazioni sui parametri per l'evento specificato.</span><span class="sxs-lookup"><span data-stu-id="f153d-134">It passes the data returned by these methods to the **DisplayEventOptions** and the **DisplayEventParameters** helper functions, which render the options and parameter information for the given event.</span></span>

<span data-ttu-id="f153d-135">Il codice seguente usa il metodo **DisplayEvent** .</span><span class="sxs-lookup"><span data-stu-id="f153d-135">The following code uses the **DisplayEvent** method.</span></span>


```C++
// Display basic information about an event
void DisplayEvent(
    IPortableDeviceServiceCapabilities* pCapabilities,
    REFGUID                             Event)
{
    CComPtr<IPortableDeviceValues> pAttributes;

    // Get the event attributes which describe the event
    HRESULT hr = pCapabilities->GetEventAttributes(Event, &pAttributes);
    if (FAILED(hr))
    {
        printf("! Failed to get the event attributes, hr = 0x%lx\n",hr);
    }

    if (SUCCEEDED(hr))
    {
        PWSTR pszFormatName = NULL;
        CComPtr<IPortableDeviceValues>          pOptions;
        CComPtr<IPortableDeviceKeyCollection>   pParameters;

        // Display the name of the event if it is available. Otherwise, fall back to displaying the GUID.
        hr = pAttributes->GetStringValue(WPD_EVENT_ATTRIBUTE_NAME, &pszFormatName);
        if (SUCCEEDED(hr))
        {
            printf("%ws\n", pszFormatName);
        }
        else
        {
            printf("%ws\n", (PWSTR)CGuidToString(Event));
        }       

        // Display the event options
        hr = pAttributes->GetIPortableDeviceValuesValue(WPD_EVENT_ATTRIBUTE_OPTIONS, &pOptions);
        if (SUCCEEDED(hr))
        {
            DisplayEventOptions(pOptions);
        }
        else
        {
            printf("! Failed to get the event options, hr = 0x%lx\n", hr);
        }       

        // Display the event parameters
        hr = pAttributes->GetIPortableDeviceKeyCollectionValue(WPD_EVENT_ATTRIBUTE_PARAMETERS, &pParameters);
        if (SUCCEEDED(hr))
        {
            DisplayEventParameters(pCapabilities, Event, pParameters);
        }
        else
        {
            printf("! Failed to get the event parameters, hr = 0x%lx\n", hr);
        }       
        
        CoTaskMemFree(pszFormatName);
        pszFormatName = NULL;
    }
}
```



<span data-ttu-id="f153d-136">La funzione helper **DisplayEventOptions** riceve un oggetto [**IPortableDeviceValues**](iportabledevicevalues.md) che contiene i dati dell'opzione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="f153d-136">The **DisplayEventOptions** helper function receives an [**IPortableDeviceValues**](iportabledevicevalues.md) object which contains the event's option data.</span></span> <span data-ttu-id="f153d-137">Chiama quindi il metodo [**IPortableDeviceValues:: GetBoolValue**](iportabledevicevalues-getboolvalue.md) per recuperare i dati delle opzioni.</span><span class="sxs-lookup"><span data-stu-id="f153d-137">It then calls the [**IPortableDeviceValues::GetBoolValue**](iportabledevicevalues-getboolvalue.md) method to retrieve the options data.</span></span> <span data-ttu-id="f153d-138">Usando questi dati, viene eseguito il rendering di una stringa che indica se le opzioni broadcast e AutoPlay sono supportate.</span><span class="sxs-lookup"><span data-stu-id="f153d-138">Using this data, it renders a string indicating whether the broadcast and autoplay options are supported.</span></span>


```C++
// Display the basic event options.
void DisplayEventOptions(
    IPortableDeviceValues* pOptions)
{
    printf("\tEvent Options:\n");
    // Read the WPD_EVENT_OPTION_IS_BROADCAST_EVENT value to see if the event is
    // a broadcast event. If the read fails, assume FALSE
    BOOL  bIsBroadcastEvent = FALSE;
    pOptions->GetBoolValue(WPD_EVENT_OPTION_IS_BROADCAST_EVENT, &bIsBroadcastEvent);
    printf("\tWPD_EVENT_OPTION_IS_BROADCAST_EVENT = %ws\n",bIsBroadcastEvent ? L"TRUE" : L"FALSE");
}
```



## <a name="related-topics"></a><span data-ttu-id="f153d-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f153d-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f153d-140">**IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="f153d-140">**IPortableDeviceKeyCollection**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="f153d-141">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="f153d-141">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="f153d-142">**IPortableDeviceServiceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="f153d-142">**IPortableDeviceServiceCapabilities**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)
</dt> <dt>

[<span data-ttu-id="f153d-143">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="f153d-143">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="f153d-144">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="f153d-144">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



