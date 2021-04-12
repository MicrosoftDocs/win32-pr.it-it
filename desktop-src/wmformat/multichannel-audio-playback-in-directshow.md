---
title: Riproduzione audio multicanale in DirectShow
description: Riproduzione audio multicanale in DirectShow
ms.assetid: 5123854a-0f1f-40f4-bf57-47622b91103f
keywords:
- Windows Media Format SDK, DirectShow
- Windows Media Format SDK, riproduzione audio multicanale
- Windows Media Format SDK, riproduzione audio
- ASF (Advanced Systems Format), DirectShow
- ASF (Advanced Systems Format), DirectShow
- ASF (Advanced Systems Format), riproduzione audio multicanale
- ASF (Advanced Systems Format), riproduzione audio multicanale
- ASF (Advanced Systems Format), riproduzione audio
- ASF (formato avanzato dei sistemi), riproduzione audio
- DirectShow, riproduzione audio multicanale
- DirectShow, riproduzione audio
- audio multicanale, riproduzione
- riproduzione audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d44c6eec473c8bbbff81d35f4127d5d132d0b6cd
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104398650"
---
# <a name="multichannel-audio-playback-in-directshow"></a><span data-ttu-id="6101f-116">Riproduzione audio multicanale in DirectShow</span><span class="sxs-lookup"><span data-stu-id="6101f-116">Multichannel Audio Playback in DirectShow</span></span>

<span data-ttu-id="6101f-117">Per riprodurre un file di Windows Media Audio multicanale in DirectShow, è necessario impostare la \_ Proprietà "HIRESOUTPUT" direttamente nel decodificatore dopo che è stata connessa al lettore WM ASF.</span><span class="sxs-lookup"><span data-stu-id="6101f-117">To play back a multichannel Windows Media Audio file in DirectShow, you must set the "\_HIRESOUTPUT" property directly on the decoder after it has been connected to the WM ASF Reader.</span></span> <span data-ttu-id="6101f-118">Non è necessaria alcuna configurazione dell'oggetto Reader.</span><span class="sxs-lookup"><span data-stu-id="6101f-118">No configuration of the Reader Object is necessary.</span></span> <span data-ttu-id="6101f-119">Tuttavia, per lavorare direttamente con DMO, è necessario wmcodecconst. h dal [codice di esempio per l'uso del pacchetto di download Windows Media audio e interfacce codec video](https://www.microsoft.com/downloads/details.aspx?FamilyId=92490D8A-4F2E-46F1-8835-B1D987B3C985&displaylang=en) .</span><span class="sxs-lookup"><span data-stu-id="6101f-119">However, to work with the DMO directly, you need wmcodecconst.h from the [Sample Code for Using the Windows Media Audio and Video Codec Interfaces](https://www.microsoft.com/downloads/details.aspx?FamilyId=92490D8A-4F2E-46F1-8835-B1D987B3C985&displaylang=en) download package.</span></span>

<span data-ttu-id="6101f-120">**Nota** Questa procedura di configurazione è supportata solo per i file non protetti da Rights Management digitali.</span><span class="sxs-lookup"><span data-stu-id="6101f-120">**Note** This configuration procedure is supported only for files that are not protected by Digital Rights Management.</span></span>

<span data-ttu-id="6101f-121">I passaggi di base per abilitare l'output multicanale sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="6101f-121">The basic steps to enable multichannel output are as follows:</span></span>

1.  <span data-ttu-id="6101f-122">Chiamare RenderFile per creare il grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="6101f-122">Call RenderFile to create the filter graph.</span></span>
2.  <span data-ttu-id="6101f-123">Ottenere un puntatore al filtro del wrapper DMO</span><span class="sxs-lookup"><span data-stu-id="6101f-123">Obtain a pointer to the DMO Wrapper filter</span></span>
3.  <span data-ttu-id="6101f-124">Disconnettere il wrapper DMO dal renderer audio</span><span class="sxs-lookup"><span data-stu-id="6101f-124">Disconnect the DMO Wrapper from the Audio Renderer</span></span>
4.  <span data-ttu-id="6101f-125">Impostare la \_ Proprietà "HIRESOUTPUT" nel decodificatore.</span><span class="sxs-lookup"><span data-stu-id="6101f-125">Set the "\_HIRESOUTPUT" property on the decoder.</span></span>
5.  <span data-ttu-id="6101f-126">Riconnettere il wrapper DMO e il renderer audio.</span><span class="sxs-lookup"><span data-stu-id="6101f-126">Reconnect the DMO Wrapper and the Audio Renderer.</span></span>
6.  <span data-ttu-id="6101f-127">Eseguire il grafo.</span><span class="sxs-lookup"><span data-stu-id="6101f-127">Run the graph.</span></span>

<span data-ttu-id="6101f-128">I frammenti di codice seguenti illustrano questi passaggi.</span><span class="sxs-lookup"><span data-stu-id="6101f-128">The following code snippets demonstrate these steps.</span></span> <span data-ttu-id="6101f-129">(Per semplicità è stato omesso tutto il controllo degli errori.</span><span class="sxs-lookup"><span data-stu-id="6101f-129">(All error checking has been omitted for the sake of simplicity.</span></span> <span data-ttu-id="6101f-130">Se si utilizza questo codice in un'applicazione, è necessario aggiungere routine di gestione degli errori appropriate.</span><span class="sxs-lookup"><span data-stu-id="6101f-130">You should add proper error handling routines if you use this code in an application.)</span></span>


```C++
    ...
    //ENABLE MULTICHANNEL OUTPUT
    //Render the file
    hr = m_pGraphBuilder->RenderFile(wFileName, NULL);

    // Get pointers to the two DMO Wrapper interfaces we need.
    // (Function bodies provided at the end of this snippet.)
    hr = GetDMOWrapper(pGB, &m_pDMOBaseFilter, &m_pWrapper); 

    //Disconnect the DMO Wrapper from the Audio Renderer
    CComPtr<IPin> pDMOOut;
    CComPtr<IPin> pRendererIn;
    hr = GetPin(m_pDMOBaseFilter, PINDIR_OUTPUT, &pDMOOut);
    hr = pDMOOut->ConnectedTo(&pRendererIn);
    hr = pDMOOut->Disconnect();
    hr = pRendererIn->Disconnect();

    //Set the property on the DMO
    VARIANT varg;
    ::VariantInit(&varg);
    varg.vt    = VT_BOOL;
    varg.boolVal = TRUE;
    CComQIPtr<IMediaObject, &IID_IMediaObject> pMediaObject(m_pWrapper);
    CComQIPtr<IPropertyBag, &IID_IPropertyBag> pPropertyBag(pMediaObject);
    hr = pPropertyBag->Write(g_wszWMACHiResOutput, &varg);

    // Reconnect the DMO Wrapper and the Audio Renderer
    hr = pGB->Connect(pDMOOut, pRendererIn);
    //END MULTICHANNEL (now the graph can be run)
...

```



<span data-ttu-id="6101f-131">Le funzioni GetDMOWrapper e GetPin del frammento di codice precedente vengono implementate nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="6101f-131">The GetDMOWrapper and GetPin functions from the previous code snippet are implemented as follows:</span></span>


```C++
// In this example, the IBaseFilter and IDMOWrapperFilter interfaces are
// declared  at global scope
HRESULT GetDMOWrapper (IFilterGraph *pGraph, IBaseFilter** m_pDMOBaseFilter, IDMOWrapperFilter** m_pWrapper) 
{
    CComPtr<IEnumFilters> pEnum;
    CComPtr<IBaseFilter> pFilter;
    ULONG cFetched;

    HRESULT hr = pGraph->EnumFilters(&pEnum);
    if (FAILED(hr)) return hr;

    while(pEnum->Next(1, &pFilter, &cFetched) == S_OK)
    {
        // If we find the IDMOWrapperFilter interface, that means we 
        // have the DMO Wrapper filter. Store both interfaces for future use.
        CComPtr<IDMOWrapperFilter> pWrapper;
        hr = pFilter->QueryInterface(IID_IDMOWrapperFilter, (void**) &pWrapper);
        if (SUCCEEDED(hr))
        {
            *m_pWrapper = pWrapper.Detach();
            *m_pDMOBaseFilter = pFilter.Detach();
            return S_OK;
        }

        pFilter.Release();
    }

    return E_FAIL;
}

HRESULT GetPin(IBaseFilter *pFilter, PIN_DIRECTION PinDir, IPin** ppPin)
{
    CComPtr<IEnumPins>  pEnum;
    CComPtr<IPin>       pPin;

         HRESULT hr = pFilter->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        return hr;
    }
    while(pEnum->Next(1, &pPin, 0) == S_OK)
    {
        PIN_DIRECTION PinDirThis;
        pPin->QueryDirection(&PinDirThis);
        if (PinDir == PinDirThis)
        {
            *ppPin = pPin.Detach();
            return S_OK;
        }
        pPin.Release();
    }
    
    return E_FAIL;
}
```



 

 




