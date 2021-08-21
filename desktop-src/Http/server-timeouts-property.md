---
title: Proprietà Timeouts del server
description: Proprietà Timeouts del server
ms.assetid: 5525c226-3786-41c4-86a2-3e077682313d
keywords:
- Proprietà Timeout server HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfd0495950a83ba2e675fc5b89efd33d3c53c90e0c21ad306d5845b6bafae324
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119562471"
---
# <a name="server-timeouts-property"></a>Proprietà Timeouts del server

L'API server HTTP consente alle applicazioni di impostare i limiti di timeout della connessione server in una sessione del server o in un gruppo di URL. La proprietà Timeout HTTP viene usata per impostare tutti i timeout in base all'applicazione. I timer **IdleConnection** **e HeaderWait** possono essere configurati anche a livello di API del server HTTP. Quando i timer sono configurati a livello di API del server HTTP, si applicano a tutte le applicazioni API del server HTTP nel computer e le impostazioni vengono mantenute al riavvio del servizio.

Per altre informazioni sulla configurazione dei timer, vedere [Configurazione dei timeout specifici dell'applicazione.](configuring-the-application-specific-timeouts.md)

Quando i timer non sono configurati per un gruppo di URL o una sessione del server, vengono applicate le configurazioni predefinite dell'API del server HTTP.

L'ordine di imposizione del timeout è il seguente:

1.  Le impostazioni predefinite a livello di API del server HTTP si applicano a tutte le applicazioni API server HTTP nel computer.
2.  I timeout della sessione del server sostituiscono le impostazioni a livello di API del server HTTP, se impostate.
3.  Le impostazioni del gruppo di URL sostituiscono le configurazioni di sessione del server, se impostate.

Nella tabella seguente sono elencati i limiti di timeout della connessione predefiniti



| Timer           | Definizione                                                                                                        | API server HTTP predefinita | Configurabile a livello di API del server HTTP | Configurabile come specifico dell'applicazione |
|-----------------|-------------------------------------------------------------------------------------------------------------------|-------------------------|--------------------------------------|--------------------------------------|
| IdleConnection  | La connessione è scaduta rimanendo inattiva.                                                                        | 120 sec                 | Sì                                  | Limitato                              |
| HeaderWait      | La connessione è scaduta durante l'attesa dell'API del server HTTP per l'analisi dell'intestazione.                                 | 120 sec                 | Sì                                  | Limitato                              |
| EntityBody      | La connessione è scaduta durante l'attesa dell'arrivo del corpo dell'entità della richiesta.                                       | 120 sec                 | No                                   | Sì                                  |
| DrainEntityBody | La connessione è scaduta durante l'attesa che l'API del server HTTP svuota il corpo dell'entità in una Keep-Alive connessione. | 120 sec                 | No                                   | Sì                                  |
| MinSendRate     | La connessione è scaduta perché la velocità di invio della risposta è più lenta rispetto al valore predefinito di 150 byte/sec.               | 150 sec                 | No                                   | Sì                                  |
| RequestQueue    | La connessione è scaduta perché la richiesta è rimasta nella coda delle richieste prima che l'applicazione la prendesse.     | 120 byte/sec           | No                                   | Sì                                  |



 

 

 




