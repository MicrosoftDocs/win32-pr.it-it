---
title: IAgentCommands GetCaption
description: IAgentCommands GetCaption
ms.assetid: bbaaaa20-c8c2-41af-a6fc-cf8849daa399
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f886413ae6bfbfe104306d7280d8c66b08bf311a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299610"
---
# <a name="iagentcommandsgetcaption"></a>IAgentCommands:: GetCaption

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetCaption(
   BSTR * pbszCaption  // address of Caption text for Commands collection
);
```

Recupera la [**didascalia**](caption-property.md) per una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="pbszCaption"></span><span id="pbszcaption"></span><span id="PBSZCAPTION"></span>*pbszCaption*
</dt> <dd>

Indirizzo di un BSTR che riceve il valore dell'impostazione del testo della [**didascalia**](caption-property.md) visualizzata per una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> </dl>

## <a name="see-also"></a>Vedere anche

[**IAgentCommands:: Caption**](iagentcommands--setcaption.md), [**IAgentCommands:: getVisible**](iagentcommands--getvisible.md), [**IAgentCommands:: getvoice**](iagentcommands--getvoice.md)


 

 