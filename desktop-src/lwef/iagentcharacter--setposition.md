---
title: Posizione IAgentCharacter
description: Posizione IAgentCharacter
ms.assetid: cc47b537-8154-4dfb-93e1-5ac3c3b50788
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0aee48ea26c714c570f7ae11b9b2dbc0fe92ef6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044494"
---
# <a name="iagentcharactersetposition"></a>IAgentCharacter:: seposition

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetPosition(
   long lLeft,  // screen coordinate of the left edge of character 
   long lTop    // screen coordinate of the top edge of character 
);
```

Imposta la posizione del frame di animazione del carattere.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="lLeft"></span><span id="lleft"></span><span id="LLEFT"></span>*lLeft*
</dt> <dd>

Coordinata dello schermo del bordo sinistro del frame di animazione caratteri in pixel rispetto all'origine dello schermo (in alto a sinistra).

</dd> <dt>

<span id="lTop"></span><span id="ltop"></span><span id="LTOP"></span>*lTop*
</dt> <dd>

Coordinata dello schermo del bordo superiore del frame di animazione caratteri in pixel rispetto all'origine dello schermo (in alto a sinistra).

</dd> </dl>

L'impostazione di questa proprietà si applica a tutti i client del carattere. Anche se il carattere viene visualizzato in una finestra dell'area a forma irregolare, la posizione del carattere è basata sul relativo frame di animazione rettangolare.

> [!Note]  
> Diversamente dal metodo [**MoveTo**](https://www.bing.com/search?q=**MoveTo**) , questa funzione non viene accodata.

 

## <a name="see-also"></a>Vedere anche

[**IAgentCharacter:: GetPosition**](iagentcharacter--getposition.md)


 

 




