---
description: SafeRelease
ms.assetid: 2e9af7bc-f478-4a9c-b28f-b0a72fa9ec75
title: SafeRelease
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d46359821dd1f7741f6038ddb2f33cec591aacdf1bf9fc7fd3e6004e9d7601e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034869"
---
# <a name="saferelease"></a>SafeRelease


Molti esempi di codice in questa documentazione usano la funzione seguente per rilasciare puntatori a interfaccia COM.


```C++
template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}
```



> [!Note]  
> Questa funzione non è definita in un'intestazione SDK. Per usare questa funzione, è necessario definirla nel proprio codice.

 

Questa funzione rilascia il *puntatore ppT* e lo imposta su **NULL.**

Un'altra opzione è usare una classe puntatore intelligente, ad esempio **CComPtr**, definita nel Active Template Library (ATL).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Media Foundation](about-the-media-foundation-sdk.md)
</dt> <dt>

[**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)
</dt> </dl>

 

 
