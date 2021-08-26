---
description: Annullamento della registrazione di un filtro
ms.assetid: 5459d172-7dfe-4786-bcf2-031e441e30a2
title: Annullamento della registrazione di un filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e26f2d524ff501fcff1db645c9ccdf1a1c9c80c4056af1af206b996f801207
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049681"
---
# <a name="unregistering-a-filter"></a>Annullamento della registrazione di un filtro

Per annullare la registrazione di un filtro, **implementare la funzione DllUnregisterServer.** All'interno di questa funzione chiamare DirectShow [**funzione AMovieDllRegisterServer2**](amoviedllregisterserver2.md) con il valore **FALSE**. Se al momento della registrazione del filtro è stato chiamato **IFilterMapper2::RegisterFilter,** chiamare qui il metodo [**IFilterMapper2::UnregisterFilter.**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-unregisterfilter)

L'esempio seguente illustra come annullare la registrazione di un filtro:


```C++
STDAPI DllUnregisterServer()
{
    HRESULT hr;
    IFilterMapper2 *pFM2 = NULL;

    hr = AMovieDllRegisterServer2(FALSE);
    if (FAILED(hr))
        return hr;
 
    hr = CoCreateInstance(CLSID_FilterMapper2, NULL, CLSCTX_INPROC_SERVER,
            IID_IFilterMapper2, (void **)&pFM2);

    if (FAILED(hr))
        return hr;

    hr = pFM2->UnregisterFilter(&CLSID_VideoCompressorCategory, 
            g_wszName, CLSID_SomeFilter);

    pFM2->Release();
    return hr;
}
```



 

 



