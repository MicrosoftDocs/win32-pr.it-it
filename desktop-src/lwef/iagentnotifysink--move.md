---
title: Spostamento IAgentNotifySink
description: Spostamento IAgentNotifySink
ms.assetid: d1809fdb-df4b-4884-b9e8-2877a814dc9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52563ff3838348b7bf8e6a2bcdfdf20a51c79723
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955774"
---
# <a name="iagentnotifysinkmove"></a><span data-ttu-id="03f34-103">IAgentNotifySink:: Move</span><span class="sxs-lookup"><span data-stu-id="03f34-103">IAgentNotifySink::Move</span></span>

<span data-ttu-id="03f34-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="03f34-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Move(
   long dwCharID,  // character ID
   long x,         // x-coordinate of new location
   long y,         // y-coordinate of new location
   long dwCause    // cause of move state
);                          
```

<span data-ttu-id="03f34-105">Notifica a un'applicazione client quando il carattere è stato spostato.</span><span class="sxs-lookup"><span data-stu-id="03f34-105">Notifies a client application when the character has been moved.</span></span>

-   <span data-ttu-id="03f34-106">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="03f34-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="03f34-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="03f34-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="03f34-108">Identificatore del carattere che è stato spostato.</span><span class="sxs-lookup"><span data-stu-id="03f34-108">Identifier of the character that has been moved.</span></span>

</dd> <dt>

<span data-ttu-id="03f34-109"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="03f34-109"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="03f34-110">Coordinata x della nuova posizione, espressa in pixel, rispetto all'origine dello schermo (in alto a sinistra).</span><span class="sxs-lookup"><span data-stu-id="03f34-110">The x-coordinate of the new position in pixels, relative to the screen origin (upper left).</span></span> <span data-ttu-id="03f34-111">La posizione di un carattere è basata sull'angolo superiore sinistro del frame di animazione.</span><span class="sxs-lookup"><span data-stu-id="03f34-111">The location of a character is based on the upper left corner of its animation frame.</span></span>

</dd> <dt>

<span data-ttu-id="03f34-112"><span id="y"></span><span id="Y"></span>*y*</span><span class="sxs-lookup"><span data-stu-id="03f34-112"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="03f34-113">Coordinata y della nuova posizione, espressa in pixel, rispetto all'origine dello schermo (in alto a sinistra).</span><span class="sxs-lookup"><span data-stu-id="03f34-113">The y-coordinate of the new position in pixels, relative to the screen origin (upper left).</span></span> <span data-ttu-id="03f34-114">La posizione di un carattere è basata sull'angolo superiore sinistro del frame di animazione.</span><span class="sxs-lookup"><span data-stu-id="03f34-114">The location of a character is based on the upper left corner of its animation frame.</span></span>

</dd> <dt>

<span data-ttu-id="03f34-115"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*</span><span class="sxs-lookup"><span data-stu-id="03f34-115"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*</span></span>
</dt> <dd>

<span data-ttu-id="03f34-116">Motivo dello spostamento dei caratteri.</span><span class="sxs-lookup"><span data-stu-id="03f34-116">The cause of the character move.</span></span> <span data-ttu-id="03f34-117">Il parametro può essere uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="03f34-117">The parameter may be one of the following:</span></span>



| <span data-ttu-id="03f34-118">Valore</span><span class="sxs-lookup"><span data-stu-id="03f34-118">Value</span></span>                                                          | <span data-ttu-id="03f34-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="03f34-119">Description</span></span>                                                                          |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="03f34-120">**const unsigned short** **NeverMoved = 0;**</span><span class="sxs-lookup"><span data-stu-id="03f34-120">**const unsigned short** **NeverMoved = 0;**</span></span><br/>        | <span data-ttu-id="03f34-121">Il carattere non è stato spostato.</span><span class="sxs-lookup"><span data-stu-id="03f34-121">Character has not been moved.</span></span>                                                        |
| <span data-ttu-id="03f34-122">**const unsigned short** **UserMoved = 1;**</span><span class="sxs-lookup"><span data-stu-id="03f34-122">**const unsigned short** **UserMoved = 1;**</span></span><br/>         | <span data-ttu-id="03f34-123">Il carattere è stato trascinato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="03f34-123">User dragged the character.</span></span>                                                          |
| <span data-ttu-id="03f34-124">ProgramMoved **short const senza segno** **= 2;**</span><span class="sxs-lookup"><span data-stu-id="03f34-124">**const unsigned short** **ProgramMoved = 2;**</span></span><br/>      | <span data-ttu-id="03f34-125">L'applicazione ha spostato il carattere.</span><span class="sxs-lookup"><span data-stu-id="03f34-125">Your application moved the character.</span></span>                                                |
| <span data-ttu-id="03f34-126">**const unsigned short** **OtherProgramMoved = 3;**</span><span class="sxs-lookup"><span data-stu-id="03f34-126">**const unsigned short** **OtherProgramMoved = 3;**</span></span><br/> | <span data-ttu-id="03f34-127">Il carattere è stato spostato da un'altra applicazione.</span><span class="sxs-lookup"><span data-stu-id="03f34-127">Another application moved the character.</span></span>                                             |
| <span data-ttu-id="03f34-128">SystemMoved **short const senza segno** **= 4**</span><span class="sxs-lookup"><span data-stu-id="03f34-128">**const unsigned short** **SystemMoved = 4**</span></span><br/>        | <span data-ttu-id="03f34-129">Il server ha spostato il carattere per mantenerlo sullo schermo dopo una modifica della risoluzione dello schermo.</span><span class="sxs-lookup"><span data-stu-id="03f34-129">The server moved the character to keep it onscreen after a screen resolution change.</span></span> |



 

</dd> </dl>

<span data-ttu-id="03f34-130">Questo evento viene inviato a tutti i client del carattere.</span><span class="sxs-lookup"><span data-stu-id="03f34-130">This event is sent to all clients of the character.</span></span>

## <a name="see-also"></a><span data-ttu-id="03f34-131">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="03f34-131">See Also</span></span>

<span data-ttu-id="03f34-132">[**IAgentCharacter:: GetMoveCause**](iagentcharacter--getmovecause.md), [ **IAgentCharacter:: MoveTo**](iagentcharacter--moveto.md)</span><span class="sxs-lookup"><span data-stu-id="03f34-132">[**IAgentCharacter::GetMoveCause**](iagentcharacter--getmovecause.md), [**IAgentCharacter::MoveTo**](iagentcharacter--moveto.md)</span></span>


 

 





