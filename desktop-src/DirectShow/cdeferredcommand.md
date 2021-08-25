---
description: I comandi posticipati vengono accodati dalle chiamate ai metodi nell'interfaccia IQueueCommand e vengono esposti dal gestore del grafico dei filtri e da alcuni filtri.
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
ms.openlocfilehash: 3413deb3c606177c937aef72a8437769dc2a97acdcbee97200880c96f36f9fc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910046"
---
# <a name="cdeferredcommand-class"></a>Classe CDeferredCommand

![Gerarchia di classi cdeferredcommand](images/cutil13.png)

I comandi posticipati vengono accodati dalle chiamate ai metodi [**nell'interfaccia IQueueCommand**](/windows/desktop/api/Control/nn-control-iqueuecommand) e vengono esposti dal gestore del grafo dei filtri e da alcuni filtri. Una chiamata riuscita a uno di questi metodi restituisce [**un'interfaccia IDeferredCommand**](/windows/desktop/api/Control/nn-control-ideferredcommand) che rappresenta il comando in coda.

Un oggetto rappresenta un singolo comando posticipato ed espone `CDeferredCommand` [**l'interfaccia IDeferredCommand,**](/windows/desktop/api/Control/nn-control-ideferredcommand) nonché altri metodi che consentono i controlli di tempo e l'esecuzione effettiva. Un `CDeferredCommand` oggetto contiene un riferimento all'oggetto [**CCmdQueue**](ccmdqueue.md) in cui viene accodato.

I conteggi dei riferimenti controllano la durata della `CDeferredCommand` classe. Quando si chiama la funzione membro [**CDeferredCommand::Invoke,**](cdeferredcommand-invoke.md) l'applicazione chiamante ottiene un puntatore a interfaccia con conteggio dei riferimenti e l'oggetto [**CCmdQueue**](ccmdqueue.md) contiene anche un conteggio dei riferimenti per il comando posticipato. La chiamata alla funzione membro [**IDeferredCommand::Cancel**](/windows/desktop/api/Control/nf-control-ideferredcommand-cancel) disconnette il comando posticipato dalla coda dei comandi e riduce quindi di uno il conteggio dei riferimenti. Una volta prelevato dalla coda, il comando non può essere inserito nuovamente nella coda.



| Membri dati protetti                                        | Descrizione                                                                                                             |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| m \_ bStream                                                    | Flag per [**l'ora del flusso**](stream-time.md) o l'ora di presentazione. da passare al metodo richiamato.                   |
| m \_ Dispatch                                                   | Accede **all'interfaccia ITypeInfo.**                                                                                   |
| m \_ dispidMethod                                               | Metodo sull'interfaccia da eseguire.                                                                                         |
| m \_ DispParams                                                 | [**Oggetto CDispParams**](cdispparams.md) contenente **l'elenco di parametri DISPPARAMS**                                  |
| m \_ hrResult                                                   | Archivia il valore **HRESULT** restituito.                                                                                  |
| m \_ iid                                                        | Identificatore univoco globale (**GUID**) dell'interfaccia.                                                                 |
| m \_ pQueue                                                     | Puntatore [**all'oggetto CCmdQueue**](ccmdqueue.md) che espone [**l'interfaccia IQueueCommand.**](/windows/desktop/api/Control/nn-control-iqueuecommand) |
| m \_ pUnk                                                       | **Puntatore IUnknown** all'interfaccia in cui verrà eseguito il comando.                                                 |
| m \_ pvarResult                                                 | Informazioni risultanti, se presenti, dal metodo richiamato.                                                                 |
| m \_ time                                                       | Ora in cui verrà eseguito il comando.                                                                                  |
| m \_ wFlags                                                     | Flag che specificano il contesto della chiamata.                                                                         |
| Funzioni di membro                                              | Descrizione                                                                                                             |
| [**CDeferredCommand**](cdeferredcommand-cdeferredcommand.md) | Costruisce un **oggetto CDeferredCommand.**                                                                               |
| [**GetFlags**](cdeferredcommand-getflags.md)                 | Recupera i flag di contesto associati al comando posticipato.                                                       |
| [**GetIID**](cdeferredcommand-getiid.md)                     | Recupera l'identificatore di interfaccia (IID) dell'interfaccia su cui verrà eseguito il metodo.                              |
| [**Getmethod**](cdeferredcommand-getmethod.md)               | Recupera l'identificatore dispatch del metodo da eseguire.                                                              |
| [**GetParams**](cdeferredcommand-getparams.md)               | Recupera **l'elenco di argomenti DISPPARAMS** nel metodo .                                                               |
| [**GetResult**](cdeferredcommand-getresult.md)               | Recupera l'elenco di argomenti risultante, se presente.                                                                   |
| [**GetTime**](cdeferredcommand-gettime.md)                   | Recupera l'ora di esecuzione del metodo.                                                                         |
| [**evocare**](cdeferredcommand-invoke.md)                     | Fornisce l'accesso ai metodi e alle proprietà esposti da un oggetto .                                                         |
| [**IsStreamTime**](cdeferredcommand-isstreamtime.md)         | Specifica se il comando deve essere eseguito in fase di flusso o di presentazione.                                         |
| Metodi di IDeferredCommand                                      | Descrizione                                                                                                             |
| [**Annulla**](cdeferredcommand-cancel.md)                     | Annulla una richiesta [**CDeferredCommand::Invoke**](cdeferredcommand-invoke.md) in coda in precedenza.                        |
| [**Attendibilità**](cdeferredcommand-confidence.md)             | Non implementato attualmente.                                                                                              |
| [**Rimanda**](cdeferredcommand-postpone.md)                 | Specifica una nuova ora di presentazione per un comando accodato in precedenza.                                                      |
| [**GetHResult**](cdeferredcommand-gethresult.md)             | Recupera il **valore HRESULT** del metodo richiamato.                                                                  |



 

 

 



