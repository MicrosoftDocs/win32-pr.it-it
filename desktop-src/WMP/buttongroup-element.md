---
title: Elemento BUTTONGROUP
description: Elemento BUTTONGROUP
ms.assetid: 4756c016-3347-4129-be5e-e822270a24de
keywords:
- Windows Media Player Skin, elemento BUTTONGROUP
- interfacce, elemento BUTTONGROUP
- Elemento BUTTONGROUP
- riferimento per le interfacce, elemento BUTTONGROUP
- elementi, BUTTONGROUP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4de489e779b5e20214778b56fd8d19c7627e444
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116905"
---
# <a name="buttongroup-element"></a><span data-ttu-id="0eb58-108">Elemento BUTTONGROUP</span><span class="sxs-lookup"><span data-stu-id="0eb58-108">BUTTONGROUP Element</span></span>

<span data-ttu-id="0eb58-109">L'elemento **ButtonGroup** fornisce un modo per raggruppare diversi pulsanti all'interno di un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="0eb58-109">The **BUTTONGROUP** element provides a way to group several buttons within a skin.</span></span> <span data-ttu-id="0eb58-110">È possibile specificare questi pulsanti usando gli elementi **ButtonElement** come elementi figlio dell'elemento **ButtonGroup** .</span><span class="sxs-lookup"><span data-stu-id="0eb58-110">These buttons can be specified by using **BUTTONELEMENT** elements as children of the **BUTTONGROUP** element.</span></span>

<span data-ttu-id="0eb58-111">L'elemento **ButtonGroup** supporta i seguenti attributi.</span><span class="sxs-lookup"><span data-stu-id="0eb58-111">The **BUTTONGROUP** element supports the following attributes.</span></span>



| <span data-ttu-id="0eb58-112">Attributo</span><span class="sxs-lookup"><span data-stu-id="0eb58-112">Attribute</span></span>                                              | <span data-ttu-id="0eb58-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0eb58-113">Description</span></span>                                                                                                                                                                                                                     |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0eb58-114">buttonCount</span><span class="sxs-lookup"><span data-stu-id="0eb58-114">buttonCount</span></span>](buttongroup-buttoncount.md)             | <span data-ttu-id="0eb58-115">Recupera il numero di pulsanti presenti in **ButtonGroup**.</span><span class="sxs-lookup"><span data-stu-id="0eb58-115">Retrieves the number of buttons in the **BUTTONGROUP**.</span></span>                                                                                                                                                                         |
| [<span data-ttu-id="0eb58-116">cursor</span><span class="sxs-lookup"><span data-stu-id="0eb58-116">cursor</span></span>](buttongroup-cursor.md)                       | <span data-ttu-id="0eb58-117">Specifica o Recupera il tipo di cursore visualizzato quando il mouse è posizionato su un pulsante in **ButtonGroup**.</span><span class="sxs-lookup"><span data-stu-id="0eb58-117">Specifies or retrieves the type of cursor that appears when the mouse is over a button in the **BUTTONGROUP**.</span></span>                                                                                                                  |
| [<span data-ttu-id="0eb58-118">disabledImage</span><span class="sxs-lookup"><span data-stu-id="0eb58-118">disabledImage</span></span>](buttongroup-disabledimage.md)         | <span data-ttu-id="0eb58-119">Specifica o Recupera il nome dell'immagine che rappresenta lo stato disabilitato dei pulsanti in **ButtonGroup**.</span><span class="sxs-lookup"><span data-stu-id="0eb58-119">Specifies or retrieves the name of the image representing the disabled state of the buttons in the **BUTTONGROUP**.</span></span>                                                                                                             |
| [<span data-ttu-id="0eb58-120">downImage</span><span class="sxs-lookup"><span data-stu-id="0eb58-120">downImage</span></span>](buttongroup-downimage.md)                 | <span data-ttu-id="0eb58-121">Specifica o Recupera il nome dell'immagine che rappresenta lo stato di inattività di **ButtonGroup**.</span><span class="sxs-lookup"><span data-stu-id="0eb58-121">Specifies or retrieves the name of the image representing the down state of the **BUTTONGROUP**.</span></span>                                                                                                                                |
| [<span data-ttu-id="0eb58-122">hoverDownImage</span><span class="sxs-lookup"><span data-stu-id="0eb58-122">hoverDownImage</span></span>](buttongroup-hoverdownimage.md)       | <span data-ttu-id="0eb58-123">Specifica o Recupera il nome dell'immagine che rappresenta lo stato di spostamento verso il basso di un pulsante in **ButtonGroup**.</span><span class="sxs-lookup"><span data-stu-id="0eb58-123">Specifies or retrieves the name of the image representing the hover-down state of a button in the **BUTTONGROUP**.</span></span> <span data-ttu-id="0eb58-124">Lo stato di spostamento verso il basso si verifica quando il pulsante è nello stato di inattività e l'utente passa il mouse su di esso con il mouse.</span><span class="sxs-lookup"><span data-stu-id="0eb58-124">The hover-down state occurs when the button is in the down state and the user hovers over it with the mouse.</span></span> |
| [<span data-ttu-id="0eb58-125">hoverImage</span><span class="sxs-lookup"><span data-stu-id="0eb58-125">hoverImage</span></span>](buttongroup-hoverimage.md)               | <span data-ttu-id="0eb58-126">Specifica o Recupera il nome dell'immagine che rappresenta lo stato del passaggio del mouse su un pulsante in **ButtonGroup**.</span><span class="sxs-lookup"><span data-stu-id="0eb58-126">Specifies or retrieves the name of the image representing the hover state of a button in the **BUTTONGROUP**.</span></span> <span data-ttu-id="0eb58-127">Lo stato del passaggio del mouse si verifica quando il pulsante si trova nello stato attivo e l'utente passa su di esso con il mouse.</span><span class="sxs-lookup"><span data-stu-id="0eb58-127">The hover state occurs when the button is in the up state and the user hovers over it with the mouse.</span></span>             |
| [<span data-ttu-id="0eb58-128">hueShift</span><span class="sxs-lookup"><span data-stu-id="0eb58-128">hueShift</span></span>](buttongroup-hueshift.md)                   | <span data-ttu-id="0eb58-129">Specifica o recupera la quantità in base alla quale viene spostata la tonalità delle immagini **ButtonGroup** .</span><span class="sxs-lookup"><span data-stu-id="0eb58-129">Specifies or retrieves the amount by which the hue of the **BUTTONGROUP** images is shifted.</span></span>                                                                                                                                    |
| [<span data-ttu-id="0eb58-130">image</span><span class="sxs-lookup"><span data-stu-id="0eb58-130">image</span></span>](buttongroup-image.md)                         | <span data-ttu-id="0eb58-131">Specifica o Recupera il nome dell'immagine che rappresenta i pulsanti di un **ButtonGroup**.</span><span class="sxs-lookup"><span data-stu-id="0eb58-131">Specifies or retrieves the name of the image representing the buttons of a **BUTTONGROUP**.</span></span>                                                                                                                                     |
| [<span data-ttu-id="0eb58-132">mappingImage</span><span class="sxs-lookup"><span data-stu-id="0eb58-132">mappingImage</span></span>](buttongroup-mappingimage.md)           | <span data-ttu-id="0eb58-133">Specifica o Recupera il nome dell'immagine che rappresenta la mappa dei pulsanti di **ButtonGroup**.</span><span class="sxs-lookup"><span data-stu-id="0eb58-133">Specifies or retrieves the name of the image representing the button map of the **BUTTONGROUP**.</span></span>                                                                                                                                |
| [<span data-ttu-id="0eb58-134">radio</span><span class="sxs-lookup"><span data-stu-id="0eb58-134">radio</span></span>](buttongroup-radio.md)                         | <span data-ttu-id="0eb58-135">Specifica o recupera un valore che indica se **ButtonGroup** è costituito da pulsanti di opzione.</span><span class="sxs-lookup"><span data-stu-id="0eb58-135">Specifies or retrieves a value indicating whether the **BUTTONGROUP** is composed of radio buttons.</span></span>                                                                                                                             |
| [<span data-ttu-id="0eb58-136">saturazione</span><span class="sxs-lookup"><span data-stu-id="0eb58-136">saturation</span></span>](buttongroup-saturation.md)               | <span data-ttu-id="0eb58-137">Specifica o Recupera il valore di saturazione delle immagini **ButtonGroup** .</span><span class="sxs-lookup"><span data-stu-id="0eb58-137">Specifies or retrieves the saturation value of the **BUTTONGROUP** images.</span></span>                                                                                                                                                      |
| [<span data-ttu-id="0eb58-138">showBackground</span><span class="sxs-lookup"><span data-stu-id="0eb58-138">showBackground</span></span>](buttongroup-showbackground.md)       | <span data-ttu-id="0eb58-139">Specifica o recupera un valore che indica se **ButtonGroup** Visualizza solo i pulsanti oppure Visualizza la bitmap completa specificata nell'attributo **Image** .</span><span class="sxs-lookup"><span data-stu-id="0eb58-139">Specifies or retrieves a value indicating whether the **BUTTONGROUP** displays only the buttons, or displays the full bitmap specified in the **image** attribute.</span></span>                                                              |
| [<span data-ttu-id="0eb58-140">transparencyColor</span><span class="sxs-lookup"><span data-stu-id="0eb58-140">transparencyColor</span></span>](buttongroup-transparencycolor.md) | <span data-ttu-id="0eb58-141">Specifica o Recupera il colore trasparente delle immagini **ButtonGroup** .</span><span class="sxs-lookup"><span data-stu-id="0eb58-141">Specifies or retrieves the transparent color of the **BUTTONGROUP** images.</span></span>                                                                                                                                                     |



 

<span data-ttu-id="0eb58-142">L'elemento **ButtonGroup** supporta i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="0eb58-142">The **BUTTONGROUP** element supports the following methods.</span></span>



| <span data-ttu-id="0eb58-143">Metodo</span><span class="sxs-lookup"><span data-stu-id="0eb58-143">Method</span></span>                                 | <span data-ttu-id="0eb58-144">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0eb58-144">Description</span></span>                                                                                     |
|----------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0eb58-145">Clicca</span><span class="sxs-lookup"><span data-stu-id="0eb58-145">click</span></span>](buttongroup-click.md)         | <span data-ttu-id="0eb58-146">Chiama il gestore dell'evento **OnClick** definito per l'oggetto **ButtonElement** con l'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="0eb58-146">Calls the **onclick** event handler defined for the **BUTTONELEMENT** with the specified index.</span></span> |
| [<span data-ttu-id="0eb58-147">GetButton</span><span class="sxs-lookup"><span data-stu-id="0eb58-147">getButton</span></span>](buttongroup-getbutton.md) | <span data-ttu-id="0eb58-148">Recupera l'oggetto **ButtonElement** con l'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="0eb58-148">Retrieves the **BUTTONELEMENT** with the specified index.</span></span>                                       |



 

<span data-ttu-id="0eb58-149">L'elemento **ButtonGroup** supporta gli attributi di ambiente e può implementare i gestori eventi di ambiente.</span><span class="sxs-lookup"><span data-stu-id="0eb58-149">The **BUTTONGROUP** element supports the ambient attributes and can implement the ambient event handlers.</span></span> <span data-ttu-id="0eb58-150">Per altre informazioni, vedere [attributi di ambiente](ambient-attributes.md) e [gestori di eventi di ambiente](ambient-event-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="0eb58-150">For more information, see [Ambient Attributes](ambient-attributes.md) and [Ambient Event Handlers](ambient-event-handlers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0eb58-151">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0eb58-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0eb58-152">**Informazioni di riferimento sulla programmazione dell'interfaccia**</span><span class="sxs-lookup"><span data-stu-id="0eb58-152">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




