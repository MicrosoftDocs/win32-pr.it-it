---
title: Arresto di IAgentCharacter
description: Arresto di IAgentCharacter
ms.assetid: 3064bb3e-37a6-4022-bffb-130735736889
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 297f187b7045b1da5773643f2765160c71fbca0d4eb7c6ec12c4032e2f1d5806
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114781"
---
# <a name="iagentcharacterstop"></a>IAgentCharacter::Stop

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT Stop(
   long dwReqID  // request ID
);
```

Arresta l'animazione specificata (richiesta) e la rimuove dalla coda di animazione del carattere.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*
</dt> <dd>

ID della richiesta da arrestare.

</dd> </dl>

**Stop** può essere usato anche per arrestare qualsiasi chiamata [**Prepare**](iagentcharacter--prepare.md) in coda.

## <a name="see-also"></a>Vedere anche

[**IAgentCharacter::P repare**](iagentcharacter--prepare.md), [ **IAgentCharacter::StopAll**](iagentcharacter--stopall.md)


 

 




