---
title: ShowPopupMenu IAgentCharacterEx
description: ShowPopupMenu IAgentCharacterEx
ms.assetid: f93c4c9e-5ef8-42d1-8f22-d6625af7978f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 535a86496f3553e0927ebe67d2c9823b738fb901
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856478"
---
# <a name="iagentcharacterexshowpopupmenu"></a>IAgentCharacterEx:: ShowPopupMenu

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT ShowPopupMenu(
   short x,  // x-coordinate of pop-up menu
   short y   // y-coordinate of pop-up menu
);
```

Consente di visualizzare il menu di scelta rapida per il carattere.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="x"></span><span id="X"></span>*x*
</dt> <dd>

Coordinata x del menu di scelta rapida del carattere in pixel rispetto all'origine dello schermo (in alto a sinistra).

</dd> <dt>

<span id="y"></span><span id="Y"></span>*y*
</dt> <dd>

Coordinata y del menu di scelta rapida del carattere in pixel rispetto all'origine dello schermo (in alto a sinistra).

</dd> </dl>

Quando si imposta [**IAgentCharacterEx:: SetAutoPopupMenu**](iagentcharacterex--setautopopupmenu.md) su **false**, il server non Visualizza più automaticamente il menu quando si fa clic con il pulsante destro del mouse sull'icona del carattere o della barra delle applicazioni. È possibile utilizzare questo metodo per visualizzare il menu.

Il menu viene visualizzato fino a quando l'utente non seleziona un comando o Visualizza un altro menu. È possibile visualizzare un solo menu popup alla volta; Pertanto, le chiamate a questo metodo cancelleranno (rimuovere) il menu precedente.

Questo metodo deve essere chiamato solo quando l'applicazione client è il client attivo del carattere; in caso contrario, avrà esito negativo.

[**IAgentCharacterEx::SetAutoPopupMenu**](iagentcharacterex--setautopopupmenu.md)

 

 




