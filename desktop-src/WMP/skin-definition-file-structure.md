---
title: Struttura del file di definizione dell'interfaccia
description: Struttura del file di definizione dell'interfaccia
ms.assetid: 6b9ea288-ec64-473b-b796-ab637517099a
keywords:
- Interfacce di Media Player di Windows, file di definizione dell'interfaccia
- interfacce, file di definizione dell'interfaccia
- file per le interfacce, definizione dell'interfaccia
- file di definizione dell'interfaccia, struttura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a64226fb918bcbf93c95ece52075e2c8e7ed13e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044981"
---
# <a name="skin-definition-file-structure"></a><span data-ttu-id="a97ca-107">Struttura del file di definizione dell'interfaccia</span><span class="sxs-lookup"><span data-stu-id="a97ca-107">Skin Definition File Structure</span></span>

<span data-ttu-id="a97ca-108">Il file di definizione dell'interfaccia deve seguire una struttura specifica.</span><span class="sxs-lookup"><span data-stu-id="a97ca-108">The skin definition file must follow a specific structure.</span></span> <span data-ttu-id="a97ca-109">Si inizia con un elemento del **tema** , si creano uno o più elementi di **visualizzazione** e quindi si definisce ogni elemento di **visualizzazione** con gli elementi dell'interfaccia utente appropriati per il tipo di visualizzazione che si vuole usare.</span><span class="sxs-lookup"><span data-stu-id="a97ca-109">You start with a **THEME** element, create one or more **VIEW** elements, and then define each **VIEW** element with the user interface elements appropriate for the type of view you want to use.</span></span>

## <a name="theme-elements"></a><span data-ttu-id="a97ca-110">Elementi del tema</span><span class="sxs-lookup"><span data-stu-id="a97ca-110">THEME Elements</span></span>

<span data-ttu-id="a97ca-111">Al livello principale, è necessario avviare il file di definizione dell'interfaccia con l'elemento del **tema** e chiuderlo.</span><span class="sxs-lookup"><span data-stu-id="a97ca-111">At the top level, you must start the skin definition file with the **THEME** element and close with it.</span></span>


```C++
<THEME>
    ...
</THEME>

```



<span data-ttu-id="a97ca-112">L'elemento **Theme** è l'elemento radice dell'interfaccia personalizzata.</span><span class="sxs-lookup"><span data-stu-id="a97ca-112">The **THEME** element is the root element for your skin.</span></span> <span data-ttu-id="a97ca-113">In un file di definizione dell'interfaccia può essere presente un solo elemento **Theme** , che deve essere al livello principale.</span><span class="sxs-lookup"><span data-stu-id="a97ca-113">There can be only one **THEME** element in a skin definition file, and it must be at the top level.</span></span> <span data-ttu-id="a97ca-114">Gli elementi del **tema** hanno attributi specifici e di ambiente, sebbene nella maggior parte dei casi non sarà necessario usarli.</span><span class="sxs-lookup"><span data-stu-id="a97ca-114">**THEME** elements have specific and ambient attributes, though most of the time you will not need to use them.</span></span> <span data-ttu-id="a97ca-115">Per ulteriori informazioni su questi attributi, vedere la Guida di riferimento per la [programmazione dell'interfaccia](skin-programming-reference.md).</span><span class="sxs-lookup"><span data-stu-id="a97ca-115">For more information about these attributes, see the [Skin Programming Reference](skin-programming-reference.md).</span></span>

## <a name="view-elements"></a><span data-ttu-id="a97ca-116">Elementi di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="a97ca-116">VIEW Elements</span></span>

<span data-ttu-id="a97ca-117">Ogni **tema** deve avere almeno un elemento di **visualizzazione** .</span><span class="sxs-lookup"><span data-stu-id="a97ca-117">Each **THEME** must have at least one **VIEW** element.</span></span> <span data-ttu-id="a97ca-118">L'elemento **View** regola l'immagine specifica visualizzata sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="a97ca-118">The **VIEW** element governs the particular image you see on the screen.</span></span> <span data-ttu-id="a97ca-119">Potrebbe essere necessario disporre di più di una visualizzazione, in modo che sia possibile spostarsi avanti e indietro.</span><span class="sxs-lookup"><span data-stu-id="a97ca-119">You may want to have more than one view, so you can switch back and forth.</span></span> <span data-ttu-id="a97ca-120">Ad esempio, potrebbe essere necessario disporre di una visualizzazione di grandi dimensioni per l'utilizzo di playlist, una visualizzazione media per il controllo delle visualizzazioni e una piccola visualizzazione che si riferisca a un angolo dello schermo.</span><span class="sxs-lookup"><span data-stu-id="a97ca-120">For example, you might want to have a large view for working with playlists, a medium view for watching visualizations, and a tiny view that fits in a corner of the screen.</span></span>

<span data-ttu-id="a97ca-121">Se si creano più visualizzazioni, è necessario assicurarsi che ogni vista disponga di un valore di attributo **ID** univoco che verrà usato per identificare la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="a97ca-121">If you are creating multiple views, you will want to make sure that each view has a unique **ID** attribute value that will be used to identify the view.</span></span> <span data-ttu-id="a97ca-122">È necessario definire l'attributo **BackgroundImage** o la visualizzazione non avrà un'immagine iniziale.</span><span class="sxs-lookup"><span data-stu-id="a97ca-122">You must define the **backgroundImage** attribute or your view will have no starting image.</span></span> <span data-ttu-id="a97ca-123">Se non si desidera visualizzare un'immagine rettangolare, è probabile che si desideri utilizzare l'attributo **clippingColor** per definire le aree dell'interfaccia che non saranno visualizzate e sarà probabilmente necessario impostare **l'attributo del** titolo dell'elemento **View** .</span><span class="sxs-lookup"><span data-stu-id="a97ca-123">If you do not want to display a rectangular image, you will probably want to use the **clippingColor** attribute to define the areas of your skin that will not display, and you will probably want to set the **titleBar** attribute of the **VIEW** element.</span></span>

<span data-ttu-id="a97ca-124">Ogni elemento di **visualizzazione** può avere anche uno o più elementi della **visualizzazione** .</span><span class="sxs-lookup"><span data-stu-id="a97ca-124">Each **VIEW** element can also have one or more **SUBVIEW** elements.</span></span> <span data-ttu-id="a97ca-125">Un elemento di **Sottovisualizzazione** è simile a una **visualizzazione** e può essere usato per parti dell'interfaccia che si desidera spostare, nascondere o mostrare.</span><span class="sxs-lookup"><span data-stu-id="a97ca-125">A **SUBVIEW** element is similar to a **VIEW** and can be used for parts of your skin that you want to move around, hide, or show.</span></span> <span data-ttu-id="a97ca-126">Ad esempio, è possibile usare un elemento di **visualizzazione** per creare una barra di scorrimento che estrae dall'interfaccia per visualizzare un equalizzatore grafico.</span><span class="sxs-lookup"><span data-stu-id="a97ca-126">For example, a **SUBVIEW** element might be used to create a sliding tray that pops out of your skin to display a graphic equalizer.</span></span> <span data-ttu-id="a97ca-127">Gli elementi di **visualizzazione subvisione** possono essere allineati con la **visualizzazione** e avere altre relazioni speciali con la **visualizzazione**.</span><span class="sxs-lookup"><span data-stu-id="a97ca-127">**SUBVIEW** elements can be aligned with the **VIEW** and have other special relationships to the **VIEW**.</span></span>

## <a name="initializing-windows-media-player"></a><span data-ttu-id="a97ca-128">Inizializzazione di Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="a97ca-128">Initializing Windows Media Player</span></span>

<span data-ttu-id="a97ca-129">È possibile impostare determinate proprietà iniziali di Windows Media Player usando gli elementi **Player**, **Settings** e **Controls** .</span><span class="sxs-lookup"><span data-stu-id="a97ca-129">You can set certain initial properties of Windows Media Player by using the **PLAYER**, **SETTINGS**, and **CONTROLS** elements.</span></span> <span data-ttu-id="a97ca-130">Ad esempio, è possibile impostare il volume su un livello iniziale o fornire un valore predefinito per un nome file.</span><span class="sxs-lookup"><span data-stu-id="a97ca-130">For example, you could set the volume to an initial level or give a default value for a file name.</span></span>

<span data-ttu-id="a97ca-131">Il codice seguente illustra come impostare il valore dell' **URL** in un'interfaccia personalizzata:</span><span class="sxs-lookup"><span data-stu-id="a97ca-131">The following code shows how to set the **URL** value in a skin:</span></span>


```C++
<PLAYER
  URL = "https://proseware.com/mellow.wma">
</PLAYER>

```



<span data-ttu-id="a97ca-132">Se si desidera impostare l'attributo **autostart** delle **Impostazioni** su false, utilizzare il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="a97ca-132">If you wanted to set the **autoStart** attribute of **SETTINGS** to False, you would use the following code:</span></span>


```C++
<PLAYER>
  <SETTINGS
    autoStart = "False">
  </SETTINGS>
</PLAYER>

```



<span data-ttu-id="a97ca-133">Si noti che l'elemento **Settings** è annidato all'interno dell'elemento **Player** .</span><span class="sxs-lookup"><span data-stu-id="a97ca-133">Note that the **SETTINGS** element is nested inside the **PLAYER** element.</span></span>

<span data-ttu-id="a97ca-134">Utilizzando questi elementi, è possibile specificare gli attributi e gli eventi seguenti in fase di progettazione:</span><span class="sxs-lookup"><span data-stu-id="a97ca-134">Using these elements, the following attributes and events can be specified at design time:</span></span>

<span data-ttu-id="a97ca-135">**Attributi dell'elemento PLAYER**</span><span class="sxs-lookup"><span data-stu-id="a97ca-135">**PLAYER Element Attributes**</span></span>

-   <span data-ttu-id="a97ca-136">**url**</span><span class="sxs-lookup"><span data-stu-id="a97ca-136">**url**</span></span>
-   <span data-ttu-id="a97ca-137">**responseBuffering**</span><span class="sxs-lookup"><span data-stu-id="a97ca-137">**Buffering**</span></span>
-   <span data-ttu-id="a97ca-138">**Currentitemchange**</span><span class="sxs-lookup"><span data-stu-id="a97ca-138">**Currentitemchange**</span></span>
-   <span data-ttu-id="a97ca-139">**Currentplaylistchange**</span><span class="sxs-lookup"><span data-stu-id="a97ca-139">**Currentplaylistchange**</span></span>
-   <span data-ttu-id="a97ca-140">**Error (Errore) (Error (Errore)e)**</span><span class="sxs-lookup"><span data-stu-id="a97ca-140">**Error**</span></span>
-   <span data-ttu-id="a97ca-141">**Markerhit**</span><span class="sxs-lookup"><span data-stu-id="a97ca-141">**Markerhit**</span></span>
-   <span data-ttu-id="a97ca-142">**Mediachange**</span><span class="sxs-lookup"><span data-stu-id="a97ca-142">**Mediachange**</span></span>
-   <span data-ttu-id="a97ca-143">**Mediacollectionchange**</span><span class="sxs-lookup"><span data-stu-id="a97ca-143">**Mediacollectionchange**</span></span>
-   <span data-ttu-id="a97ca-144">**Modechange**</span><span class="sxs-lookup"><span data-stu-id="a97ca-144">**Modechange**</span></span>
-   <span data-ttu-id="a97ca-145">**Mpenstatechange**</span><span class="sxs-lookup"><span data-stu-id="a97ca-145">**Mpenstatechange**</span></span>
-   <span data-ttu-id="a97ca-146">**Mlaylistchange**</span><span class="sxs-lookup"><span data-stu-id="a97ca-146">**Mlaylistchange**</span></span>
-   <span data-ttu-id="a97ca-147">**Mlaystatechange**</span><span class="sxs-lookup"><span data-stu-id="a97ca-147">**Mlaystatechange**</span></span>
-   <span data-ttu-id="a97ca-148">**Mositionchange**</span><span class="sxs-lookup"><span data-stu-id="a97ca-148">**Mositionchange**</span></span>
-   <span data-ttu-id="a97ca-149">**Mcriptcommand**</span><span class="sxs-lookup"><span data-stu-id="a97ca-149">**Mcriptcommand**</span></span>
-   <span data-ttu-id="a97ca-150">**Mtatuschange**</span><span class="sxs-lookup"><span data-stu-id="a97ca-150">**Mtatuschange**</span></span>

<span data-ttu-id="a97ca-151">**Attributi dell'elemento SETTINGS**</span><span class="sxs-lookup"><span data-stu-id="a97ca-151">**SETTINGS Element Attributes**</span></span>

-   <span data-ttu-id="a97ca-152">**Avvio automatico**</span><span class="sxs-lookup"><span data-stu-id="a97ca-152">**autoStart**</span></span>
-   <span data-ttu-id="a97ca-153">**bilanciare**</span><span class="sxs-lookup"><span data-stu-id="a97ca-153">**balance**</span></span>
-   <span data-ttu-id="a97ca-154">**baseURL**</span><span class="sxs-lookup"><span data-stu-id="a97ca-154">**baseURL**</span></span>
-   <span data-ttu-id="a97ca-155">**defaultFrame**</span><span class="sxs-lookup"><span data-stu-id="a97ca-155">**defaultFrame**</span></span>
-   <span data-ttu-id="a97ca-156">**enableErrorDialogs**</span><span class="sxs-lookup"><span data-stu-id="a97ca-156">**enableErrorDialogs**</span></span>
-   <span data-ttu-id="a97ca-157">**invokeURLs**</span><span class="sxs-lookup"><span data-stu-id="a97ca-157">**invokeURLs**</span></span>
-   <span data-ttu-id="a97ca-158">**mute**</span><span class="sxs-lookup"><span data-stu-id="a97ca-158">**mute**</span></span>
-   <span data-ttu-id="a97ca-159">**playCount**</span><span class="sxs-lookup"><span data-stu-id="a97ca-159">**playCount**</span></span>
-   <span data-ttu-id="a97ca-160">**tasso**</span><span class="sxs-lookup"><span data-stu-id="a97ca-160">**rate**</span></span>
-   <span data-ttu-id="a97ca-161">**volume**</span><span class="sxs-lookup"><span data-stu-id="a97ca-161">**volume**</span></span>

## <a name="controls-element-attributes"></a><span data-ttu-id="a97ca-162">Controlla gli attributi degli elementi</span><span class="sxs-lookup"><span data-stu-id="a97ca-162">CONTROLS Element Attributes</span></span>

-   <span data-ttu-id="a97ca-163">**currentMarker**</span><span class="sxs-lookup"><span data-stu-id="a97ca-163">**currentMarker**</span></span>
-   <span data-ttu-id="a97ca-164">**currentPosition**</span><span class="sxs-lookup"><span data-stu-id="a97ca-164">**currentPosition**</span></span>

## <a name="other-user-interface-elements"></a><span data-ttu-id="a97ca-165">Altri elementi dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="a97ca-165">Other User Interface Elements</span></span>

<span data-ttu-id="a97ca-166">Dopo aver definito il **tema** e gli elementi di **visualizzazione** , è necessario popolare la **visualizzazione** con elementi dell'interfaccia utente specifici.</span><span class="sxs-lookup"><span data-stu-id="a97ca-166">Once you have defined your **THEME** and **VIEW** elements, you must populate your **VIEW** with specific user interface elements.</span></span> <span data-ttu-id="a97ca-167">Non è necessario usare tutti gli elementi disponibili in un'interfaccia, solo quelli necessari.</span><span class="sxs-lookup"><span data-stu-id="a97ca-167">You do not have to use all the available elements in a skin, just the ones you need.</span></span>

<span data-ttu-id="a97ca-168">Se un elemento può essere visualizzato dall'utente, viene chiamato controllo.</span><span class="sxs-lookup"><span data-stu-id="a97ca-168">If an element can be seen by the user, it is called a control.</span></span> <span data-ttu-id="a97ca-169">Per le interfacce sono disponibili i controlli seguenti:</span><span class="sxs-lookup"><span data-stu-id="a97ca-169">The following controls are available for skins:</span></span>

-   <span data-ttu-id="a97ca-170">Pulsanti</span><span class="sxs-lookup"><span data-stu-id="a97ca-170">Buttons</span></span>
-   <span data-ttu-id="a97ca-171">Dispositivi di scorrimento, dispositivi di scorrimento personalizzati e barre di stato</span><span class="sxs-lookup"><span data-stu-id="a97ca-171">Sliders, custom sliders, and progress bars</span></span>
-   <span data-ttu-id="a97ca-172">Caselle di testo</span><span class="sxs-lookup"><span data-stu-id="a97ca-172">Text boxes</span></span>
-   <span data-ttu-id="a97ca-173">Finestre video</span><span class="sxs-lookup"><span data-stu-id="a97ca-173">Video windows</span></span>
-   <span data-ttu-id="a97ca-174">Finestre di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="a97ca-174">Visualization windows</span></span>
-   <span data-ttu-id="a97ca-175">Finestre playlist</span><span class="sxs-lookup"><span data-stu-id="a97ca-175">Playlist windows</span></span>
-   <span data-ttu-id="a97ca-176">Finestre di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="a97ca-176">Subview windows</span></span>

<span data-ttu-id="a97ca-177">Inoltre, è possibile usare diversi elementi per definire ulteriormente le azioni Media Player di Windows, ma richiedono elementi visivi come pulsanti o dispositivi di scorrimento:</span><span class="sxs-lookup"><span data-stu-id="a97ca-177">In addition, several elements can be used to further define Windows Media Player actions, but they require visual elements such as buttons or sliders:</span></span>

-   <span data-ttu-id="a97ca-178">Impostazioni video</span><span class="sxs-lookup"><span data-stu-id="a97ca-178">Video settings</span></span>
-   <span data-ttu-id="a97ca-179">Impostazioni equalizzatore</span><span class="sxs-lookup"><span data-stu-id="a97ca-179">Equalizer Settings</span></span>
-   <span data-ttu-id="a97ca-180">Impostazioni di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="a97ca-180">Visualization settings</span></span>

## <a name="buttons"></a><span data-ttu-id="a97ca-181">Pulsanti</span><span class="sxs-lookup"><span data-stu-id="a97ca-181">Buttons</span></span>

<span data-ttu-id="a97ca-182">I pulsanti sono la parte più comune di un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="a97ca-182">Buttons are the most popular part of a skin.</span></span> <span data-ttu-id="a97ca-183">È possibile utilizzare i pulsanti per attivare azioni quali riproduzione, arresto, uscita, riduzione a icona e passaggio a una visualizzazione diversa.</span><span class="sxs-lookup"><span data-stu-id="a97ca-183">You can use buttons to trigger actions such as play, stop, quit, minimize, and switch to different view.</span></span> <span data-ttu-id="a97ca-184">Windows Media Player fornisce l'autore dell'interfaccia con due tipi di elementi Button: l'elemento **Button** e l'elemento **ButtonGroup** .</span><span class="sxs-lookup"><span data-stu-id="a97ca-184">Windows Media Player provides the skin creator with two types of button elements: the **BUTTON** element and the **BUTTONGROUP** element.</span></span> <span data-ttu-id="a97ca-185">Sono inoltre disponibili diversi tipi predefiniti di pulsanti.</span><span class="sxs-lookup"><span data-stu-id="a97ca-185">In addition, there are several predefined types of buttons.</span></span>

-   <span data-ttu-id="a97ca-186">**Elemento BUTTON.**</span><span class="sxs-lookup"><span data-stu-id="a97ca-186">**BUTTON element.**</span></span> <span data-ttu-id="a97ca-187">L'elemento **Button** viene usato per i singoli pulsanti.</span><span class="sxs-lookup"><span data-stu-id="a97ca-187">The **BUTTON** element is used for individual buttons.</span></span> <span data-ttu-id="a97ca-188">Se si usa l'elemento **Button** , è necessario fornire un'immagine per ogni pulsante e definire la posizione esatta in cui si desidera che il pulsante appaia rispetto all'immagine di sfondo.</span><span class="sxs-lookup"><span data-stu-id="a97ca-188">If you use the **BUTTON** element, you must supply an image for each button and define the exact location where you want the button to appear relative to the background image.</span></span> <span data-ttu-id="a97ca-189">Uno dei vantaggi dell'elemento **Button** è la possibilità di modificare l'immagine del pulsante dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="a97ca-189">One of the advantages of the **BUTTON** element is that you can change the button image dynamically.</span></span>
-   <span data-ttu-id="a97ca-190">**Elemento BUTTONGROUP.**</span><span class="sxs-lookup"><span data-stu-id="a97ca-190">**BUTTONGROUP element.**</span></span> <span data-ttu-id="a97ca-191">L'elemento **ButtonGroup** viene usato per i gruppi di pulsanti.</span><span class="sxs-lookup"><span data-stu-id="a97ca-191">The **BUTTONGROUP** element is used for groups of buttons.</span></span> <span data-ttu-id="a97ca-192">Infatti, è necessario racchiudere ogni elemento **ButtonGroup** con una coppia di tag **ButtonGroup** .</span><span class="sxs-lookup"><span data-stu-id="a97ca-192">In fact, you must enclose each **BUTTONGROUP** element with a pair of **BUTTONGROUP** tags.</span></span> <span data-ttu-id="a97ca-193">L'uso di gruppi di pulsanti è più semplice rispetto all'uso di singoli pulsanti, perché non è necessario specificare il percorso esatto per ciascun pulsante.</span><span class="sxs-lookup"><span data-stu-id="a97ca-193">Using button groups is easier than using individual buttons because you do not have to specify the exact location for each button.</span></span> <span data-ttu-id="a97ca-194">Viene invece fornita una mappa immagine separata che definisce le azioni che si verificano quando il mouse passa sopra o fa clic su un'area sullo sfondo.</span><span class="sxs-lookup"><span data-stu-id="a97ca-194">Instead, you supply a separate image map that defines the actions that will take place when the mouse hovers over or clicks an area on your background.</span></span> <span data-ttu-id="a97ca-195">L'uso di mappe di immagini è facile grazie al fatto che è possibile creare in background e copiarlo in un livello di mapping nel programma di modifica della grafica.</span><span class="sxs-lookup"><span data-stu-id="a97ca-195">Using image maps is easy because you can take the art you created for your background and copy it to a mapping layer in your graphics editing program.</span></span> <span data-ttu-id="a97ca-196">L'uso del programma di modifica della grafica è più veloce e preciso rispetto al tentativo di definire esattamente la posizione di un singolo pulsante sullo sfondo.</span><span class="sxs-lookup"><span data-stu-id="a97ca-196">Using your graphics editing program is faster and more precise than trying to define exactly where an individual button should be placed on your background.</span></span>
-   <span data-ttu-id="a97ca-197">**Pulsanti predefiniti.**</span><span class="sxs-lookup"><span data-stu-id="a97ca-197">**Predefined buttons.**</span></span> <span data-ttu-id="a97ca-198">Sono disponibili diversi pulsanti predefiniti.</span><span class="sxs-lookup"><span data-stu-id="a97ca-198">There are several predefined buttons.</span></span> <span data-ttu-id="a97ca-199">Ad esempio, è possibile usare un pulsante PLAYelement per riprodurre file multimediali digitali e un elemento STOPelement per arrestare la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="a97ca-199">For example, you can use a PLAYELEMENT button to play digital media files, and a STOPELEMENT to stop playback.</span></span> <span data-ttu-id="a97ca-200">Vedere elemento [ButtonGroup](buttongroup-element.md) e [Button nell'elemento](button-element.md) Reference Programming Skin.</span><span class="sxs-lookup"><span data-stu-id="a97ca-200">See [BUTTONGROUP](buttongroup-element.md) Element and [BUTTON Element](button-element.md) in the Skin Programming Reference.</span></span> <span data-ttu-id="a97ca-201">Il [IMAGEBUTTON](imagebutton.md) può essere utilizzato per visualizzare le immagini che possono essere modificate in risposta a eventi specifici.</span><span class="sxs-lookup"><span data-stu-id="a97ca-201">The [IMAGEBUTTON](imagebutton.md) can be used to display images that can change in response to specific events.</span></span>

## <a name="sliders"></a><span data-ttu-id="a97ca-202">Dispositivi di scorrimento</span><span class="sxs-lookup"><span data-stu-id="a97ca-202">Sliders</span></span>

<span data-ttu-id="a97ca-203">I dispositivi di scorrimento sono utili per lavorare con le informazioni modificate nel tempo.</span><span class="sxs-lookup"><span data-stu-id="a97ca-203">Sliders are useful for working with information that changes over time.</span></span> <span data-ttu-id="a97ca-204">Ad esempio, è possibile usare un dispositivo di scorrimento per indicare la quantità di musica già riprodotta per un determinato file multimediale.</span><span class="sxs-lookup"><span data-stu-id="a97ca-204">For example, you might use a slider to indicate the amount of music that has already played for a particular media file.</span></span> <span data-ttu-id="a97ca-205">I dispositivi di scorrimento possono essere orizzontali, verticali, lineari o circolari o qualsiasi forma che può essere considerata.</span><span class="sxs-lookup"><span data-stu-id="a97ca-205">Sliders can be horizontal or vertical, linear or circular, or any shape you can think of.</span></span> <span data-ttu-id="a97ca-206">I dispositivi di scorrimento sono disponibili in tre tipi: i dispositivi di scorrimento, le barre di avanzamento e i dispositivi di scorrimento personalizzati.</span><span class="sxs-lookup"><span data-stu-id="a97ca-206">Sliders come in three varieties: sliders, progress bars, and custom sliders.</span></span>

-   <span data-ttu-id="a97ca-207">**Scorrimento.**</span><span class="sxs-lookup"><span data-stu-id="a97ca-207">**Sliders.**</span></span> <span data-ttu-id="a97ca-208">È possibile usare l'elemento **Slider** per i controlli volume o consentire all'utente di spostarsi in una parte diversa del contenuto multimediale.</span><span class="sxs-lookup"><span data-stu-id="a97ca-208">You can use the **SLIDER** element for volume controls or to allow the user to move to a different part of the media content.</span></span>
-   <span data-ttu-id="a97ca-209">**Indicatori di stato.**</span><span class="sxs-lookup"><span data-stu-id="a97ca-209">**Progress bars.**</span></span> <span data-ttu-id="a97ca-210">Gli indicatori di stato sono simili ai dispositivi di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="a97ca-210">Progress bars are similar to sliders.</span></span> <span data-ttu-id="a97ca-211">Gli indicatori di stato sono progettati per visualizzare graficamente la percentuale di un determinato processo completato, ma non per un processo con cui l'utente dovrà interagire.</span><span class="sxs-lookup"><span data-stu-id="a97ca-211">Progress bars are designed for graphically displaying the percentage of a particular process that has been completed, but not for a process that the user will want to interact with.</span></span> <span data-ttu-id="a97ca-212">È ad esempio possibile utilizzare un indicatore di stato per indicare lo stato di avanzamento del buffer.</span><span class="sxs-lookup"><span data-stu-id="a97ca-212">For example, you might want to use a progress bar to indicate buffering progress.</span></span>
-   <span data-ttu-id="a97ca-213">**Dispositivi di scorrimento personalizzati.**</span><span class="sxs-lookup"><span data-stu-id="a97ca-213">**Custom sliders.**</span></span> <span data-ttu-id="a97ca-214">Viene fornita la funzionalità di dispositivo di scorrimento personalizzata, in modo da poter creare controlli come le manopole o eseguire meccanismi di controllo insoliti.</span><span class="sxs-lookup"><span data-stu-id="a97ca-214">Custom slider functionality is provided so you can create controls such as knobs, or make unusual control mechanisms.</span></span> <span data-ttu-id="a97ca-215">Se, ad esempio, si desidera creare un controllo volume che esegue il wrapping dell'interfaccia, è possibile eseguire questa operazione con un dispositivo di scorrimento personalizzato.</span><span class="sxs-lookup"><span data-stu-id="a97ca-215">For example, if you want to create a volume control that wraps around your skin, you can do it with a custom slider.</span></span> <span data-ttu-id="a97ca-216">Per configurare il dispositivo di scorrimento personalizzato, è necessario creare una mappa immagine che contiene immagini di scala di grigi per definire le posizioni dei valori sul dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="a97ca-216">To set up the custom slider, you must create an image map that contains grayscale images to define the locations of the values on the slider.</span></span> <span data-ttu-id="a97ca-217">Questa operazione è relativamente semplice con un programma di modifica della grafica che supporta i livelli.</span><span class="sxs-lookup"><span data-stu-id="a97ca-217">This is relatively easy to do with a graphics editing program that supports layers.</span></span>

## <a name="text"></a><span data-ttu-id="a97ca-218">Testo</span><span class="sxs-lookup"><span data-stu-id="a97ca-218">Text</span></span>

<span data-ttu-id="a97ca-219">È possibile usare l'elemento di **testo** per visualizzare il testo sull'interfaccia, ad esempio i titoli delle canzoni.</span><span class="sxs-lookup"><span data-stu-id="a97ca-219">You can use the **TEXT** element to display text on your skin, such as song titles.</span></span>

## <a name="video"></a><span data-ttu-id="a97ca-220">Video</span><span class="sxs-lookup"><span data-stu-id="a97ca-220">Video</span></span>

<span data-ttu-id="a97ca-221">È possibile visualizzare il video nell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="a97ca-221">You can display video in your skin.</span></span> <span data-ttu-id="a97ca-222">L'elemento **video** consente di impostare le dimensioni e la posizione della finestra del video.</span><span class="sxs-lookup"><span data-stu-id="a97ca-222">The **VIDEO** element allows you to set the size and position of the video window.</span></span>

<span data-ttu-id="a97ca-223">È anche possibile consentire all'utente di modificare le impostazioni video con l'elemento **VIDEOSETTINGS** .</span><span class="sxs-lookup"><span data-stu-id="a97ca-223">You can also allow the user to change the video settings with the **VIDEOSETTINGS** element.</span></span> <span data-ttu-id="a97ca-224">Ad esempio, è possibile creare controlli per regolare la luminosità del video.</span><span class="sxs-lookup"><span data-stu-id="a97ca-224">For example, you can create controls to adjust the brightness of the video.</span></span>

<span data-ttu-id="a97ca-225">Se non si specifica un elemento video e il contenuto contiene video, Windows Media Player tornerà alla modalità Full e l'interfaccia non verrà visualizzata.</span><span class="sxs-lookup"><span data-stu-id="a97ca-225">If you do not supply a video element and the content contains video, Windows Media Player will return to full mode and your skin will not be displayed.</span></span>

## <a name="equalizer-settings"></a><span data-ttu-id="a97ca-226">Impostazioni equalizzatore</span><span class="sxs-lookup"><span data-stu-id="a97ca-226">Equalizer Settings</span></span>

<span data-ttu-id="a97ca-227">È possibile impostare il filtro per bande di frequenza audio specifiche usando l'elemento **EQUALIZERSETTINGS** .</span><span class="sxs-lookup"><span data-stu-id="a97ca-227">You can set the filtering for specific audio frequency bands by using the **EQUALIZERSETTINGS** element.</span></span> <span data-ttu-id="a97ca-228">È possibile aumentare i bassi, modificare gli acuti e configurare i suoni in modo che corrispondano alle orecchie o alla sala da lavoro.</span><span class="sxs-lookup"><span data-stu-id="a97ca-228">You can boost the bass, tweak the treble, and set up your sounds to match your ears or your living room.</span></span>

## <a name="visualizations"></a><span data-ttu-id="a97ca-229">Visualizzazioni</span><span class="sxs-lookup"><span data-stu-id="a97ca-229">Visualizations</span></span>

<span data-ttu-id="a97ca-230">È possibile visualizzare le visualizzazioni nell'interfaccia personalizzata.</span><span class="sxs-lookup"><span data-stu-id="a97ca-230">You can display visualizations in your skin.</span></span> <span data-ttu-id="a97ca-231">Le visualizzazioni sono effetti visivi che cambiano nel tempo quando l'audio viene riprodotto tramite Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="a97ca-231">Visualizations are visual effects that change over time as audio is playing through Windows Media Player.</span></span> <span data-ttu-id="a97ca-232">L'elemento **Effects** determina la posizione in cui verranno riprodotte le visualizzazioni, le dimensioni della finestra e le visualizzazioni che verranno riprodotte.</span><span class="sxs-lookup"><span data-stu-id="a97ca-232">The **EFFECTS** element determines where the visualizations will play, what size the window will be, and which visualizations will be played.</span></span>

## <a name="playlists"></a><span data-ttu-id="a97ca-233">Playlist</span><span class="sxs-lookup"><span data-stu-id="a97ca-233">Playlists</span></span>

<span data-ttu-id="a97ca-234">È possibile usare l'elemento **playlist** per consentire all'utente di selezionare un elemento da una playlist specifica.</span><span class="sxs-lookup"><span data-stu-id="a97ca-234">You can use the **PLAYLIST** element to let the user select an item from a specific playlist.</span></span>

## <a name="subviews"></a><span data-ttu-id="a97ca-235">Visualizzazioni secondarie</span><span class="sxs-lookup"><span data-stu-id="a97ca-235">Subviews</span></span>

<span data-ttu-id="a97ca-236">È possibile utilizzare l'elemento di **visualizzazione** secondaria per visualizzare set secondari di controlli dell'interfaccia, ad esempio una playlist o controlli video.</span><span class="sxs-lookup"><span data-stu-id="a97ca-236">You can use the **SUBVIEW** element to display secondary sets of interface controls, such as a playlist or video controls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a97ca-237">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a97ca-237">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a97ca-238">**File di interfaccia**</span><span class="sxs-lookup"><span data-stu-id="a97ca-238">**Skin Files**</span></span>](skin-files.md)
</dt> </dl>

 

 




