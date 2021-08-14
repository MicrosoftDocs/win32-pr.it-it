---
description: In un database relazionale le righe restituite da una query di ricerca devono soddisfare tutte le condizioni chiamate dalla query. Al contrario, una query Windows ricerca può restituire documenti che soddisfano le condizioni di ricerca in diversi gradi.
ms.assetid: 9f37b494-9b7a-45a6-9ee4-6d582742cbd7
title: Informazioni sui valori di pertinenza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2d28efba26d12e0260d76e02fc4e042e72612df34d383a0e22a34f4be9d9fdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118226806"
---
# <a name="understanding-relevance-values"></a>Informazioni sui valori di pertinenza

In un database relazionale le righe restituite da una query di ricerca devono soddisfare tutte le condizioni chiamate dalla query. Al contrario, una query Windows ricerca può restituire documenti che soddisfano le condizioni di ricerca in diversi gradi.

Ad esempio, una ricerca del termine "programma" in un database relazionale produce record che contengono tale ortografia specifica della parola. Se un record contiene una o cento istanze della parola non ha alcun impatto sui risultati. Al contrario, Windows ricerca restituisce un valore di pertinenza associato ai documenti corrispondenti. La pertinenza dei documenti con "programma" nel titolo è maggiore di quelli che contengono la parola solo nell'ultimo paragrafo. Analogamente, anche i documenti contenenti variazioni del termine di ricerca, ad esempio "programmi" e "programmazione", corrispondono e vengono restituiti dalla query.

Windows Le query di ricerca restituiscono valori di pertinenza integer nella colonna denominata "rank".

Inoltre:

-   I valori di classificazione restituiti dalla query sono numeri interi compresi tra 0 e 1000.
-   I valori di classificazione più elevati indicano i documenti che soddisfano meglio le condizioni di ricerca.
-   I valori di classificazione si applicano solo alla query corrente, quindi non possono essere confrontati per i risultati tra le query.
-   I valori di classificazione sono relativi agli altri documenti corrispondenti alla query. Pertanto, il valore di classificazione di un documento specifico dipende dagli altri documenti che corrispondono anche alla query.
-   I valori di classificazione per gli elementi che corrispondono a un predicato puramente relazionale sono 1000.

È possibile modificare i valori di classificazione restituiti usando i pesi delle colonne nei predicati della clausola [CONTAINS](-search-sql-contains.md) e [FREETEXT](-search-sql-freetext.md) WHERE e la clausola RANK BY.

 

 



