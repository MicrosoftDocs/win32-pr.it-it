---
description: La scalabilità è la capacità di un'applicazione di servire un carico aggiuntivo con un aumento lineare dell'utilizzo delle risorse.
ms.assetid: 8249f1af-9c96-4545-ad6a-3736c6e63c6d
title: Progettazione per la scalabilità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54ab0aa9d67afaac14c6d8f59df34183bde36113
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304625"
---
# <a name="designing-for-scalability"></a>Progettazione per la scalabilità

La scalabilità è la capacità di un'applicazione di servire un carico aggiuntivo con un aumento lineare dell'utilizzo delle risorse. La scalabilità è importante in tutte le applicazioni distribuite. I limiti alla scalabilità in genere si concentrano sull'utilizzo delle risorse e sulle dipendenze create inavvertitamente nella progettazione dell'applicazione.

Nell'elenco seguente vengono descritti i problemi di scalabilità e vengono suggerite le soluzioni:

-   Risorse intra-computer. Il numero di thread e la memoria disponibili possono limitare la scalabilità. Utilizzare un modello di threading più efficiente per l'applicazione.
-   Risorse tra computer. Il numero di computer disponibili per la distribuzione del carico di lavoro dell'applicazione può influire sulla scalabilità.
-   Affinità client. Due situazioni di affinità possono essere create inavvertitamente da un'applicazione: una situazione in cui l'applicazione dipende dallo stato dei dati inviati dal client con la relativa richiesta; e una situazione in cui l'applicazione richiede uno stato specifico del client. Evitare di progettare la dipendenza di stato tra il client e l'applicazione.
-   Affinità server. Un'applicazione COM+ può limitare la scalabilità creando un'affinità server, in cui l'applicazione dipende da un computer server specifico per ottenere informazioni. Questa affinità può verificarsi con molte applicazioni orientate ai database. Il modo migliore per evitare un collo di bottiglia affinità server consiste nel partizionare i dati in vari computer server. Ad esempio, dividere i dati del cliente tra i server in base alla chiave usata più di frequente oppure estendere un database dei clienti su più server usando il cognome del cliente (ad esempio, Server1: a-f, Server2: g-m, Server3: n-z).
    > [!Note]  
    > Il partizionamento dei dati può aggiungere una grande complessità alla logica di programmazione e deve essere eseguito solo dopo che sono state tentate altre opzioni per aumentare la scalabilità.

     

-   Durata degli oggetti. Per essere scalabile, un'applicazione COM+ deve prestare particolare attenzione alla durata degli oggetti. Mentre un oggetto esiste, sta consumando risorse. È importante assicurarsi che la durata degli oggetti che contengono risorse costose venga gestita con attenzione. Per gli oggetti ad alta richiesta che non utilizzano risorse costose, il [pool di oggetti com+](com--object-pooling.md) può aumentare la scalabilità, in quanto è possibile modificare in modo amministrativo i valori del pool per sfruttare qualsiasi hardware di cui si dispone. Si tratta di un metodo naturale per gestire le connessioni. ad esempio, se si dispone di una licenza per 20 connessioni SQL, è possibile impostarla con l'impostazione max pool.
-   Raggruppamento di componenti dell'applicazione. Per migliorare la scalabilità di un'applicazione COM+, i componenti di livello intermedio devono essere divisi in servizi dipendenti dal tempo e indipendenti dal tempo. In questo modo è possibile concentrarsi sull'uso di un servizio Microsoft Windows per implementare un'azione necessaria per i componenti. Ad esempio, è possibile scegliere di utilizzare un servizio come [Accodamento messaggi](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) o [componenti in coda com+](com--queued-components.md) per gestire attività asincrone indipendenti dal tempo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Progettazione per la disponibilità](designing-for-availability.md)
</dt> <dt>

[Progettazione per la distribuzione](designing-for-deployment.md)
</dt> <dt>

[Progettazione per la sicurezza](designing-for-security.md)
</dt> </dl>

 

 



