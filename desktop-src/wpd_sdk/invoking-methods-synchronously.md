---
description: Richiamare metodi di servizio
ms.assetid: 3a2796c8-1a39-49eb-98e1-c9e06c61f397
title: Richiamare metodi di servizio
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15b9540cf7378e13d56af2611d6216897c6750f6
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424201"
---
# <a name="invoking-service-methods"></a>Richiamare metodi di servizio

L'applicazione WpdServicesApiSample include codice che illustra come un'applicazione può richiamare in modo sincrono i metodi supportati da un determinato servizio Contatti. Questo esempio usa le interfacce seguenti



| Interfaccia    | Descrizione    |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)               | Usato per recuperare **l'interfaccia IPortableDeviceServiceMethods** per richiamare i metodi in un determinato servizio.                                                                  |
| [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods) | Usato per richiamare un metodo di servizio.                                                                                                                                        |
| [**IPortableDeviceValues**](iportabledevicevalues.md)                 | Usato per contenere i parametri del metodo in uscita e i risultati del metodo in ingresso. Può essere **NULL se** il metodo non richiede parametri o restituisce risultati. |



 

Quando l'utente sceglie l'opzione "9" dalla riga di comando, l'applicazione richiama il metodo **InvokeMethods** presente nel modulo ServiceMethods.cpp. Si noti che prima di richiamare i metodi, l'applicazione di esempio apre un servizio Contatti in un dispositivo connesso.

I metodi del servizio incapsulano le funzionalità che ogni servizio definisce e implementa. Sono univoci per ogni tipo di servizio e sono rappresentati da un GUID. Ad esempio, il servizio Contatti definisce un metodo **BeginSync** chiamato dalle applicazioni per preparare il dispositivo per la sincronizzazione degli oggetti Contact e un metodo **EndSync** per notificare al dispositivo che la sincronizzazione è stata completata. Le applicazioni eseguono un metodo chiamando [**IPortableDeviceServiceMethods::Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invoke).

I metodi di servizio non devono essere confusi con i comandi WPD. I comandi WPD fanno parte dell'interfaccia DDI (Device Driver Interface) WPD standard e sono il meccanismo per la comunicazione tra un'applicazione WPD e il driver. I comandi sono predefiniti, raggruppati per categorie, ad esempio **WPD \_ CATEGORY \_ COMMON,** e sono rappresentati da **una struttura PROPERTYKEY.** Un'applicazione invia comandi al driver di dispositivo chiamando [**IPortableDeviceService::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand). Per altre informazioni, vedere l'argomento Comandi.

Il **metodo InvokeMethods** richiama il metodo [**IPortableDeviceService::Methods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) per recuperare [**un'interfaccia IPortableDeviceServiceMethods.**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) Usando questa interfaccia, richiama i **metodi BeginSync** ed **EndSync** chiamando il [**metodo IPortableDeviceServiceMethods::Invoke.**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethods) Ogni volta che chiama **Invoke,** l'applicazione fornisce refGUID per il metodo richiamato.

Il codice seguente usa il **metodo InvokeMethods.**


```C++
// Invoke methods on the Contacts Service.
// BeginSync and EndSync are methods defined by the FullEnumerationSync Device Service.
void InvokeMethods(IPortableDeviceService* pService)
{
    HRESULT hr = S_OK;
    CComPtr<IPortableDeviceServiceMethods> pMethods;

    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceServiceMethods interface from the IPortableDeviceService interface to
    // invoke methods.
    hr = pService->Methods(&pMethods);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceServiceMethods from IPortableDeviceService, hr = 0x%lx\n",hr);
    }

    // Invoke() the BeginSync method
    if (SUCCEEDED(hr))
    {
        // This method does not take any parameters or results, so we pass in NULL
        hr = pMethods->Invoke(METHOD_FullEnumSyncSvc_BeginSync, NULL, NULL);
        if (SUCCEEDED(hr))
        {
            printf("%ws called, hr = 0x%lx\n",NAME_FullEnumSyncSvc_BeginSync, hr);
        }
        else
        {
            printf("! Failed to invoke %ws, hr = 0x%lx\n",NAME_FullEnumSyncSvc_BeginSync, hr);
        }
    }

    // Invoke the EndSync method asynchronously
    if (SUCCEEDED(hr))
    {
        // This method does not take any parameters or results, so we pass in NULL
        hr = pMethods->Invoke(METHOD_FullEnumSyncSvc_EndSync, NULL, NULL);
        if (SUCCEEDED(hr))
        {
            printf("%ws called, hr = 0x%lx\n",NAME_FullEnumSyncSvc_EndSync, hr);
        }
        else
        {
            printf("! Failed to invoke %ws, hr = 0x%lx\n",NAME_FullEnumSyncSvc_EndSync, hr);
        } 
    }
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



