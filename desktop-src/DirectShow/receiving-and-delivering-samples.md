---
description: Ricezione e distribuzione di esempi
ms.assetid: 92954b40-1424-4dee-997c-fc41089b7fa5
title: Ricezione e distribuzione di esempi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a364743e0dfc201d419a61fa4c88bde686976d6b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876382"
---
# <a name="receiving-and-delivering-samples"></a><span data-ttu-id="145dc-103">Ricezione e distribuzione di esempi</span><span class="sxs-lookup"><span data-stu-id="145dc-103">Receiving and Delivering Samples</span></span>

<span data-ttu-id="145dc-104">Nello pseudocodice seguente viene illustrato come implementare il metodo **IMemInput:: Receive** :</span><span class="sxs-lookup"><span data-stu-id="145dc-104">The following pseudocode shows how to implement the **IMemInput::Receive** method:</span></span>


```C++
HRESULT CMyInputPin::Receive(IMediaSample *pSample)
{
    CAutoLock cObjectLock(&m_csReceive);

    // Perhaps the filter needs to wait on something.
    WaitForSingleObject(m_hSomeEventThatReceiveNeedsToWaitOn, INFINITE);

    // Before using resources, make sure it is safe to proceed. Do not
    // continue if the base-class method returns anything besides S_OK.
    hr = CBaseInputPin::Receive(pSample);
    if (hr != S_OK) 
    {
        return hr;
    }

    /* It is safe to use resources allocated in Active and Pause. */

    // Deliver sample(s), via your output pin(s).
    for (each output pin)
        pOutputPin->Deliver(pSample);

    return hr;
}
```



<span data-ttu-id="145dc-105">Il metodo **Receive** utilizza il blocco di flusso, non il blocco del filtro.</span><span class="sxs-lookup"><span data-stu-id="145dc-105">The **Receive** method holds the streaming lock, not the filter lock.</span></span> <span data-ttu-id="145dc-106">Il filtro potrebbe dover attendere un determinato evento prima di poter elaborare i dati, come illustrato nella chiamata a **WaitForSingleObject**.</span><span class="sxs-lookup"><span data-stu-id="145dc-106">The filter might need to wait on some event before it can process the data, shown here by the call to **WaitForSingleObject**.</span></span> <span data-ttu-id="145dc-107">Non tutti i filtri dovranno eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="145dc-107">Not every filter will need to do this.</span></span> <span data-ttu-id="145dc-108">Il metodo [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) verifica alcune condizioni di flusso generali.</span><span class="sxs-lookup"><span data-stu-id="145dc-108">The [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method verifies some general streaming conditions.</span></span> <span data-ttu-id="145dc-109">Restituisce \_ \_ lo stato VFW E errato \_ se il filtro viene arrestato, S \_ false se il filtro sta scaricando e così via.</span><span class="sxs-lookup"><span data-stu-id="145dc-109">It returns VFW\_E\_WRONG\_STATE if the filter is stopped, S\_FALSE if the filter is flushing, and so forth.</span></span> <span data-ttu-id="145dc-110">Qualsiasi codice restituito diverso da S \_ OK indica che il metodo **Receive** deve restituire immediatamente e non elaborare l'esempio.</span><span class="sxs-lookup"><span data-stu-id="145dc-110">Any return code other than S\_OK indicates that the **Receive** method should return immediately and not process the sample.</span></span>

<span data-ttu-id="145dc-111">Dopo l'elaborazione dell'esempio, recapitarlo al filtro downstream chiamando [**CBaseOutputPin::D Eliver**](cbaseoutputpin-deliver.md).</span><span class="sxs-lookup"><span data-stu-id="145dc-111">After the sample is processed, deliver it to the downstream filter by calling [**CBaseOutputPin::Deliver**](cbaseoutputpin-deliver.md).</span></span> <span data-ttu-id="145dc-112">Questo metodo helper chiama **IMemInputPin:: Receive** sul pin di input downstream.</span><span class="sxs-lookup"><span data-stu-id="145dc-112">This helper method calls **IMemInputPin::Receive** on the downstream input pin.</span></span> <span data-ttu-id="145dc-113">Un filtro può recapitare campioni a diversi pin.</span><span class="sxs-lookup"><span data-stu-id="145dc-113">A filter might deliver samples to several pins.</span></span>

 

 



