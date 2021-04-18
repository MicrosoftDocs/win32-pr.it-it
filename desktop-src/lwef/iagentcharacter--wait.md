---
title: IAgentCharacter attesa
description: IAgentCharacter attesa
ms.assetid: 4edb9a47-9385-49da-83ff-144780853ae7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d54ac2de03c78c220803a774537230938a00a776
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331412"
---
# <a name="iagentcharacterwait"></a>IAgentCharacter:: wait

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT Wait(
   long dwReqID,    // request ID
   long * pdwReqID  // address of request ID
);
```

Include la coda di animazione del carattere nell'animazione specificata (richiesta) finché non viene completata un'altra richiesta per un altro carattere.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*
</dt> <dd>

ID della richiesta da attendere.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Indirizzo di una variabile che riceve l'ID della richiesta di **attesa** .

</dd> </dl>

Usare questo metodo solo quando si supportano più caratteri (simultanei) e si vuole sequenziare l'interazione. (Per un singolo carattere, ogni richiesta di animazione viene riprodotta in sequenza, dopo il completamento della richiesta precedente). Se si dispone di due caratteri e si desidera che la richiesta di animazione di un carattere attenda il completamento dell'animazione dell'altro carattere, impostare il metodo **wait** sull'ID richiesta di animazione dell'altro carattere.

 

 




