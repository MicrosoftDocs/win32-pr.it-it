---
title: Segnalibro IAgentNotifySink
description: Segnalibro IAgentNotifySink
ms.assetid: 172042af-a524-4ea4-955d-4e3dee079344
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1febedfc962904544a49b8621812d0518026b459
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709310"
---
# <a name="iagentnotifysinkbookmark"></a>IAgentNotifySink:: segnalibro

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT Bookmark(
   long dwBookMarkID  // bookmark ID
);                          
```

Notifica a un'applicazione client quando il relativo segnalibro viene completato.

-   Nessun valore restituito.

<dl> <dt>

<span id="dwBookMarkID"></span><span id="dwbookmarkid"></span><span id="DWBOOKMARKID"></span>*dwBookMarkID*
</dt> <dd>

Identificatore del segnalibro che ha generato l'attivazione dell'evento.

</dd> </dl>

Quando si includono tag di segnalibro in un metodo [**Speak**](speak-method.md) , è possibile tenere traccia del momento in cui si verificano con questo evento.

## <a name="see-also"></a>Vedere anche

[**IAgentCharacter:: Speak**](iagentcharacter--speak.md), [tag di output di sintesi vocale di Microsoft Agent](microsoft-agent-speech-output-tags.md)


 

 




