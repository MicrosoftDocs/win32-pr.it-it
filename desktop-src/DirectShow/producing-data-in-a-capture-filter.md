---
description: Questo argomento descrive come un filtro di acquisizione DirectShow personalizzato deve generare dati di output.
ms.assetid: e407e9ed-f1f7-43c4-a048-c27476c910ea
title: Produzione di dati in un filtro di acquisizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d9c9e5bed6fc7e01aa89bf6f495c1bbdf6e42a0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965721"
---
# <a name="producing-data-in-a-capture-filter"></a>Produzione di dati in un filtro di acquisizione

Questo argomento descrive come un filtro di acquisizione DirectShow personalizzato deve generare dati di output.

## <a name="filter-state-changes"></a>Modifica stato filtro

Un filtro di acquisizione deve produrre dati solo quando il filtro è in esecuzione. Non inviare dati dai pin quando il filtro è sospeso. Inoltre, quando il filtro viene sospeso, restituisce il **\_ \_ \_ CUE del cant di VFW** dal metodo [**CBaseFilter:: GetState**](cbasefilter-getstate.md) . Questo valore restituito informa il gestore del grafico del filtro che non deve attendere i dati dal filtro mentre il filtro è sospeso. Per altre informazioni, vedere [Stati di filtro](filter-states.md).

Il codice seguente illustra come implementare il metodo [**IMediaFilter:: GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) :


```C++
CMyVidcapFilter::GetState(DWORD dw, FILTER_STATE *pState)
{
    CheckPointer(pState, E_POINTER);
    *pState = m_State;
    if (m_State == State_Paused)
    {
        return VFW_S_CANT_CUE;
    }
    else
    {
        return S_OK;
    }
}
```



## <a name="controlling-individual-streams"></a>Controllo di singoli flussi

I pin di output di un filtro di acquisizione devono supportare l'interfaccia [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) , in modo che un'applicazione possa attivare o disattivare ogni pin singolarmente. Un'applicazione, ad esempio, può essere anteprima senza acquisizione, quindi passare alla modalità di acquisizione senza ricompilare il grafico del filtro. Per implementare questa interfaccia, è possibile usare la classe [**CBaseStreamControl**](cbasestreamcontrol.md) .

## <a name="time-stamps"></a>Timestamp

Quando il filtro acquisisce un campione, ora contrassegna l'esempio con l'ora corrente del flusso. L'ora di fine è l'ora di inizio più la durata. Se, ad esempio, il filtro sta acquisendo dieci campioni al secondo e il tempo di flusso è di 200 milioni unità quando il filtro acquisisce l'esempio, gli indicatori di data e ora devono essere 200 milioni e 201 milioni. (Ci sono 10 milioni unità al secondo).

Per calcolare l'ora del flusso, chiamare il metodo [**IReferenceClock:: GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) per ottenere l'ora di riferimento corrente, quindi sottrarre l'ora di inizio originale. In alternativa, chiamare il metodo [**CBaseFilter:: StreamTime**](cbasefilter-streamtime.md) , che esegue lo stesso calcolo. Per impostare il timestamp per un esempio, chiamare il metodo [**IMediaSample:: setime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) .

Se il filtro ha un pin di anteprima, tuttavia, gli esempi del PIN di anteprima non devono avere timestamp. Il motivo è che gli esempi raggiungeranno sempre il renderer leggermente dopo il momento dell'acquisizione. Se gli esempi sono contrassegnati con un timestamp, il renderer li considererà come in ritardo e potrebbe provare ad aggiornarli eliminando gli esempi. Per ulteriori informazioni, vedere [filtri di acquisizione video DirectShow](directshow-video-capture-filters.md). Si noti che l'interfaccia [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) richiede il pin per tenere traccia dei tempi di campionamento. Per un pin di anteprima, potrebbe essere necessario modificare l'implementazione in modo che non si basi sugli indicatori temporali.

Gli indicatori temporali devono sempre aumentare da un campione a quello successivo. Questo vale anche quando il filtro viene sospeso. Se il filtro viene eseguito, viene sospesa e quindi nuovamente eseguito, il primo campione dopo la pausa deve avere un timestamp maggiore dell'ultimo campione prima della sospensione.

A seconda dei dati che si stanno acquisendo, potrebbe essere opportuno impostare il tempo dei supporti per gli esempi.

Per altre informazioni, vedere [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri di acquisizione video DirectShow](directshow-video-capture-filters.md)
</dt> <dt>

[Time and Clocks in DirectShow](time-and-clocks-in-directshow.md)
</dt> <dt>

[Scrittura dei filtri di acquisizione](writing-capture-filters.md)
</dt> </dl>

 

 



