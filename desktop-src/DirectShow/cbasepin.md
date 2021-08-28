---
description: La classe CBasePin è una classe astratta che implementa un pin generico.
ms.assetid: 23b9a0e2-24fe-4ff9-b2bb-97630c237de9
title: Classe CBasePin (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 55f697d6ff1a2bd3ebac77a77d8ba98321f29d09a75181b52e8ef08b03eed682
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056197"
---
# <a name="cbasepin-class"></a>Classe CBasePin

![Gerarchia di classi cbasepin](images/filter02.png)

La `CBasePin` classe è una classe astratta che implementa un pin generico.

Negli argomenti seguenti viene descritto come usare questa classe:

-   [Processo di connessione CBasePin](cbasepin-connection-process.md)
-   [Notifica a CBasePin delle modifiche dello stato del filtro](notifying-cbasepin-of-filter-state-changes.md)
-   [Derivazione da CBasePin](deriving-from-cbasepin.md)



| Variabili membro protette                                               | Descrizione                                                                                                |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**m \_ pName**](cbasepin-m-pname.md)                                     | Nome del pin.                                                                                                  |
| [**m \_ Connesso**](cbasepin-m-connected.md)                             | Puntatore al segnaposto connesso a questo pin.                                                          |
| [**m \_ dir**](cbasepin-m-dir.md)                                         | Direzione del segnaposto.                                                                                      |
| [**m \_ pLock**](cbasepin-m-plock.md)                                     | Puntatore a un oggetto sezione critica.                                                                      |
| [**m \_ bRunTimeError**](cbasepin-m-bruntimeerror.md)                     | Flag che indica se si è verificato un errore di run-time.                                                 |
| [**m \_ bCanReconnectWhenActive**](cbasepin-m-bcanreconnectwhenactive.md) | Flag che indica se il pin supporta la riconnessione dinamica.                                         |
| [**m \_ bTryMyTypesFirst**](cbasepin-m-btrymytypesfirst.md)               | Flag che indica se il pin tenta i propri tipi di supporti preferiti prima di quelli del pin ricevente. |
| [**m \_ pFilter**](cbasepin-m-pfilter.md)                                 | Puntatore al filtro che ha creato il segnaposto.                                                                |
| [**m \_ pQSink**](cbasepin-m-pqsink.md)                                   | Puntatore all'oggetto che gestisce i messaggi di qualità.                                                       |
| [**m \_ TypeVersion**](cbasepin-m-typeversion.md)                         | Versione corrente del set di tipi di supporti preferiti.                                                       |
| [**m \_ mt**](cbasepin-m-mt.md)                                           | Tipo di supporto per la connessione pin corrente.                                                                 |
| [**m \_ tStart**](cbasepin-m-tstart.md)                                   | Ora di inizio del segmento.                                                                                        |
| [**m \_ tStop**](cbasepin-m-tstop.md)                                     | Ora di arresto del segmento.                                                                                         |
| [**m \_ dRate**](cbasepin-m-drate.md)                                     | Frequenza dei segmenti.                                                                                              |
| Metodi protetti                                                        | Descrizione                                                                                                |
| [**DisplayPinInfo**](cbasepin-displaypininfo.md)                        | Traccia una connessione pin durante il debug.                                                                  |
| [**DisplayTypeInfo**](cbasepin-displaytypeinfo.md)                      | Visualizza informazioni sul tipo di supporto durante il debug.                                                          |
| [**AttemptConnection**](cbasepin-attemptconnection.md)                  | Si connette a un altro pin usando un tipo di supporto specificato.                                                      |
| [**TryMediaTypes**](cbasepin-trymediatypes.md)                          | Dato un elenco di tipi di supporti, tenta di completare una connessione usando uno di questi tipi.                      |
| [**AgreeMediaType**](cbasepin-agreemediatype.md)                        | Cerca un tipo di supporto per stabilire una connessione pin.                                                        |
| [**DisconnectInternal**](cbasepin-disconnectinternal.md)                | Interrompe la connessione del pin corrente.                                                                         |
| Metodi pubblici                                                           | Descrizione                                                                                                |
| [**CBasePin**](cbasepin-cbasepin.md)                                    | Metodo del costruttore.                                                                                        |
| [**~ CBasePin**](cbasepin--cbasepin.md)                                 | Metodo del distruttore. Virtuale.                                                                                |
| [**IsConnected**](cbasepin-isconnected.md)                              | Determina se il pin è connesso a un altro pin.                                                    |
| [**GetConnected**](cbasepin-getconnected.md)                            | Recupera il pin connesso a questo pin.                                                           |
| [**IsStopped**](cbasepin-isstopped.md)                                  | Determina se il filtro contenente questo pin viene arrestato.                                              |
| [**GetMediaTypeVersion**](cbasepin-getmediatypeversion.md)              | Recupera un numero di versione per il set di tipi di supporti preferiti. Virtuale.                                  |
| [**IncrementTypeVersion**](cbasepin-incrementtypeversion.md)            | Incrementa il numero di versione nel set di tipi di supporti preferiti.                                         |
| [**Attivo**](cbasepin-active.md)                                        | Notifica al pin che il filtro è ora attivo. Virtuale.                                                   |
| [**Inattivo**](cbasepin-inactive.md)                                    | Notifica al pin che il filtro non è più attivo. Virtuale.                                             |
| [**Esegui**](cbasepin-run.md)                                              | Notifica al pin che il filtro è in esecuzione. Virtuale.                                                  |
| [**SetMediaType**](cbasepin-setmediatype.md)                            | Imposta il tipo di supporto per la connessione. Virtuale.                                                           |
| [**CheckConnect**](cbasepin-checkconnect.md)                            | Determina se una connessione pin è adatta. Virtuale.                                                  |
| [**BreakConnect**](cbasepin-breakconnect.md)                            | Rilascia il pin da una connessione. Virtuale.                                                               |
| [**CompleteConnect**](cbasepin-completeconnect.md)                      | Completa una connessione a un altro pin. Virtuale.                                                            |
| [**GetMediaType**](cbasepin-getmediatype.md)                            | Recupera un tipo di supporto preferito, in base al valore di indice. Virtuale.                                                 |
| [**CurrentStopTime**](cbasepin-currentstoptime.md)                      | Recupera l'ora di arresto del segmento.                                                                           |
| [**CurrentStartTime**](cbasepin-currentstarttime.md)                    | Recupera l'ora di inizio del segmento.                                                                          |
| [**CurrentRate**](cbasepin-currentrate.md)                              | Recupera la frequenza dei segmenti.                                                                                |
| [**Nome**](cbasepin-name.md)                                            | Recupera l'identificatore pin.                                                                              |
| [**SetReconnectWhenActive**](cbasepin-setreconnectwhenactive.md)        | Specifica se il pin supporta riconnessioni dinamiche.                                                  |
| [**CanReconnectWhenActive**](cbasepin-canreconnectwhenactive.md)        | Esegue una query se il pin supporta riconnessioni dinamiche.                                                    |
| Metodi virtuali puri                                                     | Descrizione                                                                                                |
| [**CheckMediaType**](cbasepin-checkmediatype.md)                        | Determina se il pin accetta un tipo di supporto specifico.                                                       |
| Metodi IPin                                                             | Descrizione                                                                                                |
| [**Connettere**](cbasepin-connect.md)                                      | Connette il segnaposto a un altro pin.                                                                           |
| [**ReceiveConnection**](cbasepin-receiveconnection.md)                  | Accetta una connessione da un altro pin.                                                                     |
| [**Disconnetti**](cbasepin-disconnect.md)                                | Interrompe la connessione del pin corrente.                                                                         |
| [**ConnectedTo**](cbasepin-connectedto.md)                              | Recupera il pin connesso a questo pin.                                                                   |
| [**ConnectionMediaType**](cbasepin-connectionmediatype.md)              | Recupera il tipo di supporto per la connessione del pin corrente, se presente.                                           |
| [**QueryPinInfo**](cbasepin-querypininfo.md)                            | Recupera informazioni sul segnaposto.                                                                       |
| [**QueryDirection**](cbasepin-querydirection.md)                        | Recupera la direzione del segnaposto (input o output).                                                      |
| [**QueryId**](cbasepin-queryid.md)                                      | Recupera l'identificatore pin.                                                                              |
| [**QueryAccept**](cbasepin-queryaccept.md)                              | Determina se il pin accetta un tipo di supporto specificato.                                                 |
| [**EnumMediaTypes**](cbasepin-enummediatypes.md)                        | Enumera i tipi di supporti preferiti del pin.                                                                |
| [**QueryInternalConnections**](cbasepin-queryinternalconnections.md)    | Recupera i pin connessi internamente a questo pin (all'interno del filtro).                          |
| [**EndOfStream**](cbasepin-endofstream.md)                              | Notifica al pin che non sono previsti dati aggiuntivi.                                                      |
| [**NewSegment**](cbasepin-newsegment.md)                                | Notifica al pin che i campioni multimediali ricevuti dopo questa chiamata vengono raggruppati come segmento.                     |
| Metodi di IQualityControl                                                  | Descrizione                                                                                                |
| [**Notificare**](cbasepin-notify.md)                                        | Notifica al pin che è richiesta una modifica di qualità.                                                       |
| [**SetSink**](cbasepin-setsink.md)                                      | Imposta un responsabile qualità esterno.                                                                          |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




