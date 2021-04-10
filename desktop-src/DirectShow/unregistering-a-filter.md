---
description: Annullamento della registrazione di un filtro
ms.assetid: 5459d172-7dfe-4786-bcf2-031e441e30a2
title: Annullamento della registrazione di un filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d161b7d1f169b84ba43ac734bf01708a37eb700a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883109"
---
# <a name="unregistering-a-filter"></a>Annullamento della registrazione di un filtro

Per annullare la registrazione di un filtro, implementare la funzione **DllUnregisterServer** . All'interno di questa funzione, chiamare la funzione DirectShow [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) con il valore **false**. Se è stato chiamato **IFilterMapper2:: RegisterFilter** al momento della registrazione del filtro, chiamare il metodo [**IFilterMapper2:: UnregisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-unregisterfilter) qui.

Nell'esempio seguente viene illustrato come annullare la registrazione di un filtro:


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



 

 



