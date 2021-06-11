---
title: Recupero di un puntatore all'oggetto reader (Windows Media Format 11 SDK)
description: Informazioni su come ottenere un puntatore all'oggetto reader di Windows Media Format SDK usando l'interfaccia IWMReaderAdvanced2.
ms.assetid: 70696ffc-2612-460d-b445-f200ba85d3c7
keywords:
- Windows Media Format SDK,DirectShow
- Windows Media Format SDK, oggetti lettore
- Windows Media Format SDK, interfaccia IWMReaderAdvanced2
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format),DirectShow
- Advanced Systems Format (ASF), oggetti reader
- ASF (Advanced Systems Format), oggetti reader
- Advanced Systems Format (ASF), interfaccia IWMReaderAdvanced2
- ASF (Advanced Systems Format), interfaccia IWMReaderAdvanced2
- DirectShow, oggetti Reader
- DirectShow, puntatori a oggetti reader
- Interfaccia DirectShow,IWMReaderAdvanced2
- oggetti reader, recupero di puntatori
- flussi, oggetti Reader
- flussi,puntatori a oggetti reader
- IWMReaderAdvanced2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd31bd868365b87b38eefd0c0c81e8beafef51c
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989136"
---
# <a name="obtaining-a-pointer-to-the-reader-object-windows-media-format-11-sdk"></a><span data-ttu-id="d1c7b-119">Recupero di un puntatore all'oggetto reader (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="d1c7b-119">Obtaining a Pointer to the Reader Object (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="d1c7b-120">In alcuni casi, ad esempio quando si determinano le estensioni di unità [](reader-object.md) dati impostate in un determinato flusso, potrebbe essere necessario accedere direttamente all'oggetto lettore di Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="d1c7b-120">In certain cases, for example when determining which data unit extensions are set on a given stream, you may need to access the [Reader Object](reader-object.md) of the Windows Media Format SDK directly.</span></span> <span data-ttu-id="d1c7b-121">La funzione seguente illustra come ottenere [**l'interfaccia IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) nell'oggetto reader stesso:</span><span class="sxs-lookup"><span data-stu-id="d1c7b-121">The following function shows how to obtain the [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) interface on the Reader Object itself:</span></span>


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



 

 




