---
title: IAgentCommandEx GetVoiceCaption
description: IAgentCommandEx GetVoiceCaption
ms.assetid: a81accfd-c137-4347-8ead-4ed5e7148751
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d093a971331c6c5cddf467e770dae69960ae0d616ddc9b37863a46d25becb7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105419"
---
# <a name="iagentcommandexgetvoicecaption"></a>IAgentCommandEx::GetVoiceCaption

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetVoiceCaption(
   BSTR * pbszVoiceCaption  // address of command's voice caption text
);
```

Recupera [**l'oggetto VoiceCaption**](voicecaption-property.md) per un [**oggetto Command.**](/windows/desktop/lwef/the-command-object)

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="pbszVoiceCaption"></span><span id="pbszvoicecaption"></span><span id="PBSZVOICECAPTION"></span>*pbszVoiceCaption*
</dt> <dd>

Indirizzo di un oggetto BSTR che riceve il valore del testo [**Della**](caption-property.md) didascalia visualizzato per un [**oggetto Command.**](/windows/desktop/lwef/the-command-object)

</dd> </dl>

[**VoiceCaption è**](voicecaption-property.md) il testo visualizzato per un oggetto [**Command**](/windows/desktop/lwef/the-command-object) nella finestra Comandi vocali quando l'applicazione client è attiva per l'input.

## <a name="see-also"></a>Vedere anche

[**IAgentCommandEx::SetVoiceCaption**](iagentcommandex--setvoicecaption.md), [**IAgentCommand::SetEnabled**](iagentcommand--setenabled.md), [**IAgentCommand::SetVisible**](iagentcommand--setvisible.md), [**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommandsEx::AddEx**](iagentcommandsex--addex.md), [**IAgentCommandsEx::InsertEx**](iagentcommandsex--insertex.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Add , IAgentCommands::Insert**](iagentcommands--insert.md)


 

 