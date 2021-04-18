---
title: IAgentBalloon GetFontItalic
description: IAgentBalloon GetFontItalic
ms.assetid: 03f40210-71b3-4488-9a44-5a9322db010a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e31c1a0e1e649e325e84d4a78eee087e102e8d1e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298277"
---
# <a name="iagentballoongetfontitalic"></a>IAgentBalloon::GetFontItalic

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetFontItalic(
   long * pbFontItalic  // address of variable for italic setting for 
);                      // font displayed in word balloon 
```

Indica se il tipo di carattere utilizzato in un fumetto di Word è in corsivo.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="pbFontItalic"></span><span id="pbfontitalic"></span><span id="PBFONTITALIC"></span>*pbFontItalic*
</dt> <dd>

Indirizzo di un valore che riceve **true** se il tipo di carattere è in corsivo e **false** se non è in corsivo.

</dd> </dl>

Lo stile del carattere utilizzato nella parola Balloon di un carattere viene definito nell'editor dei caratteri di Microsoft Agent. Non può essere modificato da un'applicazione. Tuttavia, l'utente può eseguire l'override delle impostazioni del tipo di carattere per tutti i caratteri tramite la finestra delle proprietà di Microsoft Agent.

 

 




