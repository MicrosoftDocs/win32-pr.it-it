---
description: Recupero di buffer
ms.assetid: be61aee9-41d5-42bc-b905-d0216d301faf
title: Recupero di buffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecf516096397eca1fce3a023ee4987d8e8feaa4b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520538"
---
# <a name="getting-buffers"></a>Recupero di buffer

Se il filtro ha un allocatore personalizzato che usa le risorse di filtro, il metodo [**IMemAllocator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) dell'allocatore deve mantenere il blocco di flusso, come per gli altri metodi di streaming:


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

 

 



