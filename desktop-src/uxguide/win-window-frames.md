---
title: Frame della finestra
description: La maggior parte dei programmi deve usare frame della finestra standard. Le applicazioni immersive possono avere una modalità schermo intero che nasconde la cornice della finestra. Prendere in considerazione l'uso di Glass in modo strategico per un aspetto più semplice, più chiaro e coeso.
ms.assetid: 6613e07a-2466-4283-88a9-02f2a3fea079
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 40aa58ab48c032519f55afa7c269be6452956912
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104570969"
---
# <a name="window-frames"></a><span data-ttu-id="a376c-105">Frame della finestra</span><span class="sxs-lookup"><span data-stu-id="a376c-105">Window Frames</span></span>

> [!NOTE]
> <span data-ttu-id="a376c-106">Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="a376c-106">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="a376c-107">Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).</span><span class="sxs-lookup"><span data-stu-id="a376c-107">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="a376c-108">La maggior parte dei programmi deve usare frame della finestra standard.</span><span class="sxs-lookup"><span data-stu-id="a376c-108">Most programs should use standard window frames.</span></span> <span data-ttu-id="a376c-109">Le applicazioni immersive possono avere una modalità schermo intero che nasconde la cornice della finestra.</span><span class="sxs-lookup"><span data-stu-id="a376c-109">Immersive applications can have a full screen mode that hides the window frame.</span></span> <span data-ttu-id="a376c-110">Prendere in considerazione l'uso di Glass in modo strategico per un aspetto più semplice, più chiaro e coeso.</span><span class="sxs-lookup"><span data-stu-id="a376c-110">Consider using glass strategically for a simpler, lighter, more cohesive look.</span></span>

<span data-ttu-id="a376c-111">Con una cornice della finestra, gli utenti possono modificare una finestra e visualizzare il titolo e l'icona per identificarne il contenuto.</span><span class="sxs-lookup"><span data-stu-id="a376c-111">With a window frame, users can manipulate a window and view the title and icon to identify its contents.</span></span>

![<span data-ttu-id="a376c-112">screenshot della cornice della finestra intorno alla finestra del blocco note</span><span class="sxs-lookup"><span data-stu-id="a376c-112">screen shot of window frame around notepad window</span></span> ](images/win-window-frames-image1.png)

<span data-ttu-id="a376c-113">Una cornice di finestra tipica.</span><span class="sxs-lookup"><span data-stu-id="a376c-113">A typical window frame.</span></span>

<span data-ttu-id="a376c-114">**Nota:** Le linee guida relative alla gestione e alla [personalizzazione](exper-branding.md) [delle finestre](win-window-mgt.md) sono presentate in articoli distinti.</span><span class="sxs-lookup"><span data-stu-id="a376c-114">**Note:** Guidelines related to [window management](win-window-mgt.md) and [branding](exper-branding.md) are presented in separate articles.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="a376c-115">Concetti relativi alla progettazione</span><span class="sxs-lookup"><span data-stu-id="a376c-115">Design concepts</span></span>

### <a name="glass-window-frames"></a><span data-ttu-id="a376c-116">Cornice della finestra Glass</span><span class="sxs-lookup"><span data-stu-id="a376c-116">Glass window frames</span></span>

<span data-ttu-id="a376c-117">I frame della finestra vetrata sono un nuovo aspetto interessante di Microsoft Windows estetico, che punta a essere sia accattivante che leggero.</span><span class="sxs-lookup"><span data-stu-id="a376c-117">The glass window frames are a striking new aspect of the Microsoft Windows aesthetic, aiming to be both attractive and lightweight.</span></span> <span data-ttu-id="a376c-118">Questi frame traslucidi offrono a Windows un aspetto aperto, meno intrusivo, che consente agli utenti di concentrarsi sui contenuti e sulle funzionalità anziché sull'interfaccia che la circonda.</span><span class="sxs-lookup"><span data-stu-id="a376c-118">These translucent frames give windows an open, less intrusive appearance, helping users focus on content and functionality rather than the interface surrounding it.</span></span>

![<span data-ttu-id="a376c-119">screenshot della cornice di vetro intorno al calcolatore</span><span class="sxs-lookup"><span data-stu-id="a376c-119">screen shot of glass frame around calculator</span></span> ](images/win-window-frames-image2.png)

<span data-ttu-id="a376c-120">Frame della finestra di vetro.</span><span class="sxs-lookup"><span data-stu-id="a376c-120">Glass window frames.</span></span>

<span data-ttu-id="a376c-121">È possibile usare il vetro in modo strategico in aree piccole all'interno di una finestra che tocca la cornice della finestra.</span><span class="sxs-lookup"><span data-stu-id="a376c-121">You can use glass strategically in small regions within a window that touch the window frame.</span></span> <span data-ttu-id="a376c-122">Tali aree sembrano essere parte della cornice della finestra, anche se tecnicamente fanno parte dell'area client della finestra.</span><span class="sxs-lookup"><span data-stu-id="a376c-122">Such regions appear to be part of the window frame, even though technically they are part of the window's client area.</span></span>

![<span data-ttu-id="a376c-123">screenshot della finestra con bordo traslucido</span><span class="sxs-lookup"><span data-stu-id="a376c-123">screen shot of window with translucent edge</span></span> ](images/win-window-frames-image3.png)

<span data-ttu-id="a376c-124">In questo esempio, il vetro viene usato nell'area client per renderlo simile a parte del frame.</span><span class="sxs-lookup"><span data-stu-id="a376c-124">In this example, glass is used in the client area to make it look like part of the frame.</span></span>

### <a name="hidden-frames"></a><span data-ttu-id="a376c-125">Frame nascosti</span><span class="sxs-lookup"><span data-stu-id="a376c-125">Hidden frames</span></span>

<span data-ttu-id="a376c-126">In alcuni casi la cornice migliore della finestra non è un frame.</span><span class="sxs-lookup"><span data-stu-id="a376c-126">Sometimes the best window frame is no frame at all.</span></span> <span data-ttu-id="a376c-127">Questo è spesso il caso della [finestra principale](glossary.md) di applicazioni a [schermo intero](glossary.md) immersive che non vengono usate insieme ad altri programmi, ad esempio lettori multimediali, giochi e applicazioni chiosco.</span><span class="sxs-lookup"><span data-stu-id="a376c-127">This is often the case for the [primary window](glossary.md) of immersive [full screen](glossary.md) applications that aren't used in conjunction with other programs, such as media players, games, and kiosk applications.</span></span>

<span data-ttu-id="a376c-128">I visualizzatori di contenuto spesso traggono vantaggio dalla possibilità di visualizzare il contenuto a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="a376c-128">Content viewers often benefit from having the option to show content full screen.</span></span> <span data-ttu-id="a376c-129">Gli esempi includono Windows Internet Explorer, raccolta foto di Windows Live, Windows Movie Maker HD, Microsoft PowerPoint e Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="a376c-129">Examples include Windows Internet Explorer , Windows Live Photo Gallery, Windows Movie Maker HD, Microsoft PowerPoint , and Microsoft Word.</span></span>

![<span data-ttu-id="a376c-130">Screenshot di Media Player nella visualizzazione a schermo intero</span><span class="sxs-lookup"><span data-stu-id="a376c-130">screen shot of media player in full-screen view</span></span> ](images/win-window-frames-image4.png)

<span data-ttu-id="a376c-131">In questo esempio, Windows Media Player può visualizzare il relativo contenuto a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="a376c-131">In this example, Windows Media Player can display its content full screen.</span></span>

### <a name="custom-frames"></a><span data-ttu-id="a376c-132">Frame personalizzati</span><span class="sxs-lookup"><span data-stu-id="a376c-132">Custom frames</span></span>

<span data-ttu-id="a376c-133">La maggior parte delle applicazioni Windows deve usare i frame della finestra standard.</span><span class="sxs-lookup"><span data-stu-id="a376c-133">Most Windows applications should use the standard window frames.</span></span> <span data-ttu-id="a376c-134">Tuttavia, per le applicazioni autonome immersive a schermo intero, ad esempio giochi e applicazioni chiosco, potrebbe essere opportuno usare frame personalizzati per qualsiasi finestra che non viene visualizzata a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="a376c-134">However, for immersive, full screen, stand-alone applications like games and kiosk applications, it may be appropriate to use custom frames for any windows that aren't shown full screen.</span></span> <span data-ttu-id="a376c-135">La motivazione a usare i frame personalizzati dovrebbe essere quella di offrire un'esperienza complessiva univoca, non solo per la [personalizzazione](exper-branding.md).</span><span class="sxs-lookup"><span data-stu-id="a376c-135">The motivation to use custom frames should be to give the overall experience a unique feel, not just for [branding](exper-branding.md).</span></span>

![<span data-ttu-id="a376c-136">illustrazione del puzzle e del frame per immagini strapazzate</span><span class="sxs-lookup"><span data-stu-id="a376c-136">illustration of scrambled picture puzzle and frame</span></span> ](images/win-window-frames-image5.png)

<span data-ttu-id="a376c-137">I frame personalizzati sono appropriati per le applicazioni autonome immersive, a schermo intero, ad esempio i giochi.</span><span class="sxs-lookup"><span data-stu-id="a376c-137">Custom frames are appropriate for immersive, full screen, stand-alone applications such as games.</span></span>

## <a name="guidelines"></a><span data-ttu-id="a376c-138">Indicazioni</span><span class="sxs-lookup"><span data-stu-id="a376c-138">Guidelines</span></span>

### <a name="window-frames"></a><span data-ttu-id="a376c-139">Frame della finestra</span><span class="sxs-lookup"><span data-stu-id="a376c-139">Window frames</span></span>

-   <span data-ttu-id="a376c-140">Usare i frame della finestra standard.</span><span class="sxs-lookup"><span data-stu-id="a376c-140">Use standard window frames.</span></span>
    -   <span data-ttu-id="a376c-141">**Eccezione:** Per offrire alle applicazioni autonome a schermo intero un'unica sensazione:</span><span class="sxs-lookup"><span data-stu-id="a376c-141">**Exception:** To give immersive full screen, stand-alone applications a unique feel:</span></span>
        -   <span data-ttu-id="a376c-142">Prendere in considerazione la possibilità di nascondere la cornice della finestra [principale](glossary.md).</span><span class="sxs-lookup"><span data-stu-id="a376c-142">Consider hiding the window frame of the [primary window](glossary.md).</span></span>
        -   <span data-ttu-id="a376c-143">Si consiglia di utilizzare frame personalizzati per la [finestra secondaria](glossary.md).</span><span class="sxs-lookup"><span data-stu-id="a376c-143">Consider using custom frames for [secondary window](glossary.md).</span></span>
        -   <span data-ttu-id="a376c-144">Se un frame personalizzato è appropriato, scegliere una progettazione leggera e non attirare eccessiva attenzione su se stessa.</span><span class="sxs-lookup"><span data-stu-id="a376c-144">If a custom frame is appropriate, choose a design that is lightweight and doesn't draw too much attention to itself.</span></span>

            <span data-ttu-id="a376c-145">**Non corretto:**</span><span class="sxs-lookup"><span data-stu-id="a376c-145">**Incorrect:**</span></span>

            ![<span data-ttu-id="a376c-146">cattura di schermata del frame di distrazione</span><span class="sxs-lookup"><span data-stu-id="a376c-146">screen shot of distracting frame</span></span> ](images/win-window-frames-image6.png)

            <span data-ttu-id="a376c-147">In questo esempio il frame personalizzato disegna troppo attenzione per se stesso.</span><span class="sxs-lookup"><span data-stu-id="a376c-147">In this example, the custom frame draws too much attention to itself.</span></span>
-   <span data-ttu-id="a376c-148">Non aggiungere controlli a una cornice della finestra.</span><span class="sxs-lookup"><span data-stu-id="a376c-148">Don't add controls to a window frame.</span></span> <span data-ttu-id="a376c-149">In alternativa, inserire i controlli all'interno della finestra.</span><span class="sxs-lookup"><span data-stu-id="a376c-149">Put the controls within the window instead.</span></span>

    <span data-ttu-id="a376c-150">**Non corretto:**</span><span class="sxs-lookup"><span data-stu-id="a376c-150">**Incorrect:**</span></span>

    ![<span data-ttu-id="a376c-151">screenshot del controllo nella cornice della finestra</span><span class="sxs-lookup"><span data-stu-id="a376c-151">screen shot of control in window frame</span></span> ](images/win-window-frames-image7.png)

    <span data-ttu-id="a376c-152">**Corretto:**</span><span class="sxs-lookup"><span data-stu-id="a376c-152">**Correct:**</span></span>

    ![<span data-ttu-id="a376c-153">screenshot del controllo nell'area client</span><span class="sxs-lookup"><span data-stu-id="a376c-153">screen shot of control in client area</span></span> ](images/win-window-frames-image8.png)

    <span data-ttu-id="a376c-154">Nell'esempio corretto, il controllo si trova all'interno dell'area client anziché della cornice della finestra.</span><span class="sxs-lookup"><span data-stu-id="a376c-154">In the correct example, the control is within the client area instead of the window frame.</span></span>

### <a name="full-screen-mode"></a><span data-ttu-id="a376c-155">Modalità schermo intero</span><span class="sxs-lookup"><span data-stu-id="a376c-155">Full screen mode</span></span>

-   <span data-ttu-id="a376c-156">Per i programmi che dispongono di una modalità schermo intero facoltativa, per abilitare la modalità schermo intero:</span><span class="sxs-lookup"><span data-stu-id="a376c-156">For programs that have an optional full screen mode, to enable full screen mode:</span></span>
    -   <span data-ttu-id="a376c-157">Disporre di un comando modale a schermo intero sulla barra dei menu o sulla barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="a376c-157">Have a modal full screen command in the menu bar or toolbar.</span></span> <span data-ttu-id="a376c-158">Quando l'utente fa clic sul comando, Mostra il comando nello stato selezionato.</span><span class="sxs-lookup"><span data-stu-id="a376c-158">When the user clicks the command, show the command in its selected state.</span></span>

        ![<span data-ttu-id="a376c-159">screenshot della finestra con la voce di menu a schermo intero</span><span class="sxs-lookup"><span data-stu-id="a376c-159">screen shot of window with full screen menu item</span></span> ](images/win-window-frames-image9.png)

        <span data-ttu-id="a376c-160">Questo esempio mostra il comando schermo intero insieme al relativo tasto di scelta rapida standard.</span><span class="sxs-lookup"><span data-stu-id="a376c-160">This example shows the full screen command along with its standard shortcut key.</span></span>

-   <span data-ttu-id="a376c-161">Utilizzare F11 per il tasto di scelta rapida schermo intero.</span><span class="sxs-lookup"><span data-stu-id="a376c-161">Use F11 for the full screen shortcut key.</span></span>
-   <span data-ttu-id="a376c-162">Se è presente una barra degli strumenti e la modalità schermo intero viene comunemente usata, avere anche un pulsante della barra degli strumenti grafico con una descrizione comando a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="a376c-162">If there is a toolbar and full screen mode is commonly used, also have a graphic toolbar button with a Full screen tooltip.</span></span>

    ![<span data-ttu-id="a376c-163">screenshot dei pulsanti a schermo intero e di ripristino</span><span class="sxs-lookup"><span data-stu-id="a376c-163">screen shot of full screen and revert buttons</span></span> ](images/win-window-frames-image10.png)

    <span data-ttu-id="a376c-164">Esempi di pulsanti della barra degli strumenti a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="a376c-164">Examples of full screen toolbar buttons.</span></span>

-   <span data-ttu-id="a376c-165">Per eseguire il ripristino dalla modalità schermo intero:</span><span class="sxs-lookup"><span data-stu-id="a376c-165">To revert back from full screen mode:</span></span>
    -   <span data-ttu-id="a376c-166">Disporre di un comando modale a schermo intero sulla barra dei menu o sulla barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="a376c-166">Have a modal full screen command in the menu bar or toolbar.</span></span> <span data-ttu-id="a376c-167">Quando l'utente fa clic sul comando, Visualizza il comando nello stato cancellato.</span><span class="sxs-lookup"><span data-stu-id="a376c-167">When the user clicks the command, show the command in its cleared state.</span></span>
    -   <span data-ttu-id="a376c-168">Utilizzare F11 per il tasto di scelta rapida schermo intero.</span><span class="sxs-lookup"><span data-stu-id="a376c-168">Use F11 for the full screen shortcut key.</span></span> <span data-ttu-id="a376c-169">Se non è già assegnato, è possibile usare ESC anche per questo scopo.</span><span class="sxs-lookup"><span data-stu-id="a376c-169">If not already assigned, Esc can also be used for this purpose.</span></span>

### <a name="glass"></a><span data-ttu-id="a376c-170">Vetro</span><span class="sxs-lookup"><span data-stu-id="a376c-170">Glass</span></span>

<span data-ttu-id="a376c-171">I frame della finestra standard utilizzano automaticamente il vetro in Windows, ma è anche possibile utilizzare il vetro in aree che toccano la cornice della finestra.</span><span class="sxs-lookup"><span data-stu-id="a376c-171">Standard window frames use glass automatically in Windows, but you can also use glass in regions that touch the window frame.</span></span>

-   <span data-ttu-id="a376c-172">**Si consiglia di usare il vetro in modo strategico in aree di piccole dimensioni toccando la cornice della finestra senza testo.**</span><span class="sxs-lookup"><span data-stu-id="a376c-172">**Consider using glass strategically in small regions touching the window frame without text.**</span></span> <span data-ttu-id="a376c-173">Questa operazione può offrire a un programma un aspetto più semplice, più chiaro e più coeso, facendo in modo che l'area appaia come parte del frame.</span><span class="sxs-lookup"><span data-stu-id="a376c-173">Doing so can give a program a simpler, lighter, more cohesive look by making the region appear to be part of the frame.</span></span>
-   ![<span data-ttu-id="a376c-174">screenshot della finestra con bordo traslucido</span><span class="sxs-lookup"><span data-stu-id="a376c-174">screen shot of window with translucent edge</span></span> ](images/win-window-frames-image3.png)
-   <span data-ttu-id="a376c-175">In questo esempio, Glass concentra l'attenzione dell'utente sul contenuto anziché sui controlli.</span><span class="sxs-lookup"><span data-stu-id="a376c-175">In this example, glass focuses the user's attention on the content instead of the controls.</span></span>
-   <span data-ttu-id="a376c-176">**Non usare il vetro in situazioni in cui uno sfondo normale della finestra sarebbe più interessante o più semplice da usare.**</span><span class="sxs-lookup"><span data-stu-id="a376c-176">**Don't use glass in situations where a plain window background would be more attractive or easier to use.**</span></span>

<span data-ttu-id="a376c-177">**Corretto:**</span><span class="sxs-lookup"><span data-stu-id="a376c-177">**Correct:**</span></span>

![<span data-ttu-id="a376c-178">screenshot della finestra con quattro elementi grafici ed etichetta</span><span class="sxs-lookup"><span data-stu-id="a376c-178">screen shot of window with four graphics and label</span></span> ](images/win-window-frames-image11.png)

<span data-ttu-id="a376c-179">In questo esempio, Glass viene usato per assegnare alla finestra Alt + Tab un aspetto leggero.</span><span class="sxs-lookup"><span data-stu-id="a376c-179">In this example, glass is used to give the Alt+Tab window a lightweight appearance.</span></span> <span data-ttu-id="a376c-180">Il vetro funziona per questa finestra perché è costituito da grafica e da un'unica etichetta con testo sicuro.</span><span class="sxs-lookup"><span data-stu-id="a376c-180">Glass works for this window because it consists of graphics and a single, strong text label.</span></span>

<span data-ttu-id="a376c-181">**Non corretto:**</span><span class="sxs-lookup"><span data-stu-id="a376c-181">**Incorrect:**</span></span>

![<span data-ttu-id="a376c-182">screenshot della finestra con dodici elementi grafici</span><span class="sxs-lookup"><span data-stu-id="a376c-182">screen shot of window with twelve graphics</span></span> ](images/win-window-frames-image12.png)

<span data-ttu-id="a376c-183">In questo esempio non corretto, l'uso di Glass sta distraendo.</span><span class="sxs-lookup"><span data-stu-id="a376c-183">In this incorrect example, the use of glass is distracting.</span></span> <span data-ttu-id="a376c-184">Una semplice sfondo della finestra sarebbe una scelta migliore.</span><span class="sxs-lookup"><span data-stu-id="a376c-184">A plain window background would be a better choice.</span></span>

 

 