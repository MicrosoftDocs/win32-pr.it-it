---
title: GetID IAgentCommand
description: GetID IAgentCommand
ms.assetid: 4d8d8be7-7003-4ef3-abba-b5232267c993
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d1f5887123df19496c0610c53fe59a3f64961cd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398865"
---
# <a name="iagentcommandgetid"></a>IAgentCommand:: GetID

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetID(
   long * pdwID  // address of ID for Command
);
```

Recupera l'ID per un [**comando**](/windows/desktop/lwef/the-command-object).

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="pdwID"></span><span id="pdwid"></span><span id="PDWID"></span>*pdwID*
</dt> <dd>

Indirizzo di una variabile che riceve l'ID di un [**comando**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

## <a name="see-also"></a>Vedere anche

[**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md), [**IAgentCommands:: Remove**](iagentcommands--remove.md)


 

 