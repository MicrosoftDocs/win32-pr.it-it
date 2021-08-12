---
description: Stati delle risorse in pool disponibili per il dispenser di risorse COM+
ms.assetid: 5037f11c-d113-49b0-b26f-0e3bc59ae8b3
title: Stati delle risorse in pool disponibili per il dispenser di risorse COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b0f28a54a85ed134bf95a8150b5bb4b9cb0d2fda15a16b0b96238ac8c2da18f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118305620"
---
# <a name="pooled-resource-states-available-to-com-resource-dispenser"></a>Stati delle risorse in pool disponibili per il dispenser di risorse COM+

In qualsiasi momento, una risorsa è in uso o non è in uso e viene integrata o non integrata in una transazione. Ciò produce quattro possibili stati delle risorse, come indicato di seguito:

-   **Risorse nell'inventario non in elenco.** Una risorsa non utilizzata da un oggetto e non integrata in una transazione è in inventario non in elenco. Una risorsa nell'inventario generale è disponibile per l'assegnazione.

-   **Risorse nell'inventario integrata.** Una risorsa non utilizzata da un oggetto, ma integrata in una transazione, è in inventario integrata. Tale risorsa è disponibile per l'assegnazione solo agli oggetti in esecuzione nella stessa transazione. Una risorsa passa dall'inventario integrata all'inventario non in elenco quando COM+ notifica al gestore del dispenser che la transazione è stata completata.

-   **Risorse in uso non in elenco.** Se una risorsa viene assegnata a un oggetto e l'istanza non è in esecuzione in una transazione o il dispenser di risorse ha identificato la risorsa come non transazionale, questa risorsa è in uso non in elenco.

-   **Risorse in uso integrata.** Se una risorsa viene assegnata a un oggetto, l'istanza è in esecuzione in una transazione e il distributore di risorse ha completato l'integrazione della risorsa nella transazione. Questa risorsa è in uso nell'elenco.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti del dispenser di risorse COM+](com--resource-dispenser-concepts.md)
</dt> <dt>

[Integrazione di una risorsa in una transazione](enlisting-a-resource-in-a-transaction.md)
</dt> </dl>

 

 



