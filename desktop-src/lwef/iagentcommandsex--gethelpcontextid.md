---
title: IAgentCommandsEx GetHelpContextID
description: IAgentCommandsEx GetHelpContextID
ms.assetid: db5f93e9-8cd3-4147-94b4-50cfe12033c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8e15088eae1025daf7c98695dcf7fd610a04c30089028af0887107228de84b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961831"
---
# <a name="iagentcommandsexgethelpcontextid"></a>IAgentCommandsEx::GetHelpContextID

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetHelpContextID(
   long * pulHelpID  // address of Commands object help topic ID
);
```

Recupera [**HelpContextID per**](helpcontextid-property.md) un [**oggetto**](/windows/desktop/lwef/the-command-object) Command.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="pulHelpID"></span><span id="pulhelpid"></span><span id="PULHELPID"></span>*pulHelpID*
</dt> <dd>

Indirizzo di una variabile che riceve il numero di contesto dell'argomento della Guida per [**l'oggetto**](/windows/desktop/lwef/the-command-object) Command.

</dd> </dl>

Se è stato creato un file della Guida Windows per l'applicazione e si è impostata la proprietà [**HelpFile**](helpfile-property.md) del carattere, Microsoft Agent chiama automaticamente la Guida quando [**HelpModeOn**](helpmodeon-property.md) è impostato su **True** e l'utente seleziona l'oggetto [**Command.**](/windows/desktop/lwef/the-command-object) Se è presente un numero di contesto in [**HelpContextID,**](helpcontextid-property.md)Agent chiama la Guida e cerca l'argomento identificato dal numero di contesto corrente. Il numero di contesto corrente è il valore di **HelpContextID** per **l'oggetto** Command.

Questa proprietà si applica solo all'uso del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.

> [!Note]  
> La compilazione di un file della Guida richiede il compilatore della Guida Windows Microsoft.

 

## <a name="see-also"></a>Vedere anche

[**IAgentCommandsEx::SetHelpContextID,**](iagentcommandsex--sethelpcontextid.md) [**IAgentCharacterEx::SetHelpModeOn,**](iagentcharacterex--sethelpmodeon.md) [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)


 

 