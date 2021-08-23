---
title: IAgentBalloonEx SetNumCharsPerLine
description: IAgentBalloonEx SetNumCharsPerLine
ms.assetid: 44025b6b-ed42-4476-b841-c244accf0f83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 098a89500606482914bfb31303a2cd79cac88f6d96d17abec58c75759f7abedc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976461"
---
# <a name="iagentballoonexsetnumcharsperline"></a>IAgentBalloonEx::SetNumCharsPerLine

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetNumCharsPerLine(
   long lCharsPerLine,  // number of characters per line setting
);
```

Imposta il numero di caratteri per riga che possono essere visualizzati nel fumetto delle parole del carattere.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.
-   Restituisce E \_ INVALIDARG se il parametro è minore di otto.

<dl> <dt>

<span id="lCharsPerLine"></span><span id="lcharsperline"></span><span id="LCHARSPERLINE"></span>*lCharsPerLine*
</dt> <dd>

Numero di righe da visualizzare nel fumetto.

</dd> </dl>

L'impostazione minima è 8 e il valore massimo è 255. Se il testo specificato nel [**metodo Speak**](speak-method.md) o [**Think**](think-method.md) supera le dimensioni del balloon corrente, Agent scorre automaticamente il testo nel balloon.

L'impostazione predefinita si basa sulle impostazioni quando il carattere viene compilato con l'editor di caratteri di Microsoft Agent.

## <a name="see-also"></a>Vedere anche

[**IAgentBalloon::GetNumCharsPerLine**](iagentballoon--getnumcharsperline.md)


 

 




