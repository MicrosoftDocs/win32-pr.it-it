---
description: Distribuzione della fine del flusso
ms.assetid: 23afdb2e-93b0-4a74-94bd-e38eb82a5995
title: Distribuzione della fine del flusso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2bd80d186bd62e6360fa1600f4ba970281315aa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876086"
---
# <a name="delivering-the-end-of-stream"></a><span data-ttu-id="a2721-103">Distribuzione della fine del flusso</span><span class="sxs-lookup"><span data-stu-id="a2721-103">Delivering the End of Stream</span></span>

<span data-ttu-id="a2721-104">Quando il pin di input riceve una notifica di fine flusso, propaga la chiamata downstream.</span><span class="sxs-lookup"><span data-stu-id="a2721-104">When the input pin receives an end-of-stream notification, it propagates the call downstream.</span></span> <span data-ttu-id="a2721-105">Anche tutti i filtri downstream che ricevono i dati da questo pin di input devono ottenere la notifica di fine del flusso.</span><span class="sxs-lookup"><span data-stu-id="a2721-105">Any downstream filters that receive data from this input pin should also get the end-of-stream notification.</span></span> <span data-ttu-id="a2721-106">Anche in questo caso, eseguire il blocco di flusso e non il blocco del filtro.</span><span class="sxs-lookup"><span data-stu-id="a2721-106">Again, take the streaming lock and not the filter lock.</span></span> <span data-ttu-id="a2721-107">Se il filtro contiene dati in sospeso non ancora recapitati, il filtro deve recapitarlo adesso, prima di inviare la notifica di fine flusso.</span><span class="sxs-lookup"><span data-stu-id="a2721-107">If the filter has pending data that was not yet delivered, the filter should deliver it now, before it sends the end-of-stream notification.</span></span> <span data-ttu-id="a2721-108">Non deve inviare dati dopo la fine del flusso.</span><span class="sxs-lookup"><span data-stu-id="a2721-108">It should not send any data after the end of the stream.</span></span>


```C++
HRESULT CMyInputPin::EndOfStream()
{
    CAutoLock lock_it(&m_csReceive);

    /* If the pin has not delivered all of the data in the stream 
       (based on what it received previously), do so now.  */

    // Propagate EndOfStream call downstream, via your output pin(s).
    for (each output pin)
    {    
        hr = pOutputPin->DeliverEndOfStream();
    }
    return S_OK;
}
```



<span data-ttu-id="a2721-109">Il metodo [**CBaseOutputPin::D eliverendofstream**](cbaseoutputpin-deliverendofstream.md) chiama [**Ipin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) sul pin di input downstream.</span><span class="sxs-lookup"><span data-stu-id="a2721-109">The [**CBaseOutputPin::DeliverEndOfStream**](cbaseoutputpin-deliverendofstream.md) method calls [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) on the downstream input pin.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2721-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a2721-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2721-111">Thread e sezioni critiche</span><span class="sxs-lookup"><span data-stu-id="a2721-111">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)
</dt> </dl>

 

 



