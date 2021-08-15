---
title: IAgentCommandEx GetHelpContextID
description: IAgentCommandEx GetHelpContextID
ms.assetid: 97b390f3-ab24-4c09-aa87-d76076eba995
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d80f259b10adbdd1460f319b6fda4e5097c11136a5bf7ffde00a11d40a99656a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118750189"
---
# <a name="iagentcommandexgethelpcontextid"></a>IAgentCommandEx::GetHelpContextID

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetHelpContextID(
   long * pulID  //  address of command's help topic ID
);
```

Recupera [**HelpContextID per**](helpcontextid-property-com.md) un [**oggetto**](/windows/desktop/lwef/the-command-object) Command.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="pulID"></span><span id="pulid"></span><span id="PULID"></span>*pulID*
</dt> <dd>

Indirizzo di una variabile che riceve il numero di contesto dell'argomento della Guida associato [**all'oggetto**](/windows/desktop/lwef/the-command-object) Command.

</dd> </dl>

Se è stato creato un file della Guida di Windows per l'applicazione e la proprietà [**HelpFile**](helpfile-property.md) del carattere è stata impostata su questo file, Microsoft Agent chiama automaticamente la Guida quando [**HelpModeOn**](helpmodeon-property.md) è impostato su **True** e l'utente seleziona il comando. Se è presente un numero di contesto in [**HelpContextID**](helpcontextid-property-com.md), Agent chiama la Guida e cerca l'argomento identificato dal numero di contesto corrente. Il numero di contesto corrente è il valore **di HelpContextID** per il comando.

> [!Note]  
> Per compilare un file della Guida è necessario il compilatore della Guida Windows Microsoft.

 

## <a name="see-also"></a>Vedere anche

[**IAgentCommandEx::SetHelpContextID**](iagentcommandex--sethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)


 

 