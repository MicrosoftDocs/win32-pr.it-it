---
title: IAgentCharacterEx SetHelpFileName
description: IAgentCharacterEx SetHelpFileName
ms.assetid: 1f8d2bd7-5821-46c0-b371-7ecbc526df72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1342baecc1e059d4fcb5d1323c0c714bd6bf7087
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116828"
---
# <a name="iagentcharacterexsethelpfilename"></a>IAgentCharacterEx::SetHelpFileName

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetHelpFileName(
   BSTR bszName  // Help filename
);
```

Imposta HelpFileName per un carattere.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*
</dt> <dd>

Nome file della Guida per il carattere.

</dd> </dl>

Se è stato creato un file della Guida di Windows per l'applicazione e si è impostata [**la proprietà filecommand del carattere**](helpfile-property.md) , l'agente Microsoft chiama automaticamente la guida quando [**HelpModeOn**](helpmodeon-property.md) è impostato su **true** e l'utente fa clic sul carattere oppure seleziona un comando dal menu di scelta rapida. Se è presente un numero di contesto nella proprietà [**HelpContextID**](helpcontextid-property.md) del comando selezionato, nella Guida viene visualizzato un argomento corrispondente al contesto della Guida corrente. in caso contrario, viene visualizzato "nessun argomento della Guida associato a questo elemento".

Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.

> [!Note]  
> La compilazione di un file della guida richiede il compilatore della Guida di Microsoft Windows.

 

## <a name="see-also"></a>Vedere anche

[**IAgentCommandsEx:: SetHelpContextID**](iagentcommandsex--sethelpcontextid.md), [**IAgentCharacterEx:: SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx:: GetHelpFileName**](iagentcharacterex--gethelpfilename.md)


 

 




