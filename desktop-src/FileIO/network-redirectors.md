---
description: Descrive la funzionalità di un redirector di rete.
ms.assetid: 3cf36f88-b282-4f75-84fe-8106fea66825
title: Redirector di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce8c887cba779fe3f6aee9811819c6638d926f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885558"
---
# <a name="network-redirectors"></a>Redirector di rete

Un redirector di rete è un driver file system (o FSD) che funziona nel modo seguente:

-   Come client in un'operazione di I/O di rete inviando richieste di I/O ai server ed elaborando le risposte dai server.
-   Come server in un'operazione di I/O di rete tramite la ricezione di richieste di I/O dai server e l'elaborazione delle richieste.

Esegue tutte le interazioni di basso livello con il server nella risoluzione del nome file fornito dall'applicazione con il percorso della risorsa nel server remoto. In questo modo, il redirector consente all'applicazione di accedere e modificare le risorse nei server remoti come se si trovassero nel computer locale.

I redirector funzionano interamente in modalità kernel. Ciò offre i vantaggi delle prestazioni seguenti rispetto alle alternative in modalità utente:

-   Può interagire con FSDs in modalità kernel in esecuzione sul server, ad esempio il server FSD, senza la necessità della modalità da utente a kernel e commutatori di contesto in modalità kernel-to-User.
-   Può interagire in modalità kernel con gestione cache sul server per memorizzare nella cache i dati di I/O inviati dal gestore della cache del server al client.
-   Le funzioni API personalizzate per le richieste di I/O remote e le modifiche apportate alle funzioni di I/O dei file standard per fornire questa funzionalità non sono necessarie.

 

 



