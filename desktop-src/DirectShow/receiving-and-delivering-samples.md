---
description: Ricezione e distribuzione di esempi
ms.assetid: 92954b40-1424-4dee-997c-fc41089b7fa5
title: Ricezione e distribuzione di esempi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e507cb3e20a8fd08c891cca5143f8bbf8c9d4f9a90bad27dc201dd43c43283e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952150"
---
# <a name="receiving-and-delivering-samples"></a>Ricezione e distribuzione di esempi

Lo pseudocodice seguente illustra come implementare **il metodo IMemInput::Receive:**


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



Il **metodo Receive** mantiene il blocco di flusso, non il blocco del filtro. Il filtro potrebbe dover attendere un evento prima di poter elaborare i dati, come illustrato qui dalla chiamata a **WaitForSingleObject.** Non tutti i filtri dovranno eseguire questa operazione. Il [**metodo CBaseInputPin::Receive**](cbaseinputpin-receive.md) verifica alcune condizioni generali di streaming. Restituisce VFW E WRONG STATE se il filtro viene arrestato, S FALSE se il filtro viene scaricato \_ \_ e così \_ \_ via. Qualsiasi codice restituito diverso da S OK indica che il metodo Receive deve restituire immediatamente e \_ non elaborare  l'esempio.

Dopo l'elaborazione dell'esempio, recapitarlo al filtro downstream chiamando [**CBaseOutputPin::D eliver.**](cbaseoutputpin-deliver.md) Questo metodo helper chiama **IMemInputPin::Receive sul** pin di input downstream. Un filtro potrebbe distribuire campioni a diversi segnaposto.

 

 



