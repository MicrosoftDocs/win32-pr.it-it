---
title: IAgentCharacter SetPosition
description: IAgentCharacter SetPosition
ms.assetid: cc47b537-8154-4dfb-93e1-5ac3c3b50788
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e973ec08cdab89c2d8c2501bd9ea1778866f5f7fa1757fe746e44495e41c275a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665641"
---
# <a name="iagentcharactersetposition"></a>IAgentCharacter::SetPosition

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetPosition(
   long lLeft,  // screen coordinate of the left edge of character 
   long lTop    // screen coordinate of the top edge of character 
);
```

Imposta la posizione del frame di animazione del carattere.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="lLeft"></span><span id="lleft"></span><span id="LLEFT"></span>*lLeft*
</dt> <dd>

Coordinata dello schermo del bordo sinistro del fotogramma di animazione del carattere in pixel, rispetto all'origine dello schermo (in alto a sinistra).

</dd> <dt>

<span id="lTop"></span><span id="ltop"></span><span id="LTOP"></span>*lTop*
</dt> <dd>

Coordinata dello schermo del bordo superiore del fotogramma di animazione del carattere in pixel, rispetto all'origine dello schermo (in alto a sinistra).

</dd> </dl>

L'impostazione di questa proprietà si applica a tutti i client del carattere. Anche se il carattere viene visualizzato in una finestra di area irregolare, la posizione del carattere è basata sul relativo frame di animazione rettangolare.

> [!Note]  
> A differenza [**del metodo MoveTo,**](https://www.bing.com/search?q=**MoveTo**) questa funzione non viene accodata.

 

## <a name="see-also"></a>Vedere anche

[**IAgentCharacter::GetPosition**](iagentcharacter--getposition.md)


 

 




