---
title: IAgentBalloonEx SetNumLines
description: IAgentBalloonEx SetNumLines
ms.assetid: 350fd273-a941-4454-a309-045d19ed8f59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d45c012d0193a0bd21ba203418920b87b2fac81b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471579"
---
# <a name="iagentballoonexsetnumlines"></a>IAgentBalloonEx::SetNumLines

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetNumLines(
   long lLines,  // number of lines setting
);
```

Imposta il numero di righe di output di testo che è possibile visualizzare nel fumetto di parola del carattere.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.
-   Restituisce E \_ INVALIDARG se il parametro è zero.

<dl> <dt>

<span id="lLines"></span><span id="llines"></span><span id="LLINES"></span>*lLines*
</dt> <dd>

Numero di righe da visualizzare nel fumetto di Word.

</dd> </dl>

L'impostazione minima è 1 e il valore massimo è 128. Se il testo specificato nel metodo [**Speak**](speak-method.md) o [**think**](think-method.md) supera le dimensioni del fumetto corrente, Agent scorre automaticamente il testo nel fumetto.

Questo metodo avrà esito negativo se è impostato il bit di stile del fumetto **SizeToText** .

L'impostazione predefinita è basata sulle impostazioni quando il carattere viene compilato con l'editor dei caratteri di Microsoft Agent.

## <a name="see-also"></a>Vedere anche

[**IAgentBalloon:: GetNumLines**](iagentballoon--getnumlines.md), [**IAgentBalloonEx:: GetStyle**](iagentballoonex--getstyle.md), [**IAgentBalloonEx:: Sestyle**](iagentballoonex--setstyle.md)


 

 




