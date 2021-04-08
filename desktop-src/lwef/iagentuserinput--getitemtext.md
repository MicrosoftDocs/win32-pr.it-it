---
title: GetItemText IAgentUserInput
description: GetItemText IAgentUserInput
ms.assetid: 69653806-c001-4015-bd05-3c261a312ede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7010172147f86282903641c46aa5137ce69c80be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104043976"
---
# <a name="iagentuserinputgetitemtext"></a>IAgentUserInput:: GetItemText

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetItemText(
   Long dwItemIndex,  // index of Command alternative
   BSTR * pbszText    // address of voice text for Command 
);
```

Recupera il testo vocale per un'alternativa del [**comando**](command-event.md) passata al callback [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwItemIndex*
</dt> <dd>

Indice di un'alternativa del [**comando**](command-event.md) passato al callback [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .

</dd> <dt>

<span id="pbszText"></span><span id="pbsztext"></span><span id="PBSZTEXT"></span>*pbszText*
</dt> <dd>

Indirizzo di un BSTR che riceve il valore del testo vocale per il [**comando**](command-event.md).

</dd> </dl>

Se l'input vocale non è l'origine del comando, ad esempio se l'utente ha selezionato il comando dal menu di scelta rapida del carattere, il server restituisce **null** per il testo vocale del [**comando**](command-event.md).

## <a name="see-also"></a>Vedere anche

[**IAgentUserInput:: GetItemConfidence**](iagentuserinput--getitemconfidence.md), [**IAgentUserInput:: GetItemID**](iagentuserinput--getitemid.md), [**IAgentUserInput:: GetAllItemData**](iagentuserinput--getallitemdata.md)


 

 




