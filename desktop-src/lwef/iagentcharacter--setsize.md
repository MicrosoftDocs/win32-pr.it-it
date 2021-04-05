---
title: IAgentCharacter dimensioni
description: IAgentCharacter dimensioni
ms.assetid: 8324ab84-2b59-4459-b375-700d72b621bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d39d5b33afa7ff59516b793f194a0ba186c2e002
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713186"
---
# <a name="iagentcharactersetsize"></a>IAgentCharacter:: sesize

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetSize(
   long * lWidth,  // width of the character frame
   long * lHeight  // height of the character frame
);
```

Imposta la dimensione del frame di animazione del carattere.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="lWidth"></span><span id="lwidth"></span><span id="LWIDTH"></span>*lWidth*
</dt> <dd>

Larghezza del fotogramma di animazione del carattere in pixel.

</dd> <dt>

<span id="lHeight"></span><span id="lheight"></span><span id="LHEIGHT"></span>*lHeight*
</dt> <dd>

Altezza del frame di animazione del carattere in pixel.

</dd> </dl>

Se si modifica la dimensione del fotogramma del carattere, il carattere viene ridimensionato in modo da impostare le dimensioni con questo metodo. L'impostazione di questa proprietà si applica a tutti i client del carattere.

Anche se il carattere viene visualizzato in una finestra dell'area a forma irregolare, la posizione del carattere è basata sul relativo frame di animazione rettangolare.

## <a name="see-also"></a>Vedere anche

[**IAgentCharacter:: GetSize**](iagentcharacter--getsize.md)


 

 




