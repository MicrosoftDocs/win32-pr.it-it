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
# <a name="retrieving-supported-service-events"></a>Recupero degli eventi del servizio supportati

L'applicazione WpdServicesApiSample include codice che illustra in che modo un'applicazione può recuperare gli eventi supportati da un determinato servizio Contatti chiamando metodi sulle interfacce seguenti.



|                                                                                      |                                                                                                       |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| Interfaccia                                                                            | Descrizione                                                                                           |
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                             | Utilizzato per recuperare l'interfaccia **IPortableDeviceServiceCapabilities** per accedere agli eventi supportati. |
| [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)     | Fornisce l'accesso agli eventi e agli attributi di evento supportati.                                         |
| [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) | Contiene l'elenco degli eventi supportati.                                                                |
| [**IPortableDeviceValues**](iportabledevicevalues.md)                               | Contiene gli attributi per un determinato evento.                                                            |



 

Quando l'utente sceglie l'opzione "4" nella riga di comando, l'applicazione richiama il metodo **ListSupportedEvents** trovato nel modulo ServiceCapabilities. cpp.

Si noti che prima di recuperare l'elenco di eventi, l'applicazione di esempio apre un servizio contatti in un dispositivo connesso.

In WPD, un evento viene descritto in base al nome, alle opzioni e ai parametri. Il nome dell'evento è una stringa descrittiva di script, ad esempio, "MyCustomEvent". Le opzioni evento indicano se un determinato evento viene trasmesso a tutti i client e se tale evento supporta AutoPlay. Gli attributi dei parametri dell'evento includono PROPERTYKEY e VARTYPE di un determinato parametro.

Quattro metodi del modulo ServiceCapabilities. cpp supportano il recupero di eventi supportati per il servizio contatti specificato: **ListSupportedEvents**, **DisplayEvent**, **DisplayEventOptions** e **DisplayEventParameters**. Il metodo **ListSupportedEvents** recupera un conteggio degli eventi supportati e l'identificatore GUID per ogni evento. Il metodo **DisplayEvent** Visualizza il nome o il GUID dell'evento, quindi chiama **DisplayEventOptions** e **DisplayEventParameters** per visualizzare i dati relativi agli eventi.

Il metodo **ListSupportedEvents** richiama il metodo [**IPortableDeviceService:: capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) per recuperare un'interfaccia [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) . Utilizzando questa interfaccia, vengono recuperati gli eventi supportati chiamando il metodo [**IPortableDeviceServiceCapabilities:: GetSupportedEvents**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedevents) . Il metodo **GetSupportedEvents** recupera i GUID per ogni evento supportato dal servizio e copia tali GUID in un oggetto [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) .

Il codice seguente illustra il recupero degli eventi del servizio supportati.


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



Dopo che il metodo **ListSupportedEvents** recupera i GUID che rappresentano ogni evento supportato dal servizio specificato, richiama il metodo **DisplayEvent** per recuperare i dati specifici dell'evento. Questi dati includono il nome dell'evento, le relative opzioni (broadcast o AutoPlay), i GUID di parametro, i tipi di parametro e così via.

Il metodo **DisplayEvent** richiama il metodo [**IPortableDeviceServiceCapabilities:: GetEventAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes) per recuperare una raccolta di attributi per l'evento specificato. Chiama quindi il metodo [**IPortableDeviceValues:: GetStringValue**](iportabledevicevalues-getstringvalue.md) e richiede che il driver restituisca un nome descrittivo per l'evento specificato. **DisplayEvent** chiama quindi [**IPortableDeviceValues:: GetIPortableDeviceValuesValue**](iportabledevicevalues-getiportabledevicevaluesvalue.md) per recuperare le opzioni dell'evento. Infine, DisplayEvent chiama [**IPortableDeviceValues:: GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md) per recuperare l'elenco dei parametri dell'evento. Passa i dati restituiti da questi metodi alle funzioni di supporto **DisplayEventOptions** e **DisplayEventParameters** , che eseguono il rendering delle opzioni e delle informazioni sui parametri per l'evento specificato.

Il codice seguente usa il metodo **DisplayEvent** .


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



La funzione helper **DisplayEventOptions** riceve un oggetto [**IPortableDeviceValues**](iportabledevicevalues.md) che contiene i dati dell'opzione dell'evento. Chiama quindi il metodo [**IPortableDeviceValues:: GetBoolValue**](iportabledevicevalues-getboolvalue.md) per recuperare i dati delle opzioni. Usando questi dati, viene eseguito il rendering di una stringa che indica se le opzioni broadcast e AutoPlay sono supportate.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)
</dt> <dt>

[**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)
</dt> <dt>

[**IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



