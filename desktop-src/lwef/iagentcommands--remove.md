---
title: Rimozione di IAgentCommands
description: Rimozione di IAgentCommands
ms.assetid: 1f41aa2d-e50b-48a8-87fc-fda4730b035a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5875d1377aecc7e28554bac6aae1ccb2b4f515f730a6ab1b0b3a83cec7573418
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477194"
---
# <a name="iagentcommandsremove"></a>IAgentCommands::Remove

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT Remove(
   long dwID  // Command ID
);
```

Rimuove l'oggetto [**Command**](/windows/desktop/lwef/the-command-object) specificato da una [**raccolta Commands.**](/windows/desktop/lwef/the-commands-collection-object)

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="dwID"></span><span id="dwid"></span><span id="DWID"></span>*dwID*
</dt> <dd>

ID di un [**comando**](/windows/desktop/lwef/the-command-object) da rimuovere dalla [**raccolta Commands.**](/windows/desktop/lwef/the-commands-collection-object)

</dd> </dl>

La rimozione di [**un comando**](/windows/desktop/lwef/the-command-object) da una raccolta [**Commands**](/windows/desktop/lwef/the-commands-collection-object) lo  rimuove anche dal menu a comparsa e dalla finestra Comandi vocali quando l'applicazione è attiva per l'input.

## <a name="see-also"></a>Vedere anche

[**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md), [**IAgentCommands::RemoveAll**](iagentcommands--removeall.md)


 

 