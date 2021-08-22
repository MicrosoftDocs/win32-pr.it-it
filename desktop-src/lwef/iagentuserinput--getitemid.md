---
title: IAgentUserInput GetItemID
description: IAgentUserInput GetItemID
ms.assetid: 3afd4d9d-51bb-4086-bf7b-7c9a2ddcd807
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde65fc10a4cb467bd69f200e3244f1a2a73c0424d64f6a4babbd2cefd18e0be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609261"
---
# <a name="iagentuserinputgetitemid"></a>IAgentUserInput::GetItemID

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetItemID(
   long dwItemIndex,    // index of Command alternative
   long * pdwCommandID  // address of a variable for number of alternatives 
);
```

Recupera l'identificatore di [**un'alternativa Command**](command-event.md) passata a un callback [**IAgentNotifySink::Command.**](iagentnotifysink--command.md)

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwItemIndex*
</dt> <dd>

Indice dell'alternativa [**Command**](command-event.md) passata al callback [**IAgentNotifySink::Command.**](iagentnotifysink--command.md)

</dd> <dt>

<span id="pdwCommandID"></span><span id="pdwcommandid"></span><span id="PDWCOMMANDID"></span>*pdwCommandID*
</dt> <dd>

Indirizzo di una variabile che riceve l'ID di un [**comando**](command-event.md).

</dd> </dl>

Se l'input vocale attiva il callback [**IAgentNotifySink::Command,**](iagentnotifysink--command.md) il [](command-event.md) server restituisce gli ID per tutti i comandi corrispondenti definiti dall'applicazione.

## <a name="see-also"></a>Vedere anche

[**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md), [**IAgentUserInput::GetItemText**](iagentuserinput--getitemtext.md), [**IAgentUserInput::GetAllItemData**](iagentuserinput--getallitemdata.md)


 

 




