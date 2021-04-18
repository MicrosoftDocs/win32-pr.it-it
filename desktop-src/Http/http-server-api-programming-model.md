---
title: Modello di programmazione
description: Il modello di programmazione API del server HTTP include cinque gruppi di attività.
ms.assetid: 8485cbdc-803f-4c10-ae4c-9ca53965d747
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: def54ac8a34d6c53ea4e2825ef39884f0141df99
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/06/2021
ms.locfileid: "104558880"
---
# <a name="programming-model"></a>Modello di programmazione

Il modello di programmazione API del server HTTP include cinque gruppi di attività:

-   [Eseguire la configurazione](setup-configuration.md)
-   [Configurazione del runtime](run-time-configuration.md)
-   [Creazione e associazione a una coda di richieste](creating-and-binding-to-a-request-queue.md)
-   [Elaborazione delle richieste](processing-requests.md)
-   [Chiusura e pulizia](shutdown-and-cleanup.md)

![Diagramma che mostra il modello di programmazione P I del server H T A P.](images/http-server-api-programming-model.png)

Per un'applicazione di esempio che illustra come gestire le azioni HTTP GET e POST Request e come inviare un errore 503 (**non \_ implementato**) se le azioni sono presenti nella richiesta che l'applicazione non gestisce, vedere applicazione di [esempio http server](http-server-sample-application.md).

 

 




