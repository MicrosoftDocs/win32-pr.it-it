---
title: IAgentCommandEx SetVoiceCaption
description: IAgentCommandEx SetVoiceCaption
ms.assetid: 672fdc13-25d3-4ced-b295-2b687767c17f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe76edb17c2b099db5e16e2b6160703c6b11e8a9f52bcbc24a9ca4bfcb7077c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477214"
---
# <a name="iagentcommandexsetvoicecaption"></a>IAgentCommandEx::SetVoiceCaption

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetVoiceCaption(
   BSTR bszVoiceCaption  // voice caption text
);
```

Imposta il [**testo VoiceCaption**](voicecaption-property.md) visualizzato per un [**oggetto Command.**](/windows/desktop/lwef/the-command-object)

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*
</dt> <dd>

Oggetto BSTR che specifica il testo per la [**proprietà VoiceCaption**](voicecaption-property.md) per un [**oggetto Command.**](/windows/desktop/lwef/the-command-object)

</dd> </dl>

Se si definisce un [**oggetto Command**](/windows/desktop/lwef/the-command-object) in una raccolta [**Commands**](/windows/desktop/lwef/the-commands-collection-object) e si imposta la relativa [**proprietà Voice,**](voice-property.md) in genere si imposta anche la [**relativa proprietà VoiceCaption.**](voicecaption-property.md) Questo testo verrà visualizzato nella finestra Comandi vocali quando l'applicazione client è attiva per l'input. Se questa proprietà non è impostata, l'impostazione della proprietà [**Caption**](caption-property.md) determina il testo visualizzato. Quando non è **impostata né la proprietà VoiceCaption** né la proprietà , il comando non viene visualizzato nella finestra Comandi vocali.

[**Didascalia**](caption-property.md)

## <a name="see-also"></a>Vedere anche

[**IAgentCommand::GetCaption**](iagentcommand--getcaption.md), [**IAgentCommand::SetEnabled**](iagentcommand--setenabled.md), [**IAgentCommand::SetVisible**](iagentcommand--setvisible.md), [**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommandsEx::AddEx**](iagentcommandsex--addex.md), [**IAgentCommandsEx::InsertEx**](iagentcommandsex--insertex.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)


 

 