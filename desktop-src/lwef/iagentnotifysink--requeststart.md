---
title: IAgentNotifySink RequestStart
description: IAgentNotifySink RequestStart
ms.assetid: acac2bf8-7472-4952-a984-a29654fb8b0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67ced12596114214cf712cef8dbbe81edb5af278
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713621"
---
# <a name="iagentnotifysinkrequeststart"></a><span data-ttu-id="a6d38-103">IAgentNotifySink::RequestStart</span><span class="sxs-lookup"><span data-stu-id="a6d38-103">IAgentNotifySink::RequestStart</span></span>

<span data-ttu-id="a6d38-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a6d38-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT RequestStart(
   long dwRequestID  // request ID
);                          
```

<span data-ttu-id="a6d38-105">Notifica a un'applicazione client l'inizio di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="a6d38-105">Notifies a client application when a request begins.</span></span>

-   <span data-ttu-id="a6d38-106">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="a6d38-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="a6d38-107"><span id="dwRequestID"></span><span id="dwrequestid"></span><span id="DWREQUESTID"></span>*dwRequestID*</span><span class="sxs-lookup"><span data-stu-id="a6d38-107"><span id="dwRequestID"></span><span id="dwrequestid"></span><span id="DWREQUESTID"></span>*dwRequestID*</span></span>
</dt> <dd>

<span data-ttu-id="a6d38-108">Identificatore della richiesta avviata.</span><span class="sxs-lookup"><span data-stu-id="a6d38-108">Identifier of the request that started.</span></span>

</dd> </dl>

<span data-ttu-id="a6d38-109">Questo evento consente di tenere traccia del momento in cui una richiesta accodata inizia a usare il relativo ID richiesta.</span><span class="sxs-lookup"><span data-stu-id="a6d38-109">This event enables you to track when a queued request begins using its request ID.</span></span>

## <a name="see-also"></a><span data-ttu-id="a6d38-110">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="a6d38-110">See Also</span></span>

<span data-ttu-id="a6d38-111">[**IAgentNotifySink:: RequestComplete**](iagentnotifysink--requestcomplete.md), [**IAgent:: Load**](iagent--load.md), [**IAgentCharacter:: GestureAt**](iagentcharacter--gestureat.md), [**IAgentCharacter:: Hide**](iagentcharacter--hide.md), [**IAgentCharacter:: interrupt**](iagentcharacter--interrupt.md), [**IAgentCharacter:: moveto**](iagentcharacter--moveto.md), [**IAgentCharacter::P repare**](iagentcharacter--prepare.md), [**IAgentCharacter::P Lay**](iagentcharacter--play.md), [**IAgentCharacter:: Show**](iagentcharacter--show.md), [**IAgentCharacter:: Speak**](iagentcharacter--speak.md), [**IAgentCharacter:: wait**](iagentcharacter--wait.md)</span><span class="sxs-lookup"><span data-stu-id="a6d38-111">[**IAgentNotifySink::RequestComplete**](iagentnotifysink--requestcomplete.md), [**IAgent::Load**](iagent--load.md), [**IAgentCharacter::GestureAt**](iagentcharacter--gestureat.md), [**IAgentCharacter::Hide**](iagentcharacter--hide.md), [**IAgentCharacter::Interrupt**](iagentcharacter--interrupt.md), [**IAgentCharacter::MoveTo**](iagentcharacter--moveto.md), [**IAgentCharacter::Prepare**](iagentcharacter--prepare.md), [**IAgentCharacter::Play**](iagentcharacter--play.md), [**IAgentCharacter::Show**](iagentcharacter--show.md), [**IAgentCharacter::Speak**](iagentcharacter--speak.md), [**IAgentCharacter::Wait**](iagentcharacter--wait.md)</span></span>


 

 




