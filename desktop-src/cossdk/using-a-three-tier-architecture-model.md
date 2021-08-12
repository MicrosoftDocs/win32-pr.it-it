---
description: Il modello di architettura a tre livelli, che è il framework fondamentale per il modello di progettazione logica, segmenta i componenti di un'applicazione in tre livelli di servizi.
ms.assetid: a03327c1-e427-4c07-b3d4-808ce81c2c96
title: Uso di un modello Three-Tier architecture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bd08ee1363504c610ed650d59b3837d292fb3a1d447c882dbd39ddba6229503
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546058"
---
# <a name="using-a-three-tier-architecture-model"></a>Uso di un modello Three-Tier architecture

Il modello di architettura a tre livelli, che è il framework fondamentale per il modello di progettazione [logica,](the-logical-model--application-definition-and-planning.md)segmenta i componenti di un'applicazione in tre livelli di servizi. Questi livelli non corrispondono necessariamente a posizioni fisiche in vari computer in una rete, ma a livelli logici dell'applicazione. Il modo in cui le parti di un'applicazione vengono distribuite in una topologia fisica può cambiare a seconda dei requisiti di sistema.

Di seguito sono riportate brevi descrizioni dei servizi allocati a ogni livello:

-   **Il livello di presentazione, o livello di servizi utente, consente a un utente di accedere all'applicazione.** Questo livello presenta i dati all'utente e facoltativamente consente la manipolazione e l'immissione dei dati. I due tipi principali di interfaccia utente per questo livello sono l'applicazione tradizionale e l'applicazione basata sul Web. Le applicazioni basate sul Web contengono spesso la maggior parte delle funzionalità di manipolazione dei dati usate dalle applicazioni tradizionali. Questa operazione viene eseguita tramite l'uso di codice HTML dinamico e di origini dati sul lato client e cursori dati.

    > [!Note]  
    > In un'applicazione a tre livelli, l'applicazione lato client sarà più magro rispetto a un'applicazione client-server perché non conterrà i componenti del servizio che ora si trovano nel livello intermedio. Ciò comporta un minore sovraccarico per l'utente, ma un maggiore traffico di rete per il sistema perché i componenti vengono distribuiti tra computer diversi.

     

-   **Il livello intermedio, o livello di servizi aziendali, è costituito da regole business e dati.** Detto anche livello di logica di *business,* il livello intermedio è il punto in cui gli sviluppatori COM+ possono risolvere i problemi aziendali cruciali e ottenere importanti vantaggi in termini di produttività. I componenti che costituiscono questo livello possono esistere in un computer server, per facilitare la condivisione delle risorse. Questi componenti possono essere usati per applicare regole business, ad esempio algoritmi aziendali e normative legali o governative, e regole dei dati, progettate per mantenere coerenti le strutture dei dati all'interno di database specifici o multipli. Poiché questi componenti di livello intermedio non sono associati a un client specifico, possono essere usati da tutte le applicazioni e possono essere spostati in posizioni diverse, come richiesto dal tempo di risposta e da altre regole. Ad esempio, è possibile inserire modifiche semplici sul lato client per ridurre al minimo i round trip di rete oppure è possibile inserire regole di dati nelle stored procedure.

-   **Il livello dati, o livello dei servizi dati, interagisce con i dati persistenti in genere archiviati in un database o in un archivio permanente.** Questo è il livello di accesso DBMS effettivo. È possibile accedervi tramite il livello dei servizi aziendali e in alcuni casi dal livello dei servizi utente. Questo livello è costituito da componenti di accesso ai dati (anziché connessioni DBMS non elaborati) per facilitare la condivisione delle risorse e consentire la configurazione dei client senza installare le librerie DBMS e i driver ODBC in ogni client.

Durante il ciclo di vita di un'applicazione, l'approccio a tre livelli offre vantaggi quali riutilizzabilità, flessibilità, gestibilità, manutenibilità e scalabilità. È possibile condividere e riutilizzare i componenti e i servizi creati e distribuirli in una rete di computer in base alle esigenze. È possibile dividere progetti di grandi dimensioni e complessi in progetti più semplici e assegnarli a programmatori o team di programmazione diversi. È anche possibile distribuire componenti e servizi in un server per tenere il passo con le modifiche e ridistribuirle con l'aumentare della base utenti, dei dati e del volume delle transazioni dell'applicazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello logico: definizione e pianificazione dell'applicazione](the-logical-model--application-definition-and-planning.md)
</dt> </dl>

 

 



