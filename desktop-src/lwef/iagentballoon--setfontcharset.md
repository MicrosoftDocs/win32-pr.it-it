---
title: IAgentBalloon SetFontCharSet
description: IAgentBalloon SetFontCharSet
ms.assetid: ce1b152d-c8af-47ec-9e6b-5768dbcf3566
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18cc462895ff9f19f7e722660608a268af13446f
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120206"
---
# <a name="iagentballoonsetfontcharset"></a>IAgentBalloon::SetFontCharSet

\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetFontCharSet(
   short sFontCharSet  // character set displayed in word balloon
); 
```

Imposta il set di caratteri del tipo di carattere visualizzato nel fumetto.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="sFontCharSet"></span><span id="sfontcharset"></span><span id="SFONTCHARSET"></span>*sFontCharSet*
</dt> <dd>

Set di caratteri del tipo di carattere. Di seguito sono riportate alcune impostazioni comuni per value:



| Valore    | Set di caratteri                                                                                       |
|-----|----------------------------------------------------------------------------------------|
| 0   | Caratteri Windows standard (ANSI).                                                    |
| 1   | Set di caratteri predefinito.                                                                 |
| 2   | Set di caratteri dei simboli.                                                              |
| 128 | Set di caratteri a byte doppio (DBCS) univoco per la versione giapponese di Windows.            |
| 129 | Set di caratteri a byte doppio (DBCS) univoco per la versione coreana di Windows.              |
| 134 | Set di caratteri a byte doppio (DBCS) univoco per la versione in cinese semplificato di Windows.  |
| 136 | Set di caratteri a byte doppio (DBCS) univoco per la versione in cinese tradizionale di Windows. |
| 255 | Caratteri estesi in genere visualizzati dalle applicazioni MS-DOS.                          |



 

</dd> </dl>

Per altri valori del set di caratteri, vedere la documentazione di Platform SDK.

Il set di caratteri predefinito usato nel fumetto delle parole di un carattere è definito nell'editor di caratteri di Microsoft Agent. È possibile modificarlo con [**IAgentBalloon::SetFontCharSet**](https://www.bing.com/search?q=**IAgentBalloon::SetFontCharSet**). Tuttavia, l'utente può eseguire l'override dell'impostazione del set di caratteri per tutti i caratteri usando la finestra delle proprietà di Microsoft Agent. Questa proprietà si applica solo all'uso del carattere da parte dell'applicazione client. L'impostazione non influisce su altri client del carattere o di altri caratteri dell'applicazione client.

## <a name="see-also"></a>Vedere anche

[**IAgentBalloon::GetFontCharSet**](iagentballoon--getfontcharset.md)


 

 




