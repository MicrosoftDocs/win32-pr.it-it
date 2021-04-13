---
title: Arresto IAgentCharacter
description: Arresto IAgentCharacter
ms.assetid: 3064bb3e-37a6-4022-bffb-130735736889
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 356c81996a9410eccb2007dc5261913e30a1b414
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396491"
---
# <a name="iagentcharacterstop"></a>IAgentCharacter:: Stop

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT Stop(
   long dwReqID  // request ID
);
```

Arresta l'animazione specificata (richiesta) e la rimuove dalla coda di animazione del carattere.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*
</dt> <dd>

ID della richiesta da arrestare.

</dd> </dl>

**Stop** può essere utilizzato anche per arrestare le chiamate di [**preparazione**](iagentcharacter--prepare.md) in coda.

## <a name="see-also"></a>Vedere anche

[**IAgentCharacter::P repare**](iagentcharacter--prepare.md), [ **IAgentCharacter:: stopAll**](iagentcharacter--stopall.md)


 

 




