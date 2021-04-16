---
description: La disponibilità è la capacità di un'applicazione di tollerare gli errori nelle risorse del server.
ms.assetid: 5d9a8216-a568-4443-b94f-1b2f2827a4be
title: Progettazione per la disponibilità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 222583c9f53a1ccc88f2a4f984f445de02a2c976
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523546"
---
# <a name="designing-for-availability"></a>Progettazione per la disponibilità

La disponibilità è la capacità di un'applicazione di tollerare gli errori nelle risorse del server. Ciò significa che il client continua a essere gestito attraverso l'errore e che, idealmente, l'errore è trasparente per il client. Ovviamente, l'errore può provenire da origini hardware o software, quindi è necessario svilupparle per entrambi i casi.

La disponibilità può essere influenzata dai fattori seguenti:

-   Modello di applicazione. Per la massima disponibilità, assicurarsi che la logica dell'applicazione critica venga eseguita utilizzando il servizio [transazioni com+](com--transactions.md) . Inoltre, l'utilizzo di un meccanismo di compensazione può essere efficace per garantire che le risorse rimangano in uno stato integro dopo gli errori.
-   Modello client. Integrare la logica di "tentativi in caso di errore" nell'applicazione client e cercare una riduzione del livello di prestazioni dell'applicazione se le risorse o i servizi non sono disponibili. Comprendere il comportamento previsto dal client dall'applicazione e creare una progettazione che consenta alternative quando si verifica un errore.
-   Disponibilità dei dati/stato. Per un accesso coerente ai dati persistenti, usare il clustering di Windows per fornire il supporto del failover.
-   Disponibilità del servizio. È possibile usare bilanciamento carico di rete per bilanciare il carico delle richieste IP in ingresso in un cluster di server.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Progettazione per la distribuzione](designing-for-deployment.md)
</dt> <dt>

[Progettazione per la scalabilità](designing-for-scalability.md)
</dt> <dt>

[Progettazione per la sicurezza](designing-for-security.md)
</dt> </dl>

 

 



