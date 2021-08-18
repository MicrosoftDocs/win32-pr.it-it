---
title: IAgentBalloon GetNumLines
description: IAgentBalloon GetNumLines
ms.assetid: 82deeed0-d4a7-46e4-9077-edd933dcf4e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461ebc4fa7c7e0ae9080544e9114db9f8c179925dae665925d893288f95de027
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118478625"
---
# <a name="iagentballoongetnumlines"></a>IAgentBalloon::GetNumLines

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetNumLines(
   long * pcLines  // address of variable for number of lines 
);                  // displayed in word balloon
```

Recupera il valore del numero di righe visualizzate in un fumetto di parole.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="pcLines"></span><span id="pclines"></span><span id="PCLINES"></span>*pcLines*
</dt> <dd>

Indirizzo di una variabile che riceve il numero di righe visualizzate.

</dd> </dl>

Il server Microsoft Agent scorre automaticamente le righe visualizzate per l'output vocale nel fumetto. Il numero di righe per un fumetto di parole di caratteri è definito nell'Editor di caratteri di Microsoft Agent. Non può essere modificato da un'applicazione.

## <a name="see-also"></a>Vedere anche

[**IAgentBalloon::GetNumCharsPerLine**](iagentballoon--getnumcharsperline.md)


 

 




