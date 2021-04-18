---
title: IAgentCommandsEx SetVoiceCaption
description: IAgentCommandsEx SetVoiceCaption
ms.assetid: f13c9ca5-70c9-42d0-b53c-45dc8980a24c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19fcc0f3ce98ff0187b7ed2f01b7131cc8e101bd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299700"
---
# <a name="iagentcommandsexsetvoicecaption"></a>IAgentCommandsEx::SetVoiceCaption

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetVoiceCaption(
   BSTR bszVoiceCaption  // voice caption text
);
```

Imposta il testo [**VoiceCaption**](voicecaption-property.md) visualizzato per l'oggetto [**Command**](/windows/desktop/lwef/the-command-object) .

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*
</dt> <dd>

BSTR che specifica il testo per la proprietà [**VoiceCaption**](voicecaption-property.md) per un [**comando**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

Se si definisce un oggetto [**Command**](/windows/desktop/lwef/the-command-object) in una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) e si imposta la relativa proprietà [**Voice**](voice-property.md) , in genere viene impostata anche la relativa proprietà [**VoiceCaption**](voicecaption-property.md) . Questo testo verrà visualizzato nella finestra comandi vocali quando l'applicazione client è di input-attivo e il carattere è visibile. Se questa proprietà non è impostata, l'impostazione per la proprietà [**Caption**](caption-property.md) determina il testo visualizzato. Quando non viene impostata la proprietà **VoiceCaption** o **Caption** , il comando non viene visualizzato nella finestra dei comandi vocali.

## <a name="see-also"></a>Vedere anche

[**IAgentCommandsEx::GetVoiceCaption**](iagentcommandsex--getvoicecaption.md)


 

 