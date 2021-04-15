---
title: IAgentUserInput GetAllItemData
description: IAgentUserInput GetAllItemData
ms.assetid: d1857b28-c745-4ed2-b49e-774f247e7348
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ced6a618d4fbbc093bf54c19fc393b7e195f2069
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104470742"
---
# <a name="iagentuserinputgetallitemdata"></a>IAgentUserInput::GetAllItemData

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetAllItemData(
   VARIANT * pdwItemIndices,  // address of variable for alternative IDs
   VARIANT * plConfidences,   // address of variable for confidence scores
   VARIANT * pbszText         // address of variable for voice text
);
```

Recupera i dati per tutte le alternative di [**comando**](command-event.md) passate a un callback [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="pdwItemIndices"></span><span id="pdwitemindices"></span><span id="PDWITEMINDICES"></span>*pdwItemIndices*
</dt> <dd>

Indirizzo di una variabile che riceve gli ID dei [**comandi**](command-event.md) passati al callback [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .

</dd> <dt>

<span id="plConfidences"></span><span id="plconfidences"></span><span id="PLCONFIDENCES"></span>*plConfidences*
</dt> <dd>

Indirizzo di una variabile che riceve i punteggi di confidenza per le alternative del [**comando**](command-event.md) passate al callback [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .

</dd> <dt>

<span id="pbszText"></span><span id="pbsztext"></span><span id="PBSZTEXT"></span>*pbszText*
</dt> <dd>

Indirizzo di una variabile che riceve il testo vocale per le alternative del [**comando**](command-event.md) passate al callback [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .

</dd> </dl>

Se l'input vocale attiva [**IAgentNotifySink:: Command**](iagentnotifysink--command.md), il server restituisce la migliore corrispondenza, la seconda corrispondenza migliore e la terza corrispondenza migliore, se vengono fornite dal motore di riconoscimento vocale. Fornisce i punteggi di confidenza relativi, nell'intervallo da-100 a 100 e il testo effettivo "sentito" dal motore di riconoscimento vocale. Se la corrispondenza migliore era un comando fornito dal server, il server invia un ID NULL, ma invia comunque un punteggio di confidenza e il testo [**vocale**](voice-property.md) .

Se l'input vocale non è l'origine dell'evento. Se, ad esempio, l'utente ha selezionato il comando dal menu popup del carattere, il server Microsoft Agent restituisce l'ID del [**comando**](command-event.md) selezionato, con un punteggio di confidenza pari a 100 e il testo vocale come null. Le altre alternative restituiscono come NULL con i punteggi di confidenza pari a zero (0) e il testo vocale come NULL.

> [!Note]  
> Non tutti i motori di riconoscimento vocale possono restituire tutti i valori per tutti i parametri di questo evento. Rivolgersi al fornitore del motore per determinare se il motore supporta l'interfaccia di Microsoft Speech API per la restituzione di alternative e punteggi di confidenza.

 

## <a name="see-also"></a>Vedere anche

[**IAgentUserInput:: GetItemConfidence**](iagentuserinput--getitemconfidence.md), [**IAgentUserInput:: GetItemText**](iagentuserinput--getitemtext.md), [**IAgentUserInput:: GetItemID**](iagentuserinput--getitemid.md)


 

 




