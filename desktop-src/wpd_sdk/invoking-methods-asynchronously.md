---
description: Richiamo asincrono di metodi del servizio
ms.assetid: d3072e34-65f2-4eeb-bcfa-e2db2d34e680
title: Richiamo asincrono di metodi del servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d312cc76cf8cb737136629c1e2c8135d1b7bd1e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232460"
---
# <a name="invoking-service-methods-asynchronously"></a>Richiamo asincrono di metodi del servizio

L'applicazione WpdServiceApiSample include codice che illustra come un'applicazione può richiamare i metodi del servizio in modo asincrono. In questo esempio vengono utilizzate le interfacce seguenti.



|                                                                                         |                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaccia                                                                               | Descrizione                                                                                                                                                             |
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                                | Utilizzato per recuperare l'interfaccia **IPortableDeviceServiceMethods** per richiamare i metodi su un servizio specificato.                                                                  |
| [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)                  | Utilizzato per richiamare un metodo del servizio.                                                                                                                                        |
| [**IPortableDeviceValues**](iportabledevicevalues.md)                                  | Utilizzato per conservare i parametri del metodo in uscita e i risultati del metodo in arrivo. Può essere **null** se il metodo non richiede parametri o restituisce alcun risultato. |
| [**IPortableDeviceServiceMethodCallback**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservicemethodcallback) | Implementata dall'applicazione per ricevere i risultati del metodo quando un metodo è stato completato.                                                                               |



 

Quando l'utente sceglie l'opzione "10" dalla riga di comando, l'applicazione richiama il metodo **InvokeMethodsAsync** trovato nel modulo ServiceMethods. cpp. Si noti che prima di richiamare i metodi, l'applicazione di esempio apre un servizio di contatti in un dispositivo connesso.

I metodi di servizio incapsulano le funzionalità che ogni servizio definisce e implementa. Sono univoche per ogni tipo di servizio e sono rappresentate da un GUID. Il servizio contatti, ad esempio, definisce un metodo **BeginSync** che le applicazioni chiamano per preparare il dispositivo per la sincronizzazione degli oggetti contatto e un metodo **EndSync** per notificare al dispositivo che la sincronizzazione è stata completata. Le applicazioni eseguono un metodo di servizio del dispositivo portatile chiamando [**IPortableDeviceServiceMethods:: Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invoke).

I metodi del servizio non devono essere confusi con i comandi WPD. I comandi WPD fanno parte dell'interfaccia DDI (WPD Device Driver Interface) standard e sono il meccanismo per la comunicazione tra un'applicazione WPD e il driver. I comandi sono predefiniti, raggruppati per categorie (ad esempio, **\_ categoria WPD \_ comune**) e sono rappresentati da una struttura **PropertyKey** . Un'applicazione invia comandi al driver di dispositivo chiamando [**IPortableDeviceService:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand). Per ulteriori informazioni, vedere l'argomento Commands (comandi).

Il metodo **InvokeMethodsAsync** richiama [**IPortableDeviceService:: Methods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) per recuperare un'interfaccia [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) . Utilizzando questa interfaccia, viene richiamata la funzione helper **InvokeMethodAsync** due volte; una volta per il metodo **BeginSync** e una volta per il metodo **EndSync** . In questo esempio, **InvokeMethodAsync** attende indefinitamente che un evento globale venga segnalato quando viene chiamato [**IPortableDeviceServiceMethodCallback:: OnComplete**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethodcallback-oncomplete) .

Il codice seguente usa il metodo **InvokeMethodsAsync** .


```C++
// Invoke methods on the Contacts Service asynchornously.
// BeginSync and EndSync are methods defined by the FullEnumerationSync Device Service.
void InvokeMethodsAsync(IPortableDeviceService* pService)
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

    // Invoke the BeginSync method asynchronously
    if (SUCCEEDED(hr))
    {
        printf("Invoking %ws asynchronously...\n",NAME_FullEnumSyncSvc_BeginSync);

        // This method does not take any parameters, so we pass in NULL
        hr = InvokeMethodAsync(pMethods, METHOD_FullEnumSyncSvc_BeginSync, NULL);
        if (FAILED(hr))
        {
            printf("! Failed to invoke %ws asynchronously, hr = 0x%lx\n",NAME_FullEnumSyncSvc_BeginSync, hr);
        }
    }

    // Invoke the EndSync method asynchronously
    if (SUCCEEDED(hr))
    {
        printf("Invoking %ws asynchronously...\n",NAME_FullEnumSyncSvc_EndSync);

        hr = InvokeMethodAsync(pMethods, METHOD_FullEnumSyncSvc_EndSync, NULL);
        if (FAILED(hr))
        {
            printf("! Failed to invoke %ws asynchronously, hr = 0x%lx\n",NAME_FullEnumSyncSvc_EndSync, hr);
        }
    }
}
```



Per ogni metodo richiamato, la funzione helper **InvokeMethodAsync** esegue le operazioni seguenti:

-   Crea un handle di evento globale che monitora per determinare il completamento del metodo.
-   Crea un oggetto **CMethodCallback** fornito come argomento per [**IPortableDeviceServiceMethods: InvokeAsync**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invokeasync).
-   Chiama il metodo **IPortableDeviceServiceMethods:: InvokeAsync** per richiamare il metodo specificato.
-   Esegue il monitoraggio dell'handle di evento globale per il completamento.
-   Esegue la pulizia.

La classe **CMethodCallback** illustra come un'applicazione può implementare [**IPortableDeviceServiceMethodCallback**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback). L'implementazione di **OnComplete** in questa classe segnala un evento per notificare all'applicazione che il metodo del servizio è stato completato. Oltre al metodo **OnComplete** , questa classe implementa **AddRef**, **QueryInterface** e **Release**, che vengono utilizzati per gestire il conteggio dei riferimenti dell'oggetto e le interfacce implementate.


```C++
class CMethodCallback : public IPortableDeviceServiceMethodCallback
{
public:
   CMethodCallback () : m_cRef(1)
   {
   }

   ~CMethodCallback ()
   {
   }

public:
    // IPortableDeviceServiceMethodCallback::QueryInterface
    virtual HRESULT STDMETHODCALLTYPE OnComplete(
        HRESULT                 hrStatus,
        IPortableDeviceValues*  /*pResults*/) // We are ignoring results as our methods will not return any results
    {
        printf("** Method completed, status HRESULT = 0x%lx **\n", hrStatus);

        if (g_hMethodCompleteEvent != NULL)
        {
            SetEvent(g_hMethodCompleteEvent);
        }          
        return S_OK;
    }

    // IUnknown::AddRef
    virtual ULONG STDMETHODCALLTYPE AddRef(void)
    {
        InterlockedIncrement((long*) &m_cRef);
        return m_cRef;
    }

    // IUnknown::QueryInterface
    virtual HRESULT STDMETHODCALLTYPE QueryInterface(
        REFIID  riid,
        LPVOID* ppvObj)
    {
        HRESULT hr = S_OK;
        if (ppvObj == NULL)
        {
            hr = E_INVALIDARG;
            return hr;
        }

        if ((riid == IID_IUnknown) ||
            (riid == IID_IPortableDeviceServiceMethodCallback))
        {
            AddRef();
            *ppvObj = this;
        }
        else
        {
            *ppvObj = NULL;
            hr = E_NOINTERFACE;
        }
        return hr;
    }

    // IUnknown::Release
    virtual ULONG STDMETHODCALLTYPE Release(void)
    {
        ULONG ulRefCount = m_cRef - 1;

        if (InterlockedDecrement((long*) &m_cRef) == 0)
        {
            delete this;
            return 0;
        }
        return ulRefCount;
    }

private:
    DWORD   m_cRef;
};
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[**IPortableDeviceServiceMethodCallback**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback)
</dt> <dt>

[**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 
