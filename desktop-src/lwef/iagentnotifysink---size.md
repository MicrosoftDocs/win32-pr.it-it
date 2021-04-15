---
title: Dimensioni IAgentNotifySink
description: Dimensioni IAgentNotifySink
ms.assetid: ef192234-bee6-4158-a5d8-4326b784e6cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 252ad15f6bb5201e8ec000292d1e89efe9368934
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515907"
---
# <a name="iagentnotifysinksize"></a>IAgentNotifySink:: size

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT Size(
   long dwCharID,  // character ID
   long lWidth,    // new width
   long lHeight,   // new height
);                          
```

Notifica a un'applicazione client quando il carattere è stato ridimensionato.

-   Nessun valore restituito.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Identificatore del carattere che è stato ridimensionato.

</dd> <dt>

<span id="lWidth"></span><span id="lwidth"></span><span id="LWIDTH"></span>*lWidth*
</dt> <dd>

Larghezza del fotogramma di animazione del carattere in pixel.

</dd> <dt>

<span id="lHeight"></span><span id="lheight"></span><span id="LHEIGHT"></span>*lHeight*
</dt> <dd>

Altezza del frame di animazione del carattere in pixel.

</dd> </dl>

Questo evento viene inviato a tutti i client del carattere.

## <a name="see-also"></a>Vedere anche

[**IAgentCharacter:: GetSize**](iagentcharacter--getsize.md), [ **IAgentCharacter:: sesize**](iagentcharacter--setsize.md)


 

 




