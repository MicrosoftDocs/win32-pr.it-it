---
title: Data e ora valide
description: La data e l'ora effettive sono una strategia di prevenzione che impedisce la distorsione della versione e gli aggiornamenti parziali rinviando i dati effettivi di informazioni a un certo punto in futuro quando la modifica ha una probabilità elevata di essere replicata completamente.
ms.assetid: 5e24f90a-dd53-4720-815e-9a1db51847a3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 448941b7ab0d85d50123985a120beb04f256d877
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044130"
---
# <a name="effective-date-and-time"></a>Data e ora valide

La *data e l'ora effettive* sono una strategia di prevenzione che impedisce la distorsione della versione e gli aggiornamenti parziali rinviando i dati effettivi di informazioni a un certo punto in futuro quando la modifica ha una probabilità elevata di essere replicata completamente. Per implementare le date effettive, gli oggetti applicazione devono includere un timestamp di data effettivo, che viene compilato quando l'oggetto viene creato o modificato. I consumer degli oggetti verificano il timestamp e rinviano l'utilizzo degli oggetti fino a quando non viene raggiunta la data e l'ora.

Alcune considerazioni importanti:

-   Le applicazioni che scelgono questo approccio devono assicurarsi che esista un set di dati applicabili da usare finché gli oggetti aggiornati non diventano effettivi.
-   Il servizio tempo distribuito in Windows NT 4,0 mantiene sincronizzati gli orologi di Windows 2000 connessi. Tuttavia, il servizio ora non è perfetto, quindi è presente una piccola finestra per la distorsione della versione.
-   L'impostazione di una data di validità valida presuppone la conoscenza della latenza di replica complessiva per il sistema distribuito in questione. In una rete stabile una regola empirica valida per le date effettive è (tempo dell'aggiornamento) + (2 \* (latenza complessiva media). Quindi, per un sistema la cui media di latenza complessiva è di 4 ore, un ritardo di 8 ore è ragionevole.
-   In una rete instabile, determinare un valore "positivo" per le date effettive è molto più difficile, poiché la latenza può essere estremamente variabile. La data effettiva è la più "efficace" in una rete instabile se combinata con altre strategie di prevenzione o rilevamento, ad esempio checksum o GUID di coerenza. Per ulteriori informazioni, vedere [checksum e conteggi degli oggetti](checksums-and-object-counts.md).

 

 




