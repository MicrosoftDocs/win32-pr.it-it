---
title: IAgentNotifySink inattivo
description: IAgentNotifySink inattivo
ms.assetid: 7770a698-31d9-4f3a-9c7e-858c480b640e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b43e060f361499b02bc0a83db697938975c76291
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298794"
---
# <a name="iagentnotifysinkidle"></a><span data-ttu-id="09bd4-103">IAgentNotifySink:: Idle</span><span class="sxs-lookup"><span data-stu-id="09bd4-103">IAgentNotifySink::Idle</span></span>

<span data-ttu-id="09bd4-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="09bd4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Idle(
   long dwCharID,  // character ID
   long bStart     // start flag
);                          
```

<span data-ttu-id="09bd4-105">Notifica a un'applicazione client quando è stato modificato lo stato di **minimo** di un carattere.</span><span class="sxs-lookup"><span data-stu-id="09bd4-105">Notifies a client application when a character's **Idling** state has changed.</span></span>

-   <span data-ttu-id="09bd4-106">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="09bd4-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="09bd4-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="09bd4-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="09bd4-108">Identificatore della richiesta avviata.</span><span class="sxs-lookup"><span data-stu-id="09bd4-108">Identifier of the request that started.</span></span>

</dd> <dt>

<span data-ttu-id="09bd4-109"><span id="bStart"></span><span id="bstart"></span><span id="BSTART"></span>*bStart*</span><span class="sxs-lookup"><span data-stu-id="09bd4-109"><span id="bStart"></span><span id="bstart"></span><span id="BSTART"></span>*bStart*</span></span>
</dt> <dd>

<span data-ttu-id="09bd4-110">Flag di avvio.</span><span class="sxs-lookup"><span data-stu-id="09bd4-110">Start flag.</span></span> <span data-ttu-id="09bd4-111">Questo valore booleano è **true** quando il carattere inizia al minimo e **false** quando si arresta al minimo.</span><span class="sxs-lookup"><span data-stu-id="09bd4-111">This Boolean value is **True** when the character begins idling and **False** when it stops idling.</span></span>

</dd> </dl>

<span data-ttu-id="09bd4-112">Questo evento consente di tenere traccia del momento in cui il server Microsoft Agent avvia o interrompe l'elaborazione inattiva per un carattere.</span><span class="sxs-lookup"><span data-stu-id="09bd4-112">This event enables you to track when the Microsoft Agent server starts or stops idle processing for a character.</span></span>

## <a name="see-also"></a><span data-ttu-id="09bd4-113">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="09bd4-113">See Also</span></span>

<span data-ttu-id="09bd4-114">[**IAgentCharacter:: GetIdleOn**](iagentcharacter--getidleon.md), [ **IAgentCharacter:: SetIdleOn**](iagentcharacter--setidleon.md)</span><span class="sxs-lookup"><span data-stu-id="09bd4-114">[**IAgentCharacter::GetIdleOn**](iagentcharacter--getidleon.md), [**IAgentCharacter::SetIdleOn**](iagentcharacter--setidleon.md)</span></span>


 

 




