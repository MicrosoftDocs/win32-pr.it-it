---
title: IAgentBalloon GetFontCharSet
description: IAgentBalloon GetFontCharSet
ms.assetid: 1ab5767a-31e3-449c-b242-f20b11336ca0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f809fbd83e44259c96184c9f364a85151ec9ddde
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120406"
---
# <a name="iagentballoongetfontcharset"></a>IAgentBalloon::GetFontCharSet

\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetFontCharSet(
   short * psFontCharSet  // character set displayed in word balloon
); 
```

Indica il set di caratteri del tipo di carattere visualizzato in un fumetto di parole.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="psFontCharSet"></span><span id="psfontcharset"></span><span id="PSFONTCHARSET"></span>*psFontCharSet*
</dt> <dd>

Indirizzo di un valore che riceve il set di caratteri del tipo di carattere. Di seguito sono riportate alcune impostazioni comuni per value:



| Valore    | Set di caratteri                                                                                       |
|-----|----------------------------------------------------------------------------------------|
| 0   | Caratteri Windows standard (ANSI).                                                    |
| 1   | Set di caratteri predefinito.                                                                 |
| 2   | Set di caratteri del simbolo.                                                              |
| 128 | Set di caratteri a byte doppio (DBCS) univoco per la versione giapponese di Windows.            |
| 129 | Set di caratteri a byte doppio (DBCS) univoco per la versione coreana di Windows.              |
| 134 | Set di caratteri a byte doppio (DBCS) univoco per la versione in cinese semplificato di Windows.  |
| 136 | Set di caratteri a byte doppio (DBCS) univoco per la versione in cinese tradizionale di Windows. |
| 255 | Caratteri estesi in genere visualizzati dalle applicazioni MS-DOS.                          |



 

</dd> </dl>

Per altri valori del set di caratteri, vedere la documentazione di Platform SDK.

Il set di caratteri predefinito usato nel fumetto di un carattere è definito nell'editor di caratteri di Microsoft Agent. È possibile modificarlo [**usando IAgentBalloon::SetFontCharSet**](iagentballoon--setfontcharset.md). Tuttavia, l'utente può eseguire l'override dell'impostazione del set di caratteri per tutti i caratteri usando la finestra delle proprietà di Microsoft Agent.

## <a name="see-also"></a>Vedere anche

[**IAgentBalloon::SetFontCharSet**](iagentballoon--setfontcharset.md)


 

 




