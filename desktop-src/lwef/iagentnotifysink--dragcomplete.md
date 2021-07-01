---
title: IAgentNotifySink DragComplete
description: IAgentNotifySink DragComplete
ms.assetid: b2d9b9c2-709e-4988-aa92-f129e3836fc7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb93fbc7bae1ac43d534962659b850561bd50a6d
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120806"
---
# <a name="iagentnotifysinkdragcomplete"></a><span data-ttu-id="09fed-103">IAgentNotifySink::D ragComplete</span><span class="sxs-lookup"><span data-stu-id="09fed-103">IAgentNotifySink::DragComplete</span></span>

<span data-ttu-id="09fed-104">\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="09fed-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT DragComplete(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x-coordinate of mouse pointer
   long y          // y-coordinate of mouse pointer
);                          
```

<span data-ttu-id="09fed-105">Notifica a un'applicazione client quando l'utente smette di trascinare un carattere.</span><span class="sxs-lookup"><span data-stu-id="09fed-105">Notifies a client application when the user stops dragging a character.</span></span>

-   <span data-ttu-id="09fed-106">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="09fed-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="09fed-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="09fed-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="09fed-108">Identificatore del carattere trascinato.</span><span class="sxs-lookup"><span data-stu-id="09fed-108">Identifier of the dragged character.</span></span>

</dd> <dt>

<span data-ttu-id="09fed-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span><span class="sxs-lookup"><span data-stu-id="09fed-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span></span>
</dt> <dd>

<span data-ttu-id="09fed-110">Parametro che indica lo stato del pulsante del mouse e del tasto di modifica.</span><span class="sxs-lookup"><span data-stu-id="09fed-110">A parameter that indicates the mouse button and modifier key state.</span></span> <span data-ttu-id="09fed-111">Il parametro può restituire qualsiasi combinazione degli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="09fed-111">The parameter can return any combination of the following:</span></span>



| <span data-ttu-id="09fed-112">Valore</span><span class="sxs-lookup"><span data-stu-id="09fed-112">Value</span></span>  | <span data-ttu-id="09fed-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="09fed-113">Description</span></span>      |
|--------|------------------|
| <span data-ttu-id="09fed-114">0x0001</span><span class="sxs-lookup"><span data-stu-id="09fed-114">0x0001</span></span> | <span data-ttu-id="09fed-115">Pulsante sinistro</span><span class="sxs-lookup"><span data-stu-id="09fed-115">Left Button</span></span>      |
| <span data-ttu-id="09fed-116">0x0010</span><span class="sxs-lookup"><span data-stu-id="09fed-116">0x0010</span></span> | <span data-ttu-id="09fed-117">Pulsante centrale</span><span class="sxs-lookup"><span data-stu-id="09fed-117">Middle Button</span></span>    |
| <span data-ttu-id="09fed-118">0x0002</span><span class="sxs-lookup"><span data-stu-id="09fed-118">0x0002</span></span> | <span data-ttu-id="09fed-119">Pulsante destro</span><span class="sxs-lookup"><span data-stu-id="09fed-119">Right Button</span></span>     |
| <span data-ttu-id="09fed-120">0x0004</span><span class="sxs-lookup"><span data-stu-id="09fed-120">0x0004</span></span> | <span data-ttu-id="09fed-121">MAIUSC+FRECCIA GIÙ</span><span class="sxs-lookup"><span data-stu-id="09fed-121">Shift Key Down</span></span>   |
| <span data-ttu-id="09fed-122">0x0008</span><span class="sxs-lookup"><span data-stu-id="09fed-122">0x0008</span></span> | <span data-ttu-id="09fed-123">CTRL+FRECCIA GIÙ</span><span class="sxs-lookup"><span data-stu-id="09fed-123">Control Key Down</span></span> |
| <span data-ttu-id="09fed-124">0x0020</span><span class="sxs-lookup"><span data-stu-id="09fed-124">0x0020</span></span> | <span data-ttu-id="09fed-125">ALT+FRECCIA GIÙ</span><span class="sxs-lookup"><span data-stu-id="09fed-125">Alt Key Down</span></span>     |



 

</dd> <dt>

<span data-ttu-id="09fed-126"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="09fed-126"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="09fed-127">Coordinata x del puntatore del mouse in pixel, rispetto all'origine dello schermo (in alto a sinistra).</span><span class="sxs-lookup"><span data-stu-id="09fed-127">The x-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="09fed-128"><span id="y"></span><span id="Y"></span>*Y*</span><span class="sxs-lookup"><span data-stu-id="09fed-128"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="09fed-129">Coordinata y del puntatore del mouse in pixel, rispetto all'origine dello schermo (in alto a sinistra).</span><span class="sxs-lookup"><span data-stu-id="09fed-129">The y-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

 

 




