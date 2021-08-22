---
title: IAgentCharacterEx GetOriginalSize
description: IAgentCharacterEx GetOriginalSize
ms.assetid: a27ae88f-3655-4375-b563-0cc320d012cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55abb64a8466b13ee41119e2a8a359ceeb182c92f7b4d2b1071547df07110052
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118750519"
---
# <a name="iagentcharacterexgetoriginalsize"></a>IAgentCharacterEx::GetOriginalSize

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetOriginalSize(
   long * plWidth,  // address of variable for character width 
   long * plHeight  // address of variable for character height
);
```

Recupera le dimensioni originali del frame di animazione del carattere.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*
</dt> <dd>

Indirizzo di una variabile che riceve la larghezza originale del fotogramma dell'animazione carattere in pixel.

</dd> <dt>

<span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*
</dt> <dd>

Indirizzo di una variabile che riceve l'altezza originale del frame di animazione carattere in pixel.

</dd> </dl>

Questa chiamata restituisce le dimensioni originali del frame di caratteri come compilato nell'editor di caratteri di Microsoft Agent.

## <a name="see-also"></a>Vedere anche

[**IAgentCharacter::GetSize**](iagentcharacter--getsize.md)


 

 




