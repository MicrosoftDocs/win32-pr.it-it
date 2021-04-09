---
title: IAgentNotifySinkEx AgentPropertyChange
description: IAgentNotifySinkEx AgentPropertyChange
ms.assetid: 8293cd77-320a-4b57-b3d8-52bc450d6aa0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e27fe9e2318af0642c2df680af3a279ab57253d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955481"
---
# <a name="iagentnotifysinkexagentpropertychange"></a>IAgentNotifySinkEx::AgentPropertyChange

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT AgentPropertyChange(
);
```

Notifica a un'applicazione client quando l'utente modifica un'impostazione della proprietà di Microsoft Agent.

-   Nessun valore restituito.

Quando l'utente modifica un'impostazione della proprietà agente Microsoft nella finestra delle proprietà di Microsoft Agent, il server invia questo evento a tutti i client a meno che il server non sia attualmente sospeso.

## <a name="see-also"></a>Vedere anche

[**IAgentNotifySinkEx::D efaultCharacterChange**](iagentnotifysinkex--defaultcharacterchange.md)


 

 




