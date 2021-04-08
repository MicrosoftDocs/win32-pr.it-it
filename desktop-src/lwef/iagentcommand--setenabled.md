---
title: IAgentCommand abilitato
description: IAgentCommand abilitato
ms.assetid: e0a724b4-3613-400f-a801-efc8bf66e355
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8377307d66257f7a9b74ac82512edc6e4ec64034
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046618"
---
# <a name="iagentcommandsetenabled"></a>IAgentCommand:: IsEnabled

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetEnabled(
   long bEnabled  // Enabled setting for Command
);
```

Imposta la proprietà [**Enabled**](enabled-property.md) per un [**comando**](/windows/desktop/lwef/the-command-object).

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*
</dt> <dd>

Valore booleano che imposta il valore dell'impostazione [**Enabled**](enabled-property.md) di un [**comando**](/windows/desktop/lwef/the-command-object). **True** Abilita il **comando**; **False** lo Disabilita. Non è possibile selezionare un **comando** disabilitato.

</dd> </dl>

Un [**comando**](/windows/desktop/lwef/the-command-object) deve avere la proprietà [**Enabled**](enabled-property.md) impostata su **true** per essere selezionabile. È inoltre necessario impostare la relativa proprietà [**Caption**](caption-property.md) e la relativa proprietà [**Visible**](visible-property.md) su **true** per la visualizzazione nel menu popup del carattere. Per fare in modo che il **comando** venga visualizzato nella **finestra comandi vocali**, è necessario impostare la relativa proprietà [**Voice**](voice-property.md).

## <a name="see-also"></a>Vedere anche

[**IAgentCommand:: GetCaption**](iagentcommand--getcaption.md), [**IAgentCommand:: sevoice**](iagentcommand--setvoice.md), [**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md)


 

 