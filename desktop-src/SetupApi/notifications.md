---
description: Le notifiche sono valori che una funzione di installazione invia a una routine di callback per specificare uno stato o un evento. Due parametri, param1 e param2, vengono inviati con la notifica e contengono informazioni aggiuntive relative alla notifica.
ms.assetid: 93434558-ae83-4ea2-9324-659e5873a8c3
title: Notifiche (API di installazione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 096d4261a99e0a837a90aa5c965a3b676843945d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315318"
---
# <a name="notifications-setup-api"></a>Notifiche (API di installazione)

Le notifiche sono valori che una funzione di installazione invia a una routine di callback per specificare uno stato o un evento. Due parametri, *param1* e *param2*, vengono inviati con la notifica e contengono informazioni aggiuntive relative alla notifica.

La routine di callback elabora la notifica e restituisce un Unsigned Integer alla funzione di installazione. A seconda della funzione di installazione, è possibile usare questo valore per specificare un'operazione o una selezione dell'utente oppure è possibile ignorarla.

Le funzioni di installazione inviano notifiche alle routine di callback usando la sintassi seguente.

``` syntax
MsgHandler(          //the specified callback routine
    Context,         //context used by the callback routine
    Notification,    //notification code
    Param1,          //additional notification information
    Param2           //additional notification information
);
```

Il parametro *context* è un puntatore void a una variabile di contesto o a una struttura che può essere utilizzata dalla routine di callback per archiviare le informazioni che devono essere mantenute tra le chiamate successive alla routine di callback.

Poiché la routine di callback specifica l'implementazione del contesto e non viene mai referenziata o modificata dalle funzioni di installazione, il contesto non è documentato nel materiale di riferimento per i messaggi di notifica che seguono.

Il parametro *Notification* specifica un valore Unsigned Integer per un evento o uno stato che determina la chiamata della routine di callback da parte della funzione di installazione.

*Param1* e *param2* sono parametri facoltativi che possono contenere informazioni aggiuntive relative alla notifica. Questi parametri sono interi senza segno. Se *param1* o *param2* restituiscono informazioni che non sono Unsigned Integer, viene eseguito il cast a un Unsigned Integer ed è necessario eseguirne il cast al tipo di dati originale prima che possa essere utilizzato dalla routine di callback.

> [!Note]  
> Le notifiche seguenti rappresentano ogni notifica utilizzata dalle funzioni di installazione. Le singole funzioni utilizzano un subset di queste notifiche. In altre parole, non tutte le notifiche vengono usate da ogni funzione.

 

Le notifiche seguenti vengono utilizzate dalle funzioni di installazione.



| Notifica                                                                     | Descrizione                                                                                   |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**\_COPYERROR SPFILENOTIFY**](spfilenotify-copyerror.md)                        | Si è verificato un errore durante un'operazione di copia del file.                                               |
| [**\_DELETEERROR SPFILENOTIFY**](spfilenotify-deleteerror.md)                    | Si è verificato un errore durante un'operazione di eliminazione del file.                                           |
| [**\_ENDCOPY SPFILENOTIFY**](spfilenotify-endcopy.md)                            | Operazione di copia file terminata.                                                              |
| [**\_ENDDELETE SPFILENOTIFY**](spfilenotify-enddelete.md)                        | Operazione di eliminazione file terminata.                                                          |
| [**\_ENDQUEUE SPFILENOTIFY**](spfilenotify-endqueue.md)                          | Commit della coda completato.                                                            |
| [**\_ENDREGISTRATION SPFILENOTIFY**](spfilenotify-endregistration.md)            | La registrazione o l'annullamento della registrazione del file è stata completata.                                  |
| [**\_ENDRENAME SPFILENOTIFY**](spfilenotify-endrename.md)                        | Operazione di ridenominazione file terminata.                                                            |
| [**\_ENDSUBQUEUE SPFILENOTIFY**](spfilenotify-endsubqueue.md)                    | Una coda secondaria (copia, Rinomina o Elimina) è terminata.                                         |
| [**SPFILENOTIFY \_ FILEextracted**](spfilenotify-fileextracted.md)                | Il file è stato estratto dal file CAB.                                                 |
| [**\_FILEINCABINET SPFILENOTIFY**](spfilenotify-fileincabinet.md)                | Viene rilevato un file nell'archivio.                                                         |
| [**\_FILEOPDELAYED SPFILENOTIFY**](spfilenotify-fileopdelayed.md)                | Il file è in uso e l'operazione corrente è stata posticipata fino al riavvio del sistema. |
| [**\_LANGMISMATCH SPFILENOTIFY**](spfilenotify-langmismatch.md)                  | La lingua dell'operazione corrente non corrisponde alla lingua di sistema.                     |
| [**\_NEEDMEDIA SPFILENOTIFY**](spfilenotify-needmedia.md)                        | È necessario un nuovo supporto di origine.                                                                 |
| [**\_NEEDNEWCABINET SPFILENOTIFY**](spfilenotify-neednewcabinet.md)              | Il file corrente viene continuato nel file CAB successivo.                                            |
| [**\_QUEUESCAN SPFILENOTIFY**](spfilenotify-queuescan.md)                        | Un nodo nella coda di file è stato analizzato.                                                    |
| [**SPFILENOTIFY \_ QUEUESCAN \_ es**](spfilenotify-queuescan-ex.md)                 | Un nodo nella coda di file è stato analizzato.                                                    |
| [**SPFILENOTIFY \_ QUEUESCAN \_ SIGNERINFO**](spfilenotify-queuescan-signerinfo.md) | Un nodo nella coda di file è stato analizzato.                                                    |
| [**\_RENAMEERROR SPFILENOTIFY**](spfilenotify-renameerror.md)                    | Si è verificato un errore durante un'operazione di ridenominazione del file.                                             |
| [**\_STARTCOPY SPFILENOTIFY**](spfilenotify-startcopy.md)                        | Un'operazione di copia file è stata avviata.                                                            |
| [**\_STARTDELETE SPFILENOTIFY**](spfilenotify-startdelete.md)                    | È stata avviata un'operazione di eliminazione di file.                                                          |
| [**\_STARTQUEUE SPFILENOTIFY**](spfilenotify-startqueue.md)                      | Il commit della coda è stato avviato.                                                              |
| [**\_STARTREGISTRATION SPFILENOTIFY**](spfilenotify-startregistration.md)        | È stata avviata la registrazione o l'annullamento della registrazione del file.                                   |
| [**\_STARTRENAME SPFILENOTIFY**](spfilenotify-startrename.md)                    | È stata avviata un'operazione di ridenominazione del file.                                                          |
| [**\_STARTSUBQUEUE SPFILENOTIFY**](spfilenotify-startsubqueue.md)                | È stata avviata una coda secondaria (copia, Rinomina o Elimina).                                       |
| [**\_TARGETEXISTS SPFILENOTIFY**](spfilenotify-targetexists.md)                  | Una copia del file specificato esiste già nella destinazione.                                    |
| [**\_TARGETNEWER SPFILENOTIFY**](spfilenotify-targetnewer.md)                    | Nella destinazione è presente una versione più recente del file specificato.                                   |



 

 

 



