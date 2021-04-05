---
title: IAgentCharacter Play
description: IAgentCharacter Play
ms.assetid: a0158693-ff62-4da4-8b68-402e8d5b1c2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 996929271156254377f08b9fc41da3932aee9da4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045402"
---
# <a name="iagentcharacterplay"></a>IAgentCharacter::P lay

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT Play(
   BSTR bszAnimation,  // name of an animation
   long * pdwReqID     // address of request ID
);
```

Riproduce l'animazione specificata.

-   Restituisce \_ OK per indicare che l'operazione è stata completata. Quando la funzione restituisce, *pdwReqID* contiene l'ID della richiesta.

<dl> <dt>

<span id="bszAnimation"></span><span id="bszanimation"></span><span id="BSZANIMATION"></span>*bszAnimation*
</dt> <dd>

Nome di un'animazione.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Indirizzo di una variabile che riceve l'ID richiesta **IAgentCharacter::P Lay** .

</dd> </dl>

Il nome di un'animazione viene definito quando il carattere viene compilato con l'editor dei caratteri di Microsoft Agent. Prima di riprodurre l'animazione specificata, il server tenta di riprodurre l'animazione **restituita** per l'animazione precedente (se ne è stata assegnata una).

Quando i dati di animazione di un carattere vengono archiviati nel computer locale dell'utente, è possibile usare il metodo **IAgentCharacter::P Lay** e specificare il nome dell'animazione. Quando si utilizza il protocollo HTTP per accedere ai dati di animazione, utilizzare il metodo [**Prepare**](iagentcharacter--prepare.md) per garantire la disponibilità dell'animazione prima di chiamare questo metodo.

## <a name="see-also"></a>Vedere anche

[**IAgentCharacter::P ripare**](iagentcharacter--prepare.md)


 

 




