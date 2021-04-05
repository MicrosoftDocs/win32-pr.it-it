---
description: Come ottenere gli eventi dall'origine di rete
ms.assetid: 46869f52-323c-41ec-95f7-e7e5d177b782
title: Come ottenere gli eventi dall'origine di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 100241b069ae8976c20c68b6055571d5ff1e5c1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753583"
---
# <a name="how-to-get-events-from-the-network-source"></a>Come ottenere gli eventi dall'origine di rete

Il resolver di origine consente a un'applicazione di creare un'origine di rete e di aprire una connessione a un URL specifico. L'origine di rete genera eventi per contrassegnare l'inizio e la fine dell'operazione asincrona di apertura di una connessione. Un'applicazione può registrarsi per questi eventi usando l'interfaccia [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) .

Questa interfaccia espone il metodo [**IMFSourceOpenMonitor:: OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) chiamato direttamente dall'origine di rete quando l'URL viene aperto in modo asincrono. L'origine di rete invia una notifica all'applicazione quando inizia ad aprire l'URL generando l'evento [MEConnectStart](meconnectstart.md) . L'origine di rete genera quindi l'evento [MEConnectEnd](meconnectend.md) al completamento dell'operazione di apertura.

> [!Note]  
> Per inviare questi eventi all'applicazione, l'origine di rete non usa l'interfaccia [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) perché questi eventi vengono generati prima della creazione dell'origine di rete. L'applicazione può ottenere tutti gli altri eventi di origine della rete usando l'interfaccia **IMFMediaEventGenerator** della sessione multimediale.

 

## <a name="to-get-events-from-the-network-source"></a>Per ottenere gli eventi dall'origine di rete

1.  Implementare l'interfaccia [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) . Nell'implementazione del metodo [**IMFSourceOpenMonitor:: OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) eseguire le operazioni seguenti:
    1.  Ottenere lo stato dell'evento chiamando [**IMFMediaEvent:: GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus). Questo metodo indica se l'operazione che ha attivato l'evento, ad esempio una chiamata al metodo del resolver di origine, ha avuto esito positivo. Se l'operazione ha esito negativo, lo stato è un codice di errore.
    2.  Elaborare l'evento in base al tipo di evento: [MEConnectStart](meconnectstart.md) o [MEConnectEnd](meconnectend.md), che l'applicazione può ottenere chiamando [**IMFMediaEvent:: GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype).
2.  Configurare una coppia chiave-valore in un oggetto archivio proprietà per archiviare un puntatore all'implementazione di [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) descritta nel passaggio 1.
    1.  Creare un oggetto archivio proprietà chiamando la funzione **PSCreateMemoryPropertyStore** .
    2.  Impostare la proprietà [**MFPKEY \_ SourceOpenMonitor**](mfpkey-sourceopenmonitor-property.md) in una struttura **PropertyKey** .
    3.  Specificare il \_ valore dei dati del tipo sconosciuto VT in una struttura **PROPVARIANT** impostando il puntatore **IUnknown** sull'implementazione dell'applicazione dell'interfaccia [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) .
    4.  Impostare la coppia chiave-valore nell'archivio delle proprietà chiamando **IPropertyStore:: SetValue**.
3.  Passare il puntatore dell'archivio delle proprietà ai metodi del resolver di origine che l'applicazione usa per creare l'origine di rete, ad esempio [**IMFSourceResolver:: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) e altri.

## <a name="example"></a>Esempio

Nell'esempio seguente viene illustrato come implementare l'interfaccia [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) per ottenere gli eventi dall'origine di rete.


```C++
class CSourceOpenMonitor : public IMFSourceOpenMonitor
{
public:
    CSourceOpenMonitor () : m_cRef(1) { }

    STDMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CSourceOpenMonitor, IMFSourceOpenMonitor),
            { 0 }
        };
        return QISearch(this, qit, riid, ppv);
    }

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        // For thread safety, return a temporary variable.
        return cRef;
    }


    STDMETHODIMP OnSourceEvent(IMFMediaEvent* pEvent)
    {
        MediaEventType eventType = MEUnknown;   // Event type
        HRESULT hrStatus = S_OK;                // Event status

        // Get the event type.
        HRESULT hr = pEvent->GetType(&eventType);

        // Get the event status. If the operation that triggered the event
        // did not succeed, the status is a failure code.
        if (SUCCEEDED(hr))
        {
            hr = pEvent->GetStatus(&hrStatus);
        }

        if (FAILED(hrStatus))
        {
            hr = hrStatus;
        }

        if (SUCCEEDED(hr))
        {
            // Switch on the event type.
            switch(eventType)
            {
                case MEConnectStart:
                    // The application does something. (Not shown.)
                    OutputDebugString(L"Connecting...\n");
                    break;

                case MEConnectEnd:
                    // The application does something. (Not shown.)
                    OutputDebugString(L"Connect End.\n");
                    break;
            }
        }
        else
        {
            // Event failed.
            // The application handled a failure. (Not shown.)
        }
        return S_OK;
    }
private:
    long    m_cRef;
};
```



Nell'esempio seguente viene illustrato come impostare la proprietà [**MFPKEY \_ SourceOpenMonitor**](mfpkey-sourceopenmonitor-property.md) nell'origine della rete quando si apre l'URL:


```C++
HRESULT CreateMediaSourceWithSourceOpenMonitor(
    PCWSTR pszURL, 
    IMFMediaSource **ppSource
    )
{
    IPropertyStore *pConfig = NULL;

    CSourceOpenMonitor *pMonitor = new (std::nothrow) CSourceOpenMonitor();

    if (pMonitor == NULL)
    {
        return E_OUTOFMEMORY;
    }

    // Configure the property store.
    HRESULT hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pConfig));

    if (SUCCEEDED(hr))
    {
        PROPVARIANT var;
        var.vt = VT_UNKNOWN;
        pMonitor->QueryInterface(IID_PPV_ARGS(&var.punkVal));

        hr = pConfig->SetValue(MFPKEY_SourceOpenMonitor, var);

        PropVariantClear(&var);
    }

    // Create the source media source.
    if (SUCCEEDED(hr))
    {
        hr = CreateMediaSource(pszURL, pConfig, ppSource);
    }

    SafeRelease(&pConfig);
    SafeRelease(&pMonitor);

    return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Rete in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 



