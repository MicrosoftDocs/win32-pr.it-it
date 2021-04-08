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
# <a name="receiving-and-delivering-samples"></a>Ricezione e distribuzione di esempi

Nello pseudocodice seguente viene illustrato come implementare il metodo **IMemInput:: Receive** :


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



Il metodo **Receive** utilizza il blocco di flusso, non il blocco del filtro. Il filtro potrebbe dover attendere un determinato evento prima di poter elaborare i dati, come illustrato nella chiamata a **WaitForSingleObject**. Non tutti i filtri dovranno eseguire questa operazione. Il metodo [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) verifica alcune condizioni di flusso generali. Restituisce \_ \_ lo stato VFW E errato \_ se il filtro viene arrestato, S \_ false se il filtro sta scaricando e così via. Qualsiasi codice restituito diverso da S \_ OK indica che il metodo **Receive** deve restituire immediatamente e non elaborare l'esempio.

Dopo l'elaborazione dell'esempio, recapitarlo al filtro downstream chiamando [**CBaseOutputPin::D Eliver**](cbaseoutputpin-deliver.md). Questo metodo helper chiama **IMemInputPin:: Receive** sul pin di input downstream. Un filtro può recapitare campioni a diversi pin.

 

 



