---
description: Riconnessione di pin
ms.assetid: 34b3e4de-e4eb-48c5-aaef-fc99b63e8691
title: Riconnessione di pin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9fc71b4d5a62ee066edaa5f97b4cc3332b2231d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521321"
---
# <a name="reconnecting-pins"></a>Riconnessione di pin

Durante una connessione pin, un filtro può disconnettere e riconnettere uno degli altri pin, come indicato di seguito:

1.  Il filtro chiama [**Ipin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) sul pin dell'altro filtro e specifica il nuovo tipo di supporto.
2.  Se **QueryAccept** restituisce S \_ OK, il filtro chiama [**IFilterGraph2:: ReconnectEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) per riconnettere i pin.

Di seguito sono riportati alcuni esempi di quando un filtro potrebbe dover riconnettere i pin:

-   **Filtri tee.** Un *filtro Tee* suddivide un flusso di input in più output senza modificare i dati nel flusso. Un filtro Tee può accettare un intervallo di tipi di supporti, ma i tipi devono corrispondere in tutte le connessioni pin. Pertanto, quando il pin di input si connette, potrebbe essere necessario rinegoziare le connessioni esistenti nei pin di output e viceversa. Per un esempio, vedere l'esempio di [filtro InfTee](inftee-filter-sample.md).
-   **Filtri trans-on-Place.** Un filtro *Trans-on-Place* modifica i dati di input nel buffer originale anziché copiare i dati in un buffer di output separato. Un filtro Trans-on-Place deve usare lo stesso allocatore per le connessioni upstream e downstream. Il primo pin per connettersi (input o output) negozia un allocatore nel modo consueto. Quando l'altro pin si connette, tuttavia, il primo allocatore potrebbe non essere accettabile. In tal caso, il secondo pin sceglie un allocatore diverso e il primo pin si riconnette usando il nuovo allocatore. Per un'implementazione di esempio, vedere la classe [**CTransInPlaceFilter**](ctransinplacefilter.md) .

Nel metodo **ReconnectEx** , il gestore del grafico del filtro disconnette e riconnette in modo asincrono i pin. Il filtro non deve tentare la riconnessione, a meno che **QueryAccept** non restituisca S \_ OK. In caso contrario, il PIN verrà lasciato disconnesso, causando errori di grafo. Inoltre, il filtro deve richiedere la riconnessione dall'interno del metodo [**Ipin:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) nello stesso thread. Se il metodo **Connect** restituisce in un thread, mentre un altro thread esegue la richiesta di riconnessione, il grafico di gestione del filtro potrebbe eseguire il grafo prima di effettuare la riconnessione, causando errori di grafo.

 

 



