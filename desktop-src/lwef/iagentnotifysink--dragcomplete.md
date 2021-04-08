---
title: IAgentNotifySink DragComplete
description: IAgentNotifySink DragComplete
ms.assetid: b2d9b9c2-709e-4988-aa92-f129e3836fc7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f53215591e3d2797c5b57e5586ccb13fc91f5902
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045232"
---
# <a name="iagentnotifysinkdragcomplete"></a><span data-ttu-id="a110f-103">IAgentNotifySink::D ragComplete</span><span class="sxs-lookup"><span data-stu-id="a110f-103">IAgentNotifySink::DragComplete</span></span>

<span data-ttu-id="a110f-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a110f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT DragComplete(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x-coordinate of mouse pointer
   long y          // y-coordinate of mouse pointer
);                          
```

<span data-ttu-id="a110f-105">Notifica a un'applicazione client quando l'utente smette di trascinare un carattere.</span><span class="sxs-lookup"><span data-stu-id="a110f-105">Notifies a client application when the user stops dragging a character.</span></span>

-   <span data-ttu-id="a110f-106">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="a110f-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="a110f-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="a110f-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="a110f-108">Identificatore del carattere trascinato.</span><span class="sxs-lookup"><span data-stu-id="a110f-108">Identifier of the dragged character.</span></span>

</dd> <dt>

<span data-ttu-id="a110f-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span><span class="sxs-lookup"><span data-stu-id="a110f-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span></span>
</dt> <dd>

<span data-ttu-id="a110f-110">Parametro che indica il pulsante del mouse e lo stato del tasto di modifica.</span><span class="sxs-lookup"><span data-stu-id="a110f-110">A parameter that indicates the mouse button and modifier key state.</span></span> <span data-ttu-id="a110f-111">Il parametro può restituire qualsiasi combinazione dei seguenti elementi:</span><span class="sxs-lookup"><span data-stu-id="a110f-111">The parameter can return any combination of the following:</span></span>



|        |                  |
|--------|------------------|
| <span data-ttu-id="a110f-112">0x0001</span><span class="sxs-lookup"><span data-stu-id="a110f-112">0x0001</span></span> | <span data-ttu-id="a110f-113">Pulsante sinistro</span><span class="sxs-lookup"><span data-stu-id="a110f-113">Left Button</span></span>      |
| <span data-ttu-id="a110f-114">0x0010</span><span class="sxs-lookup"><span data-stu-id="a110f-114">0x0010</span></span> | <span data-ttu-id="a110f-115">Pulsante centrale</span><span class="sxs-lookup"><span data-stu-id="a110f-115">Middle Button</span></span>    |
| <span data-ttu-id="a110f-116">0x0002</span><span class="sxs-lookup"><span data-stu-id="a110f-116">0x0002</span></span> | <span data-ttu-id="a110f-117">Pulsante destro</span><span class="sxs-lookup"><span data-stu-id="a110f-117">Right Button</span></span>     |
| <span data-ttu-id="a110f-118">0x0004</span><span class="sxs-lookup"><span data-stu-id="a110f-118">0x0004</span></span> | <span data-ttu-id="a110f-119">Tasto MAIUSC giù</span><span class="sxs-lookup"><span data-stu-id="a110f-119">Shift Key Down</span></span>   |
| <span data-ttu-id="a110f-120">0x0008</span><span class="sxs-lookup"><span data-stu-id="a110f-120">0x0008</span></span> | <span data-ttu-id="a110f-121">Chiave di controllo in basso</span><span class="sxs-lookup"><span data-stu-id="a110f-121">Control Key Down</span></span> |
| <span data-ttu-id="a110f-122">0x0020</span><span class="sxs-lookup"><span data-stu-id="a110f-122">0x0020</span></span> | <span data-ttu-id="a110f-123">Tasto ALT premuto</span><span class="sxs-lookup"><span data-stu-id="a110f-123">Alt Key Down</span></span>     |



 

</dd> <dt>

<span data-ttu-id="a110f-124"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="a110f-124"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="a110f-125">Coordinata x del puntatore del mouse, in pixel, rispetto all'origine dello schermo (in alto a sinistra).</span><span class="sxs-lookup"><span data-stu-id="a110f-125">The x-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="a110f-126"><span id="y"></span><span id="Y"></span>*y*</span><span class="sxs-lookup"><span data-stu-id="a110f-126"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="a110f-127">Coordinata y del puntatore del mouse, in pixel, rispetto all'origine dello schermo (in alto a sinistra).</span><span class="sxs-lookup"><span data-stu-id="a110f-127">The y-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

 

 




