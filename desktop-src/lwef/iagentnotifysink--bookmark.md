---
title: Segnalibro IAgentNotifySink
description: Segnalibro IAgentNotifySink
ms.assetid: 172042af-a524-4ea4-955d-4e3dee079344
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02562b7cbf42c3445a25edc5071476da1b2d8dc53d80923ad875fddf09e5d31b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477097"
---
# <a name="iagentnotifysinkbookmark"></a>IAgentNotifySink::Bookmark

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT Bookmark(
   long dwBookMarkID  // bookmark ID
);                          
```

Notifica a un'applicazione client il completamento del segnalibro.

-   Nessun valore restituito.

<dl> <dt>

<span id="dwBookMarkID"></span><span id="dwbookmarkid"></span><span id="DWBOOKMARKID"></span>*dwBookMarkID*
</dt> <dd>

Identificatore del segnalibro che ha generato l'evento.

</dd> </dl>

Quando si includono tag segnalibro in [**un metodo Speak,**](speak-method.md) è possibile tenere traccia di quando si verificano con questo evento.

## <a name="see-also"></a>Vedere anche

[**IAgentCharacter::Speak , Tag**](iagentcharacter--speak.md) [di output vocale di Microsoft Agent](microsoft-agent-speech-output-tags.md)


 

 




