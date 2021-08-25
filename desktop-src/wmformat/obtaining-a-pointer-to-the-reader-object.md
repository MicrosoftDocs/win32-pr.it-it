---
title: Recupero di un puntatore all'oggetto Reader (Windows Media Format 11 SDK)
description: Informazioni su come ottenere un puntatore all'oggetto Reader di Windows Media Format SDK usando l'interfaccia IWMReaderAdvanced2.
ms.assetid: 70696ffc-2612-460d-b445-f200ba85d3c7
keywords:
- Windows Media Format SDK,DirectShow
- Windows Media Format SDK, oggetti reader
- Windows Media Format SDK, interfaccia IWMReaderAdvanced2
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- Advanced Systems Format (ASF), oggetti reader
- ASF (Advanced Systems Format), oggetti reader
- Advanced Systems Format (ASF),Interfaccia IWMReaderAdvanced2
- AsF (Advanced Systems Format),Interfaccia IWMReaderAdvanced2
- DirectShow,Reader Objects
- DirectShow,puntatori a oggetti Reader
- DirectShow,Interfaccia IWMReaderAdvanced2
- oggetti reader, recupero di puntatori
- flussi, oggetti Reader
- flussi, puntatori a oggetti Reader
- IWMReaderAdvanced2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e4b2829e56d08825234dcefdc4fb1012f48c894419e7c328f10afeb76cb6c4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808051"
---
# <a name="obtaining-a-pointer-to-the-reader-object-windows-media-format-11-sdk"></a>Recupero di un puntatore all'oggetto Reader (Windows Media Format 11 SDK)

In alcuni casi, ad esempio quando si determinano le estensioni delle unità [](reader-object.md) dati impostate in un determinato flusso, potrebbe essere necessario accedere direttamente all'oggetto Lettore di Windows Media Format SDK. La funzione seguente illustra come ottenere [**l'interfaccia IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) nell'oggetto reader stesso:


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



 

 




