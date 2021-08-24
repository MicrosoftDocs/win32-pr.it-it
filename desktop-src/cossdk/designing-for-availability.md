---
description: La disponibilità è la capacità di un'applicazione di tollerare gli errori nelle risorse del server.
ms.assetid: 5d9a8216-a568-4443-b94f-1b2f2827a4be
title: Progettazione per la disponibilità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f248b9ac9ed91788713e7ef02b4e7da0a2d7eb0c2070b1240e07dbce21b5895c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637661"
---
# <a name="designing-for-availability"></a>Progettazione per la disponibilità

La disponibilità è la capacità di un'applicazione di tollerare gli errori nelle risorse del server. Ciò significa che il client continua a essere servito tramite l'errore e che, idealmente, l'errore è trasparente per il client. Ovviamente, l'errore può derivare da origini hardware o software, pertanto è necessario sviluppare per entrambi i casi.

La disponibilità può essere influenzata dai fattori seguenti:

-   Modello applicativo. Per la massima disponibilità, assicurarsi che la logica critica dell'applicazione sia eseguita usando il [servizio transazioni COM+.](com--transactions.md) Inoltre, l'uso di un meccanismo di compensazione può essere efficace per garantire che le risorse rimangano in uno stato integro dopo gli errori.
-   Modello client. Integrare la logica di "ripetizione dei tentativi in caso di errore" nell'applicazione client e cercare una riduzione delle prestazioni nell'applicazione se le risorse o i servizi non sono disponibili. Comprendere cosa si aspetta il client dall'applicazione e creare una progettazione che consenta alternative quando si verifica un errore.
-   Disponibilità di dati/stato. Per un accesso coerente ai dati persistenti, usare Windows Clustering per fornire supporto per il failover.
-   Disponibilità del servizio. È possibile usare Bilanciamento carico di rete per bilanciare il carico delle richieste IP in ingresso in un cluster di server.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Progettazione per la distribuzione](designing-for-deployment.md)
</dt> <dt>

[Progettazione per la scalabilità](designing-for-scalability.md)
</dt> <dt>

[Progettazione per la sicurezza](designing-for-security.md)
</dt> </dl>

 

 



