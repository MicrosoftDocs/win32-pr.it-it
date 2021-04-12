---
title: IAgentCommand GetEnabled
description: IAgentCommand GetEnabled
ms.assetid: b4ec25d2-b2e0-4b1b-8dc5-10fbb44149b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 238844a70ea7fde3ef0c07cad1a6f3abab5613d1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472931"
---
# <a name="iagentcommandgetenabled"></a>IAgentCommand:: GetEnabled

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetEnabled(
   long * pbEnabled  // address of Enabled setting for Command
);
```

Recupera il valore della proprietà [**Enabled**](enabled-property.md) per un [**comando**](/windows/desktop/lwef/the-command-object).

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*
</dt> <dd>

Indirizzo di una variabile che riceve **true** se il [**comando**](/windows/desktop/lwef/the-command-object) è abilitato oppure **false** se è disabilitato. Non è possibile selezionare un **comando** disabilitato.

</dd> </dl>

## <a name="see-also"></a>Vedere anche

[**IAgentCommand:: Caption**](iagentcommand--setcaption.md), [**IAgentCommand:: sevisible**](iagentcommand--setvisible.md), [**IAgentCommand:: sevoice**](iagentcommand--setvoice.md), [**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md)


 

 