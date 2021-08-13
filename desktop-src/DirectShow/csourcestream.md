---
description: La classe CSourceStream fornisce un pin di output per la classe di filtro CSource.
ms.assetid: 5ccfb129-93e2-4773-9398-5f59f2914ba7
title: Classe CSourceStream (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0f7563cabff97626ac45a150e9a763033d9ce9261e5ae528e83d174e35d4f0d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119428786"
---
# <a name="csourcestream-class"></a>Classe CSourceStream

![Gerarchia di classi csourcestream](images/source02.png)

La **classe CSourceStream** fornisce un pin di output per la [**classe di filtro CSource.**](csource.md)

Per informazioni sull'uso di questa classe, vedere [**CSource**](csource.md). Questa classe eredita la [**classe CAMThread,**](camthread.md) che fornisce un thread di lavoro per lo streaming dei dati dal pin. La **classe CSourceStream** implementa i metodi helper seguenti per inviare richieste al thread:

-   [**CSourceStream::Exit**](csourcestream-exit.md)
-   [**CSourceStream::Init**](csourcestream-init.md)
-   [**CSourceStream::P ause**](csourcestream-pause.md)
-   [**CSourceStream::Run**](csourcestream-run.md)
-   [**CSourceStream::Stop**](csourcestream-stop.md)

La prima richiesta al thread deve essere [**Init**](csourcestream-init.md). La [**richiesta Exit**](csourcestream-exit.md) termina il thread. In pratica, non è necessario chiamare direttamente nessuno di questi metodi, perché i metodi [**CSourceStream::Active**](csourcestream-active.md) e [**CSourceStream::Inactive**](csourcestream-inactive.md) del pin li chiamano in base alle esigenze.

La classe fornisce anche diversi metodi "handler":

-   [**CSourceStream::OnThreadCreate**](csourcestream-onthreadcreate.md)
-   [**CSourceStream::OnThreadDestroy**](csourcestream-onthreaddestroy.md)
-   [**CSourceStream::OnThreadStartPlay**](csourcestream-onthreadstartplay.md)

Non eseguono alcuna operazione nella classe di base, ma la classe derivata può eseguirne l'override.



| Variabili membro protette                                             | Descrizione                                                                                                                       |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**m \_ pFilter**](csourcestream-m-pfilter.md)                          | Puntatore al filtro che contiene questo segnaposto.                                                                                     |
| Metodi protetti                                                      | Descrizione                                                                                                                       |
| [**OnThreadCreate**](csourcestream-onthreadcreate.md)                 | Chiamato quando il thread di streaming viene inizializzato. Virtuale.                                                                         |
| [**OnThreadDestroy**](csourcestream-onthreaddestroy.md)               | Chiamato quando il thread di streaming sta per uscire. Virtuale.                                                                       |
| [**OnThreadStartPlay**](csourcestream-onthreadstartplay.md)           | Chiamato all'inizio del [**metodo CSourceStream::D oBufferProcessingLoop.**](csourcestream-dobufferprocessingloop.md) Virtuale. |
| [**Attivo**](csourcestream-active.md)                                 | Notifica al pin che il filtro è ora attivo.                                                                                   |
| [**Inattivo**](csourcestream-inactive.md)                             | Notifica al pin che il filtro non è più attivo.                                                                             |
| [**Getrequest**](csourcestream-getrequest.md)                         | Attende la richiesta del thread successiva.                                                                                                |
| [**CheckRequest**](csourcestream-checkrequest.md)                     | Verifica se è presente una richiesta di thread, senza blocco.                                                                            |
| [**Threadproc**](csourcestream-threadproc.md)                         | Routine thread. Virtuale.                                                                                                        |
| [**DoBufferProcessingLoop**](csourcestream-dobufferprocessingloop.md) | Genera i dati multimediali e lo recapita al pin di input downstream. Virtuale.                                                        |
| [**CheckMediaType**](csourcestream-checkmediatype.md)                 | Determina se il pin accetta un tipo di supporto specifico. Virtuale.                                                                     |
| [**GetMediaType**](csourcestream-getmediatype.md)                     | Recupera un tipo di supporto preferito. Virtuale.                                                                                        |
| Metodi pubblici                                                         | Descrizione                                                                                                                       |
| [**CSourceStream**](csourcestream-csourcestream.md)                   | Metodo del costruttore.                                                                                                               |
| [**~ CSourceStream**](csourcestream--csourcestream.md)                | Metodo del distruttore. Virtuale.                                                                                                       |
| [**Init**](csourcestream-init.md)                                     | Inizializza il thread di streaming.                                                                                                 |
| [**Esci**](csourcestream-exit.md)                                     | Segnala la chiusura del thread di streaming.                                                                                             |
| [**Esegui**](csourcestream-run.md)                                       | Segnala l'esecuzione del thread di streaming.                                                                                              |
| [**Sospendi**](csourcestream-pause.md)                                   | Segnala al thread di streaming di diventare attivo.                                                                                    |
| [**Fermare**](csourcestream-stop.md)                                     | Segnala l'arresto del thread di streaming.                                                                                             |
| Metodi virtuali puri                                                   | Descrizione                                                                                                                       |
| [**FillBuffer**](csourcestream-fillbuffer.md)                         | Riempie un campione di supporti con dati.                                                                                                   |
| Metodi IPin                                                           | Descrizione                                                                                                                       |
| [**QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid)                                        | Recupera un identificatore per il pin.                                                                                              |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Source.h (include Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Scrittura di filtri di origine](writing-source-filters.md)
</dt> </dl>

 

 




