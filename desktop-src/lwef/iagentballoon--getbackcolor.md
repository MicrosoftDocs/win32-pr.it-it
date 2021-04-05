---
title: GetBackColor IAgentBalloon
description: GetBackColor IAgentBalloon
ms.assetid: 278ed645-0e6c-4a5d-bd85-3e3b7a1e3333
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cce886c9929892c89b56f162f784dc27a472209
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044912"
---
# <a name="iagentballoongetbackcolor"></a>IAgentBalloon:: GetBackColor

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetBackColor(
   long * plBGColor  // address of variable for background color displayed
);                   // in word balloon
```

Recupera il valore per il colore di sfondo visualizzato in un fumetto di Word.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="plBGColor"></span><span id="plbgcolor"></span><span id="PLBGCOLOR"></span>*plBGColor*
</dt> <dd>

Indirizzo di una variabile che riceve l'impostazione del colore per lo sfondo del fumetto.

</dd> </dl>

Il colore di sfondo utilizzato in un fumetto di parole è definito nell'editor dei caratteri di Microsoft Agent. Non può essere modificato da un'applicazione. Tuttavia, l'utente può modificare il colore di sfondo delle parole Balloon per tutti i caratteri tramite la finestra delle proprietà di Microsoft Agent.

## <a name="see-also"></a>Vedere anche

[**IAgentBalloon:: GetForeColor**](iagentballoon--getforecolor.md)


 

 




