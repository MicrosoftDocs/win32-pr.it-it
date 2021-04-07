---
description: Scaricamento dei dati
ms.assetid: 528763a2-c0f2-4981-91dc-dd17987f5bd5
title: Scaricamento dei dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 750ddd052c18928d53511d9e955122d2d66ee59d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745634"
---
# <a name="flushing-data"></a>Scaricamento dei dati

Nello pseudocodice seguente viene illustrato come implementare il metodo [**Ipin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) :


```C++
HRESULT CMyInputPin::BeginFlush()
{
    CAutoLock lock_it(m_pLock);
   
    // First, make sure the Receive method will fail from now on.
    HRESULT hr = CBaseInputPin::BeginFlush();
    
    // Force downstream filters to release samples. If our Receive method
    // is blocked in GetBuffer or Deliver, this will unblock it.
    for (each output pin)
    {
        hr = pOutputPin->DeliverBeginFlush();
    }

    // Unblock our Receive method if it is waiting on an event.
    SetEvent(m_hSomeEventThatReceiveNeedsToWaitOn);

    // At this point, the Receive method can't be blocked. Make sure 
    // it finishes, by taking the streaming lock. (Not necessary if this 
    // is the last step.)
    { 
        CAutoLock lock_2(&m_csReceive);

        /* Now it's safe to do anything that would crash or hang 
           if Receive were executing. */
    }
    return hr;
}
```



Quando viene avviato lo scaricamento, il metodo **BeginFlush** accetta il blocco del filtro, che serializza la modifica dello stato. Non è ancora possibile eseguire il blocco di streaming perché lo svuotamento avviene nel thread dell'applicazione e il thread di streaming potrebbe trovarsi al centro di una chiamata di **ricezione** . Il PIN deve garantire che la **ricezione** non venga bloccata e che tutte le chiamate successive a **Receive** avranno esito negativo. Il metodo [**CBaseInputPin:: BeginFlush**](cbaseinputpin-beginflush.md) imposta un flag interno, [**CBaseInputPin:: m \_ bFlushing**](cbaseinputpin-m-bflushing.md). Quando il flag è **true**, il metodo **Receive** ha esito negativo.

Grazie alla chiamata a downstream di **BeginFlush** , il PIN garantisce che tutti i filtri downstream rilascino gli esempi e restituiscano le chiamate di **ricezione** . Questo garantisce a sua volta che il pin di input non è bloccato in attesa di **GetBuffer** o **Receive**. Se il metodo di **ricezione** del PIN è in attesa di un evento, ad esempio per ottenere le risorse, il metodo **BeginFlush** deve forzare l'attesa per terminare impostando l'evento. A questo punto, viene garantita la restituzione del metodo **Receive** e il flag **m \_ bFlushing** impedisce a nuove chiamate **Receive** di eseguire qualsiasi operazione.

Per alcuni filtri, questa operazione deve essere eseguita da tutti i **BeginFlush** . Il metodo **EndFlush** segnalerà al filtro che può iniziare a ricevere nuovamente gli esempi. Altri filtri potrebbero dover usare variabili o risorse in **BeginFlush** che vengono usate anche nella **ricezione**. In tal caso, il filtro deve prima tenere il blocco di streaming. Assicurarsi di non eseguire questa operazione prima di uno dei passaggi precedenti, perché potrebbe verificarsi un deadlock.

Il metodo **EndFlush** include il blocco del filtro e propaga la chiamata downstream:


```C++
HRESULT CMyInputPin::EndFlush()
{
    CAutoLock lock_it(m_pLock);
    for (each output pin)
        hr = pOutputPin->DeliverEndFlush();
    return CBaseInputPin::EndFlush();
}
```



Il metodo [**CBaseInputPin:: EndFlush**](cbaseinputpin-endflush.md) Reimposta il flag **m \_ bFlushing** su **false**, che consente al metodo **Receive** di iniziare a ricevere nuovamente gli esempi. Questo deve essere l'ultimo passaggio di **EndFlush**, perché il PIN non deve ricevere alcun campione fino al completamento dello scaricamento e alla notifica di tutti i filtri downstream.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Thread e sezioni critiche](threads-and-critical-sections.md)
</dt> </dl>

 

 



