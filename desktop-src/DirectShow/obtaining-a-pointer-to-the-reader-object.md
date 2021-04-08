---
description: Recupero di un puntatore all'oggetto Reader
ms.assetid: d1292e2f-bd0e-4961-a6fa-8cdaeb28b692
title: Acquisizione di un puntatore all'oggetto Reader (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3be22a22581c8f262ac4c6898271ebccb53a0e4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745599"
---
# <a name="obtaining-a-pointer-to-the-reader-object-directshow"></a><span data-ttu-id="d9904-103">Acquisizione di un puntatore all'oggetto Reader (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="d9904-103">Obtaining a Pointer to the Reader Object (DirectShow)</span></span>

<span data-ttu-id="d9904-104">In alcuni casi, ad esempio quando si determinano le estensioni di unità dati impostate in un determinato flusso, potrebbe essere necessario accedere direttamente all'oggetto Reader di Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="d9904-104">In certain cases, for example when determining which data unit extensions are set on a given stream, you may need to access the Reader Object of the Windows Media Format SDK directly.</span></span> <span data-ttu-id="d9904-105">La funzione seguente mostra come ottenere l'interfaccia [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) sull'oggetto Reader stesso:</span><span class="sxs-lookup"><span data-stu-id="d9904-105">The following function shows how to obtain the [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) interface on the Reader Object itself:</span></span>


```C++
#include <wmsdk.h>
HRESULT GetReaderAdvanced(IGraphBuilder *pGraph, IWMReaderAdvanced2** pReaderAdvanced2) 
{
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
    // Only the WM ASF Reader will have interface. 
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



## <a name="related-topics"></a><span data-ttu-id="d9904-106">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d9904-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9904-107">Lettura di file ASF in DirectShow</span><span class="sxs-lookup"><span data-stu-id="d9904-107">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 
