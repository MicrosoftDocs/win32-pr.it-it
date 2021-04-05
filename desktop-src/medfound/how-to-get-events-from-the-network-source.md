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
# <a name="how-to-get-events-from-the-network-source"></a><span data-ttu-id="82ebb-103">Come ottenere gli eventi dall'origine di rete</span><span class="sxs-lookup"><span data-stu-id="82ebb-103">How to Get Events from the Network Source</span></span>

<span data-ttu-id="82ebb-104">Il resolver di origine consente a un'applicazione di creare un'origine di rete e di aprire una connessione a un URL specifico.</span><span class="sxs-lookup"><span data-stu-id="82ebb-104">The source resolver enables an application to create a network source and open a connection to a specific URL.</span></span> <span data-ttu-id="82ebb-105">L'origine di rete genera eventi per contrassegnare l'inizio e la fine dell'operazione asincrona di apertura di una connessione.</span><span class="sxs-lookup"><span data-stu-id="82ebb-105">The network source raises events to mark the beginning and the end of the asynchronous operation of opening a connection.</span></span> <span data-ttu-id="82ebb-106">Un'applicazione può registrarsi per questi eventi usando l'interfaccia [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) .</span><span class="sxs-lookup"><span data-stu-id="82ebb-106">An application can register for these events by using the [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) interface.</span></span>

<span data-ttu-id="82ebb-107">Questa interfaccia espone il metodo [**IMFSourceOpenMonitor:: OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) chiamato direttamente dall'origine di rete quando l'URL viene aperto in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="82ebb-107">This interface exposes the [**IMFSourceOpenMonitor::OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) method that the network source calls directly when it opens the URL asynchronously.</span></span> <span data-ttu-id="82ebb-108">L'origine di rete invia una notifica all'applicazione quando inizia ad aprire l'URL generando l'evento [MEConnectStart](meconnectstart.md) .</span><span class="sxs-lookup"><span data-stu-id="82ebb-108">The network source notifies the application when it starts opening the URL by raising the [MEConnectStart](meconnectstart.md) event.</span></span> <span data-ttu-id="82ebb-109">L'origine di rete genera quindi l'evento [MEConnectEnd](meconnectend.md) al completamento dell'operazione di apertura.</span><span class="sxs-lookup"><span data-stu-id="82ebb-109">The network source then raises the [MEConnectEnd](meconnectend.md) event when it completes the open operation.</span></span>

> [!Note]  
> <span data-ttu-id="82ebb-110">Per inviare questi eventi all'applicazione, l'origine di rete non usa l'interfaccia [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) perché questi eventi vengono generati prima della creazione dell'origine di rete.</span><span class="sxs-lookup"><span data-stu-id="82ebb-110">To send these events to the application, the network source does not use the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface because these events are raised before the network source is created.</span></span> <span data-ttu-id="82ebb-111">L'applicazione può ottenere tutti gli altri eventi di origine della rete usando l'interfaccia **IMFMediaEventGenerator** della sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="82ebb-111">The application can get all other network source events by using the Media Session's **IMFMediaEventGenerator** interface.</span></span>

 

## <a name="to-get-events-from-the-network-source"></a><span data-ttu-id="82ebb-112">Per ottenere gli eventi dall'origine di rete</span><span class="sxs-lookup"><span data-stu-id="82ebb-112">To get events from the network source</span></span>

1.  <span data-ttu-id="82ebb-113">Implementare l'interfaccia [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) .</span><span class="sxs-lookup"><span data-stu-id="82ebb-113">Implement the [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) interface.</span></span> <span data-ttu-id="82ebb-114">Nell'implementazione del metodo [**IMFSourceOpenMonitor:: OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="82ebb-114">In your implementation of [**IMFSourceOpenMonitor::OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) method, do the following:</span></span>
    1.  <span data-ttu-id="82ebb-115">Ottenere lo stato dell'evento chiamando [**IMFMediaEvent:: GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus).</span><span class="sxs-lookup"><span data-stu-id="82ebb-115">Get the event status by calling [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus).</span></span> <span data-ttu-id="82ebb-116">Questo metodo indica se l'operazione che ha attivato l'evento, ad esempio una chiamata al metodo del resolver di origine, ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="82ebb-116">This method indicates whether the operation that triggered the event, such as a source resolver method call, succeeded.</span></span> <span data-ttu-id="82ebb-117">Se l'operazione ha esito negativo, lo stato è un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="82ebb-117">If the operation is not successful, the status is a failure code.</span></span>
    2.  <span data-ttu-id="82ebb-118">Elaborare l'evento in base al tipo di evento: [MEConnectStart](meconnectstart.md) o [MEConnectEnd](meconnectend.md), che l'applicazione può ottenere chiamando [**IMFMediaEvent:: GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype).</span><span class="sxs-lookup"><span data-stu-id="82ebb-118">Process the event based on the event type: [MEConnectStart](meconnectstart.md) or [MEConnectEnd](meconnectend.md), which the application can get by calling [**IMFMediaEvent::GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype).</span></span>
2.  <span data-ttu-id="82ebb-119">Configurare una coppia chiave-valore in un oggetto archivio proprietà per archiviare un puntatore all'implementazione di [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) descritta nel passaggio 1.</span><span class="sxs-lookup"><span data-stu-id="82ebb-119">Configure a key-value pair in a property store object to store a pointer to the [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) implementation described in step 1.</span></span>
    1.  <span data-ttu-id="82ebb-120">Creare un oggetto archivio proprietà chiamando la funzione **PSCreateMemoryPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="82ebb-120">Create a property store object by calling the **PSCreateMemoryPropertyStore** function.</span></span>
    2.  <span data-ttu-id="82ebb-121">Impostare la proprietà [**MFPKEY \_ SourceOpenMonitor**](mfpkey-sourceopenmonitor-property.md) in una struttura **PropertyKey** .</span><span class="sxs-lookup"><span data-stu-id="82ebb-121">Set the [**MFPKEY\_SourceOpenMonitor**](mfpkey-sourceopenmonitor-property.md) property in a **PROPERTYKEY** structure.</span></span>
    3.  <span data-ttu-id="82ebb-122">Specificare il \_ valore dei dati del tipo sconosciuto VT in una struttura **PROPVARIANT** impostando il puntatore **IUnknown** sull'implementazione dell'applicazione dell'interfaccia [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) .</span><span class="sxs-lookup"><span data-stu-id="82ebb-122">Provide the VT\_UNKNOWN type data value in a **PROPVARIANT** structure by setting the **IUnknown** pointer to the application's implementation of the [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) interface.</span></span>
    4.  <span data-ttu-id="82ebb-123">Impostare la coppia chiave-valore nell'archivio delle proprietà chiamando **IPropertyStore:: SetValue**.</span><span class="sxs-lookup"><span data-stu-id="82ebb-123">Set the key-value pair in the property store by calling **IPropertyStore::SetValue**.</span></span>
3.  <span data-ttu-id="82ebb-124">Passare il puntatore dell'archivio delle proprietà ai metodi del resolver di origine che l'applicazione usa per creare l'origine di rete, ad esempio [**IMFSourceResolver:: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) e altri.</span><span class="sxs-lookup"><span data-stu-id="82ebb-124">Pass the property store pointer to the source resolver methods that the application is using to create the network source, such as [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) and others.</span></span>

## <a name="example"></a><span data-ttu-id="82ebb-125">Esempio</span><span class="sxs-lookup"><span data-stu-id="82ebb-125">Example</span></span>

<span data-ttu-id="82ebb-126">Nell'esempio seguente viene illustrato come implementare l'interfaccia [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) per ottenere gli eventi dall'origine di rete.</span><span class="sxs-lookup"><span data-stu-id="82ebb-126">The following example shows how to implement the [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) interface to get events from the network source.</span></span>


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



<span data-ttu-id="82ebb-127">Nell'esempio seguente viene illustrato come impostare la proprietà [**MFPKEY \_ SourceOpenMonitor**](mfpkey-sourceopenmonitor-property.md) nell'origine della rete quando si apre l'URL:</span><span class="sxs-lookup"><span data-stu-id="82ebb-127">The following example shows how to set the [**MFPKEY\_SourceOpenMonitor**](mfpkey-sourceopenmonitor-property.md) property on the network source when you open the URL:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="82ebb-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="82ebb-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82ebb-129">Rete in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="82ebb-129">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 



