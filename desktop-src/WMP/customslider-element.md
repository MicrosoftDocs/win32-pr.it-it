---
title: Elemento CUSTOMSLIDER
description: Elemento CUSTOMSLIDER
ms.assetid: 9cba9bdd-ea5b-4a4a-a61e-e6aff29fc3e0
keywords:
- Windows Media Player Skin, elemento CUSTOMSLIDER
- interfacce, elemento CUSTOMSLIDER
- Elemento CUSTOMSLIDER
- riferimento per le interfacce, elemento CUSTOMSLIDER
- elementi, CUSTOMSLIDER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8f49fc6260df295e3266ae9ddf7b5b3eceee43d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330876"
---
# <a name="customslider-element"></a><span data-ttu-id="a019d-108">Elemento CUSTOMSLIDER</span><span class="sxs-lookup"><span data-stu-id="a019d-108">CUSTOMSLIDER Element</span></span>

<span data-ttu-id="a019d-109">L'elemento **CUSTOMSLIDER** fornisce un modo per creare e modificare un controllo dispositivo di scorrimento di qualsiasi forma, ad esempio una manopola circolare.</span><span class="sxs-lookup"><span data-stu-id="a019d-109">The **CUSTOMSLIDER** element provides a way to create and manipulate a slider control of any shape, such as a circular knob.</span></span> <span data-ttu-id="a019d-110">Nelle tabelle seguenti sono elencati gli attributi e i gestori eventi supportati da questo elemento.</span><span class="sxs-lookup"><span data-stu-id="a019d-110">The following tables list the attributes and event handlers supported by this element.</span></span>

<span data-ttu-id="a019d-111">L'elemento **CUSTOMSLIDER** supporta i seguenti attributi.</span><span class="sxs-lookup"><span data-stu-id="a019d-111">The **CUSTOMSLIDER** element supports the following attributes.</span></span>



| <span data-ttu-id="a019d-112">Attributo</span><span class="sxs-lookup"><span data-stu-id="a019d-112">Attribute</span></span>                                               | <span data-ttu-id="a019d-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a019d-113">Description</span></span>                                                                                                                 |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a019d-114">cursor</span><span class="sxs-lookup"><span data-stu-id="a019d-114">cursor</span></span>](customslider-cursor.md)                       | <span data-ttu-id="a019d-115">Specifica o Recupera il valore del cursore del controllo dispositivo di scorrimento visualizzato quando il mouse è posizionato sul dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="a019d-115">Specifies or retrieves the value of the slider control cursor that appears when the mouse is over the slider.</span></span>               |
| [<span data-ttu-id="a019d-116">disabledImage</span><span class="sxs-lookup"><span data-stu-id="a019d-116">disabledImage</span></span>](customslider-disabledimage.md)         | <span data-ttu-id="a019d-117">Specifica o recupera l'immagine del dispositivo di scorrimento usato quando il dispositivo di scorrimento è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="a019d-117">Specifies or retrieves the image of the slider used when the slider is disabled.</span></span>                                            |
| [<span data-ttu-id="a019d-118">downImage</span><span class="sxs-lookup"><span data-stu-id="a019d-118">downImage</span></span>](customslider-downimage.md)                 | <span data-ttu-id="a019d-119">Specifica o recupera l'immagine di stato inattivo del dispositivo di scorrimento personalizzato.</span><span class="sxs-lookup"><span data-stu-id="a019d-119">Specifies or retrieves the down state image of the custom slider.</span></span>                                                           |
| [<span data-ttu-id="a019d-120">hoverImage</span><span class="sxs-lookup"><span data-stu-id="a019d-120">hoverImage</span></span>](customslider-hoverimage.md)               | <span data-ttu-id="a019d-121">Specifica o recupera l'immagine visualizzata quando il mouse è posizionato sul dispositivo di scorrimento personalizzato.</span><span class="sxs-lookup"><span data-stu-id="a019d-121">Specifies or retrieves the image that displays when the mouse is over the custom slider.</span></span>                                    |
| [<span data-ttu-id="a019d-122">image</span><span class="sxs-lookup"><span data-stu-id="a019d-122">image</span></span>](customslider-image.md)                         | <span data-ttu-id="a019d-123">Specifica o Recupera il nome del file contenente le immagini corrispondenti ai vari Stati del dispositivo di scorrimento personalizzato.</span><span class="sxs-lookup"><span data-stu-id="a019d-123">Specifies or retrieves the name of the file containing the images corresponding to the various states of the custom slider.</span></span> |
| [<span data-ttu-id="a019d-124">max</span><span class="sxs-lookup"><span data-stu-id="a019d-124">max</span></span>](customslider-max.md)                             | <span data-ttu-id="a019d-125">Specifica o Recupera il valore massimo dell'intervallo definito dal dispositivo di scorrimento personalizzato.</span><span class="sxs-lookup"><span data-stu-id="a019d-125">Specifies or retrieves the maximum value of the range defined by the custom slider.</span></span>                                         |
| [<span data-ttu-id="a019d-126">min</span><span class="sxs-lookup"><span data-stu-id="a019d-126">min</span></span>](customslider-min.md)                             | <span data-ttu-id="a019d-127">Specifica o Recupera il valore minimo dell'intervallo definito dal dispositivo di scorrimento personalizzato.</span><span class="sxs-lookup"><span data-stu-id="a019d-127">Specifies or retrieves the minimum value of the range defined by the custom slider.</span></span>                                         |
| [<span data-ttu-id="a019d-128">Dimensione positionImage</span><span class="sxs-lookup"><span data-stu-id="a019d-128">positionImage</span></span>](customslider-positionimage.md)         | <span data-ttu-id="a019d-129">Specifica o recupera la mappa immagine utilizzata per determinare l'immagine di posizione del file di **immagine** da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="a019d-129">Specifies or retrieves the image map used to determine which position image from the **image** file to display.</span></span>             |
| [<span data-ttu-id="a019d-130">Descrizione comando</span><span class="sxs-lookup"><span data-stu-id="a019d-130">toolTip</span></span>](customslider-tooltip.md)                     | <span data-ttu-id="a019d-131">Specifica o Recupera il testo della descrizione comando per il dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="a019d-131">Specifies or retrieves the ToolTip text for the slider.</span></span>                                                                     |
| [<span data-ttu-id="a019d-132">transparencyColor</span><span class="sxs-lookup"><span data-stu-id="a019d-132">transparencyColor</span></span>](customslider-transparencycolor.md) | <span data-ttu-id="a019d-133">Specifica o Recupera il colore di trasparenza delle immagini del dispositivo di scorrimento personalizzato.</span><span class="sxs-lookup"><span data-stu-id="a019d-133">Specifies or retrieves the transparency color of the custom slider images.</span></span>                                                  |
| [<span data-ttu-id="a019d-134">value</span><span class="sxs-lookup"><span data-stu-id="a019d-134">value</span></span>](customslider-value.md)                         | <span data-ttu-id="a019d-135">Specifica o recupera la posizione corrente del dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="a019d-135">Specifies or retrieves the current position of the slider.</span></span>                                                                  |



 

<span data-ttu-id="a019d-136">L'elemento **CUSTOMSLIDER** può implementare i gestori eventi seguenti.</span><span class="sxs-lookup"><span data-stu-id="a019d-136">The **CUSTOMSLIDER** element can implement the following event handlers.</span></span>



| <span data-ttu-id="a019d-137">Gestore di evento</span><span class="sxs-lookup"><span data-stu-id="a019d-137">Event handler</span></span>                                         | <span data-ttu-id="a019d-138">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a019d-138">Description</span></span>                                                                                                          |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a019d-139">onDragBegin</span><span class="sxs-lookup"><span data-stu-id="a019d-139">onDragBegin</span></span>](customslider-ondragbegin.md)           | <span data-ttu-id="a019d-140">Gestisce un evento che si verifica quando l'utente fa clic e mantiene premuto il pulsante sinistro del mouse e inizia a trascinare il mouse.</span><span class="sxs-lookup"><span data-stu-id="a019d-140">Handles an event that occurs when the user clicks and holds the left mouse button down and begins to drag the mouse.</span></span> |
| [<span data-ttu-id="a019d-141">onDragEnd</span><span class="sxs-lookup"><span data-stu-id="a019d-141">onDragEnd</span></span>](customslider-ondragend.md)               | <span data-ttu-id="a019d-142">Gestisce un evento che si verifica quando viene rilasciato il pulsante sinistro del mouse dopo un'operazione di trascinamento.</span><span class="sxs-lookup"><span data-stu-id="a019d-142">Handles an event that occurs when the left mouse button is released after a dragging operation.</span></span>                      |
| [<span data-ttu-id="a019d-143">onPositionChange</span><span class="sxs-lookup"><span data-stu-id="a019d-143">onPositionChange</span></span>](customslider-onpositionchange.md) | <span data-ttu-id="a019d-144">Gestisce un evento che si verifica quando la posizione del dispositivo di scorrimento viene modificata in seguito alla selezione o al trascinamento dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a019d-144">Handles an event that occurs when the position of the slider changes as a result of the user clicking or dragging.</span></span>   |



 

<span data-ttu-id="a019d-145">L'elemento **CUSTOMSLIDER** supporta gli attributi di ambiente e può implementare i gestori eventi di ambiente.</span><span class="sxs-lookup"><span data-stu-id="a019d-145">The **CUSTOMSLIDER** element supports the ambient attributes and can implement the ambient event handlers.</span></span> <span data-ttu-id="a019d-146">Per altre informazioni, vedere [attributi di ambiente](ambient-attributes.md) e [gestori di eventi di ambiente](ambient-event-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="a019d-146">For more information, see [Ambient Attributes](ambient-attributes.md) and [Ambient Event Handlers](ambient-event-handlers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a019d-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a019d-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a019d-148">**Informazioni di riferimento sulla programmazione dell'interfaccia**</span><span class="sxs-lookup"><span data-stu-id="a019d-148">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




