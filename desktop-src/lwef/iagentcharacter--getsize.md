---
title: IAgentCharacter GetSize
description: IAgentCharacter GetSize
ms.assetid: bc2d6fe4-5945-4a35-b603-409c66f8aa2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e40c219cd0a1dc1d11738149ca7cfd9869fe682e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332756"
---
# <a name="iagentcharactergetsize"></a>IAgentCharacter:: GetSize

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetSize(
   long * plWidth,  // address of variable for character width 
   long * plHeight  // address of variable for character height
);
```

Recupera la dimensione del frame di animazione del carattere.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*
</dt> <dd>

Indirizzo di una variabile che riceve la larghezza del fotogramma di animazione dei caratteri in pixel rispetto all'origine della schermata (in alto a sinistra).

</dd> <dt>

<span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*
</dt> <dd>

Indirizzo di una variabile che riceve l'altezza del frame di animazione dei caratteri in pixel rispetto all'origine della schermata (in alto a sinistra).

</dd> </dl>

Anche se il carattere viene visualizzato in una finestra dell'area a forma irregolare, la posizione del carattere è basata sul relativo frame di animazione rettangolare.

## <a name="see-also"></a>Vedere anche

[**IAgentCharacter:: sesize**](iagentcharacter--setsize.md)


 

 




