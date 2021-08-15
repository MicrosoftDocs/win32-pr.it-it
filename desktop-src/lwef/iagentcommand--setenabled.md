---
title: IAgentCommand SetEnabled
description: IAgentCommand SetEnabled
ms.assetid: e0a724b4-3613-400f-a801-efc8bf66e355
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da164b6603d93496e3381ccc6938a3b6d8f520bcea887cfd11f031cec7d845a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976311"
---
# <a name="iagentcommandsetenabled"></a>IAgentCommand::SetEnabled

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetEnabled(
   long bEnabled  // Enabled setting for Command
);
```

Imposta la [**proprietà Enabled**](enabled-property.md) per un [**oggetto Command.**](/windows/desktop/lwef/the-command-object)

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*
</dt> <dd>

Valore booleano che imposta il valore [**dell'impostazione Enabled**](enabled-property.md) di un [**oggetto Command**](/windows/desktop/lwef/the-command-object). **True abilita** il **comando**; **False** la disabilita. Non è **possibile selezionare un** comando disabilitato.

</dd> </dl>

Per [**poter essere**](/windows/desktop/lwef/the-command-object) selezionabile, un comando deve avere la proprietà [**Enabled**](enabled-property.md) impostata su **True.** Deve anche avere la proprietà [**Caption**](caption-property.md) impostata e la relativa [**proprietà Visible**](visible-property.md) impostata su **True** per essere visualizzata nel menu a comparsa del carattere. Per visualizzare **il comando** nella finestra Comandi **vocali**, è necessario impostarne la [**proprietà**](voice-property.md)Voce.

## <a name="see-also"></a>Vedere anche

[**IAgentCommand::GetCaption**](iagentcommand--getcaption.md), [**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)


 

 