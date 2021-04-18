---
title: IAgentUserInput GetItemID
description: IAgentUserInput GetItemID
ms.assetid: 3afd4d9d-51bb-4086-bf7b-7c9a2ddcd807
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 716ae1386d87fa6051111801c5603837519eeb4c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297597"
---
# <a name="iagentuserinputgetitemid"></a>IAgentUserInput:: GetItemID

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetItemID(
   long dwItemIndex,    // index of Command alternative
   long * pdwCommandID  // address of a variable for number of alternatives 
);
```

Recupera l'identificatore di un'alternativa del [**comando**](command-event.md) passata a un callback [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwItemIndex*
</dt> <dd>

Indice dell'alternativa del [**comando**](command-event.md) passato al callback [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .

</dd> <dt>

<span id="pdwCommandID"></span><span id="pdwcommandid"></span><span id="PDWCOMMANDID"></span>*pdwCommandID*
</dt> <dd>

Indirizzo di una variabile che riceve l'ID di un [**comando**](command-event.md).

</dd> </dl>

Se l'input vocale attiva il callback [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) , il server restituisce gli ID per tutti i [**comandi**](command-event.md) corrispondenti definiti dall'applicazione.

## <a name="see-also"></a>Vedere anche

[**IAgentUserInput:: GetItemConfidence**](iagentuserinput--getitemconfidence.md), [**IAgentUserInput:: GetItemText**](iagentuserinput--getitemtext.md), [**IAgentUserInput:: GetAllItemData**](iagentuserinput--getallitemdata.md)


 

 




