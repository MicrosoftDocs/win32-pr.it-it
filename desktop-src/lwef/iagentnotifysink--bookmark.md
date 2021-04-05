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
# <a name="iagentnotifysinkbookmark"></a><span data-ttu-id="7d12b-103">IAgentNotifySink:: segnalibro</span><span class="sxs-lookup"><span data-stu-id="7d12b-103">IAgentNotifySink::Bookmark</span></span>

<span data-ttu-id="7d12b-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7d12b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Bookmark(
   long dwBookMarkID  // bookmark ID
);                          
```

<span data-ttu-id="7d12b-105">Notifica a un'applicazione client quando il relativo segnalibro viene completato.</span><span class="sxs-lookup"><span data-stu-id="7d12b-105">Notifies a client application when its bookmark completes.</span></span>

-   <span data-ttu-id="7d12b-106">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="7d12b-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="7d12b-107"><span id="dwBookMarkID"></span><span id="dwbookmarkid"></span><span id="DWBOOKMARKID"></span>*dwBookMarkID*</span><span class="sxs-lookup"><span data-stu-id="7d12b-107"><span id="dwBookMarkID"></span><span id="dwbookmarkid"></span><span id="DWBOOKMARKID"></span>*dwBookMarkID*</span></span>
</dt> <dd>

<span data-ttu-id="7d12b-108">Identificatore del segnalibro che ha generato l'attivazione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="7d12b-108">Identifier of the bookmark that resulted in triggering the event.</span></span>

</dd> </dl>

<span data-ttu-id="7d12b-109">Quando si includono tag di segnalibro in un metodo [**Speak**](speak-method.md) , è possibile tenere traccia del momento in cui si verificano con questo evento.</span><span class="sxs-lookup"><span data-stu-id="7d12b-109">When you include bookmark tags in a [**Speak**](speak-method.md) method, you can track when they occur with this event.</span></span>

## <a name="see-also"></a><span data-ttu-id="7d12b-110">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="7d12b-110">See Also</span></span>

<span data-ttu-id="7d12b-111">[**IAgentCharacter:: Speak**](iagentcharacter--speak.md), [tag di output di sintesi vocale di Microsoft Agent](microsoft-agent-speech-output-tags.md)</span><span class="sxs-lookup"><span data-stu-id="7d12b-111">[**IAgentCharacter::Speak**](iagentcharacter--speak.md), [Microsoft Agent Speech Output Tags](microsoft-agent-speech-output-tags.md)</span></span>


 

 




