---
title: Attributi dell'evento di ambiente
description: Attributi dell'evento di ambiente
ms.assetid: 56cd2701-53b3-4456-8fcd-d65f8a6aefd7
keywords:
- Interfacce di Media Player di Windows, attributi di eventi di ambiente
- interfacce, attributi di eventi di ambiente
- riferimento per interfacce, attributi di eventi di ambiente
- attributi dell'evento di ambiente
- attributi, evento di ambiente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a40522a741509e56d2e4c9201c305126067a0fe3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708734"
---
# <a name="ambient-event-attributes"></a><span data-ttu-id="ee005-108">Attributi dell'evento di ambiente</span><span class="sxs-lookup"><span data-stu-id="ee005-108">Ambient Event Attributes</span></span>

<span data-ttu-id="ee005-109">Gli attributi seguenti sono comuni a tutti gli eventi di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="ee005-109">The following attributes are common to all skin events.</span></span> <span data-ttu-id="ee005-110">È possibile accedervi con la parola chiave **Event** all'interno di un gestore eventi per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="ee005-110">They are accessed with the **event** keyword within an event handler for the element.</span></span>



| <span data-ttu-id="ee005-111">Attributo</span><span class="sxs-lookup"><span data-stu-id="ee005-111">Attribute</span></span>                              | <span data-ttu-id="ee005-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee005-112">Description</span></span>                                                                                                  |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ee005-113">altKey</span><span class="sxs-lookup"><span data-stu-id="ee005-113">altKey</span></span>](event-altkey.md)             | <span data-ttu-id="ee005-114">Recupera un valore che indica se il tasto ALT è inattivo quando si è verificato l'evento.</span><span class="sxs-lookup"><span data-stu-id="ee005-114">Retrieves a value indicating whether the ALT key was down when the event occurred.</span></span>                           |
| [<span data-ttu-id="ee005-115">pulsante</span><span class="sxs-lookup"><span data-stu-id="ee005-115">button</span></span>](event-button.md)             | <span data-ttu-id="ee005-116">Recupera un valore che indica quali pulsanti del mouse sono rimasti inattivi quando si è verificato l'evento.</span><span class="sxs-lookup"><span data-stu-id="ee005-116">Retrieves a value indicating which mouse buttons were down when the event occurred.</span></span>                          |
| [<span data-ttu-id="ee005-117">clientX</span><span class="sxs-lookup"><span data-stu-id="ee005-117">clientX</span></span>](event-clientx.md)           | <span data-ttu-id="ee005-118">Recupera la coordinata x del puntatore del mouse rispetto all'area client della finestra dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ee005-118">Retrieves the x-coordinate of the mouse pointer with respect to the client region of the application window.</span></span> |
| [<span data-ttu-id="ee005-119">clientY</span><span class="sxs-lookup"><span data-stu-id="ee005-119">clientY</span></span>](event-clienty.md)           | <span data-ttu-id="ee005-120">Recupera la coordinata y del puntatore del mouse rispetto all'area client della finestra dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ee005-120">Retrieves the y-coordinate of the mouse pointer with respect to the client region of the application window.</span></span> |
| [<span data-ttu-id="ee005-121">ctrlKey</span><span class="sxs-lookup"><span data-stu-id="ee005-121">ctrlKey</span></span>](event-ctrlkey.md)           | <span data-ttu-id="ee005-122">Recupera un valore che indica se il tasto CTRL è inattivo quando si è verificato l'evento.</span><span class="sxs-lookup"><span data-stu-id="ee005-122">Retrieves a value indicating whether the CTRL key was down when the event occurred.</span></span>                          |
| [<span data-ttu-id="ee005-123">fromElement</span><span class="sxs-lookup"><span data-stu-id="ee005-123">fromElement</span></span>](event-fromelement.md)   | <span data-ttu-id="ee005-124">Recupera l'elemento da cui proviene l'evento.</span><span class="sxs-lookup"><span data-stu-id="ee005-124">Retrieves the element the event came from.</span></span>                                                                   |
| [<span data-ttu-id="ee005-125">keyCode</span><span class="sxs-lookup"><span data-stu-id="ee005-125">keyCode</span></span>](event-keycode.md)           | <span data-ttu-id="ee005-126">Recupera il codice della chiave ASCII se è stato premuto un tasto quando si è verificato l'evento.</span><span class="sxs-lookup"><span data-stu-id="ee005-126">Retrieves the ASCII key code if a key was pressed when the event occurred.</span></span>                                   |
| [<span data-ttu-id="ee005-127">offsetX</span><span class="sxs-lookup"><span data-stu-id="ee005-127">offsetX</span></span>](event-offsetx.md)           | <span data-ttu-id="ee005-128">Recupera la coordinata x del puntatore del mouse rispetto all'elemento che genera l'evento.</span><span class="sxs-lookup"><span data-stu-id="ee005-128">Retrieves the x-coordinate of the mouse pointer with respect to the element firing the event.</span></span>                |
| [<span data-ttu-id="ee005-129">offsetY</span><span class="sxs-lookup"><span data-stu-id="ee005-129">offsetY</span></span>](event-offsety.md)           | <span data-ttu-id="ee005-130">Recupera la coordinata y del puntatore del mouse rispetto all'elemento che genera l'evento.</span><span class="sxs-lookup"><span data-stu-id="ee005-130">Retrieves the y-coordinate of the mouse pointer with respect to the element firing the event.</span></span>                |
| [<span data-ttu-id="ee005-131">screenHeight</span><span class="sxs-lookup"><span data-stu-id="ee005-131">screenHeight</span></span>](event-screenheight.md) | <span data-ttu-id="ee005-132">Recupera l'altezza in pixel delle dimensioni dello schermo disponibili.</span><span class="sxs-lookup"><span data-stu-id="ee005-132">Retrieves the height of the available screen size in pixels.</span></span>                                                 |
| [<span data-ttu-id="ee005-133">screenWidth</span><span class="sxs-lookup"><span data-stu-id="ee005-133">screenWidth</span></span>](event-screenwidth.md)   | <span data-ttu-id="ee005-134">Recupera la larghezza delle dimensioni dello schermo disponibili in pixel.</span><span class="sxs-lookup"><span data-stu-id="ee005-134">Retrieves the width of the available screen size in pixels.</span></span>                                                  |
| [<span data-ttu-id="ee005-135">screenX</span><span class="sxs-lookup"><span data-stu-id="ee005-135">screenX</span></span>](event-screenx.md)           | <span data-ttu-id="ee005-136">Recupera la coordinata x assoluta del puntatore del mouse rispetto allo schermo.</span><span class="sxs-lookup"><span data-stu-id="ee005-136">Retrieves the absolute x-coordinate of the mouse pointer with respect to the screen.</span></span>                         |
| [<span data-ttu-id="ee005-137">screenY</span><span class="sxs-lookup"><span data-stu-id="ee005-137">screenY</span></span>](event-screeny.md)           | <span data-ttu-id="ee005-138">Recupera la coordinata y assoluta del puntatore del mouse rispetto allo schermo.</span><span class="sxs-lookup"><span data-stu-id="ee005-138">Retrieves the absolute y-coordinate of the mouse pointer with respect to the screen.</span></span>                         |
| [<span data-ttu-id="ee005-139">shiftKey</span><span class="sxs-lookup"><span data-stu-id="ee005-139">shiftKey</span></span>](event-shiftkey.md)         | <span data-ttu-id="ee005-140">Recupera un valore che indica se il tasto MAIUSC è inattivo quando si è verificato l'evento.</span><span class="sxs-lookup"><span data-stu-id="ee005-140">Retrieves a value indicating whether the SHIFT key was down when the event occurred.</span></span>                         |
| [<span data-ttu-id="ee005-141">srcElement</span><span class="sxs-lookup"><span data-stu-id="ee005-141">srcElement</span></span>](event-srcelement.md)     | <span data-ttu-id="ee005-142">Recupera l'elemento che ha generato l'evento.</span><span class="sxs-lookup"><span data-stu-id="ee005-142">Retrieves the element that fired the event.</span></span>                                                                  |
| [<span data-ttu-id="ee005-143">toElement</span><span class="sxs-lookup"><span data-stu-id="ee005-143">toElement</span></span>](event-toelement.md)       | <span data-ttu-id="ee005-144">Recupera l'elemento in cui è stato spostato lo stato attivo della tastiera.</span><span class="sxs-lookup"><span data-stu-id="ee005-144">Retrieves the element the keyboard focus moved to.</span></span>                                                           |
| [<span data-ttu-id="ee005-145">x</span><span class="sxs-lookup"><span data-stu-id="ee005-145">x</span></span>](event-x.md)                       | <span data-ttu-id="ee005-146">Recupera la coordinata x del puntatore del mouse rispetto alla finestra dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ee005-146">Retrieves the x-coordinate of the mouse pointer with respect to the application window.</span></span>                      |
| [<span data-ttu-id="ee005-147">y</span><span class="sxs-lookup"><span data-stu-id="ee005-147">y</span></span>](event-y.md)                       | <span data-ttu-id="ee005-148">Recupera la coordinata y del puntatore del mouse rispetto alla finestra dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ee005-148">Retrieves the y-coordinate of the mouse pointer with respect to the application window.</span></span>                      |



 

## <a name="related-topics"></a><span data-ttu-id="ee005-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ee005-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee005-150">**Informazioni di riferimento sulla programmazione dell'interfaccia**</span><span class="sxs-lookup"><span data-stu-id="ee005-150">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




