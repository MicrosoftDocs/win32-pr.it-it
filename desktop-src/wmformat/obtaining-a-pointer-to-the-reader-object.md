---
title: Acquisizione di un puntatore all'oggetto Reader (Windows Media Format 11 SDK)
description: Recupero di un puntatore all'oggetto Reader
ms.assetid: 70696ffc-2612-460d-b445-f200ba85d3c7
keywords:
- Windows Media Format SDK, DirectShow
- Windows Media Format SDK, oggetti Reader
- Windows Media Format SDK, interfaccia IWMReaderAdvanced2
- ASF (Advanced Systems Format), DirectShow
- ASF (Advanced Systems Format), DirectShow
- ASF (Advanced Systems Format), oggetti Reader
- ASF (formato avanzato dei sistemi), oggetti Reader
- Advanced Systems Format (ASF), interfaccia IWMReaderAdvanced2
- ASF (formato avanzato dei sistemi), interfaccia IWMReaderAdvanced2
- DirectShow, oggetti Reader
- DirectShow, puntatori a oggetti Reader
- DirectShow, interfaccia IWMReaderAdvanced2
- oggetti Reader, recupero di puntatori
- flussi, oggetti Reader
- flussi, puntatori a oggetti Reader
- IWMReaderAdvanced2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63e0bb6611ba1d4e3c41fb2c00a68dd9c898505f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104340103"
---
# <a name="obtaining-a-pointer-to-the-reader-object-windows-media-format-11-sdk"></a><span data-ttu-id="01302-119">Acquisizione di un puntatore all'oggetto Reader (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="01302-119">Obtaining a Pointer to the Reader Object (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="01302-120">In alcuni casi, ad esempio quando si determinano le estensioni di unità dati impostate in un determinato flusso, potrebbe essere necessario accedere direttamente all' [oggetto Reader](reader-object.md) di Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="01302-120">In certain cases, for example when determining which data unit extensions are set on a given stream, you may need to access the [Reader Object](reader-object.md) of the Windows Media Format SDK directly.</span></span> <span data-ttu-id="01302-121">La funzione seguente mostra come ottenere l'interfaccia [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) sull'oggetto Reader stesso:</span><span class="sxs-lookup"><span data-stu-id="01302-121">The following function shows how to obtain the [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) interface on the Reader Object itself:</span></span>


```C++
HRESULT GetReaderAdvanced (IGraphBuilder *pGraph, IWMReaderAdvanced2** pReaderAdvanced2) 
{
  // We use CComPtr's to avoid headaches at cleanup time
  CComPtr<IEnumFilters> pEnum;
  CComPtr<IBaseFilter> pFilter;
  ULONG cFetched;

  HRESULT hr = pGraph->EnumFilters(&pEnum);
  if (FAILED(hr)) 
  {
    return hr;
  }

  while(pEnum->Next(1, &pFilter, &cFetched) == S_OK)
  {
    IWMHeaderInfo *pHI = NULL;
    // Only the WM ASF Reader will have interface. This filter should be
    // the first one returned in this loop.
    hr = pFilter->QueryInterface(__uuidof(IWMHeaderInfo), (void**)&pHI);
    if (SUCCEEDED(hr))
    {
      // We use the IWMDRMReader interface only as a way to get
      // a pointer to the Reader Object.
      CComPtr<IWMDRMReader> pWMDRMReader;
      CComQIPtr<IServiceProvider, &IID_IServiceProvider> pSP;

      hr = pHI->QueryInterface(__uuidof(IServiceProvider), (void**)&pSP);
      if (!pSP)
      {
        return E_NOINTERFACE;
      }
      
      hr = pSP->QueryService(IID_IWMDRMReader, IID_IWMDRMReader, (void **) &pWMDRMReader);
      if (FAILED(hr))
      {
        return hr;
      }

      CComQIPtr<IWMReaderAdvanced2, &IID_IWMReaderAdvanced2> pRA2(pWMDRMReader);
      if (pRA2)
      {
        *pReaderAdvanced2 = pRA2.Detach();
        return S_OK;
      }

    }
    pFilter.Release();
  }
  
  //if we get here, we didn't find the WM ASF Reader
  return E_FAIL;
}
```



 

 




