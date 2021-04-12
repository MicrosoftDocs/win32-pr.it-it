---
title: Canali virtuali dinamici
description: Le API del canale virtuale dinamico (DVC) estendono le API del canale virtuale esistente per Servizi Desktop remoto, note come API del canale virtuale statico (SVC).
ms.assetid: bddf0048-482d-40f3-a973-9d7bc15be8fa
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3181c0960b50289846018c3ace773a8351cb20
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395894"
---
# <a name="dynamic-virtual-channels"></a>Canali virtuali dinamici

Le API del canale virtuale dinamico (DVC) estendono le API del canale virtuale esistente per Servizi Desktop remoto, note come API del canale virtuale statico (SVC). Le API DVC affrontano diverse limitazioni esistenti nelle API SVC tra il client e il server, ad esempio:

-   Un numero limitato di canali
-   Ricostruzione di pacchetti

Le API DVC consentiranno di implementare moduli sul lato server e client di una connessione Servizi Desktop remoto che comunicano tra loro.

Analogamente a molte altre architetture client/server, viene stabilita una connessione basata su una porzione di dati comunemente concordata, definita endpoint. Un esempio simile è TCP/IP, in cui un endpoint viene stabilito tramite una combinazione di indirizzo IP del server e nome della porta. Un altro esempio è Named Pipes, in cui un endpoint è una combinazione del nome del server e del nome della pipe. In una connessione Servizi Desktop remoto sono presenti solo due parti. Pertanto, l'endpoint è costituito da una semplice stringa arbitraria che identifica in modo univoco la connessione. Analogamente a TCP/IP e named pipe, è possibile avviare più connessioni dallo stesso nome di endpoint. In questo senso, le connessioni non hanno nomi; solo un listener che attende le richieste in ingresso sull'endpoint.

Le API DVC sono costituite dai seguenti elementi:

-   API client

    Queste API sono disponibili nel client di Connessione Desktop remoto (RDC) come plug-in. Il lato client è in modalità passiva, in cui è in ascolto delle connessioni in ingresso ma non stabilisce attivamente una connessione.

-   API server

    Queste API avviano attivamente la connessione.

Per informazioni su come scrivere un modulo canale virtuale dinamico (DVC), vedere [Dettagli di implementazione di DVC](dvc-implementation-details.md).

 

 




