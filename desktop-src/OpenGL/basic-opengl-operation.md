---
title: Operazione OpenGL di base
description: Operazione OpenGL di base
ms.assetid: ad4c9321-a9e3-40c5-af80-0ad6a8b9f380
keywords:
- OpenGL, operazioni di base
- OpenGL, elaborazione dati
- OpenGL, fasi di elaborazione
- OpenGL, elenchi di visualizzazione
- visualizzazione degli elenchi OpenGL
- OpenGL, analizzatori
- analizzatori OpenGL
- Operazioni di OpenGL, per vertice
- operazioni per vertice OpenGL
- OpenGL, assembly primitivo
- OpenGL assembly primitivo
- OpenGL, rasterizzazione
- rasterizzazione OpenGL
- Operazioni OpenGL, per frammento
- operazioni per frammenti OpenGL
- framebuffer, operazioni di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77f6b9fb8c8ca4efb05d9050e0de3da807b213e7
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "103968824"
---
# <a name="basic-opengl-operation"></a><span data-ttu-id="50c66-119">Operazione OpenGL di base</span><span class="sxs-lookup"><span data-stu-id="50c66-119">Basic OpenGL Operation</span></span>

<span data-ttu-id="50c66-120">Il diagramma seguente illustra il modo in cui OpenGL elabora i dati.</span><span class="sxs-lookup"><span data-stu-id="50c66-120">The following diagram illustrates how OpenGL processes data.</span></span> <span data-ttu-id="50c66-121">Come illustrato, i comandi entrano da sinistra e passano attraverso una pipeline di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="50c66-121">As shown, commands enter from the left and proceed through a processing pipeline.</span></span> <span data-ttu-id="50c66-122">Alcuni comandi specificano oggetti geometrici da disegnare e altri controllano il modo in cui gli oggetti vengono gestiti durante le varie fasi di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="50c66-122">Some commands specify geometric objects to be drawn, and others control how the objects are handled during various processing stages.</span></span>

![Diagramma che illustra le fasi della pipeline di elaborazione dati OpenGL.](images/basic01.png)

<span data-ttu-id="50c66-124">Le fasi di elaborazione nell'operazione OpenGL di base sono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="50c66-124">The processing stages in basic OpenGL operation are as follows:</span></span>

-   <span data-ttu-id="50c66-125">**Elenco di visualizzazione** Anziché fare in modo che tutti i comandi procedano immediatamente attraverso la pipeline, è possibile scegliere di accumularne alcuni in un elenco di visualizzazione per l'elaborazione in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="50c66-125">**Display list** Rather than having all commands proceed immediately through the pipeline, you can choose to accumulate some of them in a display list for processing later.</span></span>
-   <span data-ttu-id="50c66-126">**Analizzatore** La fase di elaborazione dell'analizzatore fornisce un modo efficiente per approssimare la geometria della curva e della superficie valutando i comandi polinomiali dei valori di input.</span><span class="sxs-lookup"><span data-stu-id="50c66-126">**Evaluator** The evaluator stage of processing provides an efficient way to approximate curve and surface geometry by evaluating polynomial commands of input values.</span></span>
-   <span data-ttu-id="50c66-127">**Operazioni per vertice e assembly primitivo** OpenGL elabora i primitivespoints geometrici, i segmenti di linea e polygonsall di cui sono descritti i vertici.</span><span class="sxs-lookup"><span data-stu-id="50c66-127">**Per-vertex operations and primitive assembly** OpenGL processes geometric primitivespoints, line segments, and polygonsall of which are described by vertices.</span></span> <span data-ttu-id="50c66-128">I vertici vengono trasformati e illuminati e le primitive vengono ritagliate nel viewport in preparazione per la rasterizzazione.</span><span class="sxs-lookup"><span data-stu-id="50c66-128">Vertices are transformed and lit, and primitives are clipped to the viewport in preparation for rasterization.</span></span>
-   <span data-ttu-id="50c66-129">**Rasterizzazione** La fase di rasterizzazione produce una serie di indirizzi del buffer dei frame e valori associati usando una descrizione bidimensionale di un punto, un segmento di linea o un poligono.</span><span class="sxs-lookup"><span data-stu-id="50c66-129">**Rasterization** The rasterization stage produces a series of frame-buffer addresses and associated values using a two-dimensional description of a point, line segment, or polygon.</span></span> <span data-ttu-id="50c66-130">Ogni frammento generato viene inserito nell'ultima fase, ovvero le operazioni per frammento.</span><span class="sxs-lookup"><span data-stu-id="50c66-130">Each fragment so produced is fed into the last stage, per-fragment operations.</span></span>
-   <span data-ttu-id="50c66-131">**Operazioni per frammento** Queste sono le operazioni finali eseguite sui dati prima di essere archiviate come pixel nel framebuffer.</span><span class="sxs-lookup"><span data-stu-id="50c66-131">**Per-fragment operations** These are the final operations performed on the data before it is stored as pixels in the framebuffer.</span></span>

    <span data-ttu-id="50c66-132">Le operazioni per frammento includono gli aggiornamenti condizionali per il framebuffer in base ai valori z in ingresso e archiviati in precedenza (per il buffering z) e la combinazione dei colori dei pixel in ingresso con i colori archiviati, nonché la maschera e altre operazioni logiche sui valori dei pixel.</span><span class="sxs-lookup"><span data-stu-id="50c66-132">Per-fragment operations include conditional updates to the framebuffer based on incoming and previously stored z values (for z buffering) and blending of incoming pixel colors with stored colors, as well as masking and other logical operations on pixel values.</span></span>

<span data-ttu-id="50c66-133">I dati possono essere di input in formato pixel anziché vertici.</span><span class="sxs-lookup"><span data-stu-id="50c66-133">Data can be input in the form of pixels rather than vertices.</span></span> <span data-ttu-id="50c66-134">I dati sotto forma di pixel, ad esempio, possono descrivere un'immagine da usare nel mapping di trama, ignora la prima fase di elaborazione descritta sopra e viene invece elaborata come pixel nella fase operazioni pixel.</span><span class="sxs-lookup"><span data-stu-id="50c66-134">Data in the form of pixels, such as might describe an image for use in texture mapping, skips the first stage of processing described above and instead is processed as pixels, in the pixel operations stage.</span></span> <span data-ttu-id="50c66-135">Di seguito sono riportate le operazioni pixel, ovvero i dati pixel:</span><span class="sxs-lookup"><span data-stu-id="50c66-135">Following pixel operations, the pixel data is either:</span></span>

-   <span data-ttu-id="50c66-136">Archiviato come memoria di trama, da utilizzare nella fase di rasterizzazione.</span><span class="sxs-lookup"><span data-stu-id="50c66-136">Stored as texture memory, for use in the rasterization stage.</span></span>
-   <span data-ttu-id="50c66-137">Rasterizzato, con i frammenti risultanti Uniti nel framebuffer esattamente come se fossero stati generati da dati geometrici.</span><span class="sxs-lookup"><span data-stu-id="50c66-137">Rasterized, with the resulting fragments merged into the framebuffer just as if they were generated from geometric data.</span></span>

 

 




