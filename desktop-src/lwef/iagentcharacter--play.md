---
title: Riproduzione IAgentCharacter
description: Riproduzione IAgentCharacter
ms.assetid: a0158693-ff62-4da4-8b68-402e8d5b1c2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 320572322d7a28b52693c80eb918ebf78fcb50083e012e35c65df3a7bffdf0a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976401"
---
# <a name="iagentcharacterplay"></a>IAgentCharacter::P lay

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT Play(
   BSTR bszAnimation,  // name of an animation
   long * pdwReqID     // address of request ID
);
```

Riproduce l'animazione specificata.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita. Quando la funzione viene *restituita, pdwReqID* contiene l'ID della richiesta.

<dl> <dt>

<span id="bszAnimation"></span><span id="bszanimation"></span><span id="BSZANIMATION"></span>*bszAnimation*
</dt> <dd>

Nome di un'animazione.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Indirizzo di una variabile che riceve l'ID **richiesta IAgentCharacter::P lay.**

</dd> </dl>

Il nome di un'animazione viene definito quando il carattere viene compilato con l'editor di caratteri di Microsoft Agent. Prima di riprodurre l'animazione specificata, il server tenta di riprodurre l'animazione **Return** per l'animazione precedente (se ne è stata assegnata una).

Quando i dati di animazione di un carattere vengono archiviati nel computer locale dell'utente, è possibile usare il metodo **IAgentCharacter::P lay** e specificare il nome dell'animazione. Quando si usa il protocollo HTTP per accedere ai dati di animazione, usare il [**metodo Prepare**](iagentcharacter--prepare.md) per garantire la disponibilità dell'animazione prima di chiamare questo metodo.

## <a name="see-also"></a>Vedere anche

[**IAgentCharacter::P repare**](iagentcharacter--prepare.md)


 

 




