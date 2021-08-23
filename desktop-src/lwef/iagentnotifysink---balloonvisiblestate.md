---
title: IAgentNotifySink BalloonVisibleState
description: IAgentNotifySink BalloonVisibleState
ms.assetid: 240e049c-7167-41b7-b092-95ed2a83aad3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f61f1213c6d947f2ca23e0b67ff8eef393892f4732e4a419ec93c277a62af99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976181"
---
# <a name="iagentnotifysinkballoonvisiblestate"></a>IAgentNotifySink::BalloonVisibleState

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT BalloonVisibleState(
   long dwCharID,  // character ID
   long bVisible   // visibility flag
);                          
```

Notifica a un'applicazione client quando lo stato di visibilità del fumetto del carattere cambia.

-   Nessun valore restituito.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Identificatore del carattere il cui stato di visibilità del fumetto è stato modificato.

</dd> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

Flag di visibilità. Questo valore booleano è **True quando** il fumetto della parola del carattere diventa visibile; e **False** quando viene nascosto.

</dd> </dl>

Questo evento viene inviato a tutti i client del carattere.

 

 




