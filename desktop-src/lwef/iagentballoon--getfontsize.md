---
title: IAgentBalloon GetFontSize
description: IAgentBalloon GetFontSize
ms.assetid: 4d342ee9-abb4-431b-bd28-f62ab76705ec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccc392bd12fccfb01b8aee41a5a06ed50b388ac8223e622d75218c840f706c91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962491"
---
# <a name="iagentballoongetfontsize"></a>IAgentBalloon::GetFontSize

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetFontSize(
   long * plFontSize  // address of variable for font size 
);                    // for font displayed in word balloon 
```

Recupera il valore per le dimensioni del tipo di carattere visualizzato in un fumetto.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="plFontSize"></span><span id="plfontsize"></span><span id="PLFONTSIZE"></span>*plFontSize*
</dt> <dd>

Indirizzo di un valore che riceve le dimensioni del tipo di carattere.

</dd> </dl>

Le dimensioni predefinite del carattere utilizzate in un fumetto di parole di caratteri sono definite nell'Editor caratteri di Microsoft Agent. È possibile modificarlo con [**IAgentBalloon::SetFontSize**](https://www.bing.com/search?q=**IAgentBalloon::SetFontSize**). Tuttavia, l'utente può eseguire l'override delle impostazioni delle dimensioni del carattere per tutti i caratteri usando la finestra delle proprietà di Microsoft Agent.

 

 




