---
title: IAgentCommandWindow GetSize
description: IAgentCommandWindow GetSize
ms.assetid: 24ad3b48-6557-4790-b9c4-2cf7df92fa7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 200853d88f4f4ea70fce0f80d73f343a2a4d46935a2dfca0ebf78021b0b884ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961581"
---
# <a name="iagentcommandwindowgetsize"></a>IAgentCommandWindow::GetSize

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetSize(
   long * plWidth,  // address of variable for Voice Commands Window width
   long * plHeight  // address of variable for Voice Commands Window height
);
```

Recupera le dimensioni correnti della finestra Comandi vocali.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*
</dt> <dd>

Indirizzo di una variabile che riceve la larghezza della finestra comandi vocali in pixel, rispetto all'origine dello schermo (in alto a sinistra).

</dd> <dt>

<span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*
</dt> <dd>

Indirizzo di una variabile che riceve l'altezza della finestra Comandi vocali in pixel, rispetto all'origine dello schermo (in alto a sinistra).

</dd> </dl>

## <a name="see-also"></a>Vedere anche

[**IAgentCommandWindow::GetPosition**](iagentcommandwindow--getposition.md)


 

 




