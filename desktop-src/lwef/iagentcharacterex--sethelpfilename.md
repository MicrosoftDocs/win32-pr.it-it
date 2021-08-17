---
title: IAgentCharacterEx SetHelpFileName
description: IAgentCharacterEx SetHelpFileName
ms.assetid: 1f8d2bd7-5821-46c0-b371-7ecbc526df72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c9852e5909410f7e51789dd92419af4ef12f11ab0ae7ad0729a26b96a06fe34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477949"
---
# <a name="iagentcharacterexsethelpfilename"></a>IAgentCharacterEx::SetHelpFileName

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetHelpFileName(
   BSTR bszName  // Help filename
);
```

Imposta HelpFileName per un carattere.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*
</dt> <dd>

Nome file della Guida per il carattere.

</dd> </dl>

Se è stato creato un file della Guida di Windows per l'applicazione e si è impostata la proprietà [**HelpFile**](helpfile-property.md) del carattere, Microsoft Agent chiama automaticamente la Guida quando [**HelpModeOn**](helpmodeon-property.md) è impostato su **True** e l'utente fa clic sul carattere o seleziona un comando dal menu a comparsa. Se è presente un numero di contesto nella [**proprietà HelpContextID**](helpcontextid-property.md) del comando selezionato, la Guida visualizza un argomento corrispondente al contesto corrente della Guida. in caso contrario, viene visualizzato "Nessun argomento della Guida associato a questo elemento".

Questa proprietà si applica solo all'uso del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.

> [!Note]  
> La compilazione di un file della Guida richiede il compilatore della Guida Windows Microsoft.

 

## <a name="see-also"></a>Vedere anche

[**IAgentCommandsEx::SetHelpContextID,**](iagentcommandsex--sethelpcontextid.md) [**IAgentCharacterEx::SetHelpModeOn,**](iagentcharacterex--sethelpmodeon.md) [**IAgentCharacterEx::GetHelpFileName**](iagentcharacterex--gethelpfilename.md)


 

 




