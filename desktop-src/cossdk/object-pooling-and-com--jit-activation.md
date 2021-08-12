---
description: L'attivazione JIT COM+ compromette essenzialmente i client greedy e i server greedy per ottenere prestazioni ottimali. I client riescono a mantenere i riferimenti agli oggetti, mentre i server possono gestire più da vicino l'utilizzo della memoria.
ms.assetid: 125d39f5-af38-4a87-a649-2f77a3e77c27
title: Pool di oggetti e attivazione JIT COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beb4a61534d19559c5d3492cd73f99fe65cf837c059d5f58b226d56a6cd301d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118306149"
---
# <a name="object-pooling-and-com-jit-activation"></a>Pool di oggetti e attivazione JIT COM+

L'attivazione JIT COM+ compromette essenzialmente i client greedy e i server greedy per ottenere prestazioni ottimali. I client riescono a mantenere i riferimenti agli oggetti, mentre i server possono gestire più da vicino l'utilizzo della memoria.

È possibile perfezionare ulteriormente questo valore usando [il pool di oggetti COM+.](com--object-pooling.md) Il pooling di oggetti attivati tramite JIT consente di dedicare una determinata quantità di memoria per contenere un determinato numero di oggetti attivi in memoria, pronti per il riutilizzo immediato. Questo è il modo più opportuno quando gli oggetti sono costosi da creare, come nel caso in cui contengono più risorse.

Il pooling di oggetti attivati da JIT in questo modo consente di ottenere i vantaggi seguenti:

-   Tempi di riattivazione degli oggetti notevolmente accelerati.
-   Riutilizzo di tutte le risorse dispendiose che gli oggetti sono in possesso.
-   Gestione più precisa della memoria e dell'uso delle risorse per gli oggetti in pool.
-   Conservazione della flessibilità amministrativa in modo che l'applicazione possa essere ridimensionata per usare le risorse disponibili e adattarsi ai mutevoli requisiti di prestazioni.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti relativi all'attivazione just-in-time COM+](com--just-in-time-activation-concepts.md)
</dt> <dt>

[Pool di oggetti COM+](com--object-pooling.md)
</dt> <dt>

[Abilitazione dell'attivazione JIT per un componente](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[Transazioni e attivazione JIT COM+](transactions-and-com--jit-activation.md)
</dt> </dl>

 

 



