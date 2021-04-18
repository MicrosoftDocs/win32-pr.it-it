---
title: IAgentCommand visibile
description: IAgentCommand visibile
ms.assetid: 58a383f4-6c98-4037-b469-ae68f06c852d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b583f79a93a5b13914486fb3e1a9cb513a682e63
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299769"
---
# <a name="iagentcommandsetvisible"></a>IAgentCommand:: sevisible

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetVisible(
   long bVisible  // Visible setting for Command
);
```

Imposta il valore della proprietà [**Visible**](visible-property.md) per un [**comando**](/windows/desktop/lwef/the-command-object).

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

Valore booleano che determina la proprietà [**Visible**](visible-property.md) di un [**comando**](/windows/desktop/lwef/the-command-object). **True** Mostra il **comando**; **False** lo nasconde.

</dd> </dl>

Un [**comando**](/windows/desktop/lwef/the-command-object) deve avere la proprietà [**Visible**](visible-property.md) impostata su **true** e la relativa proprietà [**Caption**](caption-property.md) impostata su viene visualizzata nel menu di scelta rapida del carattere.

## <a name="see-also"></a>Vedere anche

[**IAgentCommand:: getVisible**](iagentcommand--getvisible.md), [**IAgentCommand:: Caption**](iagentcommand--setcaption.md), [**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md)


 

 