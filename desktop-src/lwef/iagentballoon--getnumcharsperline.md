---
title: IAgentBalloon GetNumCharsPerLine
description: IAgentBalloon GetNumCharsPerLine
ms.assetid: ae0c7fff-8c58-465e-9b4f-3260f7574b57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 887167584c46f075bc0696c46b2dde52eb27f8d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045300"
---
# <a name="iagentballoongetnumcharsperline"></a>IAgentBalloon::GetNumCharsPerLine

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetNumCharsPerLine(
   long * plCharsPerLine  // address of variable for characters per line
);                        // displayed in word balloon
```

Recupera il valore per il numero medio di caratteri per riga visualizzato in un fumetto di Word.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="pbCharsPerLine"></span><span id="pbcharsperline"></span><span id="PBCHARSPERLINE"></span>*pbCharsPerLine*
</dt> <dd>

Indirizzo di una variabile che riceve il numero di caratteri per riga.

</dd> </dl>

Il server Microsoft Agent scorre automaticamente le righe visualizzate per l'output parlato nella parola Balloon. Il numero medio di caratteri per riga per la parola Balloon di un carattere è definito nell'editor dei caratteri di Microsoft Agent. Non può essere modificato da un'applicazione.

## <a name="see-also"></a>Vedere anche

[**IAgentBalloon::GetNumLines**](iagentballoon--getnumlines.md)


 

 




