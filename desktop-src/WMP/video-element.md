---
title: Elemento VIDEO
description: Elemento VIDEO
ms.assetid: 817e0d2e-cbc3-4b61-81c0-876104125f39
keywords:
- Windows Media Player Skin, elemento VIDEO
- Skin, elemento VIDEO
- Elemento VIDEO
- riferimento per Skin, elemento VIDEO
- elementi, VIDEO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbd8ab6bd014d2968483120fd1dd98804905faa4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711104"
---
# <a name="video-element"></a><span data-ttu-id="b18bf-108">Elemento VIDEO</span><span class="sxs-lookup"><span data-stu-id="b18bf-108">VIDEO Element</span></span>

<span data-ttu-id="b18bf-109">L'elemento **video** fornisce un modo per modificare una finestra video in un'interfaccia, usando gli attributi e gli eventi seguenti.</span><span class="sxs-lookup"><span data-stu-id="b18bf-109">The **VIDEO** element provides a way to manipulate a video window in a skin, using the following attributes and events.</span></span> <span data-ttu-id="b18bf-110">Viene inoltre fornito un elemento **video** predefinito per praticità.</span><span class="sxs-lookup"><span data-stu-id="b18bf-110">A predefined **VIDEO** element is also provided for convenience.</span></span>

<span data-ttu-id="b18bf-111">L'elemento **video** supporta gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="b18bf-111">The **VIDEO** element supports the following attributes.</span></span>



| <span data-ttu-id="b18bf-112">Attributo</span><span class="sxs-lookup"><span data-stu-id="b18bf-112">Attribute</span></span>                                            | <span data-ttu-id="b18bf-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b18bf-113">Description</span></span>                                                                                                                                                                                                                              |
|------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b18bf-114">backgroundColor</span><span class="sxs-lookup"><span data-stu-id="b18bf-114">backgroundColor</span></span>](video-backgroundcolor.md)         | <span data-ttu-id="b18bf-115">Specifica o Recupera il colore di sfondo del controllo video.</span><span class="sxs-lookup"><span data-stu-id="b18bf-115">Specifies or retrieves the background color of the Video control.</span></span>                                                                                                                                                                        |
| [<span data-ttu-id="b18bf-116">cursor</span><span class="sxs-lookup"><span data-stu-id="b18bf-116">cursor</span></span>](video-cursor.md)                           | <span data-ttu-id="b18bf-117">Specifica o Recupera il valore del cursore utilizzato quando il mouse si trova su un'area selezionabile del video.</span><span class="sxs-lookup"><span data-stu-id="b18bf-117">Specifies or retrieves the cursor value that is used when the mouse is over a clickable area of the video.</span></span>                                                                                                                               |
| [<span data-ttu-id="b18bf-118">Schermo intero</span><span class="sxs-lookup"><span data-stu-id="b18bf-118">fullScreen</span></span>](video-fullscreen.md)                   | <span data-ttu-id="b18bf-119">Specifica o recupera un valore che indica se il video viene visualizzato in modalità schermo intero.</span><span class="sxs-lookup"><span data-stu-id="b18bf-119">Specifies or retrieves a value indicating whether the video is displayed in full-screen mode.</span></span> <span data-ttu-id="b18bf-120">Può essere impostato solo in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="b18bf-120">Can only be set at run time.</span></span>                                                                                                               |
| [<span data-ttu-id="b18bf-121">maintainAspectRatio</span><span class="sxs-lookup"><span data-stu-id="b18bf-121">maintainAspectRatio</span></span>](video-maintainaspectratio.md) | <span data-ttu-id="b18bf-122">Specifica o recupera un valore che indica se il video manterrà le proporzioni durante il tentativo di adattarsi alla larghezza e all'altezza definite per il controllo.</span><span class="sxs-lookup"><span data-stu-id="b18bf-122">Specifies or retrieves a value indicating whether the video will maintain the aspect ratio when trying to fit within the width and height defined for the control.</span></span>                                                                       |
| [<span data-ttu-id="b18bf-123">shrinkToFit</span><span class="sxs-lookup"><span data-stu-id="b18bf-123">shrinkToFit</span></span>](video-shrinktofit.md)                 | <span data-ttu-id="b18bf-124">Specifica o recupera un valore che indica se il video ridurrà la larghezza e l'altezza definite per il controllo video.</span><span class="sxs-lookup"><span data-stu-id="b18bf-124">Specifies or retrieves a value indicating whether the video will shrink to the width and height defined for the Video control.</span></span>                                                                                                           |
| [<span data-ttu-id="b18bf-125">stretchToFit</span><span class="sxs-lookup"><span data-stu-id="b18bf-125">stretchToFit</span></span>](video-stretchtofit.md)               | <span data-ttu-id="b18bf-126">Specifica o recupera un valore che indica se il video si estenderà per la larghezza e l'altezza definite per il controllo video.</span><span class="sxs-lookup"><span data-stu-id="b18bf-126">Specifies or retrieves a value indicating whether the video will stretch itself to the width and height defined for the Video control.</span></span>                                                                                                   |
| [<span data-ttu-id="b18bf-127">Descrizione comando</span><span class="sxs-lookup"><span data-stu-id="b18bf-127">toolTip</span></span>](video-tooltip.md)                         | <span data-ttu-id="b18bf-128">Specifica o Recupera il testo della descrizione comando per la finestra del video.</span><span class="sxs-lookup"><span data-stu-id="b18bf-128">Specifies or retrieves the ToolTip text for the video window.</span></span>                                                                                                                                                                            |
| [<span data-ttu-id="b18bf-129">senza finestra</span><span class="sxs-lookup"><span data-stu-id="b18bf-129">windowless</span></span>](video-windowless.md)                   | <span data-ttu-id="b18bf-130">Specifica o recupera un valore che indica se il controllo video sarà finestra o senza finestra; ovvero se l'intero rettangolo del controllo sarà sempre visibile o possa essere ritagliato.</span><span class="sxs-lookup"><span data-stu-id="b18bf-130">Specifies or retrieves a value indicating whether the Video control will be windowed or windowless; that is, whether the entire rectangle of the control will be visible at all times or can be clipped.</span></span> <span data-ttu-id="b18bf-131">Può essere impostato solo in fase di progettazione.</span><span class="sxs-lookup"><span data-stu-id="b18bf-131">Can only be set at design time.</span></span> |
| [<span data-ttu-id="b18bf-132">zoom</span><span class="sxs-lookup"><span data-stu-id="b18bf-132">zoom</span></span>](video-zoom.md)                               | <span data-ttu-id="b18bf-133">Specifica la percentuale in base alla quale ridimensionare il video.</span><span class="sxs-lookup"><span data-stu-id="b18bf-133">Specifies the percentage by which to scale the video.</span></span>                                                                                                                                                                                    |



 

<span data-ttu-id="b18bf-134">L'elemento **video** può implementare i gestori eventi seguenti.</span><span class="sxs-lookup"><span data-stu-id="b18bf-134">The **VIDEO** element can implement the following event handlers.</span></span>



| <span data-ttu-id="b18bf-135">Gestore di evento</span><span class="sxs-lookup"><span data-stu-id="b18bf-135">Event handler</span></span>                          | <span data-ttu-id="b18bf-136">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b18bf-136">Description</span></span>                                                                  |
|----------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="b18bf-137">onvideoend</span><span class="sxs-lookup"><span data-stu-id="b18bf-137">onvideoend</span></span>](video-onvideoend.md)     | <span data-ttu-id="b18bf-138">Gestisce un evento che si verifica quando il video interrompe il rendering e viene scaricato.</span><span class="sxs-lookup"><span data-stu-id="b18bf-138">Handles an event that occurs when the video stops rendering and is unloaded.</span></span> |
| [<span data-ttu-id="b18bf-139">onvideostart</span><span class="sxs-lookup"><span data-stu-id="b18bf-139">onvideostart</span></span>](video-onvideostart.md) | <span data-ttu-id="b18bf-140">Gestisce un evento che si verifica quando il video viene caricato e inizia a eseguire il rendering.</span><span class="sxs-lookup"><span data-stu-id="b18bf-140">Handles an event that occurs when the video is loaded and begins to render.</span></span>  |



 

<span data-ttu-id="b18bf-141">L'elemento **video** supporta gli attributi di ambiente ed è in grado di implementare i gestori eventi di ambiente, tranne nei casi indicati.</span><span class="sxs-lookup"><span data-stu-id="b18bf-141">The **VIDEO** element supports the ambient attributes and can implement the ambient event handlers, except where noted.</span></span> <span data-ttu-id="b18bf-142">Per altre informazioni, vedere [attributi di ambiente](ambient-attributes.md) e [gestori di eventi di ambiente](ambient-event-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="b18bf-142">For more information, see [Ambient Attributes](ambient-attributes.md) and [Ambient Event Handlers](ambient-event-handlers.md).</span></span>

<span data-ttu-id="b18bf-143">Gli elementi video predefiniti sono elementi **video** normali con diverse impostazioni degli attributi comuni specificati per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="b18bf-143">Predefined video elements are normal **VIDEO** elements with various common attribute settings specified by default.</span></span> <span data-ttu-id="b18bf-144">Sono disponibili gli elementi video predefiniti seguenti.</span><span class="sxs-lookup"><span data-stu-id="b18bf-144">The following predefined video elements are available.</span></span>



| <span data-ttu-id="b18bf-145">VIDEO predefinito</span><span class="sxs-lookup"><span data-stu-id="b18bf-145">Predefined VIDEO</span></span>         | <span data-ttu-id="b18bf-146">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b18bf-146">Description</span></span>                                                |
|--------------------------|------------------------------------------------------------|
| [<span data-ttu-id="b18bf-147">WMPVIDEO</span><span class="sxs-lookup"><span data-stu-id="b18bf-147">WMPVIDEO</span></span>](wmpvideo.md) | <span data-ttu-id="b18bf-148">Elemento **video** che estende il video quando viene ridimensionato.</span><span class="sxs-lookup"><span data-stu-id="b18bf-148">A **VIDEO** element that stretches the video when resized.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b18bf-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b18bf-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b18bf-150">**Informazioni di riferimento sulla programmazione dell'interfaccia**</span><span class="sxs-lookup"><span data-stu-id="b18bf-150">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




