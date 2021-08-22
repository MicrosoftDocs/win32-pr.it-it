---
title: Modello di programmazione
description: Il modello di programmazione dell'API server HTTP include cinque gruppi di attività.
ms.assetid: 8485cbdc-803f-4c10-ae4c-9ca53965d747
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30fe49dd9a50af72fc89efa6c10c56176966fda949fa177b3f081761a0d2a568
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014734"
---
# <a name="programming-model"></a>Modello di programmazione

Il modello di programmazione dell'API server HTTP include cinque gruppi di attività:

-   [Eseguire la configurazione](setup-configuration.md)
-   [Configurazione del runtime](run-time-configuration.md)
-   [Creazione e associazione a una coda di richieste](creating-and-binding-to-a-request-queue.md)
-   [Elaborazione delle richieste](processing-requests.md)
-   [Arresto e pulizia](shutdown-and-cleanup.md)

![Diagramma che illustra il modello di programmazione H T P Server A P I.](images/http-server-api-programming-model.png)

Per un'applicazione di esempio che illustra come gestire le azioni di richiesta HTTP GET e POST e come inviare un errore 503 (**NOT \_ IMPLEMENTED**) se sono presenti azioni nella richiesta che l'applicazione non gestisce, vedere Applicazione di esempio del [server HTTP](http-server-sample-application.md).

 

 




