---
description: SafeRelease
ms.assetid: 2e9af7bc-f478-4a9c-b28f-b0a72fa9ec75
title: SafeRelease
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd0661b8515c1d8a79c81eef19f49cf8996fcbf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309013"
---
# <a name="saferelease"></a>SafeRelease


Molti degli esempi di codice di questa documentazione usano la funzione seguente per rilasciare i puntatori di interfaccia COM.


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

 

Questa funzione rilascia il puntatore *PPT* e lo imposta su **null**.

Un'altra opzione consiste nell'usare una classe di puntatore intelligente, ad esempio **CComPtr**, definita nella Active Template Library (ATL).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Media Foundation](about-the-media-foundation-sdk.md)
</dt> <dt>

[**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)
</dt> </dl>

 

 
