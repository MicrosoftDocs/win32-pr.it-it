---
title: Pacchetti di risposta BITS
description: Pacchetti di risposta BITS
ms.assetid: 30755476-daa9-42ea-8fb3-5b505fc9dd75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 755e28b749d201a2c90640ea9e456f012f790453
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855485"
---
# <a name="bits-response-packets"></a>Pacchetti di risposta BITS

La tabella seguente elenca i pacchetti di risposta inviati al client BITS per i processi di caricamento e caricamento-risposta. La tabella elenca i pacchetti nella sequenza tipica che vengono inviati al client.



| Pacchetto di risposta                                      | Scopo                                                                                                                                                                                     |
|------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ACK per ping](ack-for-ping.md)                     | Riconosce la richiesta di [ping](ping.md) .                                                                                                                                                  |
| [ACK per create-Session](ack-for-create-session.md) | Conferma la richiesta di [creazione della sessione](create-session.md) e restituisce un identificatore di sessione utilizzato dal client BITS per tutte le richieste successive per identificare questa sessione di trasferimento file. |
| [ACK per il frammento](ack-for-fragment.md)             | Riconosce la richiesta del [frammento](fragment.md) e scrive il frammento nel file di caricamento sul server.                                                                                 |
| [ACK per chiusura sessione](ack-for-close-session.md)   | Conferma la richiesta di [chiusura della sessione](close-session.md) e rilascia tutte le risorse associate alla sessione.                                                                         |
| [ACK per la sessione di annullamento](ack-for-cancel-session.md) | Riconosce la richiesta di [annullamento della sessione](cancel-session.md) e rilascia tutte le risorse associate alla sessione.                                                                       |



 

 

 




