---
title: IAgentBalloon sefontname
description: IAgentBalloon sefontname
ms.assetid: 6babf5f6-2abd-46c2-ade0-899a8e4488bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f983064c5df8cde8322658bbd0c713bbf238ecf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045299"
---
# <a name="iagentballoonsetfontname"></a>IAgentBalloon:: sefontname

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetFontName(
   BSTR bszFontName  // font displayed in word balloon
);
                   
```

Imposta il tipo di carattere visualizzato nella parola Balloon.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="bszFontName"></span><span id="bszfontname"></span><span id="BSZFONTNAME"></span>*bszFontName*
</dt> <dd>

BSTR che imposta il tipo di carattere visualizzato nella parola Balloon.

</dd> </dl>

Il tipo di carattere predefinito utilizzato nella parola Balloon di un carattere viene definito nell'editor dei caratteri di Microsoft Agent. È possibile modificarlo con **IAgentBalloon:: Sefontname**. Tuttavia, l'utente può eseguire l'override dell'impostazione del tipo di carattere per tutti i caratteri utilizzando la finestra delle proprietà di Microsoft Agent.

## <a name="see-also"></a>Vedere anche

[**IAgentBalloon:: GetVisible**](iagentballoon--getvisible.md)


 

 




