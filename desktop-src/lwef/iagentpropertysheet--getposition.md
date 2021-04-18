---
title: IAgentPropertySheet GetPosition
description: IAgentPropertySheet GetPosition
ms.assetid: 5d3de366-e48a-4643-81c5-ac4808671763
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ff4dcac994901824d7dc37868d7fcfc3f39cefd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298327"
---
# <a name="iagentpropertysheetgetposition"></a>IAgentPropertySheet:: GetPosition

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetPosition(
   long * plLeft,  // address of variable for left edge of property sheet
   long * plTop    // address of variable for top edge of property sheet
);
```

Recupera la posizione della finestra delle proprietà dell'agente Microsoft.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*
</dt> <dd>

Indirizzo di una variabile che riceve la coordinata dello schermo del bordo sinistro della finestra delle proprietà, espressa in pixel, rispetto all'origine della schermata (in alto a sinistra).

</dd> <dt>

<span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*
</dt> <dd>

Indirizzo di una variabile che riceve la coordinata dello schermo del bordo superiore della finestra delle proprietà in pixel, rispetto all'origine della schermata (in alto a sinistra).

</dd> </dl>

## <a name="see-also"></a>Vedere anche

[**IAgentPropertySheet:: GetSize**](iagentpropertysheet--getsize.md)


 

 




