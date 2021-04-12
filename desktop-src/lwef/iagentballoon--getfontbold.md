---
title: IAgentBalloon GetFontBold
description: IAgentBalloon GetFontBold
ms.assetid: 5a55f771-d68e-4f66-8001-47c141661b06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 858f6f42964db1bdd7ae548d308c6f6668b05631
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221602"
---
# <a name="iagentballoongetfontbold"></a>IAgentBalloon::GetFontBold

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetFontBold(
   long * pbFontBold  // address of variable for bold setting for
);                    // font displayed in word balloon 
```

Indica se il tipo di carattere utilizzato in un fumetto di Word è in grassetto.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="pbFontBold"></span><span id="pbfontbold"></span><span id="PBFONTBOLD"></span>*pbFontBold*
</dt> <dd>

Indirizzo di un valore che riceve **true** se il tipo di carattere è grassetto e **false** se non è in grassetto.

</dd> </dl>

Lo stile del tipo di carattere utilizzato in un fumetto di parole è definito nell'editor dei caratteri di Microsoft Agent. Non può essere modificato da un'applicazione. Tuttavia, l'utente può eseguire l'override delle impostazioni del tipo di carattere per tutti i caratteri tramite la finestra delle proprietà di Microsoft Agent.

 

 




