---
title: IAgentCommand getvoice
description: IAgentCommand getvoice
ms.assetid: 69f3c91b-2ccf-4bea-8034-0c3e0a5e4ec4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2365019f71447e9d9c5a560c6506ee1dae7423df
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299614"
---
# <a name="iagentcommandgetvoice"></a>IAgentCommand:: getvoice

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetVoice(
   BSTR * pbszVoice  // address of Voice setting for Command
);
```

Recupera il valore della proprietà del testo [**vocale**](voice-property.md) per un [**comando**](/windows/desktop/lwef/the-command-object).

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="pbszVoice"></span><span id="pbszvoice"></span><span id="PBSZVOICE"></span>*pbszVoice*
</dt> <dd>

Indirizzo di un BSTR che riceve la proprietà del testo [**vocale**](voice-property.md) per un [**comando**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

Un [**comando**](/windows/desktop/lwef/the-command-object) con la relativa proprietà [**Voice**](voice-property.md) impostata e la relativa proprietà [**Enabled**](enabled-property.md) impostata su **true** saranno accessibili per la voce. Se anche la relativa proprietà [**Caption**](caption-property.md) è impostata, viene visualizzata nella finestra dei comandi vocali. Se la proprietà [**Visible**](visible-property.md) è impostata su **true**, viene visualizzata nel menu di scelta rapida del carattere.

## <a name="see-also"></a>Vedere anche

[**IAgentCommand:: sevoice**](iagentcommand--setvoice.md), [**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md)


 

 