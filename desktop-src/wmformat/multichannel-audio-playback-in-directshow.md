---
title: Riproduzione audio multicanale in DirectShow
description: Riproduzione audio multicanale in DirectShow
ms.assetid: 5123854a-0f1f-40f4-bf57-47622b91103f
keywords:
- Windows Media Format SDK,DirectShow
- Windows Media Format SDK, riproduzione audio multicanale
- Windows MEDIA Format SDK, riproduzione audio
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- Advanced Systems Format (ASF), riproduzione audio multicanale
- ASF (Advanced Systems Format), riproduzione audio multicanale
- Advanced Systems Format (ASF), riproduzione audio
- ASF (Advanced Systems Format), riproduzione audio
- DirectShow,riproduzione audio multicanale
- DirectShow,riproduzione audio
- audio multicanale, riproduzione
- riproduzione audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99734ddf32be6e0340e26fafef0f22f1127ec3652cc0db0a9d2e94ce2f694b96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808161"
---
# <a name="multichannel-audio-playback-in-directshow"></a>Riproduzione audio multicanale in DirectShow

Per riprodurre un file audio multimediale Windows multicanale in DirectShow, è necessario impostare la proprietà "HIRESOUTPUT" direttamente nel decodificatore dopo la connessione al lettore \_ ASF WM. Non è necessaria alcuna configurazione dell'oggetto lettore. Tuttavia, per usare direttamente il DMO, è necessario wmcodecconst.h dal pacchetto di download Sample Code for Using the Windows Media Audio and Video Codec Interfaces (Codice di esempio per l'uso del pacchetto di download Windows [Media Audio and Video Codec Interfaces).](https://www.microsoft.com/downloads/details.aspx?FamilyId=92490D8A-4F2E-46F1-8835-B1D987B3C985&displaylang=en)

**Nota** Questa procedura di configurazione è supportata solo per i file non protetti da Rights Management.

I passaggi di base per abilitare l'output multicanale sono i seguenti:

1.  Chiamare RenderFile per creare il grafico dei filtri.
2.  Ottenere un puntatore al filtro DMO Wrapper
3.  Disconnettere DMO wrapper dal renderer audio
4.  Impostare la \_ proprietà "HIRESOUTPUT" nel decodificatore.
5.  Riconnettere il DMO e il renderer audio.
6.  Eseguire il grafo.

I frammenti di codice seguenti illustrano questi passaggi. Tutti i controlli degli errori sono stati omessi per motivi di semplicità. Se si usa questo codice in un'applicazione, è necessario aggiungere routine di gestione degli errori appropriate.


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



Le funzioni GetDMOWrapper e GetPin del frammento di codice precedente vengono implementate nel modo seguente:


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



 

 




