---
description: Descrive la funzionalità di un redirector di rete.
ms.assetid: 3cf36f88-b282-4f75-84fe-8106fea66825
title: Redirector di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ed44bb8479c4aea5056b667688cb27ae0f1fe1ebf4f43d066a49143d5bfeadc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951080"
---
# <a name="network-redirectors"></a>Redirector di rete

Un redirector di rete è un driver file system (o FSD) che funziona nel modo seguente:

-   Come client in un'operazione di I/O di rete inviando richieste di I/O ai server ed elaborando le risposte dai server.
-   Come server in un'operazione di I/O di rete ricevendo le richieste di I/O dai server ed elaborando le richieste.

Esegue tutte le interazioni di basso livello con il server nella risoluzione del nome file fornito dall'applicazione con il percorso della risorsa nel server remoto. In questo modo, il redirector consente all'applicazione di accedere e modificare le risorse nei server remoti come se si trovavano nel computer locale.

I redirector operano interamente all'interno della modalità kernel. Ciò offre i seguenti vantaggi in termini di prestazioni rispetto alle alternative in modalità utente:

-   Può interagire con fsd in modalità kernel in esecuzione nel server, ad esempio fsd del server, senza la necessità di commutatori di contesto da utente a kernel e da kernel a utente.
-   Può interagire in modalità kernel con gestione cache nel server per memorizzare nella cache i dati di I/O inviati dal gestore cache del server sul client.
-   Le funzioni API personalizzate per le richieste di I/O remoto e le modifiche alle funzioni di I/O standard dei file per fornire questa funzionalità non sono necessarie.

 

 



