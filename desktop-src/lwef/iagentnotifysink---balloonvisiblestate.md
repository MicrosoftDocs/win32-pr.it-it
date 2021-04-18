---
title: IAgentNotifySink BalloonVisibleState
description: IAgentNotifySink BalloonVisibleState
ms.assetid: 240e049c-7167-41b7-b092-95ed2a83aad3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2dd63d8eef3a7f1a70af81e13506a7e92ad84f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298494"
---
# <a name="iagentnotifysinkballoonvisiblestate"></a>IAgentNotifySink::BalloonVisibleState

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT BalloonVisibleState(
   long dwCharID,  // character ID
   long bVisible   // visibility flag
);                          
```

Notifica a un'applicazione client quando viene modificato lo stato di visibilità del fumetto di parole del carattere.

-   Nessun valore restituito.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Identificatore del carattere il cui stato di visibilità del fumetto di parola è stato modificato.

</dd> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

Flag di visibilità. Questo valore booleano è **true** quando il fumetto di parola del carattere diventa visibile; e **false** quando viene nascosta.

</dd> </dl>

Questo evento viene inviato a tutti i client del carattere.

 

 




