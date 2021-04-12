---
title: Proprietà timeout server
description: .
ms.assetid: 5525c226-3786-41c4-86a2-3e077682313d
keywords:
- Proprietà timeout server HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8356c1e0d0e9eea2e5db9bf43882f26f9d7e3ddb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396302"
---
# <a name="server-timeouts-property"></a>Proprietà timeout server

L'API server HTTP consente alle applicazioni di impostare i limiti di timeout della connessione del server in una sessione del server o in un gruppo di URL. La proprietà timeout HTTP viene utilizzata per impostare tutti i timeout in base a un'applicazione specifica. I timer **IdleConnection** e **HeaderWait** possono anche essere configurati a livello di API del server http. Quando i timer sono configurati a livello di API del server HTTP, si applicano a tutte le applicazioni API server HTTP nel computer e le impostazioni vengono mantenute quando il servizio viene riavviato.

Per ulteriori informazioni sulla configurazione dei timer, vedere [configurazione dei timeout specifici dell'applicazione](configuring-the-application-specific-timeouts.md).

Quando i timer non sono configurati per un gruppo di URL o una sessione del server, vengono applicate le configurazioni predefinite dell'API del server HTTP.

L'ordine di applicazione del timeout è il seguente:

1.  Le impostazioni predefinite a livello di API del server HTTP si applicano a tutte le applicazioni API server HTTP del computer.
2.  I timeout della sessione del server eseguono l'override delle impostazioni a livello di API del server HTTP, se impostate.
3.  Le impostazioni del gruppo di URL eseguono l'override delle configurazioni di sessione del server, se impostate.

La tabella seguente elenca i limiti di timeout di connessione predefiniti



| Timer           | Definizione                                                                                                        | Impostazione predefinita API server HTTP | Configurabile come API server HTTP Wide | Configurabile come specifico dell'applicazione |
|-----------------|-------------------------------------------------------------------------------------------------------------------|-------------------------|--------------------------------------|--------------------------------------|
| IdleConnection  | La connessione è scaduta mentre rimane inattiva.                                                                        | 120 sec                 | Sì                                  | Limitato                              |
| HeaderWait      | La connessione è scaduta mentre è in attesa che l'API del server HTTP analizzi l'intestazione.                                 | 120 sec                 | Sì                                  | Limitato                              |
| EntityBody      | La connessione è scaduta durante l'attesa dell'arrivo del corpo dell'entità di richiesta.                                       | 120 sec                 | No                                   | Sì                                  |
| DrainEntityBody | La connessione è scaduta mentre è in attesa che l'API del server HTTP Svuoti il corpo dell'entità in una connessione Keep-Alive. | 120 sec                 | No                                   | Sì                                  |
| MinSendRate     | La connessione è scaduta perché la velocità di invio della risposta è più bassa del valore predefinito di 150 byte/sec.               | 150 sec                 | No                                   | Sì                                  |
| RequestQueue    | La connessione è scaduta perché la richiesta rimane nella coda di richieste prima che l'applicazione sia stata prelevata.     | 120 byte/sec           | No                                   | Sì                                  |



 

 

 




