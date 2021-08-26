---
title: Attesa IAgentCharacter
description: Attesa IAgentCharacter
ms.assetid: 4edb9a47-9385-49da-83ff-144780853ae7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fba3f292b9dc7a0651cf3a1a27adcfe0ea808127d8ce00ae62cb1e84cc126a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014221"
---
# <a name="iagentcharacterwait"></a>IAgentCharacter::Wait

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT Wait(
   long dwReqID,    // request ID
   long * pdwReqID  // address of request ID
);
```

Mantiene la coda di animazione del carattere in corrispondenza dell'animazione specificata (richiesta) fino al completamento di un'altra richiesta per un altro carattere.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*
</dt> <dd>

ID della richiesta da attendere.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Indirizzo di una variabile che riceve l'ID **richiesta di** attesa.

</dd> </dl>

Usare questo metodo solo quando si supportano più caratteri (simultanei) e si vuole sequenziarne l'interazione. Per un singolo carattere, ogni richiesta di animazione viene riprodotta in sequenza, dopo il completamento della richiesta precedente. Se si dispone di due caratteri e si vuole che la richiesta di animazione di un carattere attenda il completamento dell'animazione dell'altro carattere, impostare il metodo **Wait** sull'ID richiesta di animazione dell'altro carattere.

 

 




