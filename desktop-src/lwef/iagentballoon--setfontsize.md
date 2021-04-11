---
title: IAgentBalloon sefontsize
description: IAgentBalloon sefontsize
ms.assetid: c38779a6-bd7f-4d3a-9cb0-9d9fac1c7996
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4984382408739e2d093226d04b1c99582a1a25d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332247"
---
# <a name="iagentballoonsetfontsize"></a>IAgentBalloon:: sefontsize

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetFontSize(
   long lFontSize  // font size displayed in word balloon
); 
```

Imposta la dimensione del tipo di carattere visualizzato nella parola Balloon.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="lFontSize"></span><span id="lfontsize"></span><span id="LFONTSIZE"></span>*lFontSize*
</dt> <dd>

Dimensione del carattere.

</dd> </dl>

Le dimensioni predefinite del carattere utilizzate nella parola Balloon di un carattere sono definite nell'editor dei caratteri di Microsoft Agent. È possibile modificarlo con **IAgentBalloon:: sefontsize**. Tuttavia, l'utente può eseguire l'override dell'impostazione della dimensione del carattere per tutti i caratteri utilizzando la finestra delle proprietà di Microsoft Agent.

## <a name="see-also"></a>Vedere anche

[**IAgentBalloon:: GetFontSize**](iagentballoon--getfontsize.md)


 

 




