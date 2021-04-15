---
description: Il modello di architettura a tre livelli, che è il Framework fondamentale per il modello di progettazione logica, segmenta i componenti di applicazioni in tre livelli di servizi.
ms.assetid: a03327c1-e427-4c07-b3d4-808ce81c2c96
title: Uso di un modello di architettura Three-Tier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e20b765a6d103f3c349ffd9a44853f495c64a070
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401493"
---
# <a name="using-a-three-tier-architecture-model"></a>Uso di un modello di architettura Three-Tier

Il modello di architettura a tre livelli, che è il Framework fondamentale per il [modello di progettazione logica](the-logical-model--application-definition-and-planning.md), segmenta i componenti di un'applicazione in tre livelli di servizi. Questi livelli non corrispondono necessariamente a posizioni fisiche su diversi computer in una rete, ma piuttosto a livelli logici dell'applicazione. Il modo in cui le parti di un'applicazione vengono distribuite in una topologia fisica può cambiare, a seconda dei requisiti di sistema.

Di seguito sono riportate brevi descrizioni dei servizi allocati a ogni livello:

-   **Il livello presentazione o livello servizi utente consente a un utente di accedere all'applicazione.** Questo livello presenta i dati all'utente e, facoltativamente, consente la manipolazione e l'immissione di dati. I due tipi principali di interfaccia utente per questo livello sono l'applicazione tradizionale e l'applicazione basata sul Web. Le applicazioni basate sul Web ora spesso contengono la maggior parte delle funzionalità di manipolazione dei dati utilizzate dalle applicazioni tradizionali. Questa operazione viene eseguita tramite l'utilizzo di origini dati dinamiche e dei cursori dati del lato client e HTML.

    > [!Note]  
    > In un'applicazione a tre livelli, l'applicazione sul lato client sarà skinnier rispetto a un'applicazione client-server, perché non conterrà i componenti del servizio ora presenti nel livello intermedio. Ciò comporta un minor sovraccarico per l'utente, ma un maggiore traffico di rete per il sistema perché i componenti vengono distribuiti tra computer diversi.

     

-   **Il livello intermedio, o livello servizi aziendali, è costituito da regole business e dati.** Noto anche come livello di *logica di business*, il livello intermedio è il punto in cui gli sviluppatori com+ possono risolvere i problemi aziendali cruciali e raggiungere i principali vantaggi di produttività. I componenti che costituiscono questo livello possono esistere in un computer server, per facilitare la condivisione delle risorse. Questi componenti possono essere utilizzati per applicare regole di business, ad esempio algoritmi di business, normative legali o governative e regole dei dati, progettate per garantire la coerenza delle strutture di dati all'interno di database specifici o multipli. Poiché questi componenti di livello intermedio non sono collegati a un client specifico, possono essere utilizzati da tutte le applicazioni e possono essere spostati in posizioni diverse, in quanto il tempo di risposta e le altre regole richiedono. Ad esempio, è possibile posizionare semplici modifiche sul lato client per ridurre al minimo i round trip di rete oppure è possibile inserire le regole dei dati nelle stored procedure.

-   **Il livello dati, o livello di servizi dati, interagisce con i dati persistenti in genere archiviati in un database o in un archivio permanente.** Questo è il livello di accesso DBMS effettivo. È possibile accedervi tramite il livello dei servizi aziendali e in occasione del livello dei servizi utente. Questo livello è costituito da componenti di accesso ai dati, anziché da connessioni DBMS non elaborate, per facilitare la condivisione delle risorse e consentire la configurazione dei client senza installare le librerie DBMS e i driver ODBC in ogni client.

Durante il ciclo di vita di un'applicazione, l'approccio a tre livelli offre vantaggi quali riusabilità, flessibilità, gestibilità, gestibilità e scalabilità. È possibile condividere e riutilizzare i componenti e i servizi creati ed è possibile distribuirli in una rete di computer in base alle esigenze. È possibile dividere progetti di grandi dimensioni e complessi in progetti più semplici e assegnarli a programmatori o team di programmazione diversi. È inoltre possibile distribuire componenti e servizi in un server per gestire le modifiche ed è possibile ridistribuirli come aumento della base utente dell'applicazione, dei dati e del volume di transazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello logico: definizione dell'applicazione e pianificazione](the-logical-model--application-definition-and-planning.md)
</dt> </dl>

 

 



