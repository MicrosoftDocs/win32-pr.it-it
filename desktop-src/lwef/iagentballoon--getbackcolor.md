---
title: IAgentBalloon GetBackColor
description: IAgentBalloon GetBackColor
ms.assetid: 278ed645-0e6c-4a5d-bd85-3e3b7a1e3333
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7c58a913332d01f2982c28003c146420d34a86e96f3c833f667c968bd22ef19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888421"
---
# <a name="iagentballoongetbackcolor"></a>IAgentBalloon::GetBackColor

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetBackColor(
   long * plBGColor  // address of variable for background color displayed
);                   // in word balloon
```

Recupera il valore per il colore di sfondo visualizzato in un fumetto di parole.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="plBGColor"></span><span id="plbgcolor"></span><span id="PLBGCOLOR"></span>*plBGColor*
</dt> <dd>

Indirizzo di una variabile che riceve l'impostazione del colore per lo sfondo del fumetto.

</dd> </dl>

Il colore di sfondo usato in un fumetto di parole di tipo carattere è definito nell'editor di caratteri di Microsoft Agent. Non può essere modificato da un'applicazione. Tuttavia, l'utente può modificare il colore di sfondo delle aree commenti per tutti i caratteri tramite la finestra delle proprietà di Microsoft Agent.

## <a name="see-also"></a>Vedere anche

[**IAgentBalloon::GetForeColor**](iagentballoon--getforecolor.md)


 

 




