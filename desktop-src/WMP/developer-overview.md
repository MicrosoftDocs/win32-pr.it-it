---
title: Panoramica degli sviluppatori
description: Panoramica degli sviluppatori
ms.assetid: 72a330b4-5957-4159-b5e8-0c9a4491b589
keywords:
- Plug-in di Windows Media Player, visualizzazioni
- plug-in, visualizzazioni
- Visualizzazioni, panoramica degli sviluppatori
- Visualizzazioni personalizzate, panoramica degli sviluppatori
- Visualizzazioni, controlli COM
- Visualizzazioni personalizzate, controlli COM
- Visualizzazioni, input audio
- Visualizzazioni personalizzate, input audio
- Visualizzazioni, output grafico
- Visualizzazioni personalizzate, output grafico
- Visualizzazioni, strumenti di disegno
- Visualizzazioni personalizzate, strumenti di disegno
- Visualizzazioni, linguaggio di programmazione
- Visualizzazioni personalizzate, linguaggio di programmazione
- Visualizzazioni, Visual C++
- Visualizzazioni personalizzate, Visual C++
- Visualizzazioni, creazione guidata plug-in
- Visualizzazioni personalizzate, creazione guidata plug-in
- procedura guidata plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36ec8632bd5611e081a4a17d1b0390dc99a09703
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331116"
---
# <a name="developer-overview"></a><span data-ttu-id="18d3b-122">Panoramica degli sviluppatori</span><span class="sxs-lookup"><span data-stu-id="18d3b-122">Developer Overview</span></span>

<span data-ttu-id="18d3b-123">Dal punto di vista dello sviluppatore, le visualizzazioni sono programmi software che accettano i dati audio forniti da Windows Media Player e convertono i dati in un grafico che consente di osservare l'utente.</span><span class="sxs-lookup"><span data-stu-id="18d3b-123">From the developer's point of view, visualizations are software programs that take audio data provided by Windows Media Player and convert that data to graphics that will please the eye of the user.</span></span> <span data-ttu-id="18d3b-124">Gli argomenti principali che uno sviluppatore deve conoscere per creare una nuova visualizzazione sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="18d3b-124">The main subjects a developer needs to understand to create a new visualization are the following:</span></span>

## <a name="visualization-packaging"></a><span data-ttu-id="18d3b-125">Creazione di pacchetti di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="18d3b-125">Visualization Packaging</span></span>

<span data-ttu-id="18d3b-126">Le visualizzazioni sono controlli COM usati da Windows Media Player per trasformare le forme d'onda audio in grafica animata in Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="18d3b-126">Visualizations are COM controls that Windows Media Player uses to turn audio waveforms into animated graphics in Microsoft Windows.</span></span> <span data-ttu-id="18d3b-127">I controlli COM vengono inclusi in un pacchetto come librerie di collegamento dinamico (dll) di Microsoft Windows e devono essere registrati nel registro di sistema di Windows.</span><span class="sxs-lookup"><span data-stu-id="18d3b-127">The COM controls are packaged as Microsoft Windows dynamic-link libraries (DLLs) and must be registered in the Windows registry.</span></span> <span data-ttu-id="18d3b-128">Quando si esegue Windows Media Player, le visualizzazioni personalizzate registrate vengono caricate e visualizzate in base alle istruzioni dell'interfaccia utilizzata da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="18d3b-128">When Windows Media Player runs, registered custom visualizations are loaded and viewed in accordance with the instructions of the skin that Windows Media Player is using.</span></span>

## <a name="audio-input"></a><span data-ttu-id="18d3b-129">Input audio</span><span class="sxs-lookup"><span data-stu-id="18d3b-129">Audio Input</span></span>

<span data-ttu-id="18d3b-130">Windows Media Player fornisce al codice snapshot di frequenza audio e dati di forma d'onda a intervalli temporizzati misurati in frazioni di secondo.</span><span class="sxs-lookup"><span data-stu-id="18d3b-130">Windows Media Player provides your code with snapshots of audio frequency and waveform data at timed intervals measured in fractions of a second.</span></span> <span data-ttu-id="18d3b-131">L'intervallo di snapshot è determinato internamente dal Media Player di Windows.</span><span class="sxs-lookup"><span data-stu-id="18d3b-131">The snapshot interval is internally determined by the Windows Media Player.</span></span>

## <a name="graphical-output"></a><span data-ttu-id="18d3b-132">Output grafico</span><span class="sxs-lookup"><span data-stu-id="18d3b-132">Graphical Output</span></span>

<span data-ttu-id="18d3b-133">L'output grafico della visualizzazione è un contesto di dispositivo Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="18d3b-133">The graphical output from your visualization is a Microsoft Windows device context.</span></span> <span data-ttu-id="18d3b-134">Si tratta di una superficie di disegno standard di Windows che è possibile disegnare ogni volta che viene fornito uno snapshot audio.</span><span class="sxs-lookup"><span data-stu-id="18d3b-134">This is a standard Windows drawing surface that you can draw upon every time an audio snapshot is provided.</span></span> <span data-ttu-id="18d3b-135">Tutte le tecnologie Windows in background vengono gestite automaticamente.</span><span class="sxs-lookup"><span data-stu-id="18d3b-135">All of the background Windows technology is taken care of for you.</span></span> <span data-ttu-id="18d3b-136">È sufficiente eseguire il progetto nel contesto di dispositivo con i dati audio forniti.</span><span class="sxs-lookup"><span data-stu-id="18d3b-136">You just have to draw on the device context with the audio data provided.</span></span>

## <a name="drawing-tools"></a><span data-ttu-id="18d3b-137">Strumenti di disegno</span><span class="sxs-lookup"><span data-stu-id="18d3b-137">Drawing Tools</span></span>

<span data-ttu-id="18d3b-138">È possibile creare il contesto di dispositivo con funzioni standard di Microsoft Windows Graphics Device Interface (GDI), usando penne e pennelli per creare progettazioni modificate dai dati audio forniti da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="18d3b-138">You can draw on the device context with standard Microsoft Windows Graphics Device Interface (GDI) functions, using pens and brushes to create designs that are modified by the audio data supplied to you by Windows Media Player.</span></span> <span data-ttu-id="18d3b-139">GDI offre un set completo di strumenti di disegno che consentono di creare molti tipi di effetti visivi.</span><span class="sxs-lookup"><span data-stu-id="18d3b-139">GDI provides a rich set of drawing tools that can create many kinds of visual effects.</span></span>

## <a name="programming-language"></a><span data-ttu-id="18d3b-140">Linguaggio di programmazione</span><span class="sxs-lookup"><span data-stu-id="18d3b-140">Programming Language</span></span>

<span data-ttu-id="18d3b-141">Microsoft Visual C++ 6,0 e versioni successive è l'unico linguaggio supportato per la creazione di visualizzazioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="18d3b-141">Microsoft Visual C++ 6.0 and higher is the only supported language for creating custom visualizations.</span></span>

## <a name="plug-in-wizard"></a><span data-ttu-id="18d3b-142">Procedura guidata plug-in</span><span class="sxs-lookup"><span data-stu-id="18d3b-142">Plug-in Wizard</span></span>

<span data-ttu-id="18d3b-143">Windows Media Player fornisce una procedura guidata COM che è possibile aggiungere ai Visual C++ che genereranno il codice sottostante necessario per la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="18d3b-143">Windows Media Player provides a COM wizard that you can add to Visual C++ that will generate the underlying code needed for your visualization.</span></span> <span data-ttu-id="18d3b-144">Non solo sono disponibili tutti i file di origine, ma viene generata un'interfaccia di esempio che semplifica il test della visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="18d3b-144">Not only are all source files provided, but a sample skin is generated to make it easy to test your visualization.</span></span> <span data-ttu-id="18d3b-145">Il codice generato crea una visualizzazione simile a barre, con due set di impostazioni.</span><span class="sxs-lookup"><span data-stu-id="18d3b-145">The generated code creates a visualization similar to Bars, with two presets.</span></span> <span data-ttu-id="18d3b-146">È quindi possibile modificare il codice per creare una visualizzazione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="18d3b-146">You can then modify the code to create your own visualization.</span></span> <span data-ttu-id="18d3b-147">Viene inoltre generato un file del registro di sistema per registrare la visualizzazione in modo che Windows Media Player possa caricarla.</span><span class="sxs-lookup"><span data-stu-id="18d3b-147">A registry file is also generated to register your visualization so that Windows Media Player can load it.</span></span>

<span data-ttu-id="18d3b-148">Nell'argomento seguente viene descritto il modo in cui il codice di visualizzazione elabora i dati audio:</span><span class="sxs-lookup"><span data-stu-id="18d3b-148">The following topic describes how visualization code processes audio data:</span></span>

-   [<span data-ttu-id="18d3b-149">Flusso di controllo</span><span class="sxs-lookup"><span data-stu-id="18d3b-149">Flow of Control</span></span>](flow-of-control.md)

## <a name="related-topics"></a><span data-ttu-id="18d3b-150">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="18d3b-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18d3b-151">**Informazioni sulle visualizzazioni personalizzate**</span><span class="sxs-lookup"><span data-stu-id="18d3b-151">**About Custom Visualizations**</span></span>](about-custom-visualizations.md)
</dt> </dl>

 

 




