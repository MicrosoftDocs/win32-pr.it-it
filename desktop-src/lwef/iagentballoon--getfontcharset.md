---
title: IAgentBalloon GetFontCharSet
description: IAgentBalloon GetFontCharSet
ms.assetid: 1ab5767a-31e3-449c-b242-f20b11336ca0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54f544df6c09fb00d346015b610751dd23738820
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221603"
---
# <a name="iagentballoongetfontcharset"></a>IAgentBalloon::GetFontCharSet

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetFontCharSet(
   short * psFontCharSet  // character set displayed in word balloon
); 
```

Indica il set di caratteri del tipo di carattere visualizzato in un fumetto di Word.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="psFontCharSet"></span><span id="psfontcharset"></span><span id="PSFONTCHARSET"></span>*psFontCharSet*
</dt> <dd>

Indirizzo di un valore che riceve il set di caratteri del tipo di carattere. Di seguito sono riportate alcune impostazioni comuni per value:



|     |                                                                                        |
|-----|----------------------------------------------------------------------------------------|
| 0   | Caratteri Windows standard (ANSI).                                                    |
| 1   | Set di caratteri predefinito.                                                                 |
| 2   | Set di caratteri del simbolo.                                                              |
| 128 | Set di caratteri a doppio byte (DBCS) univoco per la versione giapponese di Windows.            |
| 129 | Set di caratteri a doppio byte (DBCS) univoco per la versione coreana di Windows.              |
| 134 | Set di caratteri a doppio byte (DBCS) univoco per la versione in cinese semplificato di Windows.  |
| 136 | Set di caratteri a doppio byte (DBCS) univoco per la versione cinese tradizionale di Windows. |
| 255 | Caratteri estesi generalmente visualizzati dalle applicazioni MS-DOS.                          |



 

</dd> </dl>

Per altri valori del set di caratteri, vedere la documentazione di Platform SDK.

Il set di caratteri predefinito utilizzato nella parola Balloon di un carattere viene definito nell'editor dei caratteri di Microsoft Agent. È possibile modificarlo utilizzando [**IAgentBalloon:: SetFontCharSet**](iagentballoon--setfontcharset.md). Tuttavia, l'utente può eseguire l'override dell'impostazione del set di caratteri per tutti i caratteri utilizzando la finestra delle proprietà di Microsoft Agent.

## <a name="see-also"></a>Vedere anche

[**IAgentBalloon::SetFontCharSet**](iagentballoon--setfontcharset.md)


 

 




