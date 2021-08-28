---
title: IAgentBalloonEx SetNumLines
description: IAgentBalloonEx SetNumLines
ms.assetid: 350fd273-a941-4454-a309-045d19ed8f59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3951cd4a8593d5e043e1571cdf24e14fdd9d93aef690c057860c2889022aa8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848721"
---
# <a name="iagentballoonexsetnumlines"></a>IAgentBalloonEx::SetNumLines

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetNumLines(
   long lLines,  // number of lines setting
);
```

Imposta il numero di righe di output di testo che possono essere visualizzate nel fumetto delle parole del carattere.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.
-   Restituisce E \_ INVALIDARG se il parametro è zero.

<dl> <dt>

<span id="lLines"></span><span id="llines"></span><span id="LLINES"></span>*lLines*
</dt> <dd>

Numero di righe da visualizzare nel fumetto.

</dd> </dl>

L'impostazione minima è 1 e il valore massimo è 128. Se il testo specificato nel [**metodo Speak**](speak-method.md) o [**Think**](think-method.md) supera le dimensioni del balloon corrente, Agent scorre automaticamente il testo nel balloon.

Questo metodo avrà esito negativo se è impostato il bit di stile balloon **di SizeToText.**

L'impostazione predefinita si basa sulle impostazioni quando il carattere viene compilato con l'editor di caratteri di Microsoft Agent.

## <a name="see-also"></a>Vedere anche

[**IAgentBalloon::GetNumLines**](iagentballoon--getnumlines.md), [**IAgentBalloonEx::GetStyle**](iagentballoonex--getstyle.md), [**IAgentBalloonEx::SetStyle**](iagentballoonex--setstyle.md)


 

 




