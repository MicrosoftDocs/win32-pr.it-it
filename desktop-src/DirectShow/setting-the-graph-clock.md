---
description: Impostazione del clock del grafico
ms.assetid: 23deab26-6c9a-4f94-b750-11c9b1a14ce3
title: Impostazione del clock del grafico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfe98c8dce1ab5f94664fbe1406c682e5d4e50b8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303694"
---
# <a name="setting-the-graph-clock"></a>Impostazione del clock del grafico

Quando si compila un grafico di filtro, il gestore del grafico del filtro sceglie automaticamente un orologio di riferimento per il grafico. Tutti i filtri nel grafico vengono sincronizzati con l'orologio di riferimento. In particolare, i filtri renderer utilizzano l'orologio di riferimento per determinare l'ora di presentazione di ogni campione.

In genere non esiste alcun motivo per cui un'applicazione esegua l'override della scelta dell'orologio di riferimento del gestore del grafico dei filtri. Tuttavia, è possibile eseguire questa operazione chiamando il metodo [**IMediaFilter:: SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) su Filter Graph Manager. Questo metodo accetta un puntatore all'interfaccia **IReferenceClock** del clock. Chiamare il metodo mentre il grafo viene arrestato.

Se un filtro fornisce un clock, è possibile ottenere il puntatore **IReferenceClock** chiamando **QueryInterface** sul filtro. In alternativa, è possibile implementare un clock di riferimento esterno che non viene fornito da un filtro, purché il clock esterno implementi **IReferenceClock**. Nell'esempio seguente viene illustrato come specificare un clock:


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



Questo esempio si basa sul presupposto che CreateMyPrivateClock sia una funzione definita dall'applicazione che crea un clock e restituisce un puntatore **IReferenceClock** .

È anche possibile impostare il grafo del filtro per l'esecuzione senza clock, chiamando **SetSyncSource** con il valore **null**. Se non è presente alcun clock, il grafico viene eseguito il più rapidamente possibile. Senza clock, i filtri renderer non attendono l'ora di presentazione di un campione. Ma eseguono il rendering di ogni campione non appena arriva. L'impostazione del grafico per l'esecuzione senza un clock è utile se si desidera elaborare i dati in modo rapido, invece di visualizzarne l'anteprima in tempo reale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività DirectShow di base](basic-directshow-tasks.md)
</dt> <dt>

[**Classe CBaseReferenceClock**](cbasereferenceclock.md)
</dt> <dt>

[Time and Clocks in DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



