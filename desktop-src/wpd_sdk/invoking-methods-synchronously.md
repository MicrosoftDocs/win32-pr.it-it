---
description: Richiamare metodi di servizio
ms.assetid: 3a2796c8-1a39-49eb-98e1-c9e06c61f397
title: Richiamare metodi di servizio
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b568ea169d0f3c6465d9879eb9eb01c0b46b526
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315546"
---
# <a name="invoking-service-methods"></a>Richiamare metodi di servizio

L'applicazione WpdServicesApiSample include codice che illustra come un'applicazione può richiamare in modo sincrono i metodi supportati da un determinato servizio contatti. In questo esempio vengono utilizzate le interfacce seguenti



|                                                                        |                                                                                                                                                                         |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaccia                                                              | Descrizione                                                                                                                                                             |
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)               | Utilizzato per recuperare l'interfaccia **IPortableDeviceServiceMethods** per richiamare i metodi su un servizio specificato.                                                                  |
| [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods) | Utilizzato per richiamare un metodo del servizio.                                                                                                                                        |
| [**IPortableDeviceValues**](iportabledevicevalues.md)                 | Utilizzato per conservare i parametri del metodo in uscita e i risultati del metodo in arrivo. Può essere **null** se il metodo non richiede parametri o restituisce alcun risultato. |



 

Quando l'utente sceglie l'opzione "9" dalla riga di comando, l'applicazione richiama il metodo **InvokeMethods** trovato nel modulo ServiceMethods. cpp. Si noti che prima di richiamare i metodi, l'applicazione di esempio apre un servizio di contatti in un dispositivo connesso.

I metodi di servizio incapsulano le funzionalità che ogni servizio definisce e implementa. Sono univoche per ogni tipo di servizio e sono rappresentate da un GUID. Il servizio contatti, ad esempio, definisce un metodo **BeginSync** che le applicazioni chiamano per preparare il dispositivo per la sincronizzazione degli oggetti contatto e un metodo **EndSync** per notificare al dispositivo che la sincronizzazione è stata completata. Le applicazioni eseguono un metodo chiamando [**IPortableDeviceServiceMethods:: Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invoke).

I metodi del servizio non devono essere confusi con i comandi WPD. I comandi WPD fanno parte dell'interfaccia DDI (WPD Device Driver Interface) standard e sono il meccanismo per la comunicazione tra un'applicazione WPD e il driver. I comandi sono predefiniti, raggruppati per categorie, ad esempio, **la \_ categoria WPD \_ comune** e sono rappresentati da una struttura **PropertyKey** . Un'applicazione invia comandi al driver di dispositivo chiamando [**IPortableDeviceService:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand). Per ulteriori informazioni, vedere l'argomento Commands (comandi).

Il metodo **InvokeMethods** richiama il metodo [**IPortableDeviceService:: Methods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) per recuperare un'interfaccia [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) . Utilizzando questa interfaccia, vengono richiamati i metodi **BeginSync** e **EndSync** chiamando il metodo [**IPortableDeviceServiceMethods:: Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethods) . Ogni volta che chiama **Invoke**, l'applicazione fornisce REFGUID per il metodo richiamato.

Il codice seguente usa il metodo **InvokeMethods** .


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

 

 



