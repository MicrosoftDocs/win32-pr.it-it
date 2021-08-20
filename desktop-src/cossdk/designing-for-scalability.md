---
description: La scalabilità è la capacità di un'applicazione di gestire un carico aggiuntivo con un aumento lineare dell'utilizzo delle risorse.
ms.assetid: 8249f1af-9c96-4545-ad6a-3736c6e63c6d
title: Progettazione per la scalabilità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 344e4ce9afcc5f55430550d3ec71c5b56f0f5a4e15b29ef5ea86cea407aeb750
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118102284"
---
# <a name="designing-for-scalability"></a>Progettazione per la scalabilità

La scalabilità è la capacità di un'applicazione di gestire un carico aggiuntivo con un aumento lineare dell'utilizzo delle risorse. La scalabilità è importante in qualsiasi applicazione distribuita. I limiti alla scalabilità sono in genere al centro dell'uso delle risorse e delle dipendenze create inavvertitamente nella progettazione dell'applicazione.

L'elenco seguente descrive i problemi di scalabilità e suggerisce soluzioni:

-   Risorse all'interno del computer. Il numero di thread e la memoria disponibili possono limitare la scalabilità. Usare un modello di threading più efficiente per l'applicazione.
-   Risorse tra computer. Il numero di computer disponibili per distribuire il carico di lavoro dell'applicazione può influire sulla scalabilità.
-   Affinità client. Un'applicazione può creare inavvertitamente due situazioni di affinità: una situazione in cui l'applicazione dipende dallo stato dai dati inviati dal client con la richiesta; e in una situazione in cui l'applicazione richiede uno stato specifico del client. Evitare di progettare la dipendenza dello stato tra il client e l'applicazione.
-   Affinità server. Un'applicazione COM+ può limitarne la scalabilità creando un'affinità server, in cui l'applicazione dipende dall'invio di informazioni a un computer server specifico. Questa affinità può verificarsi con molte applicazioni orientate al database. Il modo migliore per evitare un collo di bottiglia dell'affinità server è partizionare i dati in vari computer server. Ad esempio, dividere i dati dei clienti tra i server per la chiave a cui si accede più di frequente o estendersi a un database del cliente su più server usando il cognome del cliente (ad esempio, Server1: a-f, Server2: g-m, Server3: n-z).
    > [!Note]  
    > Il partizionamento dei dati può aggiungere una grande complessità alla logica di programmazione e deve essere eseguito solo dopo che sono state tentate altre opzioni per aumentare la scalabilità.

     

-   Durata degli oggetti. Per essere scalabile, un'applicazione COM+ deve prestare particolare attenzione all'intervallo di vita degli oggetti. Mentre un oggetto esiste, utilizza risorse. È importante assicurarsi che la durata degli oggetti che contengono risorse dispendiose sia gestita con attenzione. Per gli oggetti ad alta richiesta che non utilizzano risorse dispendiose, il pool di oggetti [COM+](com--object-pooling.md) può aumentare la scalabilità perché è possibile modificare a livello amministrativo i valori di pool per sfruttare i vantaggi dell'hardware. Ed è un modo naturale per gestire le connessioni: ad esempio, se si ha una licenza per 20 connessioni SQL, è possibile determinarlo con l'impostazione Pool massimo.
-   Raggruppamento dei componenti dell'applicazione. Per migliorare la scalabilità di un'applicazione COM+, i componenti di livello intermedio devono essere suddivisi in servizi dipendenti dal tempo e indipendenti dal tempo. In questo modo è possibile concentrarsi sull'uso di un servizio Microsoft Windows per implementare un'azione del componente richiesta. Ad esempio, è possibile scegliere di usare un servizio come [Accodamento](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) messaggi o componenti in coda [COM+](com--queued-components.md) per gestire attività asincrone indipendenti dal tempo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Progettazione per la disponibilità](designing-for-availability.md)
</dt> <dt>

[Progettazione per la distribuzione](designing-for-deployment.md)
</dt> <dt>

[Progettazione per la sicurezza](designing-for-security.md)
</dt> </dl>

 

 



