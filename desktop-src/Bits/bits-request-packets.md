---
title: Pacchetti di richiesta BITS
description: Pacchetti di richiesta BITS
ms.assetid: 4d8fd5f3-7621-438f-926f-38ece7a52f52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6738f77477342f1329818ae7c2ffb5c010b074c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955219"
---
# <a name="bits-request-packets"></a>Pacchetti di richiesta BITS

I pacchetti di richiesta descrivono le richieste client. In un determinato momento può essere presente una sola richiesta in attesa; prima di inviare un'altra richiesta, è necessario ricevere un [ACK](bits-response-packets.md) per la richiesta corrente dal server.

La tabella seguente elenca i pacchetti di richiesta inviati al server BITS per i processi di caricamento e caricamento-risposta. La tabella elenca i pacchetti nella sequenza tipica che vengono inviati al server.



| Richiedi pacchetto                       | Scopo                                                                                                                                                        |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Ping](ping.md)                     | Stabilisce una connessione e negozia la sicurezza con il server.                                                                                              |
| [Creazione sessione](create-session.md) | Richiede una sessione di caricamento con il server BITS.                                                                                                               |
| [Frammento](fragment.md)             | Invia un frammento del file al server BITS. Il numero di richieste di frammenti inviate dipende dalle dimensioni del frammento scelte e dalle dimensioni del file di caricamento. |
| [Chiudi sessione](close-session.md)   | Termina la sessione di caricamento dei file con il server BITS.                                                                                                             |
| [Annulla-sessione](cancel-session.md) | Termina la sessione di caricamento dei file con il server BITS. In genere, si invia il pacchetto di Cancel-Session se l'utente ha annullato il processo.                                 |



 

Il pacchetto ping è facoltativo. Anziché inviare un pacchetto ping, è possibile utilizzare il pacchetto Create-Session per stabilire una connessione e negoziare la sicurezza. Tuttavia, è più efficiente usare il pacchetto ping a questo scopo.

 

 




