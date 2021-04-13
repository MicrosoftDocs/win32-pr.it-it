---
title: IAgentUserInput GetItemConfidence
description: IAgentUserInput GetItemConfidence
ms.assetid: 7d1ca2f0-416c-43c3-99a8-9f287cb88de1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 846e1fca9ea1245a62fc68330d68263b63fb7cfd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328199"
---
# <a name="iagentuserinputgetitemconfidence"></a>IAgentUserInput::GetItemConfidence

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetItemConfidence(
   long dwItemIndex,    // index of Command alternative
   long * plConfidence  // address of confidence value for Command 
);
```

Recupera il valore di confidenza per un [**comando**](command-event.md) passato a un callback [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwItemIndex*
</dt> <dd>

Indice di un'alternativa del [**comando**](command-event.md) passato al callback [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .

</dd> <dt>

<span id="plConfidence"></span><span id="plconfidence"></span><span id="PLCONFIDENCE"></span>*plConfidence*
</dt> <dd>

Indirizzo di una variabile che riceve il Punteggio di confidenza per un'alternativa del [**comando**](command-event.md) passata al callback [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .

</dd> </dl>

Se l'input vocale non è l'origine del comando, ad esempio se l'utente ha selezionato il comando dal menu popup del carattere, il server Microsoft Agent restituisce il valore di confidenza della corrispondenza migliore come 100 e i valori di confidenza per tutte le altre alternative come zero (0).

## <a name="see-also"></a>Vedere anche

[**IAgentUserInput:: GetItemID**](iagentuserinput--getitemid.md), [**IAgentUserInput:: GetAllItemData**](iagentuserinput--getallitemdata.md), [**IAgentUserInput:: GetItemText**](iagentuserinput--getitemtext.md)


 

 




