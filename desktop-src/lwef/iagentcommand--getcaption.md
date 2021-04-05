---
title: IAgentCommand GetCaption
description: IAgentCommand GetCaption
ms.assetid: e333faca-e2c2-478a-a803-cbc401793e4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b44540ba9105e79ba675f8bf78be20e8961f98d0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872342"
---
# <a name="iagentcommandgetcaption"></a>IAgentCommand:: GetCaption

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetCaption(
   BSTR * pbszCaption  // address of Caption for Command
);
```

Recupera la [**didascalia**](caption-property.md) di un [**comando**](/windows/desktop/lwef/the-command-object).

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="pbszCaption"></span><span id="pbszcaption"></span><span id="PBSZCAPTION"></span>*pbszCaption*
</dt> <dd>

Indirizzo di un BSTR che riceve il valore del testo della [**didascalia**](caption-property.md) visualizzato per un [**comando**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

## <a name="see-also"></a>Vedere anche

[**IAgentCommand:: Caption**](iagentcommand--setcaption.md), [**IAgentCommand:: seenabled**](iagentcommand--setenabled.md), [**IAgentCommand:: sevisible**](iagentcommand--setvisible.md), [**IAgentCommand:: sevoice**](iagentcommand--setvoice.md), [**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md)


 

 