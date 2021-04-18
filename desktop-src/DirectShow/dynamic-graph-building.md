---
description: Creazione di grafici dinamici
ms.assetid: 13fed430-979b-40f7-91ba-aff2d811bd92
title: Creazione di grafici dinamici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 710bf5f648fc91e8db6bf62d81b41327f874ddf7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304008"
---
# <a name="dynamic-graph-building"></a>Creazione di grafici dinamici

Se è necessario modificare un grafico filtro esistente, è possibile arrestare il grafo, apportare le modifiche e riavviare il grafo. Questo è in genere l'approccio migliore. In alcune circostanze, tuttavia, potrebbe essere necessario modificare un grafico mentre è ancora in esecuzione. Ad esempio:

-   L'applicazione inserisce un filtro effetti video durante la riproduzione.
-   Un filtro di origine alterna i tipi di supporto a metà, eventualmente richiedendo un nuovo filtro di decompressione.
-   L'applicazione aggiunge un nuovo flusso video al grafico.

Questi sono tutti esempi di *compilazione dinamica dei grafici*, un termine che copre qualsiasi tipo di modifica a un grafico di filtro mentre il grafo continua a essere eseguito. La compilazione dinamica dei grafici può essere avviata da un'applicazione o da un filtro nel grafico. Sono possibili tre scenari distinti:

-   [Modifiche al formato dinamico](dynamic-format-changes.md): un filtro può modificare i formati A metà, senza dover rimuovere o sostituire alcun filtro.
-   [Riconnessione dinamica](dynamic-reconnection.md): modifica del grafico mediante l'aggiunta o la rimozione di filtri.
-   [Catene](filter-chains.md)di filtri: aggiunta, rimozione e controllo di catene di filtri.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su DirectShow](about-directshow.md)
</dt> </dl>

 

 



