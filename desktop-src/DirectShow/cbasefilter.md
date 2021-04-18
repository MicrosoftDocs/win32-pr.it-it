---
description: La classe CBaseFilter è una classe astratta per l'implementazione di filtri.
ms.assetid: 4610c8d6-9d7d-47ca-b1d5-0a867153a5f6
title: Classe CBaseFilter (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fe032d0614b1067c9351b643d457a718b4917a8b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330412"
---
# <a name="cbasefilter-class"></a>Classe CBaseFilter

![gerarchia di classi cbasefilter](images/filter01.png)

La `CBaseFilter` classe è una classe astratta per l'implementazione di filtri. Per implementare un filtro utilizzando questa classe, è necessario eseguire almeno i passaggi seguenti:

-   Derivare una nuova classe da `CBaseFilter` .
-   Includere le variabili membro che definiscono i pin sul filtro. I pin devono ereditare dalla classe [**CBasePin**](cbasepin.md) .
-   Eseguire l'override del metodo virtuale pure [**CBaseFilter:: GetPin**](cbasefilter-getpin.md), che recupera i pin sul filtro.
-   Eseguire l'override del metodo virtuale pure [**CBaseFilter:: GetPinCount**](cbasefilter-getpincount.md), che recupera il numero di pin.
-   Fornire metodi per la generazione, l'elaborazione o il rendering di esempi di supporti.

Diverse classi base derivano da `CBaseFilter` , tra cui [**CSource**](csource.md), [**CBaseRenderer**](cbaserenderer.md)e [**CTransformFilter**](ctransformfilter.md). È in genere più semplice implementare un filtro con una di queste classi specializzate, anziché usare `CBaseFilter` direttamente.



| Variabili membro protette                                     | Descrizione                                                                                        |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [**m \_ stato**](cbasefilter-m-state.md)                        | Stato corrente del filtro.                                                                       |
| [**\_pClock m**](cbasefilter-m-pclock.md)                      | Puntatore al clock di riferimento del filtro.                                                           |
| [**\_tStart m**](cbasefilter-m-tstart.md)                      | Tempo di riferimento che corrisponde al tempo di flusso 0.                                                  |
| [**\_CLSID m**](cbasefilter-m-clsid.md)                        | Identificatore di classe (CLSID) del filtro.                                                            |
| [**\_pLock m**](cbasefilter-m-plock.md)                        | Puntatore a una sezione critica utilizzata per serializzare le modifiche di stato.                             |
| [**\_pname m**](cbasefilter-m-pname.md)                        | Nome del filtro.                                                                                       |
| [**\_pGraph m**](cbasefilter-m-pgraph.md)                      | Puntatore al gestore del grafico dei filtri.                                                               |
| [**\_pSink m**](cbasefilter-m-psink.md)                        | Puntatore all'interfaccia [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) in gestione grafico dei filtri.   |
| [**\_PinVersion m**](cbasefilter-m-pinversion.md)              | Versione corrente del set di pin in questo filtro.                                                 |
| Metodi pubblici                                                 | Descrizione                                                                                        |
| [**CBaseFilter**](cbasefilter-cbasefilter.md)                 | Metodo del costruttore.                                                                                |
| [**~ CBaseFilter**](cbasefilter--cbasefilter.md)              | Metodo del distruttore.                                                                                 |
| [**StreamTime**](cbasefilter-streamtime.md)                   | Recupera l'ora corrente del flusso. Virtuale.                                                        |
| [**IsActive**](cbasefilter-isactive.md)                       | Determina se il filtro è attualmente attivo (in esecuzione o in pausa).                             |
| [**IsStopped**](cbasefilter-isstopped.md)                     | Determina se il filtro è attualmente arrestato.                                                |
| [**NotifyEvent**](cbasefilter-notifyevent.md)                 | Invia una notifica degli eventi al gestore del grafico dei filtri.                                           |
| [**GetFilterGraph**](cbasefilter-getfiltergraph.md)           | Recupera un puntatore al gestore del grafico dei filtri.                                                   |
| [**ReconnectPin**](cbasefilter-reconnectpin.md)               | Interrompe una connessione al PIN esistente e la riconnette allo stesso pin, usando un tipo di supporto specificato. |
| [**GetPinVersion**](cbasefilter-getpinversion.md)             | Recupera un numero di versione per il set di pin in questo filtro. Virtuale.                            |
| [**IncrementPinVersion**](cbasefilter-incrementpinversion.md) | Incrementa il numero di versione nel set di pin.                                                  |
| [**GetSetupData**](cbasefilter-getsetupdata.md)               | Recupera i dati di registrazione per il filtro. Virtuale.                                           |
| Metodi virtuali puri                                           | Descrizione                                                                                        |
| [**GetPinCount**](cbasefilter-getpincount.md)                 | Recupera il numero di pin.                                                                      |
| [**GetPin**](cbasefilter-getpin.md)                           | Recupera un PIN.                                                                                   |
| Metodi IPersist                                               | Descrizione                                                                                        |
| [**GetClassID**](cbasefilter-getclassid.md)                   | Recupera l'identificatore di classe.                                                                    |
| Metodi IMediaFilter                                           | Descrizione                                                                                        |
| [**GetState**](cbasefilter-getstate.md)                       | Recupera lo stato del filtro (in esecuzione, arrestato o sospeso).                                        |
| [**SetSyncSource**](cbasefilter-setsyncsource.md)             | Imposta un clock di riferimento per il filtro.                                                             |
| [**GetSyncSource**](cbasefilter-getsyncsource.md)             | Recupera l'orologio di riferimento utilizzato dal filtro.                                            |
| [**Interrompere**](cbasefilter-stop.md)                               | Arresta il filtro.                                                                                  |
| [**Sospendere**](cbasefilter-pause.md)                             | Sospende il filtro.                                                                                 |
| [**Correre**](cbasefilter-run.md)                                 | Esegue il filtro.                                                                                   |
| Metodi IBaseFilter                                            | Descrizione                                                                                        |
| [**EnumPins**](cbasefilter-enumpins.md)                       | Enumera i pin in questo filtro.                                                                |
| [**FindPin**](cbasefilter-findpin.md)                         | Recupera il pin con l'identificatore specificato.                                                   |
| [**QueryFilterInfo**](cbasefilter-queryfilterinfo.md)         | Recupera le informazioni sul filtro.                                                            |
| [**JoinFilterGraph**](cbasefilter-joinfiltergraph.md)         | Notifica al filtro che è stato aggiunto o lasciato un grafico di filtro.                                     |
| [**QueryVendorInfo**](cbasefilter-queryvendorinfo.md)         | Recupera una stringa contenente le informazioni sul fornitore.                                                  |
| Metodi IAMovieSetup                                           | Descrizione                                                                                        |
| [**Registra**](cbasefilter-register.md)                       | Aggiunge il filtro al registro di sistema.                                                                   |
| [**Unregister**](cbasefilter-unregister.md)                   | Rimuove il filtro dal registro di sistema.                                                              |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




