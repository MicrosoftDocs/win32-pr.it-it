---
title: IAgentNotifySink
description: IAgentNotifySink
ms.assetid: vs|msagent|~\paface_2xet.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb2ccfd4acf4a64c229379aeea5847fbe044b7d5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046666"
---
# <a name="iagentnotifysink"></a><span data-ttu-id="63f0a-103">IAgentNotifySink</span><span class="sxs-lookup"><span data-stu-id="63f0a-103">IAgentNotifySink</span></span>

<span data-ttu-id="63f0a-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="63f0a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="63f0a-105">IAgentNotifySink notifica ai client quando si verificano determinate modifiche di stato.</span><span class="sxs-lookup"><span data-stu-id="63f0a-105">IAgentNotifySink notifies clients when certain state changes occur.</span></span> <span data-ttu-id="63f0a-106">Queste funzioni sono disponibili anche da [IAgentNotifySinkEx](iagentnotifysinkex.md).</span><span class="sxs-lookup"><span data-stu-id="63f0a-106">These functions are also available from [IAgentNotifySinkEx](iagentnotifysinkex.md).</span></span>

<span data-ttu-id="63f0a-107">**Metodi nell'ordine Vtable**</span><span class="sxs-lookup"><span data-stu-id="63f0a-107">**Methods in Vtable Order**</span></span>



| <span data-ttu-id="63f0a-108">IAgentNotifySink</span><span class="sxs-lookup"><span data-stu-id="63f0a-108">IAgentNotifySink</span></span>                                                      | <span data-ttu-id="63f0a-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="63f0a-109">Description</span></span>                                                                              |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="63f0a-110">**Comando**</span><span class="sxs-lookup"><span data-stu-id="63f0a-110">**Command**</span></span>](command-method.md)                                     | <span data-ttu-id="63f0a-111">Si verifica quando il server elabora un comando definito dal client.</span><span class="sxs-lookup"><span data-stu-id="63f0a-111">Occurs when the server processes a client-defined command.</span></span>                               |
| [<span data-ttu-id="63f0a-112">**ActivateInputState**</span><span class="sxs-lookup"><span data-stu-id="63f0a-112">**ActivateInputState**</span></span>](iagentnotifysink--activateinputstate.md)    | <span data-ttu-id="63f0a-113">Si verifica quando un carattere diventa o smette di essere input-Active.</span><span class="sxs-lookup"><span data-stu-id="63f0a-113">Occurs when a character becomes or ceases to be input-active.</span></span>                            |
| [<span data-ttu-id="63f0a-114">**BalloonVisibleState**</span><span class="sxs-lookup"><span data-stu-id="63f0a-114">**BalloonVisibleState**</span></span>](iagentnotifysink---balloonvisiblestate.md) | <span data-ttu-id="63f0a-115">Si verifica quando cambia lo stato **visibile** del carattere.</span><span class="sxs-lookup"><span data-stu-id="63f0a-115">Occurs when the character's **Visible** state changes.</span></span>                                   |
| [<span data-ttu-id="63f0a-116">**Evento Click**</span><span class="sxs-lookup"><span data-stu-id="63f0a-116">**Click Event**</span></span>](click-event.md)                                    | <span data-ttu-id="63f0a-117">Si verifica quando si fa clic su un carattere.</span><span class="sxs-lookup"><span data-stu-id="63f0a-117">Occurs when a character is clicked.</span></span>                                                      |
| [<span data-ttu-id="63f0a-118">**Evento DblClick**</span><span class="sxs-lookup"><span data-stu-id="63f0a-118">**DblClick Event**</span></span>](dblclick-event.md)                              | <span data-ttu-id="63f0a-119">Si verifica quando si fa doppio clic su un carattere.</span><span class="sxs-lookup"><span data-stu-id="63f0a-119">Occurs when a character is double-clicked.</span></span>                                               |
| [<span data-ttu-id="63f0a-120">**DragStart**</span><span class="sxs-lookup"><span data-stu-id="63f0a-120">**DragStart**</span></span>](/windows/desktop/lwef/dragstart-event)                                | <span data-ttu-id="63f0a-121">Si verifica quando un utente inizia a trascinare un carattere.</span><span class="sxs-lookup"><span data-stu-id="63f0a-121">Occurs when a user starts dragging a character.</span></span>                                          |
| [<span data-ttu-id="63f0a-122">**DragComplete**</span><span class="sxs-lookup"><span data-stu-id="63f0a-122">**DragComplete**</span></span>](https://www.bing.com/search?q=**DragComplete**)                          | <span data-ttu-id="63f0a-123">Si verifica quando un utente smette di trascinare un carattere.</span><span class="sxs-lookup"><span data-stu-id="63f0a-123">Occurs when a user stops dragging a character.</span></span>                                           |
| [<span data-ttu-id="63f0a-124">**RequestStart**</span><span class="sxs-lookup"><span data-stu-id="63f0a-124">**RequestStart**</span></span>](iagentnotifysink--requeststart.md)                | <span data-ttu-id="63f0a-125">Si verifica quando il server inizia a elaborare un oggetto [**Request**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="63f0a-125">Occurs when the server begins processing a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>    |
| [<span data-ttu-id="63f0a-126">**RequestComplete**</span><span class="sxs-lookup"><span data-stu-id="63f0a-126">**RequestComplete**</span></span>](iagentnotifysink--requestcomplete.md)          | <span data-ttu-id="63f0a-127">Si verifica quando il server completa l'elaborazione di un oggetto [**Request**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="63f0a-127">Occurs when the server completes processing a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> |
| [<span data-ttu-id="63f0a-128">**Segnalibro**</span><span class="sxs-lookup"><span data-stu-id="63f0a-128">**Bookmark**</span></span>](iagentnotifysink--bookmark.md)                        | <span data-ttu-id="63f0a-129">Si verifica quando il server elabora un segnalibro.</span><span class="sxs-lookup"><span data-stu-id="63f0a-129">Occurs when the server processes a bookmark.</span></span>                                             |
| [<span data-ttu-id="63f0a-130">**Inattivo**</span><span class="sxs-lookup"><span data-stu-id="63f0a-130">**Idle**</span></span>](iagentnotifysink--idle.md)                                | <span data-ttu-id="63f0a-131">Si verifica all'avvio o alla fine dell'elaborazione inattiva del server.</span><span class="sxs-lookup"><span data-stu-id="63f0a-131">Occurs when the server starts or ends idle processing.</span></span>                                   |
| [<span data-ttu-id="63f0a-132">**Spostare**</span><span class="sxs-lookup"><span data-stu-id="63f0a-132">**Move**</span></span>](iagentnotifysink--move.md)                                | <span data-ttu-id="63f0a-133">Si verifica quando un carattere è stato spostato.</span><span class="sxs-lookup"><span data-stu-id="63f0a-133">Occurs when a character has been moved.</span></span>                                                  |
| [<span data-ttu-id="63f0a-134">**Dimensione**</span><span class="sxs-lookup"><span data-stu-id="63f0a-134">**Size**</span></span>](iagentnotifysink---size.md)                               | <span data-ttu-id="63f0a-135">Si verifica quando un carattere è stato ridimensionato.</span><span class="sxs-lookup"><span data-stu-id="63f0a-135">Occurs when a character has been resized.</span></span>                                                |
| [<span data-ttu-id="63f0a-136">**BalloonVisibleState**</span><span class="sxs-lookup"><span data-stu-id="63f0a-136">**BalloonVisibleState**</span></span>](iagentnotifysink---balloonvisiblestate.md) | <span data-ttu-id="63f0a-137">Si verifica quando cambia lo stato di visibilità del fumetto di parole di un carattere.</span><span class="sxs-lookup"><span data-stu-id="63f0a-137">Occurs when the visibility state of a character's word balloon changes.</span></span>                  |



 

<span data-ttu-id="63f0a-138">Gli eventi IAgentNotifySink:: Restart e IAgentNotifySink:: Shutdown, supportati nelle versioni precedenti di Microsoft Agent, sono ora obsoleti.</span><span class="sxs-lookup"><span data-stu-id="63f0a-138">The IAgentNotifySink::Restart and IAgentNotifySink::Shutdown events, supported in earlier versions of Microsoft Agent, are now obsolete.</span></span> <span data-ttu-id="63f0a-139">Sebbene supportato per la compatibilità con le versioni precedenti, il server non invia più questi eventi.</span><span class="sxs-lookup"><span data-stu-id="63f0a-139">While supported for backward compatibility, the server no longer sends these events.</span></span>

 

 