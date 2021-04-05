---
title: AddEx IAgentCommandsEx
description: AddEx IAgentCommandsEx
ms.assetid: 54be4793-89ac-475b-8a6a-5b8c18bb4b38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7487bb7c7af0295d82355c7a1f7fb50e30aa6e1f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725935"
---
# <a name="iagentcommandsexaddex"></a>IAgentCommandsEx:: AddEx

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT AddEx(
   BSTR bszCaption,       // Caption setting for Command
   BSTR bszVoice,         // Voice setting for Command
   BSTR bszVoiceCaption,  // VoiceCaption setting for Command
   long bEnabled,         // Enabled setting for Command
   long bVisible,         // Visible setting for Command
   long ulHelpID,         // HelpContextID setting for Command
   long * pdwID           // address for variable for ID
);
```

Aggiunge un [**comando**](/windows/desktop/lwef/the-command-object) a una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*
</dt> <dd>

BSTR che specifica il valore del testo della [**didascalia**](caption-property.md) visualizzato per un [**comando**](/windows/desktop/lwef/the-command-object) in una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> <dt>

<span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*
</dt> <dd>

BSTR che specifica il valore dell'impostazione del testo [**vocale**](voice-property.md) per un [**comando**](/windows/desktop/lwef/the-command-object) in una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> <dt>

<span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*
</dt> <dd>

BSTR che specifica il valore del testo [**VoiceCaption**](voicecaption-property.md) visualizzato per un [**comando**](/windows/desktop/lwef/the-command-object) in una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> <dt>

<span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*
</dt> <dd>

Espressione booleana che specifica l'impostazione [**Enabled**](enabled-property.md) per un [**comando**](/windows/desktop/lwef/the-command-object) in una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) . Se il parametro è **true**, il **comando** è abilitato e può essere selezionato. Se **false**, il **comando** è disabilitato.

</dd> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

Espressione booleana che specifica l'impostazione [**visibile**](visible-property.md) per un [**comando**](/windows/desktop/lwef/the-command-object) in una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) . Se il parametro è **true**, il **comando** sarà visibile nel menu popup del carattere (se viene impostata anche la proprietà [**Caption**](caption-property.md) ).

</dd> <dt>

<span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulHelpID*
</dt> <dd>

Il numero di contesto dell'argomento della Guida associato all'oggetto [**Command**](/windows/desktop/lwef/the-command-object) ; utilizzato per fornire la Guida sensibile al contesto per il comando.

</dd> <dt>

<span id="pdwID_"></span><span id="pdwid_"></span><span id="PDWID_"></span>*pdwID* 
</dt> <dd>

Indirizzo di una variabile che riceve l'ID per il [**comando**](/windows/desktop/lwef/the-command-object)aggiunto.

</dd> </dl>

[**IAgentCommandsEx:: AddEx**](https://www.bing.com/search?q=**IAgentCommandsEx::AddEx**) estende [**IAgentCommands:: Add**](iagentcommands--add.md) includendo la proprietà [**HelpContextID**](helpcontextid-property.md) . È inoltre possibile impostare la proprietà utilizzando [ **IAgentCommandsEx:: SetHelpContextID**](iagentcommandsex--sethelpcontextid.md)

## <a name="see-also"></a>Vedere anche

[**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommandsEx:: SetHelpContextID**](iagentcommandsex--sethelpcontextid.md), [**IAgentCommand:: Caption**](iagentcommand--setcaption.md), [**IAgentCommand:: seenabled**](iagentcommand--setenabled.md), [**IAgentCommand:: sevisible**](iagentcommand--setvisible.md), [**IAgentCommand:: sevoice**](iagentcommand--setvoice.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md), [**IAgentCommandsEx:: InsertEx**](iagentcommandsex--insertex.md), [**IAgentCommands:: Remove**](iagentcommands--remove.md), [**IAgentCommands:: RemoveAll**](iagentcommands--removeall.md)


 

 