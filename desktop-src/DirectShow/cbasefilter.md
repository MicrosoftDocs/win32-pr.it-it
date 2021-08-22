---
description: La classe CBaseFilter è una classe astratta per l'implementazione di filtri.
ms.assetid: 4610c8d6-9d7d-47ca-b1d5-0a867153a5f6
title: Classe CBaseFilter (Amfilter.h)
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
ms.openlocfilehash: fbffdf47e019494570506dac164735a2471d0617daa190ad74fb3c8910a7dede
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118659637"
---
# <a name="cbasefilter-class"></a>Classe CBaseFilter

![Gerarchia di classi cbasefilter](images/filter01.png)

La `CBaseFilter` classe è una classe astratta per l'implementazione di filtri. Per implementare un filtro usando questa classe, è necessario eseguire almeno la procedura seguente:

-   Derivare una nuova classe da `CBaseFilter` .
-   Includere variabili membro che definiscono i pin nel filtro. I pin devono ereditare dalla [**classe CBasePin.**](cbasepin.md)
-   Eseguire l'override del metodo virtuale [**puro CBaseFilter::GetPin**](cbasefilter-getpin.md), che recupera i pin sul filtro.
-   Eseguire l'override del metodo virtuale [**puro CBaseFilter::GetPinCount**](cbasefilter-getpincount.md), che recupera il numero di pin.
-   Fornire metodi per la generazione, l'elaborazione o il rendering di esempi di supporti.

Diverse classi di base derivano da , tra cui `CBaseFilter` [**CSource**](csource.md), [**CBaseRenderer**](cbaserenderer.md)e [**CTransformFilter**](ctransformfilter.md). In genere è più semplice implementare un filtro con una di queste classi specializzate, anziché `CBaseFilter` usarlo direttamente.



| Variabili membro protette                                     | Descrizione                                                                                        |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [**m \_ Stato**](cbasefilter-m-state.md)                        | Stato corrente del filtro.                                                                       |
| [**m \_ pClock**](cbasefilter-m-pclock.md)                      | Puntatore all'orologio di riferimento del filtro.                                                           |
| [**m \_ tStart**](cbasefilter-m-tstart.md)                      | Ora di riferimento corrispondente all'ora del flusso 0.                                                  |
| [**m \_ clsid**](cbasefilter-m-clsid.md)                        | Identificatore di classe (CLSID) del filtro.                                                            |
| [**m \_ pLock**](cbasefilter-m-plock.md)                        | Puntatore a una sezione critica utilizzata per serializzare le modifiche dello stato.                             |
| [**m \_ pName**](cbasefilter-m-pname.md)                        | Nome del filtro.                                                                                       |
| [**m \_ pGraph**](cbasefilter-m-pgraph.md)                      | Puntatore al gestore del grafico dei filtri.                                                               |
| [**m \_ pSink**](cbasefilter-m-psink.md)                        | Puntatore [**all'interfaccia IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) nel gestore del grafico dei filtri.   |
| [**m \_ PinVersion**](cbasefilter-m-pinversion.md)              | Versione corrente del set di pin su questo filtro.                                                 |
| Metodi pubblici                                                 | Descrizione                                                                                        |
| [**CBaseFilter**](cbasefilter-cbasefilter.md)                 | Metodo del costruttore.                                                                                |
| [**~ CBaseFilter**](cbasefilter--cbasefilter.md)              | Metodo del distruttore.                                                                                 |
| [**StreamTime**](cbasefilter-streamtime.md)                   | Recupera l'ora corrente del flusso. Virtuale.                                                        |
| [**Isactive**](cbasefilter-isactive.md)                       | Determina se il filtro è attualmente attivo (in esecuzione o sospeso).                             |
| [**IsStopped**](cbasefilter-isstopped.md)                     | Determina se il filtro è attualmente arrestato.                                                |
| [**NotifyEvent**](cbasefilter-notifyevent.md)                 | Invia una notifica di evento al gestore del grafico dei filtri.                                           |
| [**GetFilterGraph**](cbasefilter-getfiltergraph.md)           | Recupera un puntatore al gestore del grafico dei filtri.                                                   |
| [**RiconnettersiPin**](cbasefilter-reconnectpin.md)               | Interrompe una connessione del pin esistente e la riconnette allo stesso pin, usando un tipo di supporto specificato. |
| [**GetPinVersion**](cbasefilter-getpinversion.md)             | Recupera un numero di versione per il set di pin in questo filtro. Virtuale.                            |
| [**IncrementPinVersion**](cbasefilter-incrementpinversion.md) | Incrementa il numero di versione sul set di pin.                                                  |
| [**GetSetupData**](cbasefilter-getsetupdata.md)               | Recupera i dati di registrazione per il filtro. Virtuale.                                           |
| Metodi virtuali puri                                           | Descrizione                                                                                        |
| [**GetPinCount**](cbasefilter-getpincount.md)                 | Recupera il numero di pin.                                                                      |
| [**GetPin**](cbasefilter-getpin.md)                           | Recupera un segnaposto.                                                                                   |
| Metodi IPersist                                               | Descrizione                                                                                        |
| [**GetClassID**](cbasefilter-getclassid.md)                   | Recupera l'identificatore di classe.                                                                    |
| Metodi IMediaFilter                                           | Descrizione                                                                                        |
| [**GetState**](cbasefilter-getstate.md)                       | Recupera lo stato del filtro (in esecuzione, arrestato o sospeso).                                        |
| [**SetSyncSource**](cbasefilter-setsyncsource.md)             | Imposta un clock di riferimento per il filtro.                                                             |
| [**GetSyncSource**](cbasefilter-getsyncsource.md)             | Recupera l'orologio di riferimento utilizzato dal filtro.                                            |
| [**Fermare**](cbasefilter-stop.md)                               | Arresta il filtro.                                                                                  |
| [**Sospendi**](cbasefilter-pause.md)                             | Sospende il filtro.                                                                                 |
| [**Esegui**](cbasefilter-run.md)                                 | Esegue il filtro.                                                                                   |
| Metodi IBaseFilter                                            | Descrizione                                                                                        |
| [**EnumPins**](cbasefilter-enumpins.md)                       | Enumera i pin per questo filtro.                                                                |
| [**FindPin**](cbasefilter-findpin.md)                         | Recupera il pin con l'identificatore specificato.                                                   |
| [**QueryFilterInfo**](cbasefilter-queryfilterinfo.md)         | Recupera informazioni sul filtro.                                                            |
| [**JoinFilterGraph**](cbasefilter-joinfiltergraph.md)         | Notifica al filtro che è stato unito o lasciato un grafo di filtro.                                     |
| [**QueryVendorInfo**](cbasefilter-queryvendorinfo.md)         | Recupera una stringa contenente le informazioni sul fornitore.                                                  |
| Metodi di IAMovieSetup                                           | Descrizione                                                                                        |
| [**Registra**](cbasefilter-register.md)                       | Aggiunge il filtro al Registro di sistema.                                                                   |
| [**Unregister**](cbasefilter-unregister.md)                   | Rimuove il filtro dal Registro di sistema.                                                              |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




