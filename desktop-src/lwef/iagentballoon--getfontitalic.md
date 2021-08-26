---
title: IAgentBalloon GetFontItalic
description: IAgentBalloon GetFontItalic
ms.assetid: 03f40210-71b3-4488-9a44-5a9322db010a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5535896cc3c40ae3cb04c3078621cc91df4869649cbe72cb106c3d99ec0299ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062021"
---
# <a name="iagentballoongetfontitalic"></a>IAgentBalloon::GetFontItalic

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetFontItalic(
   long * pbFontItalic  // address of variable for italic setting for 
);                      // font displayed in word balloon 
```

Indica se il tipo di carattere utilizzato in un fumetto è in corsivo.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="pbFontItalic"></span><span id="pbfontitalic"></span><span id="PBFONTITALIC"></span>*pbFontItalic*
</dt> <dd>

Indirizzo di un valore che riceve **True** se il tipo di carattere è in corsivo e **False in** caso contrario.

</dd> </dl>

Lo stile del carattere utilizzato nel fumetto delle parole di un carattere è definito nell'editor di caratteri di Microsoft Agent. Non può essere modificato da un'applicazione. Tuttavia, l'utente può eseguire l'override delle impostazioni dei caratteri per tutti i caratteri tramite la finestra delle proprietà di Microsoft Agent.

 

 




