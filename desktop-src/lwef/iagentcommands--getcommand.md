---
title: IAgentCommands GetCommand
description: IAgentCommands GetCommand
ms.assetid: 0f4a9152-d5dc-4045-b469-8a03f0369e34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e81043bb8dbe8a6d050f226d09f03b396d0f8f9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046735"
---
# <a name="iagentcommandsgetcommand"></a>IAgentCommands:: GetCommand

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetCommand(
   long dwCommandID,         // Command ID
   IUnknown ** ppunkCommand  // address of IUnknown interface
);                    
```

Recupera un oggetto [**Command**](/windows/desktop/lwef/the-command-object) dalla raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwCommandID*
</dt> <dd>

ID di un oggetto [**Command**](/windows/desktop/lwef/the-command-object) nella raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> <dt>

<span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*
</dt> <dd>

Indirizzo dell'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) per l'oggetto [**Command**](/windows/desktop/lwef/the-command-object) .

</dd> </dl>

## <a name="see-also"></a>Vedere anche

[**IAgentCommand**](iagentcommand.md)


 

 