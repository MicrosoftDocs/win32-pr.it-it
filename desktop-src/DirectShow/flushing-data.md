---
description: Scaricamento dei dati
ms.assetid: 528763a2-c0f2-4981-91dc-dd17987f5bd5
title: Scaricamento dei dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8a435bf40ae9f71b35707935812c3a935a95df1904db00a652634b171f20a10
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965461"
---
# <a name="flushing-data"></a>Scaricamento dei dati

Lo pseudocodice seguente illustra come implementare il [**metodo IPin::BeginFlush:**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush)


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



All'avvio dello scaricamento, il **metodo BeginFlush** accetta il blocco del filtro, che serializza la modifica dello stato. Non è ancora sicuro prendere il blocco di streaming, perché lo scaricamento avviene nel thread dell'applicazione e il thread di streaming potrebbe essere nel mezzo di una **chiamata Receive.** Il pin deve garantire che **Receive** non sia bloccato e che tutte le chiamate successive a **Receive** avranno esito negativo. Il [**metodo CBaseInputPin::BeginFlush**](cbaseinputpin-beginflush.md) imposta un flag interno, [**CBaseInputPin::m \_ bFlushing**](cbaseinputpin-m-bflushing.md). Quando il flag è **TRUE,** il **metodo Receive ha** esito negativo.

Recapitare la **chiamata BeginFlush** a valle, il pin garantisce che tutti i filtri downstream rilascino gli esempi e restituisca dalle **chiamate Receive.** Ciò garantisce a sua volta che il pin di input non venga bloccato in attesa di **GetBuffer** o **Receive.** Se il metodo **Receive del** pin attende un evento (ad esempio, per ottenere risorse), il metodo **BeginFlush** deve forzare l'attesa a terminare impostando l'evento . A questo punto, è **garantito** che il metodo Receive restituisca e il flag **m \_ bFlushing** impedisce alle nuove chiamate **Receive** di eseguire qualsiasi operazione.

Per alcuni filtri, è necessario **eseguire solo BeginFlush.** Il **metodo EndFlush** segnalerà al filtro che può iniziare di nuovo a ricevere campioni. Altri filtri potrebbero dover usare variabili o risorse in **BeginFlush** che vengono usate anche in **Receive**. In tal caso, il filtro deve contenere prima il blocco di streaming. Assicurarsi di non eseguire questa operazione prima di uno dei passaggi precedenti, perché potrebbe verificarsi un deadlock.

Il **metodo EndFlush** contiene il blocco del filtro e propaga la chiamata a valle:


```C++
HRESULT CMyInputPin::EndFlush()
{
    CAutoLock lock_it(m_pLock);
    for (each output pin)
        hr = pOutputPin->DeliverEndFlush();
    return CBaseInputPin::EndFlush();
}
```



Il [**metodo CBaseInputPin::EndFlush**](cbaseinputpin-endflush.md) reimposta il flag **m \_ bFlushing** su **FALSE,** che consente al metodo **Receive** di iniziare a ricevere nuovamente gli esempi. Questo deve essere l'ultimo passaggio in **EndFlush,** perché il pin non deve ricevere campioni fino al completamento dello scaricamento e non vengono notificati tutti i filtri downstream.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Thread e sezioni critiche](threads-and-critical-sections.md)
</dt> </dl>

 

 



