---
title: IAgentCharacter GetPosition
description: IAgentCharacter GetPosition
ms.assetid: 79343337-2700-48cb-a09d-1a356ea560e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40cdff0d6876fc7257e05014f3d9ba695db5d168
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332759"
---
# <a name="iagentcharactergetposition"></a>IAgentCharacter:: GetPosition

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetPosition(
   long * plLeft,  // address of variable for left edge of character 
   long * plTop    // address of variable for top edge of character 
);
```

Recupera la posizione del frame di animazione del carattere.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*
</dt> <dd>

Indirizzo di una variabile che riceve la coordinata dello schermo del bordo sinistro del frame di animazione caratteri in pixel rispetto all'origine della schermata (in alto a sinistra).

</dd> <dt>

<span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*
</dt> <dd>

Indirizzo di una variabile che riceve la coordinata dello schermo del bordo superiore del frame di animazione del carattere in pixel rispetto all'origine della schermata (in alto a sinistra).

</dd> </dl>

Anche se il carattere viene visualizzato in una finestra dell'area a forma irregolare, la posizione del carattere è basata sul relativo frame di animazione rettangolare.

## <a name="see-also"></a>Vedere anche

[**IAgentCharacter:: seposition**](iagentcharacter--setposition.md), [ **IAgentCharacter:: GetSize**](iagentcharacter--getsize.md)


 

 




