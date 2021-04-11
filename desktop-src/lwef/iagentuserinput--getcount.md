---
title: IAgentUserInput GetCount
description: IAgentUserInput GetCount
ms.assetid: 9c127387-b680-405a-9a62-ee08cc70813a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ac4b597f7367eff10154bde256698ef371c3619
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104220857"
---
# <a name="iagentuserinputgetcount"></a>IAgentUserInput:: GetCount

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetCount(
   long * pdwCount  // address of a variable for number of alternatives 
);
```

Recupera il numero di alternative del [**comando**](command-event.md) passate a un callback [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="pdwCount"></span><span id="pdwcount"></span><span id="PDWCOUNT"></span>*pdwCount*
</dt> <dd>

Indirizzo di una variabile che riceve il numero di [**comandi**](command-event.md) alternativi identificati dal server.

</dd> </dl>

Se l'input vocale non è l'origine del comando, ad esempio se l'utente ha selezionato il comando dal menu di scelta rapida del carattere, **GetCount** restituisce 1. Se **GetCount** restituisce zero (0), il motore di riconoscimento vocale ha rilevato l'input parlato ma ha determinato che non esiste alcun comando corrispondente.

 

 




