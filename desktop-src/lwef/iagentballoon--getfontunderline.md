---
title: IAgentBalloon GetFontUnderline
description: IAgentBalloon GetFontUnderline
ms.assetid: 19886e94-8095-4650-bd88-34ea9d96ddaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5acf35453209679dc96c85b3017fbe76b19d53b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045301"
---
# <a name="iagentballoongetfontunderline"></a>IAgentBalloon::GetFontUnderline

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetFontUnderline(
   long * pbFontUnderline  // address of variable for underline setting
);                         // for font displayed in word balloon 
```

Indica se il tipo di carattere utilizzato in un fumetto di Word dispone del set di stili di sottolineatura.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="pbFontUnderline"></span><span id="pbfontunderline"></span><span id="PBFONTUNDERLINE"></span>*pbFontUnderline*
</dt> <dd>

Indirizzo di un valore che riceve **true** se lo stile di sottolineatura del tipo di carattere è impostato e **false** in caso contrario.

</dd> </dl>

Lo stile del tipo di carattere utilizzato in un fumetto di parole è definito nell'editor dei caratteri di Microsoft Agent. Non può essere modificato da un'applicazione. Tuttavia, l'utente può eseguire l'override delle impostazioni del tipo di carattere per tutti i caratteri utilizzando la finestra delle proprietà di Microsoft Agent.

 

 




