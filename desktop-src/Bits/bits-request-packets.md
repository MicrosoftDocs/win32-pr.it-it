---
title: Pacchetti di richiesta BITS
description: Pacchetti di richiesta BITS
ms.assetid: 4d8fd5f3-7621-438f-926f-38ece7a52f52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60921c9adb8e1312a6b74cd129e591db5a3be7807394807b984eb3fff153b3a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588681"
---
# <a name="bits-request-packets"></a>Pacchetti di richiesta BITS

I pacchetti di richiesta descrivono le richieste client. Può essere presente una sola richiesta in sospeso in un determinato momento. è necessario ricevere un [Ack](bits-response-packets.md) per la richiesta corrente dal server prima di inviare un'altra richiesta.

Nella tabella seguente sono elencati i pacchetti di richiesta inviati al server BITS per i processi di caricamento e caricamento-risposta. La tabella elenca i pacchetti nella sequenza tipica che vengono inviati al server.



| Richiedere un pacchetto                       | Scopo                                                                                                                                                        |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Ping](ping.md)                     | Stabilisce una connessione e negozia la sicurezza con il server.                                                                                              |
| [Create-Session](create-session.md) | Richiede una sessione di caricamento con il server BITS.                                                                                                               |
| [Frammento](fragment.md)             | Invia un frammento del file al server BITS. Il numero di richieste di frammento inviate dipende dalla dimensione del frammento scelta e dalle dimensioni del file di caricamento. |
| [Chiudi sessione](close-session.md)   | Termina la sessione di caricamento file con il server BITS.                                                                                                             |
| [Annulla sessione](cancel-session.md) | Termina la sessione di caricamento file con il server BITS. In genere, si invia il pacchetto Cancel-Session se l'utente ha annullato il processo.                                 |



 

Il pacchetto Ping è facoltativo. Anziché inviare un pacchetto Ping, è possibile usare il pacchetto Create-Session per stabilire una connessione e negoziare la sicurezza. Tuttavia, è più efficiente usare il pacchetto Ping a questo scopo.

 

 




