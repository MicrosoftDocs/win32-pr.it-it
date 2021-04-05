---
title: IAgentCommandWindow GetPosition
description: IAgentCommandWindow GetPosition
ms.assetid: d85a7a2c-f0ea-4612-aa73-2e44c49e4e18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a8c036d02c210ecb26da5dfde207bfe56afe8a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955556"
---
# <a name="iagentcommandwindowgetposition"></a>IAgentCommandWindow:: GetPosition

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetPosition(
   long * plLeft,  // address of variable for left edge of Voice Commands Window
   long * plTop    // address of variable for top edge of Voice Commands Window
);
```

Recupera la posizione della finestra dei comandi vocali.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*
</dt> <dd>

Indirizzo di una variabile che riceve la coordinata dello schermo del bordo sinistro della finestra dei comandi vocali, in pixel, rispetto all'origine dello schermo (in alto a sinistra).

</dd> <dt>

<span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*
</dt> <dd>

Indirizzo di una variabile che riceve la coordinata dello schermo del bordo superiore della finestra dei comandi vocali, in pixel, rispetto all'origine della schermata (in alto a sinistra).

</dd> </dl>

## <a name="see-also"></a>Vedere anche

[**IAgentCommandWindow:: GetSize**](iagentcommandwindow--getsize.md)


 

 




