---
description: In un database relazionale è necessario che le righe restituite da una query di ricerca soddisfino tutte le condizioni richiamate dalla query. Una query di ricerca di Windows, invece, può restituire i documenti che soddisfano le condizioni di ricerca a vari gradi.
ms.assetid: 9f37b494-9b7a-45a6-9ee4-6d582742cbd7
title: Informazioni sui valori di pertinenza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a24c71ad523ad869c6ff05b81ff75367031ad38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878794"
---
# <a name="understanding-relevance-values"></a>Informazioni sui valori di pertinenza

In un database relazionale è necessario che le righe restituite da una query di ricerca soddisfino tutte le condizioni richiamate dalla query. Una query di ricerca di Windows, invece, può restituire i documenti che soddisfano le condizioni di ricerca a vari gradi.

Ad esempio, una ricerca del termine "programma" in un database relazionale produce record che contengono tale ortografia specifica della parola. Se un record contiene una o 100 istanze della parola non ha alcun effetto sui risultati. Al contrario, la ricerca di Windows restituisce un valore di pertinenza associato ai documenti corrispondenti. La pertinenza dei documenti con "Program" nel titolo è superiore a quella che contengono la parola solo nell'ultimo paragrafo. Analogamente, anche i documenti contenenti varianti del termine di ricerca, ad esempio "programmi" e "programmazione", corrispondono e vengono restituiti dalla query.

Le query di ricerca di Windows restituiscono valori di pertinenza Integer nella colonna denominata "Rank".

Inoltre:

-   I valori di pertinenza restituiti dalla query sono numeri interi compresi tra 0 e 1000.
-   I valori di rango superiore indicano i documenti che soddisfano meglio le condizioni di ricerca.
-   I valori di pertinenza si applicano solo alla query corrente, quindi non possono essere confrontati per i risultati nelle query.
-   I valori di pertinenza sono relativi agli altri documenti corrispondenti alla query. Pertanto, il valore di pertinenza di un determinato documento dipende dagli altri documenti che corrispondono anche alla query.
-   I valori di pertinenza per gli elementi che corrispondono a un predicato puramente relazionale sono 1000.

È possibile modificare i valori di rango restituiti usando i pesi delle colonne nei predicati [Contains](-search-sql-contains.md) e [FREETEXT](-search-sql-freetext.md) where e la clausola Rank by.

 

 



