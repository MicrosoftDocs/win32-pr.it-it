---
title: IAgentCharacter GetPosition
description: IAgentCharacter GetPosition
ms.assetid: 79343337-2700-48cb-a09d-1a356ea560e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a63e75111b7694fcb993e141b8534e8f174efd1a1a252f250167ecb597149f7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609991"
---
# <a name="iagentcharactergetposition"></a>IAgentCharacter::GetPosition

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetPosition(
   long * plLeft,  // address of variable for left edge of character 
   long * plTop    // address of variable for top edge of character 
);
```

Recupera la posizione del fotogramma dell'animazione del carattere.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*
</dt> <dd>

Indirizzo di una variabile che riceve la coordinata dello schermo del bordo sinistro del fotogramma di animazione carattere in pixel, rispetto all'origine dello schermo (in alto a sinistra).

</dd> <dt>

<span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*
</dt> <dd>

Indirizzo di una variabile che riceve la coordinata dello schermo del bordo superiore del frame di animazione carattere in pixel, rispetto all'origine dello schermo (in alto a sinistra).

</dd> </dl>

Anche se il carattere viene visualizzato in una finestra di area di forma irregolare, la posizione del carattere si basa sul relativo frame di animazione rettangolare.

## <a name="see-also"></a>Vedere anche

[**IAgentCharacter::SetPosition**](iagentcharacter--setposition.md), [ **IAgentCharacter::GetSize**](iagentcharacter--getsize.md)


 

 




