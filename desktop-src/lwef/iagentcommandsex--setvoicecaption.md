---
title: IAgentCommandsEx SetVoiceCaption
description: IAgentCommandsEx SetVoiceCaption
ms.assetid: f13c9ca5-70c9-42d0-b53c-45dc8980a24c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85de69b4b594f93adfb0ff554819243c94986420a79c35e8d7a64a3c2eaccb6f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716141"
---
# <a name="iagentcommandsexsetvoicecaption"></a>IAgentCommandsEx::SetVoiceCaption

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetVoiceCaption(
   BSTR bszVoiceCaption  // voice caption text
);
```

Imposta il [**testo VoiceCaption**](voicecaption-property.md) visualizzato per l'oggetto Command. [](/windows/desktop/lwef/the-command-object)

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*
</dt> <dd>

Oggetto BSTR che specifica il testo per la [**proprietà VoiceCaption**](voicecaption-property.md) per un [**oggetto Command.**](/windows/desktop/lwef/the-command-object)

</dd> </dl>

Se si definisce un [**oggetto Command**](/windows/desktop/lwef/the-command-object) in una raccolta [**Commands**](/windows/desktop/lwef/the-commands-collection-object) e si imposta la relativa [**proprietà Voice,**](voice-property.md) in genere si imposta anche la [**relativa proprietà VoiceCaption.**](voicecaption-property.md) Questo testo verrà visualizzato nella finestra Comandi vocali quando l'applicazione client è attiva per l'input e il carattere è visibile. Se questa proprietà non è impostata, l'impostazione della [**proprietà Caption**](caption-property.md) determina il testo visualizzato. Quando non è **impostata la proprietà VoiceCaption** o **Caption,** il comando non viene visualizzato nella finestra Comandi vocali.

## <a name="see-also"></a>Vedere anche

[**IAgentCommandsEx::GetVoiceCaption**](iagentcommandsex--getvoicecaption.md)


 

 