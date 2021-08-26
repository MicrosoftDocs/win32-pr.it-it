---
description: Impostazione dell Graph clock
ms.assetid: 23deab26-6c9a-4f94-b750-11c9b1a14ce3
title: Impostazione dell Graph clock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ab93fcefe4ba88aa7724bf59b775c493313783b2f4ad3801925e16b9a1818c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904141"
---
# <a name="setting-the-graph-clock"></a>Impostazione dell Graph clock

Quando si crea un grafo di filtro, Gestione filtri Graph sceglie automaticamente un orologio di riferimento per il grafico. Tutti i filtri nel grafico vengono sincronizzati con l'orologio di riferimento. In particolare, i filtri del renderer usano l'orologio di riferimento per determinare l'ora di presentazione di ogni esempio.

In genere, un'applicazione non deve eseguire l'override dell'orologio di riferimento Graph filtro di Manager. È tuttavia possibile eseguire questa operazione chiamando il [**metodo IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) in Filter Graph Manager. Questo metodo accetta un puntatore **all'interfaccia IReferenceClock del** clock. Chiamare il metodo mentre il grafo viene arrestato.

Se un filtro fornisce un clock, è possibile ottenere il puntatore **IReferenceClock** chiamando **QueryInterface** sul filtro. In alternativa, è possibile implementare un clock di riferimento esterno non fornito da un filtro, purché l'orologio esterno **implementi IReferenceClock**. L'esempio seguente illustra come specificare un orologio:


```C++
IGraphBuilder *pGraph = 0;
IReferenceClock *pClock = 0;

CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER, 
    IID_IGraphBuilder, (void **)&pGraph);

// Build the graph.
pGraph->RenderFile(L"C:\\Example.avi", 0);

// Create your clock.
hr = CreateMyPrivateClock(&pClock);
if (SUCCEEDED(hr))
{
    // Set the graph clock.
    IMediaFilter *pMediaFilter = 0;
    pGraph->QueryInterface(IID_IMediaFilter, (void**)&pMediaFilter);
    pMediaFilter->SetSyncSource(pClock);
    pClock->Release();
    pMediaFilter->Release();
}
```



Questo esempio presuppone che CreateMyPrivateClock sia una funzione definita dall'applicazione che crea un orologio e restituisce un **puntatore IReferenceClock.**

È anche possibile impostare l'esecuzione del grafico dei filtri senza clock chiamando **SetSyncSource** con il valore **NULL.** Se non è presente alcun orologio, il grafico viene eseguito il più rapidamente possibile. Senza clock, i filtri del renderer non attendono l'ora di presentazione di un esempio. Esegue invece il rendering di ogni campione non appena arriva. L'impostazione del grafico per l'esecuzione senza orologio è utile se si vuole elaborare i dati rapidamente, anziché visualizzarne l'anteprima in tempo reale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività DirectShow di base](basic-directshow-tasks.md)
</dt> <dt>

[**Classe CBaseReferenceClock**](cbasereferenceclock.md)
</dt> <dt>

[Ora e orologi in DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



