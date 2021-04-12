---
title: IAgentCommandEx GetVoiceCaption
description: IAgentCommandEx GetVoiceCaption
ms.assetid: a81accfd-c137-4347-8ead-4ed5e7148751
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6f367a7956d1029eae47064a0778264e3b77f5a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104336935"
---
# <a name="iagentcommandexgetvoicecaption"></a>IAgentCommandEx::GetVoiceCaption

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetVoiceCaption(
   BSTR * pbszVoiceCaption  // address of command's voice caption text
);
```

Recupera [**VoiceCaption**](voicecaption-property.md) per un [**comando**](/windows/desktop/lwef/the-command-object).

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="pbszVoiceCaption"></span><span id="pbszvoicecaption"></span><span id="PBSZVOICECAPTION"></span>*pbszVoiceCaption*
</dt> <dd>

Indirizzo di un BSTR che riceve il valore del testo della [**didascalia**](caption-property.md) visualizzato per un [**comando**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

[**VoiceCaption**](voicecaption-property.md) è il testo visualizzato per un oggetto [**Command**](/windows/desktop/lwef/the-command-object) nella finestra comandi vocali quando l'applicazione client è di input-attivo.

## <a name="see-also"></a>Vedere anche

[**IAgentCommandEx:: SetVoiceCaption**](iagentcommandex--setvoicecaption.md), [**IAgentCommand:: IsEnabled**](iagentcommand--setenabled.md), [**IAgentCommand:: sevisible**](iagentcommand--setvisible.md), [**IAgentCommand:: sevoice**](iagentcommand--setvoice.md), [**IAgentCommandsEx:: AddEx**](iagentcommandsex--addex.md), [**IAgentCommandsEx:: InsertEx**](iagentcommandsex--insertex.md), [**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md)


 

 