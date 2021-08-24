---
description: Questo argomento descrive come un filtro di acquisizione DirectShow personalizzato deve generare dati di output.
ms.assetid: e407e9ed-f1f7-43c4-a048-c27476c910ea
title: Produzione di dati in un filtro di acquisizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcbc604c94953239b8be70ced28c9c0d6cf43eefa308c9d624db9a33d62152ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748181"
---
# <a name="producing-data-in-a-capture-filter"></a>Produzione di dati in un filtro di acquisizione

Questo argomento descrive come un filtro di acquisizione DirectShow personalizzato deve generare dati di output.

## <a name="filter-state-changes"></a>Filtrare le modifiche dello stato

Un filtro di acquisizione deve produrre dati solo quando il filtro è in esecuzione. Non inviare dati dai pin quando il filtro viene sospeso. Restituire anche **VFW \_ S \_ CANT \_ CUE** dal metodo [**CBaseFilter::GetState**](cbasefilter-getstate.md) quando il filtro viene sospeso. Questo valore restituito indica a Filter Graph Manager che non deve attendere i dati dal filtro mentre il filtro è sospeso. Per altre informazioni, vedere [Filtra stati](filter-states.md).

Il codice seguente illustra come implementare il [**metodo IMediaFilter::GetState:**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate)


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



## <a name="controlling-individual-streams"></a>Controllo dei singoli Flussi

I pin di output di un filtro di acquisizione devono supportare [**l'interfaccia IAMStreamControl,**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) in modo che un'applicazione possa attivare o disattivare ogni pin singolarmente. Ad esempio, un'applicazione può visualizzare in anteprima senza acquisire e quindi passare alla modalità di acquisizione senza ricompilare il grafico dei filtri. È possibile usare la [**classe CBaseStreamControl**](cbasestreamcontrol.md) per implementare questa interfaccia.

## <a name="time-stamps"></a>Timestamp

Quando il filtro acquisisce un campione, imposta il timestamp dell'esempio con l'ora corrente del flusso. L'ora di fine è l'ora di inizio e la durata. Ad esempio, se il filtro acquisisce dieci campioni al secondo e l'ora del flusso è di 200.000.000 unità quando il filtro acquisisce l'esempio, i timestamp devono essere 2000000000 e 201000000. Sono presenti 10.000.000 unità al secondo.

Per calcolare l'ora del flusso, chiamare il metodo [**IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) per ottenere l'ora di riferimento corrente e quindi sottostrarre l'ora di inizio originale. In alternativa, chiamare il [**metodo CBaseFilter::StreamTime,**](cbasefilter-streamtime.md) che esegue lo stesso calcolo. Per impostare il timestamp in un esempio, chiamare il [**metodo IMediaSample::SetTime.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime)

Se il filtro ha un segnaposto di anteprima, tuttavia, gli esempi del segnaposto di anteprima non devono avere timestamp. Il motivo è che gli esempi raggiungeranno sempre il renderer leggermente dopo il momento dell'acquisizione. Se gli esempi sono contrassegnati con timestamp, il renderer li tratterà come in ritardo e potrebbe provare a recuperare eliminando i campioni. Per altre informazioni, vedere DirectShow [filtri di acquisizione](directshow-video-capture-filters.md)video. Si noti che [**l'interfaccia IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) richiede il pin per tenere traccia dei tempi di campionamento. Per un segnaposto di anteprima, potrebbe essere necessario modificare l'implementazione in modo che non si basa sui timestamp.

I timestamp devono sempre aumentare da un campione all'altro. Questo vale anche quando il filtro viene sospeso. Se il filtro viene eseguito, sospeso e quindi eseguito di nuovo, il primo esempio dopo la sospensione deve avere un timestamp maggiore rispetto all'ultimo esempio prima della sospensione.

A seconda dei dati che si sta acquisendo, potrebbe essere opportuno impostare l'ora dei supporti sugli esempi.

Per altre informazioni, vedere [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filtri di acquisizione video](directshow-video-capture-filters.md)
</dt> <dt>

[Ora e orologi in DirectShow](time-and-clocks-in-directshow.md)
</dt> <dt>

[Scrittura di filtri di acquisizione](writing-capture-filters.md)
</dt> </dl>

 

 



