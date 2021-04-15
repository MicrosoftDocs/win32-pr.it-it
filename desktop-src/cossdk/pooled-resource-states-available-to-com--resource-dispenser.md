---
description: Stati risorse in pool disponibili per il dispenser di risorse COM+
ms.assetid: 5037f11c-d113-49b0-b26f-0e3bc59ae8b3
title: Stati risorse in pool disponibili per il dispenser di risorse COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff0bc59dcc2b7e95e060c0d6e96a5880d09d26e3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483429"
---
# <a name="pooled-resource-states-available-to-com-resource-dispenser"></a>Stati risorse in pool disponibili per il dispenser di risorse COM+

In qualsiasi momento, una risorsa è in uso o non è in uso e può essere integrata o non integrata in una transazione. In questo modo si producono quattro stati possibili per le risorse, come indicato di seguito:

-   **Risorse nell'inventario rimosso.** Una risorsa che non è utilizzata da un oggetto e non è integrata in una transazione si trova nell'inventario rimosso. Una risorsa nell'inventario generale è disponibile per l'assegnazione.

-   **Risorse nell'inventario integrato.** Una risorsa che non è utilizzata da un oggetto ma è integrata in una transazione è nell'inventario integrato. Tale risorsa è disponibile per l'assegnazione solo a oggetti in esecuzione nella stessa transazione. Una risorsa passa dall'inventario integrato all'inventario rimosso quando COM+ notifica al gestore del dispenser che la transazione è stata completata.

-   **Risorse in uso rimosso.** Se una risorsa viene assegnata a un oggetto e l'istanza non è in esecuzione in una transazione o il dispenser di risorse ha identificato la risorsa come non transazionale, questa risorsa è in uso non integrato.

-   **Risorse in uso integrata.** Se una risorsa viene assegnata a un oggetto, l'istanza è in esecuzione in una transazione e il dispenser di risorse ha integrato correttamente la risorsa nella transazione, questa risorsa viene utilizzata nell'elenco.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti relativi al dispenser di risorse COM+](com--resource-dispenser-concepts.md)
</dt> <dt>

[Integrazione di una risorsa in una transazione](enlisting-a-resource-in-a-transaction.md)
</dt> </dl>

 

 



