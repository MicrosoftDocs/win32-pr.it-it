---
description: Recupero di buffer
ms.assetid: be61aee9-41d5-42bc-b905-d0216d301faf
title: Recupero di buffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f727045142b9432da93511ecea1f3238aa24ad213fdc7715f5e2e45a91ab19a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119536901"
---
# <a name="getting-buffers"></a>Recupero di buffer

Se il filtro ha un allocatore personalizzato che usa le risorse di filtro, il metodo [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) dell'allocatore deve contenere il blocco di streaming, come per altri metodi di streaming:


```C++
HRESULT CMyInputAllocator::GetBuffer(
    IMediaSample **ppBuffer,
    REFERENCE_TIME *pStartTime, 
    REFERENCE_TIME *pEndTime,
    DWORD dwFlags)
{
    CAutoLock cObjectLock(&m_csReceive);

    /* Use resources. */

    return CMemAllocator::GetBuffer(ppBuffer, pStartTime, pEndTime, dwFlags);    
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Thread e sezioni critiche](threads-and-critical-sections.md)
</dt> </dl>

 

 



