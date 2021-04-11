---
title: DblClick IAgentNotifySink
description: DblClick IAgentNotifySink
ms.assetid: 7e86cc9b-8bc3-405e-9bbf-764cec9c3130
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9ec7372d524027588dae5a0a3aafaf07146556e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395991"
---
# <a name="iagentnotifysinkdblclick"></a><span data-ttu-id="2b3f0-103">IAgentNotifySink::D blClick</span><span class="sxs-lookup"><span data-stu-id="2b3f0-103">IAgentNotifySink::DblClick</span></span>

<span data-ttu-id="2b3f0-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2b3f0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT DblClick(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x coordinate of mouse pointer
   long y          // y coordinate of mouse pointer
);                          
```

<span data-ttu-id="2b3f0-105">Notifica a un'applicazione client quando l'utente fa doppio clic su un carattere.</span><span class="sxs-lookup"><span data-stu-id="2b3f0-105">Notifies a client application when the user double-clicks a character.</span></span>

-   <span data-ttu-id="2b3f0-106">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="2b3f0-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="2b3f0-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="2b3f0-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="2b3f0-108">Identificatore del carattere a doppio clic.</span><span class="sxs-lookup"><span data-stu-id="2b3f0-108">Identifier of the double-clicked character.</span></span>

</dd> <dt>

<span data-ttu-id="2b3f0-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span><span class="sxs-lookup"><span data-stu-id="2b3f0-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span></span>
</dt> <dd>

<span data-ttu-id="2b3f0-110">Parametro che indica il pulsante del mouse e lo stato del tasto di modifica.</span><span class="sxs-lookup"><span data-stu-id="2b3f0-110">A parameter that indicates the mouse button and modifier key state.</span></span> <span data-ttu-id="2b3f0-111">Il parametro può restituire qualsiasi combinazione dei seguenti elementi:</span><span class="sxs-lookup"><span data-stu-id="2b3f0-111">The parameter can return any combination of the following:</span></span>



|        |                                                |
|--------|------------------------------------------------|
| <span data-ttu-id="2b3f0-112">0x0001</span><span class="sxs-lookup"><span data-stu-id="2b3f0-112">0x0001</span></span> | <span data-ttu-id="2b3f0-113">Pulsante sinistro</span><span class="sxs-lookup"><span data-stu-id="2b3f0-113">Left Button</span></span>                                    |
| <span data-ttu-id="2b3f0-114">0x0010</span><span class="sxs-lookup"><span data-stu-id="2b3f0-114">0x0010</span></span> | <span data-ttu-id="2b3f0-115">Pulsante centrale</span><span class="sxs-lookup"><span data-stu-id="2b3f0-115">Middle Button</span></span>                                  |
| <span data-ttu-id="2b3f0-116">0x0002</span><span class="sxs-lookup"><span data-stu-id="2b3f0-116">0x0002</span></span> | <span data-ttu-id="2b3f0-117">Pulsante destro</span><span class="sxs-lookup"><span data-stu-id="2b3f0-117">Right Button</span></span>                                   |
| <span data-ttu-id="2b3f0-118">0x0004</span><span class="sxs-lookup"><span data-stu-id="2b3f0-118">0x0004</span></span> | <span data-ttu-id="2b3f0-119">Tasto MAIUSC giù</span><span class="sxs-lookup"><span data-stu-id="2b3f0-119">Shift Key Down</span></span>                                 |
| <span data-ttu-id="2b3f0-120">0x0008</span><span class="sxs-lookup"><span data-stu-id="2b3f0-120">0x0008</span></span> | <span data-ttu-id="2b3f0-121">Chiave di controllo in basso</span><span class="sxs-lookup"><span data-stu-id="2b3f0-121">Control Key Down</span></span>                               |
| <span data-ttu-id="2b3f0-122">0x0020</span><span class="sxs-lookup"><span data-stu-id="2b3f0-122">0x0020</span></span> | <span data-ttu-id="2b3f0-123">Tasto ALT premuto</span><span class="sxs-lookup"><span data-stu-id="2b3f0-123">Alt Key Down</span></span>                                   |
| <span data-ttu-id="2b3f0-124">0x1000</span><span class="sxs-lookup"><span data-stu-id="2b3f0-124">0x1000</span></span> | <span data-ttu-id="2b3f0-125">Si è verificato l'evento sull'icona della barra delle applicazioni del carattere</span><span class="sxs-lookup"><span data-stu-id="2b3f0-125">Event occurred on the character's taskbar icon</span></span> |



 

</dd> <dt>

<span data-ttu-id="2b3f0-126"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="2b3f0-126"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="2b3f0-127">Coordinata x del puntatore del mouse, in pixel, rispetto all'origine dello schermo (in alto a sinistra).</span><span class="sxs-lookup"><span data-stu-id="2b3f0-127">The x-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="2b3f0-128"><span id="y"></span><span id="Y"></span>*y*</span><span class="sxs-lookup"><span data-stu-id="2b3f0-128"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="2b3f0-129">Coordinata y del puntatore del mouse, in pixel, rispetto all'origine dello schermo (in alto a sinistra).</span><span class="sxs-lookup"><span data-stu-id="2b3f0-129">The y-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

<span data-ttu-id="2b3f0-130">Questo evento viene inviato al client attivo di input del carattere.</span><span class="sxs-lookup"><span data-stu-id="2b3f0-130">This event is sent to the input-active client of the character.</span></span> <span data-ttu-id="2b3f0-131">Se nessuno dei client del carattere è attivo per l'input, il server invia una notifica al client attivo del carattere.</span><span class="sxs-lookup"><span data-stu-id="2b3f0-131">If none of the character's clients are input-active, the server notifies the character's active client.</span></span> <span data-ttu-id="2b3f0-132">Se il carattere è visibile, il server rende anche attivo l'input del client e invia [**IAgentNotifySink:: ActivateInputState**](iagentnotifysink--activateinputstate.md).</span><span class="sxs-lookup"><span data-stu-id="2b3f0-132">If the character is visible, the server also makes that client input-active and sends the [**IAgentNotifySink::ActivateInputState**](iagentnotifysink--activateinputstate.md).</span></span> <span data-ttu-id="2b3f0-133">Se il carattere è nascosto, viene visualizzato automaticamente anche il carattere.</span><span class="sxs-lookup"><span data-stu-id="2b3f0-133">If the character is hidden, the character is also automatically shown.</span></span>

 

 




