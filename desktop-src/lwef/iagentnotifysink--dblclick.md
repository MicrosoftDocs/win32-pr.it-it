---
title: IAgentNotifySink DblClick
description: IAgentNotifySink DblClick
ms.assetid: 7e86cc9b-8bc3-405e-9bbf-764cec9c3130
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88193f228f94d24384e6bf2b874e9208d67f3e9c
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120924"
---
# <a name="iagentnotifysinkdblclick"></a><span data-ttu-id="b6c02-103">IAgentNotifySink::D blClick</span><span class="sxs-lookup"><span data-stu-id="b6c02-103">IAgentNotifySink::DblClick</span></span>

<span data-ttu-id="b6c02-104">\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b6c02-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT DblClick(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x coordinate of mouse pointer
   long y          // y coordinate of mouse pointer
);                          
```

<span data-ttu-id="b6c02-105">Notifica a un'applicazione client quando l'utente fa doppio clic su un carattere.</span><span class="sxs-lookup"><span data-stu-id="b6c02-105">Notifies a client application when the user double-clicks a character.</span></span>

-   <span data-ttu-id="b6c02-106">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="b6c02-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="b6c02-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="b6c02-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="b6c02-108">Identificatore del carattere su cui si è fatto doppio clic.</span><span class="sxs-lookup"><span data-stu-id="b6c02-108">Identifier of the double-clicked character.</span></span>

</dd> <dt>

<span data-ttu-id="b6c02-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span><span class="sxs-lookup"><span data-stu-id="b6c02-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span></span>
</dt> <dd>

<span data-ttu-id="b6c02-110">Parametro che indica lo stato del pulsante del mouse e del tasto di modifica.</span><span class="sxs-lookup"><span data-stu-id="b6c02-110">A parameter that indicates the mouse button and modifier key state.</span></span> <span data-ttu-id="b6c02-111">Il parametro può restituire qualsiasi combinazione degli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="b6c02-111">The parameter can return any combination of the following:</span></span>



| <span data-ttu-id="b6c02-112">Valore</span><span class="sxs-lookup"><span data-stu-id="b6c02-112">Value</span></span>  | <span data-ttu-id="b6c02-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b6c02-113">Description</span></span>                               |
|--------|------------------------------------------------|
| <span data-ttu-id="b6c02-114">0x0001</span><span class="sxs-lookup"><span data-stu-id="b6c02-114">0x0001</span></span> | <span data-ttu-id="b6c02-115">Pulsante sinistro</span><span class="sxs-lookup"><span data-stu-id="b6c02-115">Left Button</span></span>                                    |
| <span data-ttu-id="b6c02-116">0x0010</span><span class="sxs-lookup"><span data-stu-id="b6c02-116">0x0010</span></span> | <span data-ttu-id="b6c02-117">Pulsante centrale</span><span class="sxs-lookup"><span data-stu-id="b6c02-117">Middle Button</span></span>                                  |
| <span data-ttu-id="b6c02-118">0x0002</span><span class="sxs-lookup"><span data-stu-id="b6c02-118">0x0002</span></span> | <span data-ttu-id="b6c02-119">Pulsante destro</span><span class="sxs-lookup"><span data-stu-id="b6c02-119">Right Button</span></span>                                   |
| <span data-ttu-id="b6c02-120">0x0004</span><span class="sxs-lookup"><span data-stu-id="b6c02-120">0x0004</span></span> | <span data-ttu-id="b6c02-121">MAIUSC+FRECCIA GIÙ</span><span class="sxs-lookup"><span data-stu-id="b6c02-121">Shift Key Down</span></span>                                 |
| <span data-ttu-id="b6c02-122">0x0008</span><span class="sxs-lookup"><span data-stu-id="b6c02-122">0x0008</span></span> | <span data-ttu-id="b6c02-123">CTRL+FRECCIA GIÙ</span><span class="sxs-lookup"><span data-stu-id="b6c02-123">Control Key Down</span></span>                               |
| <span data-ttu-id="b6c02-124">0x0020</span><span class="sxs-lookup"><span data-stu-id="b6c02-124">0x0020</span></span> | <span data-ttu-id="b6c02-125">ALT+FRECCIA GIÙ</span><span class="sxs-lookup"><span data-stu-id="b6c02-125">Alt Key Down</span></span>                                   |
| <span data-ttu-id="b6c02-126">0x1000</span><span class="sxs-lookup"><span data-stu-id="b6c02-126">0x1000</span></span> | <span data-ttu-id="b6c02-127">Evento che si è verificato sull'icona della barra delle applicazioni del carattere</span><span class="sxs-lookup"><span data-stu-id="b6c02-127">Event occurred on the character's taskbar icon</span></span> |



 

</dd> <dt>

<span data-ttu-id="b6c02-128"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="b6c02-128"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="b6c02-129">Coordinata x del puntatore del mouse in pixel rispetto all'origine dello schermo (in alto a sinistra).</span><span class="sxs-lookup"><span data-stu-id="b6c02-129">The x-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="b6c02-130"><span id="y"></span><span id="Y"></span>*Y*</span><span class="sxs-lookup"><span data-stu-id="b6c02-130"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="b6c02-131">Coordinata y del puntatore del mouse in pixel rispetto all'origine dello schermo (in alto a sinistra).</span><span class="sxs-lookup"><span data-stu-id="b6c02-131">The y-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

<span data-ttu-id="b6c02-132">Questo evento viene inviato al client attivo di input del carattere.</span><span class="sxs-lookup"><span data-stu-id="b6c02-132">This event is sent to the input-active client of the character.</span></span> <span data-ttu-id="b6c02-133">Se nessuno dei client del carattere è attivo per l'input, il server invia una notifica al client attivo del carattere.</span><span class="sxs-lookup"><span data-stu-id="b6c02-133">If none of the character's clients are input-active, the server notifies the character's active client.</span></span> <span data-ttu-id="b6c02-134">Se il carattere è visibile, il server rende attivo anche l'input del client e invia [**IAgentNotifySink::ActivateInputState**](iagentnotifysink--activateinputstate.md).</span><span class="sxs-lookup"><span data-stu-id="b6c02-134">If the character is visible, the server also makes that client input-active and sends the [**IAgentNotifySink::ActivateInputState**](iagentnotifysink--activateinputstate.md).</span></span> <span data-ttu-id="b6c02-135">Se il carattere è nascosto, viene visualizzato automaticamente anche il carattere.</span><span class="sxs-lookup"><span data-stu-id="b6c02-135">If the character is hidden, the character is also automatically shown.</span></span>

 

 




