---
title: Data e ora di validità
description: La data e l'ora effettive sono una strategia di evitabilità che impedisce lo scostamento delle versioni e gli aggiornamenti parziali rinviando i dati effettivi delle informazioni a un certo punto nel futuro, quando la modifica ha una probabilità elevata di essere replicata completamente.
ms.assetid: 5e24f90a-dd53-4720-815e-9a1db51847a3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6d95c80627c878bbc9d8cb6ac16436e6dae3e12cf262e797724cd5053f371ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118695364"
---
# <a name="effective-date-and-time"></a>Data e ora di validità

 La data e l'ora effettive sono una strategia di evitabilità che impedisce lo scostamento delle versioni e gli aggiornamenti parziali rinviando i dati effettivi delle informazioni a un certo punto nel futuro, quando la modifica ha una probabilità elevata di essere replicata completamente. Per implementare le date di validità, gli oggetti applicazione devono includere un timestamp della data effettiva, che viene compilato quando l'oggetto viene creato o modificato. I consumer degli oggetti verificano il timestamp e rinviano l'uso degli oggetti fino a quando non vengono raggiunte la data e l'ora.

Alcune considerazioni importanti:

-   Le applicazioni che scelgono questo approccio devono garantire che sia disponibile un set di dati applicabili da usare fino a quando gli oggetti aggiornati non diventano effettivi.
-   Il servizio ora distribuito in Windows NT 4.0 mantiene sincronizzati gli orologi del Windows 2000 connesso. Nessun servizio ora è perfetto, quindi c'è una piccola finestra per l'a inclinazione delle versioni.
-   L'impostazione di una data valida presuppone la conoscenza della latenza di replica complessiva per il sistema distribuito in questione. In una rete stabile una buona regola generale per le date effettive è l'ora dell'aggiornamento+ (2 \* (latenza complessiva media)). Pertanto, per un sistema la cui latenza complessiva media è di 4 ore, un ritardo di 8 ore è ragionevole.
-   In una rete instabile, determinare un valore "valido" per le date effettive è molto più difficile, perché la latenza può essere estremamente variabile. La data di validità è più "efficace" in una rete instabile in combinazione con altre strategie di prevenzione o rilevamento, ad esempio checksum o GUID di coerenza. Per altre informazioni, vedere [Checksum e conteggi degli oggetti.](checksums-and-object-counts.md)

 

 




