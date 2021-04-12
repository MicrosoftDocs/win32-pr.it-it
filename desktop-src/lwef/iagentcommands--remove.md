---
title: IAgentCommands rimuovere
description: IAgentCommands rimuovere
ms.assetid: 1f41aa2d-e50b-48a8-87fc-fda4730b035a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d0c3321de3d06b5e2ebea873a4bace91482d8c5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104223618"
---
# <a name="iagentcommandsremove"></a>IAgentCommands:: Remove

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT Remove(
   long dwID  // Command ID
);
```

Rimuove il [**comando**](/windows/desktop/lwef/the-command-object) specificato da un insieme di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="dwID"></span><span id="dwid"></span><span id="DWID"></span>*dwID*
</dt> <dd>

ID di un [**comando**](/windows/desktop/lwef/the-command-object) da rimuovere dalla raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> </dl>

La rimozione di un [**comando**](/windows/desktop/lwef/the-command-object) da una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) lo rimuove anche dal menu a comparsa e dalla **finestra comandi vocali** quando l'applicazione è di input-attivo.

## <a name="see-also"></a>Vedere anche

[**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md), [**IAgentCommands:: RemoveAll**](iagentcommands--removeall.md)


 

 