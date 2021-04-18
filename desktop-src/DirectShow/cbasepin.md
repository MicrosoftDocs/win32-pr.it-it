---
description: La classe CBasePin è una classe astratta che implementa un pin generico.
ms.assetid: 23b9a0e2-24fe-4ff9-b2bb-97630c237de9
title: Classe CBasePin (Amfilter. h)
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
ms.openlocfilehash: 3ba7b3a85b512b2ad8d6e85aa38627a2abc68c21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328079"
---
# <a name="cbasepin-class"></a>Classe CBasePin

![gerarchia di classi CBasePin](images/filter02.png)

La `CBasePin` classe è una classe astratta che implementa un pin generico.

Negli argomenti seguenti viene descritto come utilizzare questa classe:

-   [Processo di connessione CBasePin](cbasepin-connection-process.md)
-   [Notifica di CBasePin delle modifiche allo stato del filtro](notifying-cbasepin-of-filter-state-changes.md)
-   [Derivazione da CBasePin](deriving-from-cbasepin.md)



| Variabili membro protette                                               | Descrizione                                                                                                |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**\_pname m**](cbasepin-m-pname.md)                                     | Nome del PIN.                                                                                                  |
| [**m \_ connesso**](cbasepin-m-connected.md)                             | Puntatore al pin connesso a questo pin.                                                          |
| [**\_dir**](cbasepin-m-dir.md)                                         | Direzione del PIN.                                                                                      |
| [**\_pLock m**](cbasepin-m-plock.md)                                     | Puntatore a un oggetto sezione critica.                                                                      |
| [**\_bRunTimeError m**](cbasepin-m-bruntimeerror.md)                     | Flag che indica se si è verificato un errore in fase di esecuzione.                                                 |
| [**\_bCanReconnectWhenActive m**](cbasepin-m-bcanreconnectwhenactive.md) | Flag che indica se il pin supporta la riconnessione dinamica.                                         |
| [**\_bTryMyTypesFirst m**](cbasepin-m-btrymytypesfirst.md)               | Flag che indica se il pin tenta i propri tipi di supporti preferiti prima di quelli del PIN di ricezione. |
| [**\_pFilter m**](cbasepin-m-pfilter.md)                                 | Puntatore al filtro che ha creato il PIN.                                                                |
| [**\_pQSink m**](cbasepin-m-pqsink.md)                                   | Puntatore all'oggetto che gestisce i messaggi di qualità.                                                       |
| [**\_TypeVersion m**](cbasepin-m-typeversion.md)                         | Versione corrente del set di tipi di supporti preferiti.                                                       |
| [**\_mt m**](cbasepin-m-mt.md)                                           | Tipo di supporto per la connessione al pin corrente.                                                                 |
| [**\_tStart m**](cbasepin-m-tstart.md)                                   | Ora di inizio del segmento.                                                                                        |
| [**\_tStop m**](cbasepin-m-tstop.md)                                     | Ora di arresto del segmento.                                                                                         |
| [**\_drate m**](cbasepin-m-drate.md)                                     | Frequenza segmento.                                                                                              |
| Metodi protetti                                                        | Descrizione                                                                                                |
| [**DisplayPinInfo**](cbasepin-displaypininfo.md)                        | Traccia una connessione del PIN durante il debug.                                                                  |
| [**DisplayTypeInfo**](cbasepin-displaytypeinfo.md)                      | Visualizza le informazioni sul tipo di supporto durante il debug.                                                          |
| [**AttemptConnection**](cbasepin-attemptconnection.md)                  | Si connette a un altro PIN utilizzando un tipo di supporto specificato.                                                      |
| [**TryMediaTypes**](cbasepin-trymediatypes.md)                          | Dato un elenco di tipi di supporto, tenta di completare una connessione usando uno di questi tipi.                      |
| [**AgreeMediaType**](cbasepin-agreemediatype.md)                        | Cerca un tipo di supporto per creare una connessione pin.                                                        |
| [**DisconnectInternal**](cbasepin-disconnectinternal.md)                | Interrompe la connessione al pin corrente.                                                                         |
| Metodi pubblici                                                           | Descrizione                                                                                                |
| [**CBasePin**](cbasepin-cbasepin.md)                                    | Metodo del costruttore.                                                                                        |
| [**~ CBasePin**](cbasepin--cbasepin.md)                                 | Metodo del distruttore. Virtuale.                                                                                |
| [**IsConnected**](cbasepin-isconnected.md)                              | Determina se il PIN è connesso a un altro pin.                                                    |
| [**GetConnected**](cbasepin-getconnected.md)                            | Recupera il pin connesso a questo pin.                                                           |
| [**IsStopped**](cbasepin-isstopped.md)                                  | Determina se il filtro contenente questo pin è stato arrestato.                                              |
| [**GetMediaTypeVersion**](cbasepin-getmediatypeversion.md)              | Recupera un numero di versione per il set di tipi di supporto preferiti. Virtuale.                                  |
| [**IncrementTypeVersion**](cbasepin-incrementtypeversion.md)            | Incrementa il numero di versione nel set di tipi di supporti preferiti.                                         |
| [**Attivo**](cbasepin-active.md)                                        | Notifica al pin che il filtro è ora attivo. Virtuale.                                                   |
| [**Inattivo**](cbasepin-inactive.md)                                    | Notifica al pin che il filtro non è più attivo. Virtuale.                                             |
| [**Correre**](cbasepin-run.md)                                              | Notifica al pin che il filtro è ora in esecuzione. Virtuale.                                                  |
| [**SetMediaType**](cbasepin-setmediatype.md)                            | Imposta il tipo di supporto per la connessione. Virtuale.                                                           |
| [**CheckConnect**](cbasepin-checkconnect.md)                            | Determina se una connessione pin è adatta. Virtuale.                                                  |
| [**BreakConnect**](cbasepin-breakconnect.md)                            | Rilascia il pin da una connessione. Virtuale.                                                               |
| [**CompleteConnect**](cbasepin-completeconnect.md)                      | Completa una connessione a un altro pin. Virtuale.                                                            |
| [**GetMediaType**](cbasepin-getmediatype.md)                            | Recupera un tipo di supporto preferito, in base al valore di indice. Virtuale.                                                 |
| [**CurrentStopTime**](cbasepin-currentstoptime.md)                      | Recupera l'ora di arresto del segmento.                                                                           |
| [**CurrentStartTime**](cbasepin-currentstarttime.md)                    | Recupera l'ora di inizio del segmento.                                                                          |
| [**PercentualeCorrente**](cbasepin-currentrate.md)                              | Recupera la velocità del segmento.                                                                                |
| [**Nome**](cbasepin-name.md)                                            | Recupera l'identificatore del PIN.                                                                              |
| [**SetReconnectWhenActive**](cbasepin-setreconnectwhenactive.md)        | Specifica se il pin supporta la riconnessione dinamica.                                                  |
| [**CanReconnectWhenActive**](cbasepin-canreconnectwhenactive.md)        | Esegue una query se il pin supporta la riconnessione dinamica.                                                    |
| Metodi virtuali puri                                                     | Descrizione                                                                                                |
| [**CheckMediaType**](cbasepin-checkmediatype.md)                        | Determina se il pin accetta un tipo di supporto specifico.                                                       |
| Metodi IPin                                                             | Descrizione                                                                                                |
| [**Connettersi**](cbasepin-connect.md)                                      | Connette il pin a un altro pin.                                                                           |
| [**ReceiveConnection**](cbasepin-receiveconnection.md)                  | Accetta una connessione da un altro pin.                                                                     |
| [**Disconnetti**](cbasepin-disconnect.md)                                | Interrompe la connessione al pin corrente.                                                                         |
| [**ConnectedTo**](cbasepin-connectedto.md)                              | Recupera il pin connesso a questo pin.                                                                   |
| [**ConnectionMediaType**](cbasepin-connectionmediatype.md)              | Recupera il tipo di supporto per la connessione pin corrente, se presente.                                           |
| [**QueryPinInfo**](cbasepin-querypininfo.md)                            | Recupera le informazioni sul pin.                                                                       |
| [**QueryDirection**](cbasepin-querydirection.md)                        | Recupera la direzione del PIN (input o output).                                                      |
| [**QueryId**](cbasepin-queryid.md)                                      | Recupera l'identificatore del PIN.                                                                              |
| [**QueryAccept**](cbasepin-queryaccept.md)                              | Determina se il pin accetta un tipo di supporto specificato.                                                 |
| [**EnumMediaTypes**](cbasepin-enummediatypes.md)                        | Enumera i tipi di supporto preferiti del PIN.                                                                |
| [**QueryInternalConnections**](cbasepin-queryinternalconnections.md)    | Recupera i pin connessi internamente a questo pin (all'interno del filtro).                          |
| [**EndOfStream**](cbasepin-endofstream.md)                              | Notifica al pin che non sono previsti dati aggiuntivi.                                                      |
| [**NewSegment**](cbasepin-newsegment.md)                                | Notifica al pin che gli esempi di supporti ricevuti dopo questa chiamata vengono raggruppati come segmento.                     |
| Metodi IQualityControl                                                  | Descrizione                                                                                                |
| [**Notifica**](cbasepin-notify.md)                                        | Notifica al pin che è richiesta una modifica di qualità.                                                       |
| [**SetSink**](cbasepin-setsink.md)                                      | Imposta un gestore qualità esterno.                                                                          |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




