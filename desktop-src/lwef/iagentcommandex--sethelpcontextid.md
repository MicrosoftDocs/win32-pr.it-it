---
title: IAgentCommandEx SetHelpContextID
description: IAgentCommandEx SetHelpContextID
ms.assetid: 861d55dc-f584-495c-a148-016af8f7a3e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6b876276d42ff07081b60194e90beff3ad9ef19fec383c50d70a551e1c9a5e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118750193"
---
# <a name="iagentcommandexsethelpcontextid"></a>IAgentCommandEx::SetHelpContextID

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetHelpContextID(
   long ulID  //  ID for help topic
);
```

Imposta [**HelpContextID per**](helpcontextid-property-com.md) un [**oggetto**](/windows/desktop/lwef/the-command-object) Command.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="ulID"></span><span id="ulid"></span><span id="ULID"></span>*ulID*
</dt> <dd>

Numero di contesto dell'argomento della Guida associato [**all'oggetto**](/windows/desktop/lwef/the-command-object) Command. utilizzato per fornire la Guida sensibile al contesto per il comando.

</dd> </dl>

Se è stato creato un Windows file della Guida per l'applicazione e si imposta questo valore nella proprietà [**HelpFile del**](helpfile-property.md) carattere. Microsoft Agent chiama automaticamente la Guida quando [**HelpModeOn**](helpmodeon-property.md) è impostato su **True** e l'utente seleziona il comando. Se è presente un numero di contesto in [**HelpContextID**](helpcontextid-property-com.md), Agent chiama la Guida e cerca l'argomento identificato dal numero di contesto corrente. Il numero di contesto corrente è il valore **di HelpContextID** per il comando.

> [!Note]  
> La compilazione di un file della Guida richiede il compilatore della Guida Windows Microsoft.

 

## <a name="see-also"></a>Vedere anche

[**IAgentCommandEx::GetHelpContextID**](iagentcommandex--gethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)


 

 