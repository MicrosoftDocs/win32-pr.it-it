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
# <a name="getting-buffers"></a><span data-ttu-id="ed060-103">Recupero di buffer</span><span class="sxs-lookup"><span data-stu-id="ed060-103">Getting Buffers</span></span>

<span data-ttu-id="ed060-104">Se il filtro ha un allocatore personalizzato che usa le risorse di filtro, il metodo [**IMemAllocator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) dell'allocatore deve mantenere il blocco di flusso, come per gli altri metodi di streaming:</span><span class="sxs-lookup"><span data-stu-id="ed060-104">If your filter has a custom allocator that uses filter resources, the allocator's [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) method should hold the streaming lock, as with other streaming methods:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="ed060-105">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ed060-105">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed060-106">Thread e sezioni critiche</span><span class="sxs-lookup"><span data-stu-id="ed060-106">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)
</dt> </dl>

 

 



