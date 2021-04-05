---
title: IAgentCommandsEx SetHelpContextID
description: IAgentCommandsEx SetHelpContextID
ms.assetid: b49d8184-f8dd-4359-9d45-3f038af18da5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14ed692185adbd60a73085b367b30b14fb646ab6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725922"
---
# <a name="iagentcommandsexsethelpcontextid"></a>IAgentCommandsEx::SetHelpContextID

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetHelpContextID(
   long ulHelpID  // ID for help topic
);
```

Imposta [**HelpContextID**](helpcontextid-property.md) per un oggetto [**comando**](/windows/desktop/lwef/the-command-object) .

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulHelpID*
</dt> <dd>

Il numero di contesto dell'argomento della Guida associato all'oggetto [**Command**](/windows/desktop/lwef/the-command-object) ; utilizzato per fornire la Guida sensibile al contesto per il comando.

</dd> </dl>

Se è stato creato un file della Guida di Windows per l'applicazione e questo è stato impostato [**nella proprietà**](helpfile-property.md) fileguida del carattere. Agent chiama automaticamente la guida quando [**HelpModeOn**](helpmodeon-property.md) è impostato su **true** e l'utente seleziona il comando. Se è presente un numero di contesto in [**HelpContextID**](helpcontextid-property.md), Agent chiama la guida e cerca l'argomento identificato dal numero di contesto corrente. Il numero di contesto corrente è il valore di **HelpContextID** per il comando. Se è presente un numero di contesto nella proprietà **HelpContextID** del comando selezionato, help Visualizza un argomento corrispondente al contesto della Guida corrente. in caso contrario, viene visualizzato "nessun argomento della Guida associato a questo elemento".

Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.

> [!Note]  
> La compilazione di un file della guida richiede il compilatore della Guida di Microsoft Windows.

 

## <a name="see-also"></a>Vedere anche

[**IAgentCommandsEx:: GetHelpContextID**](iagentcommandsex--gethelpcontextid.md), [**IAgentCharacterEx:: SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx:: SetHelpFileName**](iagentcharacterex--sethelpfilename.md)


 

 