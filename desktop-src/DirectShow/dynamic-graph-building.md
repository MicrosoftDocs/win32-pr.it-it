---
description: Compilazione Graph dinamica
ms.assetid: 13fed430-979b-40f7-91ba-aff2d811bd92
title: Compilazione Graph dinamica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8c7296b95bc97461eb5a16ee577acb4bd267ee1a25f9be357a00fef7d4bdba5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118652791"
---
# <a name="dynamic-graph-building"></a>Compilazione Graph dinamica

Se è necessario modificare un grafo filtro esistente, è possibile arrestare il grafo, apportare le modifiche e riavviare il grafo. Questo è in genere l'approccio migliore. In alcuni casi, tuttavia, potrebbe essere necessario modificare un grafo mentre è ancora in esecuzione. Ad esempio:

-   L'applicazione inserisce un filtro degli effetti video durante la riproduzione.
-   Un filtro di origine cambia i tipi di supporti midstream, probabilmente richiedendo un nuovo filtro di decompressione.
-   L'applicazione aggiunge un nuovo flusso video al grafico.

Questi sono tutti esempi di *creazione dinamica di grafi,* un termine che copre qualsiasi tipo di modifica a un grafico filtro mentre il grafico continua a essere eseguito. La creazione dinamica di grafi può essere avviata da un'applicazione o da un filtro nel grafico. Sono possibili tre scenari distinti:

-   [Modifiche di formato dinamico:](dynamic-format-changes.md)un filtro può modificare i formati midstream, senza la necessità di rimuovere o sostituire filtri.
-   [Riconnessione dinamica:](dynamic-reconnection.md)modifica del grafico aggiungendo o rimuovendo filtri.
-   [Catene di filtri:](filter-chains.md)aggiunta, rimozione e controllo di catene di filtri.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni DirectShow](about-directshow.md)
</dt> </dl>

 

 



