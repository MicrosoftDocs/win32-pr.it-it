---
title: IAgentCommandsEx GetVoiceCaption
description: IAgentCommandsEx GetVoiceCaption
ms.assetid: 0e505295-386a-421f-a43c-6da03c8a2b6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec2a6d5138b9b7074d1c9a2002f45a0076fe5d957ae5e47d865c693f73e8b37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609434"
---
# <a name="iagentcommandsexgetvoicecaption"></a>IAgentCommandsEx::GetVoiceCaption

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetVoiceCaption(
   BSTR * pbszVoiceCaption  // address of command's voice caption
);
```

Recupera [**l'oggetto VoiceCaption**](voicecaption-property.md) per un [**oggetto**](/windows/desktop/lwef/the-command-object) Command.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="pbszVoiceCaption"></span><span id="pbszvoicecaption"></span><span id="PBSZVOICECAPTION"></span>*pbszVoiceCaption*
</dt> <dd>

Indirizzo di un oggetto BSTR che riceve il valore del testo [**della**](caption-property.md) didascalia visualizzato per un [**oggetto Command.**](/windows/desktop/lwef/the-command-object)

</dd> </dl>

Il testo restituito è impostato per [**l'oggetto Command**](/windows/desktop/lwef/the-command-object) e viene visualizzato nella finestra Comandi vocali quando l'applicazione client è attiva per l'input.

Questa proprietà si applica solo all'uso del carattere da parte dell'applicazione client. L'impostazione non influisce su altri client del carattere o di altri caratteri dell'applicazione client.

## <a name="see-also"></a>Vedere anche

[**IAgentCommandsEx::SetVoiceCaption**](iagentcommandsex--setvoicecaption.md)


 

 