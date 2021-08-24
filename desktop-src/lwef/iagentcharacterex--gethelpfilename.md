---
title: IAgentCharacterEx GetHelpFileName
description: IAgentCharacterEx GetHelpFileName
ms.assetid: 52d5a874-ad3e-4833-9e3e-ff485414c54c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba5acdcfef90d1918f5c4697127b4449e96f2667b20a2de0230fcdf2cd6dd43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105529"
---
# <a name="iagentcharacterexgethelpfilename"></a>IAgentCharacterEx::GetHelpFileName

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetHelpFileName(
   BSTR * pbszName  // address of Help filename
);
```

Recupera HelpFileName per un carattere.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="pbszName"></span><span id="pbszname"></span><span id="PBSZNAME"></span>*pbszName*
</dt> <dd>

Indirizzo di una variabile che riceve il nome file della Guida per il carattere.

</dd> </dl>

Se è stato creato un file della Guida di Windows per l'applicazione e si è impostata la proprietà [**HelpFile**](helpfile-property.md) del carattere, Microsoft Agent chiama automaticamente la Guida quando [**HelpModeOn**](helpmodeon-property.md) è impostato su **True** e l'utente fa clic sul carattere o seleziona un comando dal menu a comparsa. Se è presente un numero di contesto nella proprietà [**HelpContextID**](helpcontextid-property.md) del comando selezionato, la Guida visualizza un argomento corrispondente al contesto della Guida corrente. In caso contrario, viene visualizzato "Nessun argomento della Guida associato a questo elemento".

Questa proprietà si applica solo all'uso del carattere da parte dell'applicazione client. L'impostazione non influisce su altri client del carattere o di altri caratteri dell'applicazione client.

> [!Note]  
> La compilazione di un file della Guida richiede il compilatore della Guida Windows Microsoft.

 

## <a name="see-also"></a>Vedere anche

[**IAgentCommandsEx::SetHelpContextID**](iagentcommandsex--sethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)


 

 




