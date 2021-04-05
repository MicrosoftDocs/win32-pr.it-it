---
title: IAgentCharacter GetVisible
description: IAgentCharacter GetVisible
ms.assetid: 6e8e3a68-a7bb-4afb-a753-836fe82a0b24
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0593b9b3a193b9d5910888b81b4ecba90469b1e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117595"
---
# <a name="iagentcharactergetvisible"></a>IAgentCharacter:: GetVisible

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for character Visible setting
);
```

Determina se il frame di animazione del carattere è attualmente visibile.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*
</dt> <dd>

Indirizzo di una variabile che riceve **true** se il frame del carattere è visibile e **false** se è nascosto.

</dd> </dl>

È possibile utilizzare questo metodo per determinare se il frame del carattere è attualmente visibile. Per rendere visibile un carattere, usare il metodo [**show**](/windows/desktop/lwef/iagentcharacter--show) . Per nascondere un carattere, usare il metodo [**Hide**](/windows/desktop/lwef/iagentcharacter--hide) .

 

 