---
title: IAgentUserInput GetAllItemData
description: IAgentUserInput GetAllItemData
ms.assetid: d1857b28-c745-4ed2-b49e-774f247e7348
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d74c59e05e021fdff05ee8991c4563a7a4be918f6ecb244c26402b5234b240b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105147"
---
# <a name="iagentuserinputgetallitemdata"></a>IAgentUserInput::GetAllItemData

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetAllItemData(
   VARIANT * pdwItemIndices,  // address of variable for alternative IDs
   VARIANT * plConfidences,   // address of variable for confidence scores
   VARIANT * pbszText         // address of variable for voice text
);
```

Recupera i dati per tutte [**le alternative Command**](command-event.md) passate a un callback [**IAgentNotifySink::Command.**](iagentnotifysink--command.md)

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="pdwItemIndices"></span><span id="pdwitemindices"></span><span id="PDWITEMINDICES"></span>*pdwItemIndices*
</dt> <dd>

Indirizzo di una variabile che riceve gli ID [**dei**](command-event.md) comandi passati al callback [**IAgentNotifySink::Command.**](iagentnotifysink--command.md)

</dd> <dt>

<span id="plConfidences"></span><span id="plconfidences"></span><span id="PLCONFIDENCES"></span>*plConfidences*
</dt> <dd>

Indirizzo di una variabile che riceve i punteggi di attendibilità per le alternative [**Command**](command-event.md) passate al callback [**IAgentNotifySink::Command.**](iagentnotifysink--command.md)

</dd> <dt>

<span id="pbszText"></span><span id="pbsztext"></span><span id="PBSZTEXT"></span>*pbszText*
</dt> <dd>

Indirizzo di una variabile che riceve il testo vocale per le alternative [**Command**](command-event.md) passate al callback [**IAgentNotifySink::Command.**](iagentnotifysink--command.md)

</dd> </dl>

Se l'input vocale attiva [**IAgentNotifySink::Command,**](iagentnotifysink--command.md)il server restituisce la corrispondenza migliore, la seconda migliore e la terza corrispondenza migliore, se vengono fornite dal motore di riconoscimento vocale. Fornisce i punteggi di attendibilità relativi, nell'intervallo compreso tra -100 e 100, e il testo effettivo "ascoltato" dal motore di riconoscimento vocale. Se la corrispondenza migliore è un comando fornito dal server, il server invia un ID NULL, ma invia comunque un punteggio di attendibilità e il [**testo**](voice-property.md) vocale.

se l'input vocale non è l'origine dell'evento; Ad esempio, se l'utente ha selezionato il comando dal menu a comparsa del [](command-event.md) carattere, il server Microsoft Agent restituisce l'ID del comando selezionato, con un punteggio di attendibilità pari a 100 e il testo vocale null. Le altre alternative restituiscono NULL con punteggi di attendibilità pari a zero (0) e testo vocale null.

> [!Note]  
> Non tutti i motori di riconoscimento vocale possono restituire tutti i valori per tutti i parametri di questo evento. Rivolgersi al fornitore del motore per determinare se il motore supporta l'interfaccia microsoft Speech API per la restituzione di alternative e punteggi di attendibilità.

 

## <a name="see-also"></a>Vedere anche

[**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md), [**IAgentUserInput::GetItemText**](iagentuserinput--getitemtext.md), [**IAgentUserInput::GetItemID**](iagentuserinput--getitemid.md)


 

 




