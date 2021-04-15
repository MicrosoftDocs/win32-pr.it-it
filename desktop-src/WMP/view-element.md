---
title: Elemento VIEW
description: Elemento VIEW
ms.assetid: e1dfde08-33a0-4f12-8db0-ad62e4a1d467
keywords:
- Interfacce Media Player di Windows, elemento di visualizzazione
- Skin, elemento VIEW
- Elemento VIEW
- riferimento per le interfacce, elemento di visualizzazione
- elementi, visualizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07e907cced22b4d1cd498054df06ac8677a7488b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396235"
---
# <a name="view-element"></a><span data-ttu-id="96547-108">Elemento VIEW</span><span class="sxs-lookup"><span data-stu-id="96547-108">VIEW Element</span></span>

<span data-ttu-id="96547-109">L'elemento **View** contiene i dettagli dell'interfaccia utente di un oggetto Skin e usa gli attributi, i metodi e i gestori eventi illustrati nelle tabelle seguenti.</span><span class="sxs-lookup"><span data-stu-id="96547-109">The **VIEW** element contains the user interface details of a skin, and uses the attributes, methods, and event handlers shown in the following tables.</span></span>

<span data-ttu-id="96547-110">È possibile definire più elementi di **visualizzazione** come elementi figlio dell'elemento **Theme** di un'interfaccia per fornire interfacce diverse per situazioni diverse.</span><span class="sxs-lookup"><span data-stu-id="96547-110">Multiple **VIEW** elements can be defined as children of the **THEME** element of a skin to provide different interfaces for different situations.</span></span> <span data-ttu-id="96547-111">Gli elementi della **vista** non possono essere specificati come elementi figlio di un altro elemento e contengono tutti gli altri elementi dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="96547-111">**VIEW** elements cannot be specified as children of any other element, and they contain all other skin elements.</span></span> <span data-ttu-id="96547-112">Si noti che ogni vista ha un proprio ambito di variabili, ovvero non può condividere i valori di attributo con altre visualizzazioni.</span><span class="sxs-lookup"><span data-stu-id="96547-112">Note that each view has its own variable scope, which means it cannot share attribute values with other views.</span></span>

<span data-ttu-id="96547-113">L'attributo **View** Global può essere usato per fare riferimento a un elemento di **visualizzazione** specifico da qualsiasi punto al suo interno.</span><span class="sxs-lookup"><span data-stu-id="96547-113">The **view** global attribute can be used to reference a specific **VIEW** element from anywhere within it.</span></span> <span data-ttu-id="96547-114">Si tratta di un'alternativa all'utilizzo del relativo attributo **ID** , che deve essere utilizzato dall'interno di altri elementi di **visualizzazione** o dall'interno dell'elemento del **tema** .</span><span class="sxs-lookup"><span data-stu-id="96547-114">This is an alternative to using its **id** attribute, which must be used from within other **VIEW** elements or from within the **THEME** element.</span></span>

<span data-ttu-id="96547-115">L'elemento **View** supporta gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="96547-115">The **VIEW** element supports the following attributes.</span></span> <span data-ttu-id="96547-116">Gli attributi contrassegnati con un asterisco ( \* ) sono supportati anche dall'elemento **subview** .</span><span class="sxs-lookup"><span data-stu-id="96547-116">Attributes marked with an asterisk (\*) are also supported by the **SUBVIEW** element.</span></span>



| <span data-ttu-id="96547-117">Attributo</span><span class="sxs-lookup"><span data-stu-id="96547-117">Attribute</span></span>                                                       | <span data-ttu-id="96547-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="96547-118">Description</span></span>                                                                                                             |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96547-119">[BackgroundColor](view-backgroundcolor.md)\*</span><span class="sxs-lookup"><span data-stu-id="96547-119">[backgroundColor](view-backgroundcolor.md) \*</span></span>                  | <span data-ttu-id="96547-120">Specifica o Recupera il colore di sfondo della **vista** o della **vista**.</span><span class="sxs-lookup"><span data-stu-id="96547-120">Specifies or retrieves the background color of the **VIEW** or **SUBVIEW**.</span></span>                                             |
| <span data-ttu-id="96547-121">[backgroundImage](view-backgroundimage.md) \*</span><span class="sxs-lookup"><span data-stu-id="96547-121">[backgroundImage](view-backgroundimage.md) \*</span></span>                  | <span data-ttu-id="96547-122">Consente di specificare o recuperare l'immagine di sfondo della **vista** o della **vista**.</span><span class="sxs-lookup"><span data-stu-id="96547-122">Specifies or retrieves the background image of the **VIEW** or **SUBVIEW**.</span></span>                                             |
| [<span data-ttu-id="96547-123">backgroundImageHueShift</span><span class="sxs-lookup"><span data-stu-id="96547-123">backgroundImageHueShift</span></span>](view-backgroundimagehueshift.md)     | <span data-ttu-id="96547-124">Specifica o recupera la quantità in base alla quale viene spostata la tonalità dell'immagine di sfondo.</span><span class="sxs-lookup"><span data-stu-id="96547-124">Specifies or retrieves the amount by which the hue of the background image is shifted.</span></span>                                  |
| [<span data-ttu-id="96547-125">backgroundImageSaturation</span><span class="sxs-lookup"><span data-stu-id="96547-125">backgroundImageSaturation</span></span>](view-backgroundimagesaturation.md) | <span data-ttu-id="96547-126">Specifica o Recupera il valore di saturazione dell'immagine di sfondo.</span><span class="sxs-lookup"><span data-stu-id="96547-126">Specifies or retrieves the saturation value of the background image.</span></span>                                                    |
| <span data-ttu-id="96547-127">[backgroundTiled](view-backgroundtiled.md)\*</span><span class="sxs-lookup"><span data-stu-id="96547-127">[backgroundTiled](view-backgroundtiled.md) \*</span></span>                  | <span data-ttu-id="96547-128">Specifica o recupera un valore che indica se l'immagine di sfondo  della vista **o della vista è** affiancata.</span><span class="sxs-lookup"><span data-stu-id="96547-128">Specifies or retrieves a value indicating whether the background image of the **VIEW** or **SUBVIEW** is tiled.</span></span>         |
| [<span data-ttu-id="96547-129">category</span><span class="sxs-lookup"><span data-stu-id="96547-129">category</span></span>](view-category.md)                                   | <span data-ttu-id="96547-130">Specifica o recupera la categoria per la quale verrà visualizzata l'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="96547-130">Specifies or retrieves the category for which the user interface will appear.</span></span>                                           |
| [<span data-ttu-id="96547-131">focusObjectID</span><span class="sxs-lookup"><span data-stu-id="96547-131">focusObjectID</span></span>](view-focusobjectid.md)                         | <span data-ttu-id="96547-132">Specifica o recupera un valore che indica quale elemento dispone dello stato attivo della tastiera.</span><span class="sxs-lookup"><span data-stu-id="96547-132">Specifies or retrieves a value indicating which element has keyboard focus.</span></span>                                             |
| [<span data-ttu-id="96547-133">maxHeight</span><span class="sxs-lookup"><span data-stu-id="96547-133">maxHeight</span></span>](view-maxheight.md)                                 | <span data-ttu-id="96547-134">Specifica o recupera l'altezza massima della **visualizzazione** durante il ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="96547-134">Specifies or retrieves the maximum height of the **VIEW** when resizing.</span></span>                                                |
| [<span data-ttu-id="96547-135">maxWidth</span><span class="sxs-lookup"><span data-stu-id="96547-135">maxWidth</span></span>](view-maxwidth.md)                                   | <span data-ttu-id="96547-136">Specifica o recupera la larghezza massima della **visualizzazione** durante il ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="96547-136">Specifies or retrieves the maximum width of the **VIEW** when resizing.</span></span>                                                 |
| [<span data-ttu-id="96547-137">minHeight</span><span class="sxs-lookup"><span data-stu-id="96547-137">minHeight</span></span>](view-minheight.md)                                 | <span data-ttu-id="96547-138">Specifica o recupera l'altezza minima della **visualizzazione** durante il ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="96547-138">Specifies or retrieves the minimum height of the **VIEW** when resizing.</span></span>                                                |
| [<span data-ttu-id="96547-139">minWidth</span><span class="sxs-lookup"><span data-stu-id="96547-139">minWidth</span></span>](view-minwidth.md)                                   | <span data-ttu-id="96547-140">Specifica o recupera la larghezza minima della **visualizzazione** durante il ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="96547-140">Specifies or retrieves the minimum width of the **VIEW** when resizing.</span></span>                                                 |
| [<span data-ttu-id="96547-141">ridimensionabile</span><span class="sxs-lookup"><span data-stu-id="96547-141">resizable</span></span>](view-resizable.md)                                 | <span data-ttu-id="96547-142">Specifica o recupera un valore che indica se la **vista** può essere ridimensionata.</span><span class="sxs-lookup"><span data-stu-id="96547-142">Specifies or retrieves a value indicating whether the **VIEW** can be resized.</span></span>                                          |
| [<span data-ttu-id="96547-143">resizeBackgroundImage</span><span class="sxs-lookup"><span data-stu-id="96547-143">resizeBackgroundImage</span></span>](view-resizebackgroundimage.md)         | <span data-ttu-id="96547-144">Specifica o recupera un valore che indica se è possibile ridimensionare l'immagine di sfondo.</span><span class="sxs-lookup"><span data-stu-id="96547-144">Specifies or retrieves a value indicating whether the background image can be resized.</span></span>                                  |
| [<span data-ttu-id="96547-145">scriptFile</span><span class="sxs-lookup"><span data-stu-id="96547-145">scriptFile</span></span>](view-scriptfile.md)                               | <span data-ttu-id="96547-146">Specifica i nomi file dei file JScript associati.</span><span class="sxs-lookup"><span data-stu-id="96547-146">Specifies the file names of accompanying JScript files.</span></span>                                                                 |
| [<span data-ttu-id="96547-147">timerInterval</span><span class="sxs-lookup"><span data-stu-id="96547-147">timerInterval</span></span>](view-timerinterval.md)                         | <span data-ttu-id="96547-148">Specifica o recupera l'intervallo, in millisecondi, in cui il timer genera eventi nel gestore eventi **OnTimer** .</span><span class="sxs-lookup"><span data-stu-id="96547-148">Specifies or retrieves the interval, in milliseconds, at which the timer fires events to the **ontimer** event handler.</span></span> |
| [<span data-ttu-id="96547-149">title</span><span class="sxs-lookup"><span data-stu-id="96547-149">title</span></span>](view-title.md)                                         | <span data-ttu-id="96547-150">Specifica o Recupera il titolo della **visualizzazione**.</span><span class="sxs-lookup"><span data-stu-id="96547-150">Specifies or retrieves the title of the **VIEW**.</span></span> <span data-ttu-id="96547-151">Può essere impostato solo in fase di progettazione.</span><span class="sxs-lookup"><span data-stu-id="96547-151">Can only be set at design time.</span></span>                                       |
| [<span data-ttu-id="96547-152">titleBar</span><span class="sxs-lookup"><span data-stu-id="96547-152">titleBar</span></span>](view-titlebar.md)                                   | <span data-ttu-id="96547-153">Specifica o recupera un valore che indica se la barra del titolo della finestra è visualizzata.</span><span class="sxs-lookup"><span data-stu-id="96547-153">Specifies or retrieves a value indicating whether the window title bar is shown.</span></span>                                        |
| <span data-ttu-id="96547-154">[transparencyColor](view-transparencycolor.md)\*</span><span class="sxs-lookup"><span data-stu-id="96547-154">[transparencyColor](view-transparencycolor.md) \*</span></span>              | <span data-ttu-id="96547-155">Specifica o Recupera il colore di trasparenza dell'immagine di sfondo.</span><span class="sxs-lookup"><span data-stu-id="96547-155">Specifies or retrieves the transparency color of the background image.</span></span>                                                  |



 

<span data-ttu-id="96547-156">L'elemento **View** supporta i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="96547-156">The **VIEW** element supports the following methods.</span></span>



| <span data-ttu-id="96547-157">Metodo</span><span class="sxs-lookup"><span data-stu-id="96547-157">Method</span></span>                                              | <span data-ttu-id="96547-158">Descrizione</span><span class="sxs-lookup"><span data-stu-id="96547-158">Description</span></span>                                                |
|-----------------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="96547-159">close</span><span class="sxs-lookup"><span data-stu-id="96547-159">close</span></span>](view-close.md)                             | <span data-ttu-id="96547-160">Chiude la **visualizzazione**.</span><span class="sxs-lookup"><span data-stu-id="96547-160">Closes the **VIEW**.</span></span>                                       |
| [<span data-ttu-id="96547-161">massimizzare</span><span class="sxs-lookup"><span data-stu-id="96547-161">maximize</span></span>](view-maximize.md)                       | <span data-ttu-id="96547-162">Ingrandisce la **visualizzazione**.</span><span class="sxs-lookup"><span data-stu-id="96547-162">Maximizes the **VIEW**.</span></span>                                    |
| [<span data-ttu-id="96547-163">minimizzare</span><span class="sxs-lookup"><span data-stu-id="96547-163">minimize</span></span>](view-minimize.md)                       | <span data-ttu-id="96547-164">Riduce al minimo la **visualizzazione**.</span><span class="sxs-lookup"><span data-stu-id="96547-164">Minimizes the **VIEW**.</span></span>                                    |
| [<span data-ttu-id="96547-165">restore</span><span class="sxs-lookup"><span data-stu-id="96547-165">restore</span></span>](view-restore.md)                         | <span data-ttu-id="96547-166">Ripristina la **visualizzazione**.</span><span class="sxs-lookup"><span data-stu-id="96547-166">Restores the **VIEW**.</span></span>                                     |
| [<span data-ttu-id="96547-167">returnToMediaCenter</span><span class="sxs-lookup"><span data-stu-id="96547-167">returnToMediaCenter</span></span>](view-returntomediacenter.md) | <span data-ttu-id="96547-168">Restituisce l'utente alla modalità completa di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="96547-168">Returns the user to the full mode of Windows Media Player.</span></span> |
| [<span data-ttu-id="96547-169">size</span><span class="sxs-lookup"><span data-stu-id="96547-169">size</span></span>](view-size.md)                               | <span data-ttu-id="96547-170">Ridimensiona la **visualizzazione** in un bordo specificato.</span><span class="sxs-lookup"><span data-stu-id="96547-170">Resizes the **VIEW** on a specified edge.</span></span>                  |



 

<span data-ttu-id="96547-171">L'elemento **View** può implementare i gestori eventi seguenti.</span><span class="sxs-lookup"><span data-stu-id="96547-171">The **VIEW** element can implement the following event handlers.</span></span>



| <span data-ttu-id="96547-172">Gestore di evento</span><span class="sxs-lookup"><span data-stu-id="96547-172">Event handler</span></span>               | <span data-ttu-id="96547-173">Descrizione</span><span class="sxs-lookup"><span data-stu-id="96547-173">Description</span></span>                                                                |
|-----------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="96547-174">OnClose</span><span class="sxs-lookup"><span data-stu-id="96547-174">onclose</span></span>](view-onclose.md) | <span data-ttu-id="96547-175">Gestisce un evento che si verifica quando la **visualizzazione** sta per essere chiusa.</span><span class="sxs-lookup"><span data-stu-id="96547-175">Handles an event that occurs when the **VIEW** is about to be closed.</span></span>      |
| [<span data-ttu-id="96547-176">OnError</span><span class="sxs-lookup"><span data-stu-id="96547-176">onerror</span></span>](view-onerror.md) | <span data-ttu-id="96547-177">Gestisce un evento di errore se **Settings. enableErrorDialogs** è impostato su false.</span><span class="sxs-lookup"><span data-stu-id="96547-177">Handles an error event if **Settings.enableErrorDialogs** is set to false.</span></span> |
| [<span data-ttu-id="96547-178">OnLoad</span><span class="sxs-lookup"><span data-stu-id="96547-178">onload</span></span>](view-onload.md)   | <span data-ttu-id="96547-179">Gestisce un evento che si verifica quando la **visualizzazione** viene visualizzata per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="96547-179">Handles an event that occurs when the **VIEW** is first displayed.</span></span>         |
| [<span data-ttu-id="96547-180">OnTimer</span><span class="sxs-lookup"><span data-stu-id="96547-180">ontimer</span></span>](view-ontimer.md) | <span data-ttu-id="96547-181">Gestisce gli eventi del timer.</span><span class="sxs-lookup"><span data-stu-id="96547-181">Handles timer events.</span></span>                                                      |



 

<span data-ttu-id="96547-182">L'elemento **View** supporta gli attributi di ambiente ed è in grado di implementare i gestori eventi di ambiente, tranne nei casi indicati.</span><span class="sxs-lookup"><span data-stu-id="96547-182">The **VIEW** element supports the ambient attributes and can implement the ambient event handlers, except where noted.</span></span> <span data-ttu-id="96547-183">Per ulteriori informazioni, vedere [attributi di ambiente](ambient-attributes.md) e [gestori eventi di ambiente](ambient-event-handlers.md),</span><span class="sxs-lookup"><span data-stu-id="96547-183">For more information, see [Ambient Attributes](ambient-attributes.md) and [Ambient Event Handlers](ambient-event-handlers.md),</span></span>

## <a name="related-topics"></a><span data-ttu-id="96547-184">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="96547-184">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96547-185">**Informazioni di riferimento sulla programmazione dell'interfaccia**</span><span class="sxs-lookup"><span data-stu-id="96547-185">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




