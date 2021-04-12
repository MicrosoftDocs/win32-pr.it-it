---
title: IAgentBalloonEx SetNumCharsPerLine
description: IAgentBalloonEx SetNumCharsPerLine
ms.assetid: 44025b6b-ed42-4476-b841-c244accf0f83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32a44abe14de6bb1cef631a51b4516d083657016
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331847"
---
# <a name="iagentballoonexsetnumcharsperline"></a>IAgentBalloonEx::SetNumCharsPerLine

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetNumCharsPerLine(
   long lCharsPerLine,  // number of characters per line setting
);
```

Imposta il numero di caratteri per riga che è possibile visualizzare nel fumetto di parola del carattere.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.
-   Restituisce E \_ INVALIDARG se il parametro è minore di otto.

<dl> <dt>

<span id="lCharsPerLine"></span><span id="lcharsperline"></span><span id="LCHARSPERLINE"></span>*lCharsPerLine*
</dt> <dd>

Numero di righe da visualizzare nel fumetto di Word.

</dd> </dl>

L'impostazione minima è 8 e il valore massimo è 255. Se il testo specificato nel metodo [**Speak**](speak-method.md) o [**think**](think-method.md) supera le dimensioni del fumetto corrente, Agent scorre automaticamente il testo nel fumetto.

L'impostazione predefinita è basata sulle impostazioni quando il carattere viene compilato con l'editor dei caratteri di Microsoft Agent.

## <a name="see-also"></a>Vedere anche

[**IAgentBalloon::GetNumCharsPerLine**](iagentballoon--getnumcharsperline.md)


 

 




