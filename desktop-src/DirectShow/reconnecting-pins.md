---
description: Riconnessione dei pin
ms.assetid: 34b3e4de-e4eb-48c5-aaef-fc99b63e8691
title: Riconnessione dei pin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d8bb214307a5c17639d98ae07284abddca4d5beb11b966150d8b7ec46013853
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072775"
---
# <a name="reconnecting-pins"></a>Riconnessione dei pin

Durante una connessione pin, un filtro può disconnettere e riconnettere uno degli altri pin, come indicato di seguito:

1.  Il filtro chiama [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) sul pin dell'altro filtro e specifica il nuovo tipo di supporto.
2.  Se **QueryAccept restituisce** S \_ OK, il filtro chiama [**IFilterGraph2::ReconnectEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) per riconnettere i segnaposto.

Di seguito sono riportati alcuni esempi di quando un filtro potrebbe dover riconnettere i pin:

-   **Filtri tee.** Un *filtro tee suddivide* un flusso di input in più output senza modificare i dati nel flusso. Un filtro tee può accettare un intervallo di tipi di supporti, ma i tipi devono corrispondere in tutte le connessioni pin. Pertanto, quando il pin di input si connette, il filtro potrebbe dover rinegoziare le connessioni esistenti sui pin di output e viceversa. Per un esempio, vedere [l'esempio di filtro InfTee.](inftee-filter-sample.md)
-   **Filtri sul posto.** Un *filtro trans-in-place* modifica i dati di input nel buffer originale anziché copiarli in un buffer di output separato. Un filtro trans-in-place deve usare lo stesso allocatore per le connessioni upstream e downstream. Il primo pin per la connessione (input o output) negozia un allocatore nel modo consueto. Quando l'altro pin si connette, tuttavia, il primo allocatore potrebbe non essere accettabile. In tal caso, il secondo pin sceglie un allocatore diverso e il primo pin si riconnette usando il nuovo allocatore. Per un'implementazione di esempio, vedere [**la classe CTransInPlaceFilter.**](ctransinplacefilter.md)

Nel metodo **ReconnectEx,** Filter Graph Manager disconnette e riconnette i pin in modo asincrono. Il filtro non deve tentare la riconnessione a meno **che QueryAccept non restituisca** S \_ OK. In caso contrario, il segnaposto verrà lasciato disconnesso, causando errori del grafico. Inoltre, il filtro deve richiedere la riconnessione dall'interno del metodo [**IPin::Connessione,**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) nello stesso thread. Se il **metodo Connessione** restituisce in un thread, mentre un altro thread effettua la richiesta di riconnessione, Filter Graph Manager potrebbe eseguire il grafo prima di eseguire la riconnessione, causando errori del grafico.

 

 



