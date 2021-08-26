---
title: IAgentNotifySinkEx AgentPropertyChange
description: IAgentNotifySinkEx AgentPropertyChange
ms.assetid: 8293cd77-320a-4b57-b3d8-52bc450d6aa0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7d7a0737428d20b297d83ac92c3ce6957dac0390c719c17b96a00983a0a57af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961491"
---
# <a name="iagentnotifysinkexagentpropertychange"></a>IAgentNotifySinkEx::AgentPropertyChange

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT AgentPropertyChange(
);
```

Notifica a un'applicazione client quando l'utente modifica l'impostazione di una proprietà di Microsoft Agent.

-   Nessun valore restituito.

Quando l'utente modifica l'impostazione di una proprietà di Microsoft Agent nella finestra delle proprietà di Microsoft Agent, il server invia questo evento a tutti i client, a meno che il server non sia attualmente sospeso.

## <a name="see-also"></a>Vedere anche

[**IAgentNotifySinkEx::D efaultCharacterChange**](iagentnotifysinkex--defaultcharacterchange.md)


 

 




