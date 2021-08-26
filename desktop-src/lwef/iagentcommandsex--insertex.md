---
title: IAgentCommandsEx InsertEx
description: IAgentCommandsEx InsertEx
ms.assetid: 037c47df-f026-42dc-8c37-2704518d3fd2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2b43a9e449e16a3be3017a67082da20cb31eb1352a81f699908b0b94267ea90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961821"
---
# <a name="iagentcommandsexinsertex"></a>IAgentCommandsEx::InsertEx

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT InsertEx(
   BSTR bszCaption,       // Caption setting for Command
   BSTR bszVoice,         // Voice setting for Command
   BSTR bszVoiceCaption,  // VoiceCaption setting for Command
   long bEnabled,         // Enabled setting for Command
   long bVisible,         // Visible setting for Command
   long ulHelpID,         // HelpContextID setting for Command
   long dwRefID,          // reference Command for insertion
   long dBefore,          // insertion position flag
   long * pdwID           // address for variable for Command ID
);
```

Inserisce un [**oggetto Command**](/windows/desktop/lwef/the-command-object) in una [**raccolta Commands.**](/windows/desktop/lwef/the-commands-collection-object)

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*
</dt> <dd>

Valore BSTR che specifica il valore del testo [**della**](caption-property.md) didascalia visualizzato per il [**comando**](/windows/desktop/lwef/the-command-object).

</dd> <dt>

<span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*
</dt> <dd>

Valore BSTR che specifica il valore dell'impostazione [**Testo**](voice-property.md) vocale per un [**comando**](/windows/desktop/lwef/the-command-object).

</dd> <dt>

<span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*
</dt> <dd>

Oggetto BSTR che specifica il valore del testo [**VoiceCaption**](voicecaption-property.md) visualizzato per un [**oggetto Command**](/windows/desktop/lwef/the-command-object) in una [**raccolta Commands.**](/windows/desktop/lwef/the-commands-collection-object)

</dd> <dt>

<span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*
</dt> <dd>

Espressione booleana che specifica [**l'impostazione Enabled**](enabled-property.md) per un [**oggetto Command.**](/windows/desktop/lwef/the-command-object) Se il parametro è **True,** il **comando** è abilitato e può essere selezionato. se **False,** il **comando è** disabilitato.

</dd> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

Espressione booleana che specifica [**l'impostazione Visible**](visible-property.md) per un [**oggetto Command.**](/windows/desktop/lwef/the-command-object) Se il parametro **è True,** **il comando** sarà visibile nel menu a comparsa del carattere (se è impostata anche la proprietà [**Caption).**](caption-property.md)

</dd> <dt>

<span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulHelpID*
</dt> <dd>

Numero di contesto dell'argomento della Guida associato [**all'oggetto**](/windows/desktop/lwef/the-command-object) Command. utilizzato per fornire la Guida sensibile al contesto per il comando.

</dd> <dt>

<span id="dwRefID"></span><span id="dwrefid"></span><span id="DWREFID"></span>*dwRefID*
</dt> <dd>

ID di un comando [**usato**](/windows/desktop/lwef/the-command-object) come riferimento per l'inserimento relativo del nuovo **comando**.

</dd> <dt>

<span id="dBefore"></span><span id="dbefore"></span><span id="DBEFORE"></span>*dBefore*
</dt> <dd>

Espressione booleana che specifica dove inserire l'oggetto [**Command.**](/windows/desktop/lwef/the-command-object) Se questo parametro è **True,** il nuovo comando viene inserito prima **del** comando a cui si fa **riferimento;** se **False**, il nuovo **comando viene inserito** dopo il comando a cui si fa **riferimento.**

</dd> <dt>

<span id="pdwID_"></span><span id="pdwid_"></span><span id="PDWID_"></span>*pdwID* 
</dt> <dd>

Indirizzo di una variabile che riceve l'ID per il comando [**inserito.**](/windows/desktop/lwef/the-command-object)

</dd> </dl>

[**IAgentCommandsEx::InsertEx**](https://www.bing.com/search?q=**IAgentCommandsEx::InsertEx**) estende [**IAgentCommands::Insert**](iagentcommands--insert.md) includendo la [**proprietà HelpContextID.**](helpcontextid-property.md) È anche possibile impostare la proprietà [ **usando IAgentCommandsEx::SetHelpContextID**](iagentcommandsex--sethelpcontextid.md)

## <a name="see-also"></a>Vedere anche

[**IAgentCommandsEx::AddEx**](iagentcommandsex--addex.md), [**IAgentCommandsEx::SetHelpContextID**](iagentcommandsex--sethelpcontextid.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Remove**](iagentcommands--remove.md), [**IAgentCommands::RemoveAll**](iagentcommands--removeall.md)


 

 