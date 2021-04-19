---
description: La classe CSourceStream fornisce un pin di output per la classe filtro CSource.
ms.assetid: 5ccfb129-93e2-4773-9398-5f59f2914ba7
title: Classe CSourceStream (source. h)
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
ms.openlocfilehash: 36b9085df8c15e765c751be8b5fcdfd4f4a02140
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330288"
---
# <a name="csourcestream-class"></a>Classe CSourceStream

![gerarchia di classi csourcestream](images/source02.png)

La classe **CSourceStream** fornisce un pin di output per la classe filtro [**CSource**](csource.md) .

Per informazioni sull'utilizzo di questa classe, vedere [**CSource**](csource.md). Questa classe eredita la classe [**CAMThread**](camthread.md) , che fornisce un thread di lavoro per lo streaming dei dati dal pin. La classe **CSourceStream** implementa i seguenti metodi helper per inviare richieste al thread:

-   [**CSourceStream:: Exit**](csourcestream-exit.md)
-   [**CSourceStream:: init**](csourcestream-init.md)
-   [**CSourceStream::P ause**](csourcestream-pause.md)
-   [**CSourceStream:: Run**](csourcestream-run.md)
-   [**CSourceStream:: Stop**](csourcestream-stop.md)

La prima richiesta al thread deve essere [**init**](csourcestream-init.md). La richiesta di [**uscita**](csourcestream-exit.md) termina il thread. In pratica, non è necessario chiamare direttamente uno di questi metodi, perché i metodi [**CSourceStream:: Active**](csourcestream-active.md) e [**CSourceStream:: inactive**](csourcestream-inactive.md) del pin li chiamano in base alle esigenze.

La classe fornisce anche diversi metodi "handler":

-   [**CSourceStream::OnThreadCreate**](csourcestream-onthreadcreate.md)
-   [**CSourceStream::OnThreadDestroy**](csourcestream-onthreaddestroy.md)
-   [**CSourceStream::OnThreadStartPlay**](csourcestream-onthreadstartplay.md)

Non eseguono alcuna operazione nella classe di base, ma la classe derivata può eseguirne l'override.



| Variabili membro protette                                             | Descrizione                                                                                                                       |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**\_pFilter m**](csourcestream-m-pfilter.md)                          | Puntatore al filtro che contiene questo pin.                                                                                     |
| Metodi protetti                                                      | Descrizione                                                                                                                       |
| [**OnThreadCreate**](csourcestream-onthreadcreate.md)                 | Chiamato quando viene inizializzato il thread di streaming. Virtuale.                                                                         |
| [**OnThreadDestroy**](csourcestream-onthreaddestroy.md)               | Chiamato quando il thread di streaming sta per uscire. Virtuale.                                                                       |
| [**OnThreadStartPlay**](csourcestream-onthreadstartplay.md)           | Chiamato all'inizio del metodo [**CSourceStream::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) . Virtuale. |
| [**Attivo**](csourcestream-active.md)                                 | Notifica al pin che il filtro è ora attivo.                                                                                   |
| [**Inattivo**](csourcestream-inactive.md)                             | Notifica al pin che il filtro non è più attivo.                                                                             |
| [**GetRequest**](csourcestream-getrequest.md)                         | Attende la richiesta successiva del thread.                                                                                                |
| [**CheckRequest**](csourcestream-checkrequest.md)                     | Verifica se è presente una richiesta di thread senza blocco.                                                                            |
| [**ThreadProc**](csourcestream-threadproc.md)                         | Routine thread. Virtuale.                                                                                                        |
| [**DoBufferProcessingLoop**](csourcestream-dobufferprocessingloop.md) | Genera i dati multimediali e li recapita al pin di input downstream. Virtuale.                                                        |
| [**CheckMediaType**](csourcestream-checkmediatype.md)                 | Determina se il pin accetta un tipo di supporto specifico. Virtuale.                                                                     |
| [**GetMediaType**](csourcestream-getmediatype.md)                     | Recupera un tipo di supporto preferito. Virtuale.                                                                                        |
| Metodi pubblici                                                         | Descrizione                                                                                                                       |
| [**CSourceStream**](csourcestream-csourcestream.md)                   | Metodo del costruttore.                                                                                                               |
| [**~ CSourceStream**](csourcestream--csourcestream.md)                | Metodo del distruttore. Virtuale.                                                                                                       |
| [**Init**](csourcestream-init.md)                                     | Inizializza il thread di streaming.                                                                                                 |
| [**Esci**](csourcestream-exit.md)                                     | Segnala al thread di streaming di uscire.                                                                                             |
| [**Correre**](csourcestream-run.md)                                       | Segnala l'esecuzione del thread di streaming.                                                                                              |
| [**Sospendere**](csourcestream-pause.md)                                   | Segnala al thread di streaming che diventa attivo.                                                                                    |
| [**Interrompere**](csourcestream-stop.md)                                     | Segnala al thread di streaming di arrestarsi.                                                                                             |
| Metodi virtuali puri                                                   | Descrizione                                                                                                                       |
| [**FillBuffer**](csourcestream-fillbuffer.md)                         | Compila un esempio multimediale con i dati.                                                                                                   |
| Metodi IPin                                                           | Descrizione                                                                                                                       |
| [**QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid)                                        | Recupera un identificatore per il PIN.                                                                                              |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Source. h (Includi Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Scrittura di filtri di origine](writing-source-filters.md)
</dt> </dl>

 

 




