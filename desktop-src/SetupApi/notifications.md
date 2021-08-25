---
description: Le notifiche sono valori inviati da una funzione di installazione a una routine di callback per specificare uno stato o un evento. Due parametri, Param1 e Param2, vengono inviati con la notifica e contengono informazioni aggiuntive relative alla notifica.
ms.assetid: 93434558-ae83-4ea2-9324-659e5873a8c3
title: Notifiche (API di installazione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f602e2062be01e3f521147d7a820d3afc1424f5421667716d3f8d4273f0dd866
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992661"
---
# <a name="notifications-setup-api"></a>Notifiche (API di installazione)

Le notifiche sono valori inviati da una funzione di installazione a una routine di callback per specificare uno stato o un evento. Due parametri, *Param1* e *Param2,* vengono inviati con la notifica e contengono informazioni aggiuntive relative alla notifica.

La routine di callback elabora la notifica e restituisce un intero senza segno alla funzione di installazione. A seconda della funzione di installazione, è possibile usare questo valore per specificare un'operazione o una selezione utente oppure è possibile ignorarlo.

Le funzioni di installazione inviano notifiche alle routine di callback usando la sintassi seguente.

``` syntax
MsgHandler(          //the specified callback routine
    Context,         //context used by the callback routine
    Notification,    //notification code
    Param1,          //additional notification information
    Param2           //additional notification information
);
```

Il *parametro Context* è un puntatore void a una variabile di contesto o a una struttura che la routine di callback può usare per archiviare le informazioni che devono essere mantenute tra le chiamate successive alla routine di callback.

Poiché la routine di callback specifica l'implementazione del contesto e non viene mai fatto riferimento o modificato dalle funzioni di installazione, il contesto non è documentato nel materiale di riferimento per i messaggi di notifica che seguono.

Il *parametro Notification* specifica un valore intero senza segno per un evento o uno stato che fa sì che la funzione di installazione chiami la routine di callback.

*Param1* e *Param2* sono parametri facoltativi che possono contenere informazioni aggiuntive rilevanti per la notifica. Questi parametri sono interi senza segno. Se *Param1* o *Param2* restituiscono informazioni che non sono un intero senza segno, viene eseguito il cast a un intero senza segno e deve essere ricastato al tipo di dati originale prima di poter essere usato dalla routine di callback.

> [!Note]  
> Le notifiche seguenti rappresentano ogni notifica usata dalle funzioni di installazione. Le singole funzioni usano un subset di queste notifiche. In altre parole, non tutte le notifiche vengono usate da ogni funzione.

 

Le notifiche seguenti vengono usate dalle funzioni di installazione.



| Notifica                                                                     | Descrizione                                                                                   |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**SPFILENOTIFY \_ COPYERROR**](spfilenotify-copyerror.md)                        | Si è verificato un errore durante un'operazione di copia di file.                                               |
| [**SPFILENOTIFY \_ DELETEERROR**](spfilenotify-deleteerror.md)                    | Si è verificato un errore durante un'operazione di eliminazione di file.                                           |
| [**SPFILENOTIFY \_ ENDCOPY**](spfilenotify-endcopy.md)                            | Un'operazione di copia file è stata terminata.                                                              |
| [**SPFILENOTIFY \_ ENDDELETE**](spfilenotify-enddelete.md)                        | Un'operazione di eliminazione di file è stata terminata.                                                          |
| [**SPFILENOTIFY \_ ENDQUEUE**](spfilenotify-endqueue.md)                          | Il commit della coda è stato completato.                                                            |
| [**SPFILENOTIFY \_ ENDREGISTRATION**](spfilenotify-endregistration.md)            | La registrazione o l'annullamento della registrazione del file è stato completato.                                  |
| [**SPFILENOTIFY \_ ENDRENAME**](spfilenotify-endrename.md)                        | Un'operazione di ridenominazione file è stata terminata.                                                            |
| [**SPFILENOTIFY \_ ENDSUBQUEUE**](spfilenotify-endsubqueue.md)                    | Una coda secondaria (copia, ridenominazione o eliminazione) è terminata.                                         |
| [**SPFILENOTIFY \_ FILEEXTRACTED**](spfilenotify-fileextracted.md)                | Il file è stato estratto dall'archivio.                                                 |
| [**SPFILENOTIFY \_ FILEINCABINET**](spfilenotify-fileincabinet.md)                | Viene rilevato un file nell'archivio.                                                         |
| [**SPFILENOTIFY \_ FILEOPDELAYED**](spfilenotify-fileopdelayed.md)                | Il file era in uso e l'operazione corrente è stata ritardata fino al riavvio del sistema. |
| [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md)                  | La lingua dell'operazione corrente non corrisponde alla lingua di sistema.                     |
| [**SPFILENOTIFY \_ NEEDMEDIA**](spfilenotify-needmedia.md)                        | È necessario un nuovo supporto di origine.                                                                 |
| [**SPFILENOTIFY \_ NEEDNEWCABINET**](spfilenotify-neednewcabinet.md)              | Il file corrente continua nell'archivio successivo.                                            |
| [**SPFILENOTIFY \_ QUEUESCAN**](spfilenotify-queuescan.md)                        | È stato analizzato un nodo nella coda di file.                                                    |
| [**SPFILENOTIFY \_ QUEUESCAN \_ EX**](spfilenotify-queuescan-ex.md)                 | È stato analizzato un nodo nella coda di file.                                                    |
| [**SPFILENOTIFY \_ QUEUESCAN \_ SIGNERINFO**](spfilenotify-queuescan-signerinfo.md) | È stato analizzato un nodo nella coda di file.                                                    |
| [**SPFILENOTIFY \_ RENAMEERROR**](spfilenotify-renameerror.md)                    | Si è verificato un errore durante un'operazione di ridenominazione file.                                             |
| [**SPFILENOTIFY \_ STARTCOPY**](spfilenotify-startcopy.md)                        | È stata avviata un'operazione di copia file.                                                            |
| [**SPFILENOTIFY \_ STARTDELETE**](spfilenotify-startdelete.md)                    | È stata avviata un'operazione di eliminazione di file.                                                          |
| [**SPFILENOTIFY \_ STARTQUEUE**](spfilenotify-startqueue.md)                      | È stato avviato il commit della coda.                                                              |
| [**SPFILENOTIFY \_ STARTREGISTRATION**](spfilenotify-startregistration.md)        | La registrazione o l'annullamento della registrazione del file è stato avviato.                                   |
| [**SPFILENOTIFY \_ STARTRENAME**](spfilenotify-startrename.md)                    | È stata avviata un'operazione di ridenominazione file.                                                          |
| [**SPFILENOTIFY \_ STARTSUBQUEUE**](spfilenotify-startsubqueue.md)                | È stata avviata una coda secondaria (copia, ridenominazione o eliminazione).                                       |
| [**SPFILENOTIFY \_ TARGETEXISTS**](spfilenotify-targetexists.md)                  | Nella destinazione esiste già una copia del file specificato.                                    |
| [**SPFILENOTIFY \_ TARGETNEWER**](spfilenotify-targetnewer.md)                    | Nella destinazione esiste una versione più recente del file specificato.                                   |



 

 

 



