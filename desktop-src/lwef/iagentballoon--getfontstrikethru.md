---
title: IAgentBalloon GetFontStrikethru
description: IAgentBalloon GetFontStrikethru
ms.assetid: b5c253e8-dca7-44a6-b63b-a33e6e793a40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2001ec0125949144843d500f125b3502e94723db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396799"
---
# <a name="iagentballoongetfontstrikethru"></a>IAgentBalloon::GetFontStrikethru

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetFontStrikethru(
   long * pbFontStrikethru  // address of variable for strikethrough setting 
);                          // for font displayed in word balloon 
```

Indica se il tipo di carattere utilizzato in un fumetto di Word dispone del set di stili barrato.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="pbFontStrikethru"></span><span id="pbfontstrikethru"></span><span id="PBFONTSTRIKETHRU"></span>*pbFontStrikethru*
</dt> <dd>

Indirizzo di un valore che riceve **true** se lo stile barrato del carattere è impostato e **false** in caso contrario.

</dd> </dl>

Lo stile del tipo di carattere utilizzato in un fumetto di parole è definito nell'editor dei caratteri di Microsoft Agent. Non può essere modificato da un'applicazione. Tuttavia, l'utente può eseguire l'override delle impostazioni del tipo di carattere per tutti i caratteri utilizzando la finestra delle proprietà di Microsoft Agent.

 

 




