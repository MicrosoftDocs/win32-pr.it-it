---
title: IAgentCharacter GetVisibilityCause
description: IAgentCharacter GetVisibilityCause
ms.assetid: 46f681de-1c99-4f90-a3fe-aae04bb75339
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6013385144b82b79a0f17ae6443b094a9d9c8a4c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396983"
---
# <a name="iagentcharactergetvisibilitycause"></a><span data-ttu-id="5c29b-103">IAgentCharacter::GetVisibilityCause</span><span class="sxs-lookup"><span data-stu-id="5c29b-103">IAgentCharacter::GetVisibilityCause</span></span>

<span data-ttu-id="5c29b-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5c29b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVisibilityCause(
   long * pdwCause  // address of variable for cause of character visible state
);
```

<span data-ttu-id="5c29b-105">Recupera la motivo dello stato visibile del carattere.</span><span class="sxs-lookup"><span data-stu-id="5c29b-105">Retrieves the cause of the character's visible state.</span></span>

-   <span data-ttu-id="5c29b-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="5c29b-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="5c29b-107"><span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*</span><span class="sxs-lookup"><span data-stu-id="5c29b-107"><span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*</span></span>
</dt> <dd>

<span data-ttu-id="5c29b-108">Indirizzo di una variabile che riceve la modifica dello stato dell'ultima visibilità del carattere e sarà uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="5c29b-108">Address of a variable that receives the cause of the character's last visibility state change and will be one of the following:</span></span>



| <span data-ttu-id="5c29b-109">Valore</span><span class="sxs-lookup"><span data-stu-id="5c29b-109">Value</span></span>                                                                   | <span data-ttu-id="5c29b-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5c29b-110">Description</span></span>                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c29b-111">**const unsigned short** **NeverShown = 0;**</span><span class="sxs-lookup"><span data-stu-id="5c29b-111">**const unsigned short** **NeverShown = 0;**</span></span><br/>                 | <span data-ttu-id="5c29b-112">Il carattere non è stato visualizzato.</span><span class="sxs-lookup"><span data-stu-id="5c29b-112">Character has not been shown.</span></span>                                                               |
| <span data-ttu-id="5c29b-113">**const unsigned short** **UserHid = 1;**</span><span class="sxs-lookup"><span data-stu-id="5c29b-113">**const unsigned short** **UserHid = 1;**</span></span><br/>                    | <span data-ttu-id="5c29b-114">L'utente ha nascosto il carattere con il menu di scelta rapida dell'icona della barra delle applicazioni del carattere o usando l'input vocale.</span><span class="sxs-lookup"><span data-stu-id="5c29b-114">User hid the character with the character's taskbar icon pop-up menu or using speech input.</span></span> |
| <span data-ttu-id="5c29b-115">UserShowed **short const senza segno** **= 2;**</span><span class="sxs-lookup"><span data-stu-id="5c29b-115">**const unsigned short** **UserShowed = 2;**</span></span><br/>                 | <span data-ttu-id="5c29b-116">L'utente ha mostrato il carattere.</span><span class="sxs-lookup"><span data-stu-id="5c29b-116">User showed the character.</span></span>                                                                  |
| <span data-ttu-id="5c29b-117">**const unsigned short** **ProgramHid = 3;**</span><span class="sxs-lookup"><span data-stu-id="5c29b-117">**const unsigned short** **ProgramHid = 3;**</span></span><br/>                 | <span data-ttu-id="5c29b-118">L'applicazione ha nascosto il carattere.</span><span class="sxs-lookup"><span data-stu-id="5c29b-118">Your application hid the character.</span></span>                                                         |
| <span data-ttu-id="5c29b-119">ProgramShowed **short const senza segno** **= 4;**</span><span class="sxs-lookup"><span data-stu-id="5c29b-119">**const unsigned short** **ProgramShowed = 4;**</span></span><br/>              | <span data-ttu-id="5c29b-120">L'applicazione ha mostrato il carattere.</span><span class="sxs-lookup"><span data-stu-id="5c29b-120">Your application showed the character.</span></span>                                                      |
| <span data-ttu-id="5c29b-121">**const unsigned short** **OtherProgramHid = 5;**</span><span class="sxs-lookup"><span data-stu-id="5c29b-121">**const unsigned short** **OtherProgramHid = 5;**</span></span><br/>            | <span data-ttu-id="5c29b-122">Il carattere è stato nascosto da un'altra applicazione.</span><span class="sxs-lookup"><span data-stu-id="5c29b-122">Another application hid the character.</span></span>                                                      |
| <span data-ttu-id="5c29b-123">OtherProgramShowed **short senza segno const** **= 6;**</span><span class="sxs-lookup"><span data-stu-id="5c29b-123">**const unsigned short** **OtherProgramShowed = 6;**</span></span><br/>         | <span data-ttu-id="5c29b-124">Un'altra applicazione ha mostrato il carattere.</span><span class="sxs-lookup"><span data-stu-id="5c29b-124">Another application showed the character.</span></span>                                                   |
| <span data-ttu-id="5c29b-125">UserHidViaCharacterMenu **short const senza segno** **= 7**</span><span class="sxs-lookup"><span data-stu-id="5c29b-125">**const unsigned short** **UserHidViaCharacterMenu = 7**</span></span><br/>     | <span data-ttu-id="5c29b-126">L'utente ha nascosto il carattere con il menu di scelta rapida del carattere.</span><span class="sxs-lookup"><span data-stu-id="5c29b-126">User hid the character with the character's pop-up menu.</span></span>                                    |
| <span data-ttu-id="5c29b-127">**const unsigned short** **UserHidViaTaskbarIcon = UserHid**</span><span class="sxs-lookup"><span data-stu-id="5c29b-127">**const unsigned short** **UserHidViaTaskbarIcon = UserHid**</span></span><br/> | <span data-ttu-id="5c29b-128">L'utente ha nascosto il carattere con il menu di scelta rapida dell'icona della barra delle applicazioni del carattere o usando l'input vocale.</span><span class="sxs-lookup"><span data-stu-id="5c29b-128">User hid the character with the character's taskbar icon pop-up menu or using speech input.</span></span> |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="5c29b-129">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="5c29b-129">See Also</span></span>

[<span data-ttu-id="5c29b-130">**IAgentNotifySink::VisibleState**</span><span class="sxs-lookup"><span data-stu-id="5c29b-130">**IAgentNotifySink::VisibleState**</span></span>](iagentnotifysink--visiblestate.md)


 

 





