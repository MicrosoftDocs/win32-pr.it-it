---
title: IAgentNotifySink VisibleState
description: IAgentNotifySink VisibleState
ms.assetid: b0346296-74e9-448f-aa6d-a9fb1e645f05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3525c079ecd1b566ac2230f06e3effa1ceb7a694
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298733"
---
# <a name="iagentnotifysinkvisiblestate"></a><span data-ttu-id="2a5d8-103">IAgentNotifySink::VisibleState</span><span class="sxs-lookup"><span data-stu-id="2a5d8-103">IAgentNotifySink::VisibleState</span></span>

<span data-ttu-id="2a5d8-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2a5d8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT VisibleState(
   long dwCharID,  // character ID
   long bVisible,  // visibility flag
   long dwCause,   // cause of visible state
);                          
```

<span data-ttu-id="2a5d8-105">Notifica a un'applicazione client quando viene modificato lo stato di visibilità del carattere.</span><span class="sxs-lookup"><span data-stu-id="2a5d8-105">Notifies a client application when the visibility state of the character changes.</span></span>

-   <span data-ttu-id="2a5d8-106">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="2a5d8-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="2a5d8-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="2a5d8-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="2a5d8-108">Identificatore del carattere il cui stato di visibilità viene modificato.</span><span class="sxs-lookup"><span data-stu-id="2a5d8-108">Identifier of the character whose visibility state is changed.</span></span>

</dd> <dt>

<span data-ttu-id="2a5d8-109"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span><span class="sxs-lookup"><span data-stu-id="2a5d8-109"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="2a5d8-110">Flag di visibilità.</span><span class="sxs-lookup"><span data-stu-id="2a5d8-110">Visibility flag.</span></span> <span data-ttu-id="2a5d8-111">Questo valore booleano è **true** quando il carattere diventa visibile e **false** quando il carattere viene nascosto.</span><span class="sxs-lookup"><span data-stu-id="2a5d8-111">This Boolean value is **True** when character becomes visible and **False** when the character becomes hidden.</span></span>

</dd> <dt>

<span data-ttu-id="2a5d8-112"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*</span><span class="sxs-lookup"><span data-stu-id="2a5d8-112"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*</span></span>
</dt> <dd>

<span data-ttu-id="2a5d8-113">Motivo dell'Ultima modifica apportata allo stato di visibilità del carattere.</span><span class="sxs-lookup"><span data-stu-id="2a5d8-113">Cause of last change to the character's visibility state.</span></span> <span data-ttu-id="2a5d8-114">Il parametro può essere uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="2a5d8-114">The parameter may be one of the following:</span></span>



| <span data-ttu-id="2a5d8-115">Valore</span><span class="sxs-lookup"><span data-stu-id="2a5d8-115">Value</span></span>                                                                   | <span data-ttu-id="2a5d8-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2a5d8-116">Description</span></span>                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a5d8-117">**const unsigned short** **NeverShown = 0;**</span><span class="sxs-lookup"><span data-stu-id="2a5d8-117">**const unsigned short** **NeverShown = 0;**</span></span><br/>                 | <span data-ttu-id="2a5d8-118">Il carattere non è stato visualizzato.</span><span class="sxs-lookup"><span data-stu-id="2a5d8-118">Character has not been shown.</span></span>                                                               |
| <span data-ttu-id="2a5d8-119">**const unsigned short** **UserHid = 1;**</span><span class="sxs-lookup"><span data-stu-id="2a5d8-119">**const unsigned short** **UserHid = 1;**</span></span><br/>                    | <span data-ttu-id="2a5d8-120">L'utente ha nascosto il carattere con il menu di scelta rapida dell'icona della barra delle applicazioni del carattere o con input vocale.</span><span class="sxs-lookup"><span data-stu-id="2a5d8-120">User hid the character with the character's taskbar icon pop-up menu or with speech input..</span></span> |
| <span data-ttu-id="2a5d8-121">UserShowed **short const senza segno** **= 2;**</span><span class="sxs-lookup"><span data-stu-id="2a5d8-121">**const unsigned short** **UserShowed = 2;**</span></span><br/>                 | <span data-ttu-id="2a5d8-122">L'utente ha mostrato il carattere.</span><span class="sxs-lookup"><span data-stu-id="2a5d8-122">User showed the character.</span></span>                                                                  |
| <span data-ttu-id="2a5d8-123">**const unsigned short** **ProgramHid = 3;**</span><span class="sxs-lookup"><span data-stu-id="2a5d8-123">**const unsigned short** **ProgramHid = 3;**</span></span><br/>                 | <span data-ttu-id="2a5d8-124">L'applicazione ha nascosto il carattere.</span><span class="sxs-lookup"><span data-stu-id="2a5d8-124">Your application hid the character.</span></span>                                                         |
| <span data-ttu-id="2a5d8-125">ProgramShowed **short const senza segno** **= 4;**</span><span class="sxs-lookup"><span data-stu-id="2a5d8-125">**const unsigned short** **ProgramShowed = 4;**</span></span><br/>              | <span data-ttu-id="2a5d8-126">L'applicazione ha mostrato il carattere.</span><span class="sxs-lookup"><span data-stu-id="2a5d8-126">Your application showed the character.</span></span>                                                      |
| <span data-ttu-id="2a5d8-127">**const unsigned short** **OtherProgramHid = 5;**</span><span class="sxs-lookup"><span data-stu-id="2a5d8-127">**const unsigned short** **OtherProgramHid = 5;**</span></span><br/>            | <span data-ttu-id="2a5d8-128">Il carattere è stato nascosto da un'altra applicazione.</span><span class="sxs-lookup"><span data-stu-id="2a5d8-128">Another application hid the character.</span></span>                                                      |
| <span data-ttu-id="2a5d8-129">OtherProgramShowed **short senza segno const** **= 6;**</span><span class="sxs-lookup"><span data-stu-id="2a5d8-129">**const unsigned short** **OtherProgramShowed = 6;**</span></span><br/>         | <span data-ttu-id="2a5d8-130">Un'altra applicazione ha mostrato il carattere.</span><span class="sxs-lookup"><span data-stu-id="2a5d8-130">Another application showed the character.</span></span>                                                   |
| <span data-ttu-id="2a5d8-131">UserHidViaCharacterMenu **short const senza segno** **= 7**</span><span class="sxs-lookup"><span data-stu-id="2a5d8-131">**const unsigned short** **UserHidViaCharacterMenu = 7**</span></span><br/>     | <span data-ttu-id="2a5d8-132">L'utente ha nascosto il carattere con il menu di scelta rapida del carattere.</span><span class="sxs-lookup"><span data-stu-id="2a5d8-132">User hid the character with the character's pop-up menu.</span></span>                                    |
| <span data-ttu-id="2a5d8-133">**const unsigned short** **UserHidViaTaskbarIcon = UserHid**</span><span class="sxs-lookup"><span data-stu-id="2a5d8-133">**const unsigned short** **UserHidViaTaskbarIcon = UserHid**</span></span><br/> | <span data-ttu-id="2a5d8-134">L'utente ha nascosto il carattere con il menu di scelta rapida dell'icona della barra delle applicazioni del carattere o usando l'input vocale.</span><span class="sxs-lookup"><span data-stu-id="2a5d8-134">User hid the character with the character's taskbar icon pop-up menu or using speech input.</span></span> |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="2a5d8-135">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="2a5d8-135">See Also</span></span>

<span data-ttu-id="2a5d8-136">[**IAgentCharacter:: getVisible**](iagentcharacter--getvisible.md), [ **IAgentCharacter:: GetVisibilityCause**](iagentcharacter--getvisibilitycause.md)</span><span class="sxs-lookup"><span data-stu-id="2a5d8-136">[**IAgentCharacter::GetVisible**](iagentcharacter--getvisible.md), [**IAgentCharacter::GetVisibilityCause**](iagentcharacter--getvisibilitycause.md)</span></span>


 

 





