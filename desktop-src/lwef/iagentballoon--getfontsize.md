---
title: IAgentBalloon GetFontSize
description: IAgentBalloon GetFontSize
ms.assetid: 4d342ee9-abb4-431b-bd28-f62ab76705ec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d14b1a921f1f5c9927f58ab9e561569ba3bc98fa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104222071"
---
# <a name="iagentballoongetfontsize"></a>IAgentBalloon:: GetFontSize

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetFontSize(
   long * plFontSize  // address of variable for font size 
);                    // for font displayed in word balloon 
```

Recupera il valore per la dimensione del tipo di carattere visualizzato in un fumetto di Word.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="plFontSize"></span><span id="plfontsize"></span><span id="PLFONTSIZE"></span>*plFontSize*
</dt> <dd>

Indirizzo di un valore che riceve la dimensione del tipo di carattere.

</dd> </dl>

Le dimensioni predefinite del tipo di carattere utilizzate in un fumetto di parole sono definite nell'editor dei caratteri di Microsoft Agent. È possibile modificarlo con [**IAgentBalloon:: sefontsize**](https://www.bing.com/search?q=**IAgentBalloon::SetFontSize**). Tuttavia, l'utente può eseguire l'override delle impostazioni relative alle dimensioni del carattere per tutti i caratteri utilizzando la finestra delle proprietà di Microsoft Agent.

 

 




