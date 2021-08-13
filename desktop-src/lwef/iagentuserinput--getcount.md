---
title: IAgentUserInput GetCount
description: IAgentUserInput GetCount
ms.assetid: 9c127387-b680-405a-9a62-ee08cc70813a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f52c296dd152fd1e31a87e21d80f8b25d52ae880b300487cdcba746e81dfa0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749518"
---
# <a name="iagentuserinputgetcount"></a>IAgentUserInput::GetCount

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetCount(
   long * pdwCount  // address of a variable for number of alternatives 
);
```

Recupera il numero di alternative [**Command**](command-event.md) passate a un callback [**IAgentNotifySink::Command.**](iagentnotifysink--command.md)

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="pdwCount"></span><span id="pdwcount"></span><span id="PDWCOUNT"></span>*pdwCount*
</dt> <dd>

Indirizzo di una variabile che riceve il numero di alternative [**di**](command-event.md) comandi identificate dal server.

</dd> </dl>

Se l'input vocale non è l'origine del comando, ad esempio se l'utente ha selezionato il comando dal menu a comparsa del carattere, **GetCount** restituisce 1. Se **GetCount restituisce** zero (0), il motore di riconoscimento vocale ha rilevato l'input parlato, ma ha determinato che non è presente alcun comando corrispondente.

 

 




