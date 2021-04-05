---
title: IAgentCommandsEx GetHelpContextID
description: IAgentCommandsEx GetHelpContextID
ms.assetid: db5f93e9-8cd3-4147-94b4-50cfe12033c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a49a633a66622626973e450b9566033b1ad96e7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046662"
---
# <a name="iagentcommandsexgethelpcontextid"></a>IAgentCommandsEx::GetHelpContextID

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetHelpContextID(
   long * pulHelpID  // address of Commands object help topic ID
);
```

Recupera [**HelpContextID**](helpcontextid-property.md) per un oggetto [**comando**](/windows/desktop/lwef/the-command-object) .

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="pulHelpID"></span><span id="pulhelpid"></span><span id="PULHELPID"></span>*pulHelpID*
</dt> <dd>

Indirizzo di una variabile che riceve il numero di contesto dell'argomento della Guida per l'oggetto [**Command**](/windows/desktop/lwef/the-command-object) .

</dd> </dl>

Se è stato creato un file della Guida di Windows per l'applicazione e si è impostata la proprietà [**Filecommand**](/windows/desktop/lwef/the-command-object) [**del carattere**](helpfile-property.md) , l'agente Microsoft chiama automaticamente la guida quando [**HelpModeOn**](helpmodeon-property.md) è impostato su **true** e l'utente seleziona l'oggetto Command. Se è presente un numero di contesto in [**HelpContextID**](helpcontextid-property.md), Agent chiama la guida e cerca l'argomento identificato dal numero di contesto corrente. Il numero di contesto corrente è il valore di **HelpContextID** per l'oggetto **Command** .

Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.

> [!Note]  
> La compilazione di un file della guida richiede il compilatore della Guida di Microsoft Windows.

 

## <a name="see-also"></a>Vedere anche

[**IAgentCommandsEx:: SetHelpContextID**](iagentcommandsex--sethelpcontextid.md), [**IAgentCharacterEx:: SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx:: SetHelpFileName**](iagentcharacterex--sethelpfilename.md)


 

 