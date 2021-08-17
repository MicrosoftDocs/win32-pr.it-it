---
title: IAgentBalloon GetBorderColor
description: IAgentBalloon GetBorderColor
ms.assetid: e6c592c3-0e14-474f-a829-6028f2de5791
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46ed636d5209402959adbb2a777577a87c8cc23f8eed4faeb8ac003981e5e2d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118478635"
---
# <a name="iagentballoongetbordercolor"></a>IAgentBalloon::GetBorderColor

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetBorderColor (
  long * plBorderColor// address of variable for border color displayed
);                    // for word balloon
```

Recupera il valore per il colore del bordo visualizzato per un fumetto di parole.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="plBorderColor"></span><span id="plbordercolor"></span><span id="PLBORDERCOLOR"></span>*plBorderColor*
</dt> <dd>

Indirizzo di una variabile che riceve l'impostazione del colore per il bordo del fumetto.

</dd> </dl>

Il colore del bordo per un fumetto di parole di tipo carattere è definito nell'editor di caratteri di Microsoft Agent. Non può essere modificato da un'applicazione. Tuttavia, l'utente può modificare il colore del bordo delle aree commenti per tutti i caratteri tramite la finestra delle proprietà di Microsoft Agent.

## <a name="see-also"></a>Vedere anche

[**IAgentBalloon::GetBackColor**](iagentballoon--getbackcolor.md), [ **IAgentBalloon::GetForeColor**](iagentballoon--getforecolor.md)


 

 




