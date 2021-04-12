---
title: Gestori eventi di ambiente
description: Gestori eventi di ambiente
ms.assetid: ec806b92-a66d-499d-9bb3-cea7e82676bb
keywords:
- Interfacce di Media Player Windows, gestori eventi di ambiente
- interfacce, gestori eventi di ambiente
- riferimento per le interfacce, i gestori eventi di ambiente
- gestori eventi di ambiente
- eventi, ambiente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dc05cf90956464afbb030f3cd5dc4af194b0da2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395538"
---
# <a name="ambient-event-handlers"></a><span data-ttu-id="6b39f-108">Gestori eventi di ambiente</span><span class="sxs-lookup"><span data-stu-id="6b39f-108">Ambient Event Handlers</span></span>

<span data-ttu-id="6b39f-109">I gestori eventi seguenti possono essere implementati per la maggior parte degli elementi di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="6b39f-109">The following event handlers can be implemented for most skin elements.</span></span> <span data-ttu-id="6b39f-110">Gli attributi dell'evento di ambiente a cui si accede con la parola chiave **Event** possono essere utilizzati all'interno di un gestore eventi per determinare lo stato della tastiera e del mouse al momento dell'evento.</span><span class="sxs-lookup"><span data-stu-id="6b39f-110">The ambient event attributes accessed with the **event** keyword can be used within an event handler to determine the state of the keyboard and mouse at the time of the event.</span></span>



| <span data-ttu-id="6b39f-111">Gestore di evento</span><span class="sxs-lookup"><span data-stu-id="6b39f-111">Event handler</span></span>                                   | <span data-ttu-id="6b39f-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6b39f-112">Description</span></span>                                                                                                                                                                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6b39f-113">*attributo* \_ OnChange</span><span class="sxs-lookup"><span data-stu-id="6b39f-113">*attribute*\_onchange</span></span>](attribute-onchange.md) | <span data-ttu-id="6b39f-114">Quando un attributo Skin cambia valore, si verifica un evento che può essere gestito da un gestore eventi.</span><span class="sxs-lookup"><span data-stu-id="6b39f-114">When a skin attribute changes value, an event occurs that can be handled by an event handler.</span></span> <span data-ttu-id="6b39f-115">Il nome del gestore eventi è il nome dell'attributo seguito da un carattere di sottolineatura e da "onChange", ad esempio "valore \_ OnChange".</span><span class="sxs-lookup"><span data-stu-id="6b39f-115">The name of the event handler is the name of the attribute followed by an underscore and "onchange", such as "value\_onchange".</span></span> |
| [<span data-ttu-id="6b39f-116">onblur</span><span class="sxs-lookup"><span data-stu-id="6b39f-116">onblur</span></span>](onblur.md)                            | <span data-ttu-id="6b39f-117">Gestisce un evento che si verifica quando l'elemento perde lo stato attivo della tastiera.</span><span class="sxs-lookup"><span data-stu-id="6b39f-117">Handles an event that occurs when the element loses the keyboard focus.</span></span>                                                                                                                                                       |
| [<span data-ttu-id="6b39f-118">OnClick</span><span class="sxs-lookup"><span data-stu-id="6b39f-118">onclick</span></span>](onclick.md)                          | <span data-ttu-id="6b39f-119">Gestisce un evento che si verifica quando l'utente fa clic sull'elemento.</span><span class="sxs-lookup"><span data-stu-id="6b39f-119">Handles an event that occurs when the user clicks the element.</span></span>                                                                                                                                                                |
| [<span data-ttu-id="6b39f-120">ondblclick</span><span class="sxs-lookup"><span data-stu-id="6b39f-120">ondblclick</span></span>](ondblclick.md)                    | <span data-ttu-id="6b39f-121">Gestisce un evento che si verifica quando l'utente fa doppio clic sull'elemento.</span><span class="sxs-lookup"><span data-stu-id="6b39f-121">Handles an event that occurs when the user double-clicks the element.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="6b39f-122">onendalphablend</span><span class="sxs-lookup"><span data-stu-id="6b39f-122">onendalphablend</span></span>](onendalphablend.md)          | <span data-ttu-id="6b39f-123">Gestisce un evento che si verifica quando un elemento completa un'operazione **alphaBlendTo** .</span><span class="sxs-lookup"><span data-stu-id="6b39f-123">Handles an event that occurs when an element completes an **alphaBlendTo** operation.</span></span>                                                                                                                                         |
| [<span data-ttu-id="6b39f-124">onendmove</span><span class="sxs-lookup"><span data-stu-id="6b39f-124">onendmove</span></span>](onendmove.md)                      | <span data-ttu-id="6b39f-125">Gestisce un evento che si verifica quando un elemento completa un'operazione **MoveTo** .</span><span class="sxs-lookup"><span data-stu-id="6b39f-125">Handles an event that occurs when an element completes a **moveTo** operation.</span></span>                                                                                                                                                |
| [<span data-ttu-id="6b39f-126">onfocus</span><span class="sxs-lookup"><span data-stu-id="6b39f-126">onfocus</span></span>](onfocus.md)                          | <span data-ttu-id="6b39f-127">Gestisce un evento che si verifica quando l'elemento riceve lo stato attivo della tastiera.</span><span class="sxs-lookup"><span data-stu-id="6b39f-127">Handles an event that occurs when the element receives the keyboard focus.</span></span>                                                                                                                                                    |
| [<span data-ttu-id="6b39f-128">OnKeyDown</span><span class="sxs-lookup"><span data-stu-id="6b39f-128">onkeydown</span></span>](onkeydown.md)                      | <span data-ttu-id="6b39f-129">Gestisce un evento che si verifica quando viene premuto un tasto.</span><span class="sxs-lookup"><span data-stu-id="6b39f-129">Handles an event that occurs when a key is pressed.</span></span>                                                                                                                                                                           |
| [<span data-ttu-id="6b39f-130">OnKeyPress</span><span class="sxs-lookup"><span data-stu-id="6b39f-130">onkeypress</span></span>](onkeypress.md)                    | <span data-ttu-id="6b39f-131">Gestisce un evento che si verifica quando l'utente preme un tasto alfanumerico.</span><span class="sxs-lookup"><span data-stu-id="6b39f-131">Handles an event that occurs when the user presses an alphanumeric key.</span></span>                                                                                                                                                       |
| [<span data-ttu-id="6b39f-132">OnKeyUp</span><span class="sxs-lookup"><span data-stu-id="6b39f-132">onkeyup</span></span>](onkeyup.md)                          | <span data-ttu-id="6b39f-133">Gestisce un evento che si verifica quando viene rilasciato un tasto.</span><span class="sxs-lookup"><span data-stu-id="6b39f-133">Handles an event that occurs when a key is released.</span></span>                                                                                                                                                                          |
| [<span data-ttu-id="6b39f-134">OnMouseDown</span><span class="sxs-lookup"><span data-stu-id="6b39f-134">onmousedown</span></span>](onmousedown.md)                  | <span data-ttu-id="6b39f-135">Gestisce un evento che si verifica quando l'utente fa clic su un pulsante del mouse.</span><span class="sxs-lookup"><span data-stu-id="6b39f-135">Handles an event that occurs when the user clicks a mouse button.</span></span>                                                                                                                                                             |
| [<span data-ttu-id="6b39f-136">OnMouseMove</span><span class="sxs-lookup"><span data-stu-id="6b39f-136">onmousemove</span></span>](onmousemove.md)                  | <span data-ttu-id="6b39f-137">Gestisce un evento che si verifica quando l'utente sposta il puntatore del mouse mentre è posizionato su un elemento.</span><span class="sxs-lookup"><span data-stu-id="6b39f-137">Handles an event that occurs when the user moves the mouse pointer while it is over an element.</span></span>                                                                                                                               |
| [<span data-ttu-id="6b39f-138">onmouseout</span><span class="sxs-lookup"><span data-stu-id="6b39f-138">onmouseout</span></span>](onmouseout.md)                    | <span data-ttu-id="6b39f-139">Gestisce un evento che si verifica quando l'utente sposta il puntatore del mouse sull'elemento.</span><span class="sxs-lookup"><span data-stu-id="6b39f-139">Handles an event that occurs when the user moves the pointer off the element.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="6b39f-140">onmouseover</span><span class="sxs-lookup"><span data-stu-id="6b39f-140">onmouseover</span></span>](onmouseover.md)                  | <span data-ttu-id="6b39f-141">Gestisce un evento che si verifica quando l'utente posiziona il puntatore del mouse sull'elemento.</span><span class="sxs-lookup"><span data-stu-id="6b39f-141">Handles an event that occurs when the user first places the pointer over the element.</span></span>                                                                                                                                         |
| [<span data-ttu-id="6b39f-142">OnMouseUp</span><span class="sxs-lookup"><span data-stu-id="6b39f-142">onmouseup</span></span>](onmouseup.md)                      | <span data-ttu-id="6b39f-143">Gestisce un evento che si verifica quando l'utente rilascia un pulsante del mouse mentre il puntatore è posizionato sull'elemento.</span><span class="sxs-lookup"><span data-stu-id="6b39f-143">Handles an event that occurs when the user releases a mouse button while the pointer is over the element.</span></span>                                                                                                                     |
| [<span data-ttu-id="6b39f-144">OnResize</span><span class="sxs-lookup"><span data-stu-id="6b39f-144">onresize</span></span>](onresize.md)                        | <span data-ttu-id="6b39f-145">Gestisce un evento che si verifica quando un controllo viene ridimensionato.</span><span class="sxs-lookup"><span data-stu-id="6b39f-145">Handles an event that occurs when a control resizes.</span></span>                                                                                                                                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="6b39f-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6b39f-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b39f-147">**Attributi dell'evento di ambiente**</span><span class="sxs-lookup"><span data-stu-id="6b39f-147">**Ambient Event Attributes**</span></span>](ambient-event-attributes.md)
</dt> <dt>

[<span data-ttu-id="6b39f-148">**Informazioni di riferimento sulla programmazione dell'interfaccia**</span><span class="sxs-lookup"><span data-stu-id="6b39f-148">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




