---
title: IAgentNotifySink RequestComplete
description: IAgentNotifySink RequestComplete
ms.assetid: 995bc961-f175-4429-94a4-91962161298b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0265a7111369dec687fd74b9c66c27275a40e164
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331999"
---
# <a name="iagentnotifysinkrequestcomplete"></a><span data-ttu-id="b1229-103">IAgentNotifySink::RequestComplete</span><span class="sxs-lookup"><span data-stu-id="b1229-103">IAgentNotifySink::RequestComplete</span></span>

<span data-ttu-id="b1229-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b1229-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT RequestComplete(
   long dwRequestID,  // request ID
   long hrStatus      // status code
);                          
```

<span data-ttu-id="b1229-105">Notifica a un'applicazione client il completamento di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="b1229-105">Notifies a client application when a request completes.</span></span>

-   <span data-ttu-id="b1229-106">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="b1229-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="b1229-107"><span id="dwRequestID"></span><span id="dwrequestid"></span><span id="DWREQUESTID"></span>*dwRequestID*</span><span class="sxs-lookup"><span data-stu-id="b1229-107"><span id="dwRequestID"></span><span id="dwrequestid"></span><span id="DWREQUESTID"></span>*dwRequestID*</span></span>
</dt> <dd>

<span data-ttu-id="b1229-108">Identificatore della richiesta avviata.</span><span class="sxs-lookup"><span data-stu-id="b1229-108">Identifier of the request that started.</span></span>

</dd> <dt>

<span data-ttu-id="b1229-109"><span id="hrStatus"></span><span id="hrstatus"></span><span id="HRSTATUS"></span>*hrStatus*</span><span class="sxs-lookup"><span data-stu-id="b1229-109"><span id="hrStatus"></span><span id="hrstatus"></span><span id="HRSTATUS"></span>*hrStatus*</span></span>
</dt> <dd>

<span data-ttu-id="b1229-110">Codice di stato.</span><span class="sxs-lookup"><span data-stu-id="b1229-110">Status code.</span></span> <span data-ttu-id="b1229-111">Questo parametro restituisce il codice di stato per la richiesta.</span><span class="sxs-lookup"><span data-stu-id="b1229-111">This parameter returns the status code for the request.</span></span>

</dd> </dl>

<span data-ttu-id="b1229-112">Questo evento consente di tenere traccia del momento in cui un metodo in coda viene completato utilizzando il relativo ID richiesta.</span><span class="sxs-lookup"><span data-stu-id="b1229-112">This event enables you to track when a queued method completes using its request ID.</span></span>

## <a name="see-also"></a><span data-ttu-id="b1229-113">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="b1229-113">See Also</span></span>

<span data-ttu-id="b1229-114">[**IAgentNotifySink:: RequestStart**](iagentnotifysink--requeststart.md), [**IAgent:: Load**](iagent--load.md), [**IAgentCharacter:: GestureAt**](iagentcharacter--gestureat.md), [**IAgentCharacter:: Hide**](iagentcharacter--hide.md), [**IAgentCharacter:: interrupt**](iagentcharacter--interrupt.md), [**IAgentCharacter:: moveto**](iagentcharacter--moveto.md), [**IAgentCharacter::P repare**](iagentcharacter--prepare.md), [**IAgentCharacter::P Lay**](iagentcharacter--play.md), [**IAgentCharacter:: Show**](iagentcharacter--show.md), [**IAgentCharacter:: Speak**](iagentcharacter--speak.md), [**IAgentCharacter:: wait**](iagentcharacter--wait.md)</span><span class="sxs-lookup"><span data-stu-id="b1229-114">[**IAgentNotifySink::RequestStart**](iagentnotifysink--requeststart.md), [**IAgent::Load**](iagent--load.md), [**IAgentCharacter::GestureAt**](iagentcharacter--gestureat.md), [**IAgentCharacter::Hide**](iagentcharacter--hide.md), [**IAgentCharacter::Interrupt**](iagentcharacter--interrupt.md), [**IAgentCharacter::MoveTo**](iagentcharacter--moveto.md), [**IAgentCharacter::Prepare**](iagentcharacter--prepare.md), [**IAgentCharacter::Play**](iagentcharacter--play.md), [**IAgentCharacter::Show**](iagentcharacter--show.md), [**IAgentCharacter::Speak**](iagentcharacter--speak.md), [**IAgentCharacter::Wait**](iagentcharacter--wait.md)</span></span>


 

 




