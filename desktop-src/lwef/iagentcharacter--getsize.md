---
title: IAgentCharacter GetSize
description: IAgentCharacter GetSize
ms.assetid: bc2d6fe4-5945-4a35-b603-409c66f8aa2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5af078eb9980399793e00f8bd3deaefef7f048a900423c1ee50ac8d4f4a310b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962231"
---
# <a name="iagentcharactergetsize"></a>IAgentCharacter::GetSize

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetSize(
   long * plWidth,  // address of variable for character width 
   long * plHeight  // address of variable for character height
);
```

Recupera le dimensioni del frame di animazione del carattere.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*
</dt> <dd>

Indirizzo di una variabile che riceve la larghezza del fotogramma dell'animazione del carattere in pixel, rispetto all'origine dello schermo (in alto a sinistra).

</dd> <dt>

<span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*
</dt> <dd>

Indirizzo di una variabile che riceve l'altezza del fotogramma dell'animazione del carattere in pixel, rispetto all'origine dello schermo (in alto a sinistra).

</dd> </dl>

Anche se il carattere viene visualizzato in una finestra di area irregolare, la posizione del carattere è basata sul relativo frame di animazione rettangolare.

## <a name="see-also"></a>Vedere anche

[**IAgentCharacter::SetSize**](iagentcharacter--setsize.md)


 

 




