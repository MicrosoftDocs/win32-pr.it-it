---
title: IAgentCommandEx GetHelpContextID
description: IAgentCommandEx GetHelpContextID
ms.assetid: 97b390f3-ab24-4c09-aa87-d76076eba995
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f330e8ae8cd8bdaff5e27ccd00352b41b07be2b6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104399002"
---
# <a name="iagentcommandexgethelpcontextid"></a>IAgentCommandEx::GetHelpContextID

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetHelpContextID(
   long * pulID  //  address of command's help topic ID
);
```

Recupera [**HelpContextID**](helpcontextid-property-com.md) per un oggetto [**comando**](/windows/desktop/lwef/the-command-object) .

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="pulID"></span><span id="pulid"></span><span id="PULID"></span>*pulID*
</dt> <dd>

Indirizzo di una variabile che riceve il numero di contesto dell'argomento della Guida associato all'oggetto [**Command**](/windows/desktop/lwef/the-command-object) .

</dd> </dl>

Se è stato creato un file della Guida di Windows per l'applicazione e si imposta [**la proprietà**](helpfile-property.md) filecommand del carattere su questo file, l'agente Microsoft chiama automaticamente la guida quando [**HelpModeOn**](helpmodeon-property.md) è impostato su **true** e l'utente seleziona il comando. Se è presente un numero di contesto in [**HelpContextID**](helpcontextid-property-com.md), Agent chiama la guida e cerca l'argomento identificato dal numero di contesto corrente. Il numero di contesto corrente è il valore di **HelpContextID** per il comando.

> [!Note]  
> La compilazione di un file della guida richiede il compilatore della Guida di Microsoft Windows.

 

## <a name="see-also"></a>Vedere anche

[**IAgentCommandEx:: SetHelpContextID**](iagentcommandex--sethelpcontextid.md), [**IAgentCharacterEx:: SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx:: SetHelpFileName**](iagentcharacterex--sethelpfilename.md)


 

 