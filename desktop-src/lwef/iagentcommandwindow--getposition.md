---
title: IAgentCommandWindow GetPosition
description: IAgentCommandWindow GetPosition
ms.assetid: d85a7a2c-f0ea-4612-aa73-2e44c49e4e18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52571311a87ee0846dcaf515912762069fe3025a25c5a2589770ee9738bb2de7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716101"
---
# <a name="iagentcommandwindowgetposition"></a>IAgentCommandWindow::GetPosition

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetPosition(
   long * plLeft,  // address of variable for left edge of Voice Commands Window
   long * plTop    // address of variable for top edge of Voice Commands Window
);
```

Recupera la posizione della finestra Comandi vocali.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*
</dt> <dd>

Indirizzo di una variabile che riceve la coordinata dello schermo del bordo sinistro della finestra Comandi vocali in pixel, rispetto all'origine dello schermo (in alto a sinistra).

</dd> <dt>

<span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*
</dt> <dd>

Indirizzo di una variabile che riceve la coordinata dello schermo del bordo superiore della finestra comandi vocali in pixel, rispetto all'origine dello schermo (in alto a sinistra).

</dd> </dl>

## <a name="see-also"></a>Vedere anche

[**IAgentCommandWindow::GetSize**](iagentcommandwindow--getsize.md)


 

 




