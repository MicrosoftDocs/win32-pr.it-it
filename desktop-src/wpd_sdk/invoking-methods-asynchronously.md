---
description: Chiamata asincrona dei metodi del servizio
ms.assetid: d3072e34-65f2-4eeb-bcfa-e2db2d34e680
title: Chiamata asincrona dei metodi del servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3288f739b92de78ed25193756791d422fb1a87cf304e97f4aee904a85ed784b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118697238"
---
# <a name="invoking-service-methods-asynchronously"></a>Chiamata asincrona dei metodi del servizio

L'applicazione WpdServiceApiSample include codice che illustra come un'applicazione può richiamare i metodi del servizio in modo asincrono. Questo esempio usa le interfacce seguenti.



| Interfaccia    | Descrizione          |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                                | Usato per recuperare **l'interfaccia IPortableDeviceServiceMethods** per richiamare i metodi in un determinato servizio.                                                                  |
| [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)                  | Usato per richiamare un metodo di servizio.                                                                                                                                        |
| [**IPortableDeviceValues**](iportabledevicevalues.md)                                  | Usato per contenere i parametri del metodo in uscita e i risultati del metodo in ingresso. Può essere **NULL se** il metodo non richiede parametri o restituisce risultati. |
| [**IPortableDeviceServiceMethodCallback**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservicemethodcallback) | Implementato dall'applicazione per ricevere i risultati del metodo al termine di un metodo.                                                                               |



 

Quando l'utente sceglie l'opzione "10" dalla riga di comando, l'applicazione richiama il metodo **InvokeMethodsAsync** disponibile nel modulo ServiceMethods.cpp. Si noti che prima di richiamare i metodi, l'applicazione di esempio apre un servizio Contatti in un dispositivo connesso.

I metodi del servizio incapsulano le funzionalità che ogni servizio definisce e implementa. Sono univoci per ogni tipo di servizio e sono rappresentati da un GUID. Ad esempio, il servizio Contatti definisce un metodo **BeginSync** chiamato dalle applicazioni per preparare il dispositivo per la sincronizzazione degli oggetti Contact e un metodo **EndSync** per notificare al dispositivo che la sincronizzazione è stata completata. Le applicazioni eseguono un metodo di servizio dispositivo portabile chiamando [**IPortableDeviceServiceMethods::Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invoke).

I metodi di servizio non devono essere confusi con i comandi WPD. I comandi WPD fanno parte dell'interfaccia DDI (Device Driver Interface) WPD standard e sono il meccanismo per la comunicazione tra un'applicazione WPD e il driver. I comandi sono predefiniti, raggruppati per categorie (ad esempio, **WPD \_ CATEGORY \_ COMMON)** e sono rappresentati da **una struttura PROPERTYKEY.** Un'applicazione invia comandi al driver di dispositivo chiamando [**IPortableDeviceService::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand). Per altre informazioni, vedere l'argomento Comandi.

Il **metodo InvokeMethodsAsync** richiama [**IPortableDeviceService::Methods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) per recuperare [**un'interfaccia IPortableDeviceServiceMethods.**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) Usando questa interfaccia, richiama due volte la funzione helper **InvokeMethodAsync.** una volta per **il metodo BeginSync** e una volta per il **metodo EndSync.** In questo esempio **InvokeMethodAsync** attende per un tempo indefinito che un evento globale sia segnalato quando viene chiamato [**IPortableDeviceServiceMethodCallback::OnComplete.**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethodcallback-oncomplete)

Il codice seguente usa il **metodo InvokeMethodsAsync.**


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



La funzione helper **InvokeMethodAsync** esegue le operazioni seguenti per ogni metodo richiamato:

-   Crea un handle di evento globale monitorato per determinare il completamento del metodo.
-   Crea un **oggetto CMethodCallback** fornito come argomento a [**IPortableDeviceServiceMethods:InvokeAsync.**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invokeasync)
-   Chiama il **metodo IPortableDeviceServiceMethods::InvokeAsync** per richiamare il metodo specificato.
-   Monitora l'handle di evento globale per il completamento.
-   Esegue la pulizia.

La **classe CMethodCallback** illustra come un'applicazione può implementare [**IPortableDeviceServiceMethodCallback.**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback) L'implementazione **di OnComplete** in questa classe segnala un evento per notificare all'applicazione che il metodo del servizio è stato completato. Oltre al metodo **OnComplete,** questa classe implementa **AddRef**, **QueryInterface** e **Release**, che vengono usati per mantenere il conteggio dei riferimenti dell'oggetto e le interfacce implementate.


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

 

 
