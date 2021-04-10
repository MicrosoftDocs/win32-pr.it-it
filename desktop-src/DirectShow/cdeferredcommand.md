---
description: I comandi posticipati sono accodati dalle chiamate ai metodi sull'interfaccia IQueueCommand e vengono esposti da Filter Graph Manager e da alcuni filtri.
ms.assetid: b2b177c6-af2b-4585-914f-001a6355a298
title: Classe CDeferredCommand
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand
api_type:
- COM
api_location: ''
ms.openlocfilehash: 8d3db3f35b5589a6cd17791d72aa9931124ccfbb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125301"
---
# <a name="cdeferredcommand-class"></a>Classe CDeferredCommand

![gerarchia di classi cdeferredcommand](images/cutil13.png)

I comandi posticipati sono accodati dalle chiamate ai metodi sull'interfaccia [**IQueueCommand**](/windows/desktop/api/Control/nn-control-iqueuecommand) e vengono esposti da Filter Graph Manager e da alcuni filtri. Una chiamata riuscita a uno di questi metodi restituisce un'interfaccia [**IDeferredCommand**](/windows/desktop/api/Control/nn-control-ideferredcommand) che rappresenta il comando in coda.

Un `CDeferredCommand` oggetto rappresenta un singolo comando posticipato ed espone l'interfaccia [**IDeferredCommand**](/windows/desktop/api/Control/nn-control-ideferredcommand) , oltre ad altri metodi che consentono controlli temporali ed esecuzioni effettive. Un `CDeferredCommand` oggetto contiene un riferimento all'oggetto [**CCmdQueue**](ccmdqueue.md) in cui viene accodato.

I conteggi dei riferimenti controllano la durata della `CDeferredCommand` classe. Quando si chiama la funzione membro [**CDeferredCommand:: Invoke**](cdeferredcommand-invoke.md) , l'applicazione chiamante ottiene un puntatore a interfaccia con conteggio dei riferimenti e l'oggetto [**CCmdQueue**](ccmdqueue.md) include anche un conteggio dei riferimenti nel comando posticipato. La chiamata della funzione membro [**IDeferredCommand:: Cancel**](/windows/desktop/api/Control/nf-control-ideferredcommand-cancel) accetta il comando posticipato dalla coda dei comandi e quindi riduce il conteggio dei riferimenti di uno. Una volta tolta la coda, il comando non può essere reinserito nella coda.



| Membri dati protetti                                        | Descrizione                                                                                                             |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| \_bStream m                                                    | Flag per l'ora di [**flusso**](stream-time.md) o di presentazione. da passare al metodo richiamato.                   |
| \_invio m                                                   | Accede all'interfaccia **ITypeInfo** .                                                                                   |
| \_dispidMethod m                                               | Metodo sull'interfaccia da eseguire.                                                                                         |
| \_DISPPARAMS m                                                 | Oggetto [**CDispParams**](cdispparams.md) che contiene l'elenco di parametri **DISPPARAMS**                                  |
| \_hrResult m                                                   | Archivia il valore **HRESULT** restituito.                                                                                  |
| \_IID m                                                        | Identificatore univoco globale (**GUID**) dell'interfaccia.                                                                 |
| \_pQueue m                                                     | Puntatore all'oggetto [**CCmdQueue**](ccmdqueue.md) che espone l'interfaccia [**IQueueCommand**](/windows/desktop/api/Control/nn-control-iqueuecommand) . |
| \_punk m                                                       | Puntatore **IUnknown** all'interfaccia in cui verrà eseguito il comando.                                                 |
| \_pvarResult m                                                 | Eventuali informazioni risultanti dal metodo richiamato.                                                                 |
| \_ora m                                                       | Ora in cui verrà eseguito il comando.                                                                                  |
| \_wFlags m                                                     | Flag che specificano il contesto della chiamata.                                                                         |
| Funzioni di membro                                              | Descrizione                                                                                                             |
| [**CDeferredCommand**](cdeferredcommand-cdeferredcommand.md) | Costruisce un oggetto **CDeferredCommand** .                                                                               |
| [**GetFlags**](cdeferredcommand-getflags.md)                 | Recupera i flag di contesto associati al comando posticipato.                                                       |
| [**GetIID**](cdeferredcommand-getiid.md)                     | Recupera l'identificatore di interfaccia (IID) dell'interfaccia in cui verrà eseguito il metodo.                              |
| [**GetMethod**](cdeferredcommand-getmethod.md)               | Recupera l'identificatore di invio del metodo da eseguire.                                                              |
| [**GetParams**](cdeferredcommand-getparams.md)               | Recupera l'elenco di argomenti **DISPPARAMS** al metodo.                                                               |
| [**GetResult**](cdeferredcommand-getresult.md)               | Recupera l'elenco di argomenti risultante, se esistente.                                                                   |
| [**GetTime**](cdeferredcommand-gettime.md)                   | Recupera l'ora in cui verrà eseguito il metodo.                                                                         |
| [**Richiamare**](cdeferredcommand-invoke.md)                     | Fornisce l'accesso ai metodi e alle proprietà esposti da un oggetto.                                                         |
| [**IsStreamTime**](cdeferredcommand-isstreamtime.md)         | Specifica se il comando deve essere eseguito in fase di flusso o di presentazione.                                         |
| Metodi IDeferredCommand                                      | Descrizione                                                                                                             |
| [**Annulla**](cdeferredcommand-cancel.md)                     | Annulla una richiesta [**CDeferredCommand:: Invoke**](cdeferredcommand-invoke.md) precedentemente accodata.                        |
| [**Attendibilità**](cdeferredcommand-confidence.md)             | Non implementato attualmente.                                                                                              |
| [**Rimanda**](cdeferredcommand-postpone.md)                 | Specifica una nuova ora di presentazione per un comando accodato in precedenza.                                                      |
| [**GetHResult**](cdeferredcommand-gethresult.md)             | Recupera il valore **HRESULT** del metodo richiamato.                                                                  |



 

 

 



