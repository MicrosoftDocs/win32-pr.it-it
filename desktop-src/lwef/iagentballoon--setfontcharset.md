---
title: IAgentBalloon SetFontCharSet
description: IAgentBalloon SetFontCharSet
ms.assetid: ce1b152d-c8af-47ec-9e6b-5768dbcf3566
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6202aa144d13c3c7435be03721a3f8fd4878b93
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298869"
---
# <a name="iagentballoonsetfontcharset"></a>IAgentBalloon::SetFontCharSet

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetFontCharSet(
   short sFontCharSet  // character set displayed in word balloon
); 
```

Imposta il set di caratteri del tipo di carattere visualizzato nella parola Balloon.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="sFontCharSet"></span><span id="sfontcharset"></span><span id="SFONTCHARSET"></span>*sFontCharSet*
</dt> <dd>

Set di caratteri del tipo di carattere. Di seguito sono riportate alcune impostazioni comuni per value:



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

Il set di caratteri predefinito utilizzato nella parola Balloon di un carattere viene definito nell'editor dei caratteri di Microsoft Agent. È possibile modificarlo con [**IAgentBalloon:: SetFontCharSet**](https://www.bing.com/search?q=**IAgentBalloon::SetFontCharSet**). Tuttavia, l'utente può eseguire l'override dell'impostazione del set di caratteri per tutti i caratteri utilizzando la finestra delle proprietà di Microsoft Agent. Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.

## <a name="see-also"></a>Vedere anche

[**IAgentBalloon::GetFontCharSet**](iagentballoon--getfontcharset.md)


 

 




