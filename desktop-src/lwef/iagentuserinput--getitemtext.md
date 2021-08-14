---
title: IAgentUserInput GetItemText
description: IAgentUserInput GetItemText
ms.assetid: 69653806-c001-4015-bd05-3c261a312ede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd9c1392bd56e3bb59212edeb79d862260786edb87583c0e8fdf049e8345b40
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119359041"
---
# <a name="iagentuserinputgetitemtext"></a>IAgentUserInput::GetItemText

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetItemText(
   Long dwItemIndex,  // index of Command alternative
   BSTR * pbszText    // address of voice text for Command 
);
```

Recupera il testo vocale per [**un'alternativa Command**](command-event.md) passata al callback [**IAgentNotifySink::Command.**](iagentnotifysink--command.md)

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwItemIndex*
</dt> <dd>

Indice di un'alternativa [**Command**](command-event.md) passata al callback [**IAgentNotifySink::Command.**](iagentnotifysink--command.md)

</dd> <dt>

<span id="pbszText"></span><span id="pbsztext"></span><span id="PBSZTEXT"></span>*pbszText*
</dt> <dd>

Indirizzo di un BSTR che riceve il valore del testo vocale per il [**comando**](command-event.md).

</dd> </dl>

Se l'input vocale non è l'origine del comando, ad esempio se l'utente ha selezionato il [](command-event.md)comando dal menu a comparsa del carattere, il server restituisce **NULL** per il testo vocale del comando.

## <a name="see-also"></a>Vedere anche

[**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md), [**IAgentUserInput::GetItemID**](iagentuserinput--getitemid.md), [**IAgentUserInput::GetAllItemData**](iagentuserinput--getallitemdata.md)


 

 




