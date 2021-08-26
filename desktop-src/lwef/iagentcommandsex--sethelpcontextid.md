---
title: IAgentCommandsEx SetHelpContextID
description: IAgentCommandsEx SetHelpContextID
ms.assetid: b49d8184-f8dd-4359-9d45-3f038af18da5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1e4ff5941d9f120c42cb2fa17d93a4f2a0c23e89d61dbee078b3ab5c3ffe611
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888241"
---
# <a name="iagentcommandsexsethelpcontextid"></a>IAgentCommandsEx::SetHelpContextID

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetHelpContextID(
   long ulHelpID  // ID for help topic
);
```

Imposta [**HelpContextID per**](helpcontextid-property.md) un [**oggetto**](/windows/desktop/lwef/the-command-object) Command.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulHelpID*
</dt> <dd>

Numero di contesto dell'argomento della Guida associato [**all'oggetto**](/windows/desktop/lwef/the-command-object) Command. utilizzato per fornire la Guida sensibile al contesto per il comando.

</dd> </dl>

Se è stato creato un Windows file della Guida per l'applicazione e si imposta questo valore nella proprietà [**HelpFile del**](helpfile-property.md) carattere. Agent chiama automaticamente la Guida [**quando HelpModeOn**](helpmodeon-property.md) è impostato **su True** e l'utente seleziona il comando. Se è presente un numero di contesto in [**HelpContextID**](helpcontextid-property.md), Agent chiama la Guida e cerca l'argomento identificato dal numero di contesto corrente. Il numero di contesto corrente è il valore **di HelpContextID** per il comando. Se è presente un numero di contesto nella proprietà **HelpContextID** del comando selezionato, la Guida visualizza un argomento corrispondente al contesto della Guida corrente. In caso contrario, viene visualizzato "Nessun argomento della Guida associato a questo elemento".

Questa proprietà si applica solo all'uso del carattere da parte dell'applicazione client. L'impostazione non influisce su altri client del carattere o di altri caratteri dell'applicazione client.

> [!Note]  
> La compilazione di un file della Guida richiede il compilatore della Guida Windows Microsoft.

 

## <a name="see-also"></a>Vedere anche

[**IAgentCommandsEx::GetHelpContextID**](iagentcommandsex--gethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)


 

 