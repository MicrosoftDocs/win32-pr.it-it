---
title: Esercitazione Introduzione con DirectWrite
description: Questo documento illustra come usare DirectWrite e Direct2D per creare testo semplice che contiene un singolo formato e quindi il testo che contiene più formati.
ms.assetid: cc2758d7-3f47-452a-8d81-3f777fe490ec
keywords:
- DirectWrite, esercitazione
- DirectWrite, esercitazione introduttiva
- DirectWrite, Direct2D
- Direct2D
- DirectWrite, interfaccia IDWriteTextLayout
- Interfaccia IDWriteTextLayout
- DirectWrite, interfaccia IDWriteTypography
- Interfaccia IDWriteTypography
- DirectWrite, interfaccia IDWriteTextFormat
- Interfaccia IDWriteTextFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48fb385ff78650a16599a32d76d7c51ba575de47
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338446"
---
# <a name="tutorial-getting-started-with-directwrite"></a><span data-ttu-id="f439f-113">Esercitazione: Introduzione con DirectWrite</span><span class="sxs-lookup"><span data-stu-id="f439f-113">Tutorial: Getting Started with DirectWrite</span></span>

<span data-ttu-id="f439f-114">Questo documento illustra come usare [DirectWrite](direct-write-portal.md) e [Direct2D](rendering-by-using-direct2d.md) per creare testo semplice che contiene un singolo formato e quindi il testo che contiene più formati.</span><span class="sxs-lookup"><span data-stu-id="f439f-114">This document shows you how to use [DirectWrite](direct-write-portal.md) and [Direct2D](rendering-by-using-direct2d.md) to create simple text that contains a single format, and then text that contains multiple formats.</span></span>

<span data-ttu-id="f439f-115">Questa esercitazione contiene le parti seguenti:</span><span class="sxs-lookup"><span data-stu-id="f439f-115">This tutorial contains the following parts:</span></span>

-   [<span data-ttu-id="f439f-116">Codice sorgente</span><span class="sxs-lookup"><span data-stu-id="f439f-116">Source Code</span></span>](#source-code)
-   [<span data-ttu-id="f439f-117">Disegno di testo semplice</span><span class="sxs-lookup"><span data-stu-id="f439f-117">Drawing Simple Text</span></span>](#drawing-simple-text)
    -   [<span data-ttu-id="f439f-118">Parte 1: dichiarare le risorse DirectWrite e Direct2D.</span><span class="sxs-lookup"><span data-stu-id="f439f-118">Part 1: Declare DirectWrite and Direct2D Resources.</span></span>](#part-1-declare-directwrite-and-direct2d-resources)
    -   [<span data-ttu-id="f439f-119">Parte 2: creare risorse indipendenti dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f439f-119">Part 2: Create Device Independent Resources.</span></span>](#part-2-create-device-independent-resources)
    -   [<span data-ttu-id="f439f-120">Parte 3: creare Device-Dependent risorse.</span><span class="sxs-lookup"><span data-stu-id="f439f-120">Part 3: Create Device-Dependent Resources.</span></span>](#part-3-create-device-dependent-resources)
    -   [<span data-ttu-id="f439f-121">Parte 4: creare il testo usando il metodo DrawText Direct2D.</span><span class="sxs-lookup"><span data-stu-id="f439f-121">Part 4: Draw Text By Using the Direct2D DrawText Method.</span></span>](#part-4-draw-text-by-using-the-direct2d-drawtext-method)
    -   [<span data-ttu-id="f439f-122">Parte 5: rendering del contenuto della finestra tramite Direct2D</span><span class="sxs-lookup"><span data-stu-id="f439f-122">Part 5: Render the Window Contents Using Direct2D</span></span>](#part-5-render-the-window-contents-using-direct2d)
-   [<span data-ttu-id="f439f-123">Disegno di testo con più formati.</span><span class="sxs-lookup"><span data-stu-id="f439f-123">Drawing Text with Multiple Formats.</span></span>](#drawing-text-with-multiple-formats)
    -   [<span data-ttu-id="f439f-124">Parte 1: creare un'interfaccia IDWriteTextLayout.</span><span class="sxs-lookup"><span data-stu-id="f439f-124">Part 1: Create an IDWriteTextLayout Interface.</span></span>](#part-1-create-an-idwritetextlayout-interface)
    -   [<span data-ttu-id="f439f-125">Parte 2: applicazione della formattazione con IDWriteTextLayout.</span><span class="sxs-lookup"><span data-stu-id="f439f-125">Part 2: Applying Formatting with IDWriteTextLayout.</span></span>](#part-2-applying-formatting-with-idwritetextlayout)
    -   [<span data-ttu-id="f439f-126">Parte 3: aggiunta di funzionalità tipografiche con IDWriteTypography.</span><span class="sxs-lookup"><span data-stu-id="f439f-126">Part 3: Adding Typographic Features with IDWriteTypography.</span></span>](#part-3-adding-typographic-features-with-idwritetypography)
    -   [<span data-ttu-id="f439f-127">Parte 4: creare il testo usando il metodo DrawTextLayout di Direct2D.</span><span class="sxs-lookup"><span data-stu-id="f439f-127">Part 4: Draw Text Using the Direct2D DrawTextLayout Method.</span></span>](#part-4-draw-text-using-the-direct2d-drawtextlayout-method)

## <a name="source-code"></a><span data-ttu-id="f439f-128">Codice sorgente</span><span class="sxs-lookup"><span data-stu-id="f439f-128">Source Code</span></span>

<span data-ttu-id="f439f-129">Il codice sorgente illustrato in questa panoramica viene tratto dall' [esempio di Hello World DirectWrite](/samples/browse/?redirectedfrom=MSDN-samples).</span><span class="sxs-lookup"><span data-stu-id="f439f-129">The source code shown in this overview is taken from the [DirectWrite Hello World sample](/samples/browse/?redirectedfrom=MSDN-samples).</span></span> <span data-ttu-id="f439f-130">Ogni parte è implementata in una classe separata (SimpleText e multiformattedtext) e viene visualizzata in una finestra figlio separata.</span><span class="sxs-lookup"><span data-stu-id="f439f-130">Each part is implemented in a separate class (SimpleText and MultiformattedText) and is displayed in a separate child window.</span></span> <span data-ttu-id="f439f-131">Ogni classe rappresenta una finestra di Microsoft Win32.</span><span class="sxs-lookup"><span data-stu-id="f439f-131">Each class represents a Microsoft Win32 window.</span></span> <span data-ttu-id="f439f-132">Oltre al metodo *WndProc* , ogni classe contiene i metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="f439f-132">In addition to the *WndProc* method, each class contains the following methods:</span></span>



| <span data-ttu-id="f439f-133">Funzione</span><span class="sxs-lookup"><span data-stu-id="f439f-133">Function</span></span>                              | <span data-ttu-id="f439f-134">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f439f-134">Description</span></span>                                                                                         |
|---------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f439f-135">**CreateDeviceIndependentResources**</span><span class="sxs-lookup"><span data-stu-id="f439f-135">**CreateDeviceIndependentResources**</span></span>  | <span data-ttu-id="f439f-136">Crea risorse indipendenti dal dispositivo, in modo che possano essere riutilizzate ovunque.</span><span class="sxs-lookup"><span data-stu-id="f439f-136">Creates resources that are device independent, so they can be reused anywhere.</span></span>                      |
| <span data-ttu-id="f439f-137">**DiscardDeviceIndependentResources**</span><span class="sxs-lookup"><span data-stu-id="f439f-137">**DiscardDeviceIndependentResources**</span></span> | <span data-ttu-id="f439f-138">Rilascia le risorse indipendenti dal dispositivo dopo che non sono più necessarie.</span><span class="sxs-lookup"><span data-stu-id="f439f-138">Releases the device-independent resources after they are no longer needed.</span></span>                          |
| <span data-ttu-id="f439f-139">**CreateDeviceResources**</span><span class="sxs-lookup"><span data-stu-id="f439f-139">**CreateDeviceResources**</span></span>             | <span data-ttu-id="f439f-140">Crea risorse, ad esempio pennelli e destinazioni di rendering, associate a un determinato dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f439f-140">Creates resources, such as brushes and render targets, that are tied to a particular device.</span></span>        |
| <span data-ttu-id="f439f-141">**DiscardDeviceResources**</span><span class="sxs-lookup"><span data-stu-id="f439f-141">**DiscardDeviceResources**</span></span>            | <span data-ttu-id="f439f-142">Rilascia le risorse dipendenti dal dispositivo dopo che non sono più necessarie.</span><span class="sxs-lookup"><span data-stu-id="f439f-142">Releases the device-dependent resources after they are no longer needed.</span></span>                            |
| <span data-ttu-id="f439f-143">**DrawD2DContent**</span><span class="sxs-lookup"><span data-stu-id="f439f-143">**DrawD2DContent**</span></span>                    | <span data-ttu-id="f439f-144">USA [Direct2D](../direct2d/direct2d-portal.md) per eseguire il rendering sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="f439f-144">Uses [Direct2D](../direct2d/direct2d-portal.md) to render to the screen.</span></span>                              |
| <span data-ttu-id="f439f-145">**DrawText**</span><span class="sxs-lookup"><span data-stu-id="f439f-145">**DrawText**</span></span>                          | <span data-ttu-id="f439f-146">Disegna la stringa di testo tramite [Direct2D](../direct2d/direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="f439f-146">Draws the text string by using [Direct2D](../direct2d/direct2d-portal.md).</span></span>                            |
| <span data-ttu-id="f439f-147">**OnResize**</span><span class="sxs-lookup"><span data-stu-id="f439f-147">**OnResize**</span></span>                          | <span data-ttu-id="f439f-148">Ridimensiona la destinazione di rendering [Direct2D](../direct2d/direct2d-portal.md) quando la dimensione della finestra viene modificata.</span><span class="sxs-lookup"><span data-stu-id="f439f-148">Resizes the [Direct2D](../direct2d/direct2d-portal.md) render target when the window size is changed.</span></span> |



 

<span data-ttu-id="f439f-149">È possibile utilizzare l'esempio fornito oppure utilizzare le istruzioni seguenti per aggiungere [DirectWrite](direct-write-portal.md) e [Direct2D](rendering-by-using-direct2d.md) alla propria applicazione Win32.</span><span class="sxs-lookup"><span data-stu-id="f439f-149">You can use the sample provided, or use the instructions that follow to add [DirectWrite](direct-write-portal.md) and [Direct2D](rendering-by-using-direct2d.md) to your own Win32 application.</span></span> <span data-ttu-id="f439f-150">Per ulteriori informazioni sull'esempio e sui file di progetto associati, vedere l' [esempio DirectWriteHelloWorld](/samples/browse/?redirectedfrom=MSDN-samples).</span><span class="sxs-lookup"><span data-stu-id="f439f-150">For more information about the sample and the associated project files, see the [DirectWriteHelloWorld sample](/samples/browse/?redirectedfrom=MSDN-samples).</span></span>

## <a name="drawing-simple-text"></a><span data-ttu-id="f439f-151">Disegno di testo semplice</span><span class="sxs-lookup"><span data-stu-id="f439f-151">Drawing Simple Text</span></span>

<span data-ttu-id="f439f-152">Questa sezione illustra come usare [DirectWrite](direct-write-portal.md) e [Direct2D](../direct2d/direct2d-portal.md) per eseguire il rendering di un testo semplice con un solo formato, come illustrato nella schermata seguente.</span><span class="sxs-lookup"><span data-stu-id="f439f-152">This section shows how to use [DirectWrite](direct-write-portal.md) and [Direct2D](../direct2d/direct2d-portal.md) to render simple text that has a single format, as shown in the following screen shot.</span></span>

![Screenshot di "Hello World using DirectWrite!"](images/simplecropped.png)

<span data-ttu-id="f439f-155">Il disegno di testo semplice sullo schermo richiede quattro componenti:</span><span class="sxs-lookup"><span data-stu-id="f439f-155">Drawing simple text to the screen requires four components:</span></span>

-   <span data-ttu-id="f439f-156">Stringa di caratteri di cui eseguire il rendering.</span><span class="sxs-lookup"><span data-stu-id="f439f-156">A character string to render.</span></span>
-   <span data-ttu-id="f439f-157">Istanza di [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat).</span><span class="sxs-lookup"><span data-stu-id="f439f-157">An instance of [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat).</span></span>
-   <span data-ttu-id="f439f-158">Dimensioni dell'area in cui includere il testo.</span><span class="sxs-lookup"><span data-stu-id="f439f-158">The dimensions of the area to contain the text.</span></span>
-   <span data-ttu-id="f439f-159">Oggetto in grado di eseguire il rendering del testo.</span><span class="sxs-lookup"><span data-stu-id="f439f-159">An object that can render the text.</span></span> <span data-ttu-id="f439f-160">In questa esercitazione.</span><span class="sxs-lookup"><span data-stu-id="f439f-160">In this tutorial.</span></span> <span data-ttu-id="f439f-161">si usa una destinazione di rendering [Direct2D](../direct2d/direct2d-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="f439f-161">you use a [Direct2D](../direct2d/direct2d-portal.md) render target.</span></span>

<span data-ttu-id="f439f-162">L'interfaccia [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) descrive il nome della famiglia di caratteri, le dimensioni, il peso, lo stile e l'estensione usati per formattare il testo e descrive le informazioni sulle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="f439f-162">The [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface describes the font-family name, size, weight, style, and stretch used to format text, and it describes locale information.</span></span> <span data-ttu-id="f439f-163">**IDWriteTextFormat** definisce inoltre i metodi per l'impostazione e il recupero delle proprietà seguenti:</span><span class="sxs-lookup"><span data-stu-id="f439f-163">**IDWriteTextFormat** also defines methods for setting and getting the following properties:</span></span>

-   <span data-ttu-id="f439f-164">Interlinea.</span><span class="sxs-lookup"><span data-stu-id="f439f-164">The line spacing.</span></span>
-   <span data-ttu-id="f439f-165">Allineamento del testo relativo ai bordi sinistro e destro della casella di layout.</span><span class="sxs-lookup"><span data-stu-id="f439f-165">The text alignment relative to the left and right edges of the layout box.</span></span>
-   <span data-ttu-id="f439f-166">Allineamento del paragrafo rispetto alla parte superiore e inferiore della casella di layout.</span><span class="sxs-lookup"><span data-stu-id="f439f-166">The paragraph alignment relative to the top and bottom of the layout box.</span></span>
-   <span data-ttu-id="f439f-167">Direzione di lettura.</span><span class="sxs-lookup"><span data-stu-id="f439f-167">The reading direction.</span></span>
-   <span data-ttu-id="f439f-168">Granularità del testo che ha causato l'overflow della casella di layout.</span><span class="sxs-lookup"><span data-stu-id="f439f-168">The text trimming granularity for text that overflows the layout box.</span></span>
-   <span data-ttu-id="f439f-169">L'arresto della tabulazione incrementale.</span><span class="sxs-lookup"><span data-stu-id="f439f-169">The incremental tab stop.</span></span>
-   <span data-ttu-id="f439f-170">Direzione del flusso di paragrafo.</span><span class="sxs-lookup"><span data-stu-id="f439f-170">The paragraph flow direction.</span></span>

<span data-ttu-id="f439f-171">L'interfaccia [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) è necessaria per il disegno di testo che usa entrambi i processi descritti in questo documento.</span><span class="sxs-lookup"><span data-stu-id="f439f-171">The [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface is required for drawing text that uses both of the processes described in this document .</span></span>

<span data-ttu-id="f439f-172">Prima di poter creare un oggetto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) o qualsiasi altro oggetto [DirectWrite](direct-write-portal.md) , è necessaria un'istanza di [**IDWriteFactory archiviata nei**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) .</span><span class="sxs-lookup"><span data-stu-id="f439f-172">Before you can create an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object, or any other [DirectWrite](direct-write-portal.md) object, you need an [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) instance.</span></span> <span data-ttu-id="f439f-173">Usare un **IDWriteFactory archiviata nei** per creare istanze di **IDWriteTextFormat** e altri oggetti DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="f439f-173">You use an **IDWriteFactory** to create **IDWriteTextFormat** instances and other DirectWrite objects.</span></span> <span data-ttu-id="f439f-174">Per ottenere un'istanza di Factory, usare la funzione [**DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) .</span><span class="sxs-lookup"><span data-stu-id="f439f-174">To obtain a factory instance, use the [**DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) function.</span></span>

### <a name="part-1-declare-directwrite-and-direct2d-resources"></a><span data-ttu-id="f439f-175">Parte 1: dichiarare le risorse DirectWrite e Direct2D.</span><span class="sxs-lookup"><span data-stu-id="f439f-175">Part 1: Declare DirectWrite and Direct2D Resources.</span></span>

<span data-ttu-id="f439f-176">In questa parte, si dichiarano gli oggetti che verranno usati in un secondo momento per la creazione e la visualizzazione di testo come membri dati privati della classe.</span><span class="sxs-lookup"><span data-stu-id="f439f-176">In this part, you declare the objects that you will use later for creating and displaying text as private data members of your class.</span></span> <span data-ttu-id="f439f-177">Tutte le interfacce, le funzioni e i tipi di DataType per [DirectWrite](direct-write-portal.md) sono dichiarati nel file di intestazione *DWrite. h* e quelli per [Direct2D](../direct2d/direct2d-portal.md) sono dichiarati in *d2d1. h*; Se questa operazione non è già stata eseguita, includere le intestazioni nel progetto.</span><span class="sxs-lookup"><span data-stu-id="f439f-177">All of the interfaces, functions, and datatypes for [DirectWrite](direct-write-portal.md) are declared in the *dwrite.h* header file, and those for [Direct2D](../direct2d/direct2d-portal.md) are declared in the *d2d1.h*; if you haven't already done this, include these headers in your project.</span></span>

1.  <span data-ttu-id="f439f-178">Nel file di intestazione della classe (SimpleText. h) dichiarare i puntatori alle interfacce [**IDWriteFactory archiviata nei**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) e [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) come membri privati.</span><span class="sxs-lookup"><span data-stu-id="f439f-178">In your class header file (SimpleText.h), declare pointers to [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) and [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interfaces as private members.</span></span>
    ```C++
    IDWriteFactory* pDWriteFactory_;
    IDWriteTextFormat* pTextFormat_;
    
    ```

    

2.  <span data-ttu-id="f439f-179">Dichiarare i membri che contengono la stringa di testo di cui eseguire il rendering e la lunghezza della stringa.</span><span class="sxs-lookup"><span data-stu-id="f439f-179">Declare members to hold the text string to render and the length of the string.</span></span>
    ```C++
    const wchar_t* wszText_;
    UINT32 cTextLength_;
    
    ```

    

3.  <span data-ttu-id="f439f-180">Dichiarare i puntatori alle interfacce [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)e [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) per il rendering del testo con [Direct2D](../direct2d/direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="f439f-180">Declare pointers to [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget), and [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) interfaces for rendering the text with [Direct2D](../direct2d/direct2d-portal.md).</span></span>
    ```C++
    ID2D1Factory* pD2DFactory_;
    ID2D1HwndRenderTarget* pRT_;
    ID2D1SolidColorBrush* pBlackBrush_;
    
    ```

    

### <a name="part-2-create-device-independent-resources"></a><span data-ttu-id="f439f-181">Parte 2: creare risorse indipendenti dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f439f-181">Part 2: Create Device Independent Resources.</span></span>

<span data-ttu-id="f439f-182">[Direct2D](rendering-by-using-direct2d.md) fornisce due tipi di risorse: risorse dipendenti dal dispositivo e risorse indipendenti dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f439f-182">[Direct2D](rendering-by-using-direct2d.md) provides two types of resources: device-dependent resources and device-independent resources.</span></span> <span data-ttu-id="f439f-183">Le risorse dipendenti dal dispositivo sono associate a un dispositivo di rendering e non funzionano più se il dispositivo è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="f439f-183">Device-dependent resources are associated with a rendering device and no longer function if that device is removed.</span></span> <span data-ttu-id="f439f-184">Le risorse indipendenti dal dispositivo, d'altra parte, possono durare per l'ambito dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f439f-184">Device-independent resources, on the other hand, can last for the scope of your application.</span></span>

<span data-ttu-id="f439f-185">Le risorse di [DirectWrite](direct-write-portal.md) sono indipendenti dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f439f-185">[DirectWrite](direct-write-portal.md) resources are device-independent.</span></span>

<span data-ttu-id="f439f-186">In questa sezione vengono create le risorse indipendenti dal dispositivo utilizzate dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f439f-186">In this section, you create the device-independent resources that are used by your application.</span></span> <span data-ttu-id="f439f-187">Queste risorse devono essere liberate con una chiamata al metodo di **rilascio** dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="f439f-187">These resources must be freed with a call to the **Release** method of the interface.</span></span>

<span data-ttu-id="f439f-188">Alcune risorse utilizzate devono essere create solo una volta e non sono associate a un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f439f-188">Some of the resources that are used have to be created only one time and are not tied to a device.</span></span> <span data-ttu-id="f439f-189">L'inizializzazione per queste risorse viene inserita nel metodo *SimpleText:: CreateDeviceIndependentResources* , che viene chiamato durante l'inizializzazione della classe.</span><span class="sxs-lookup"><span data-stu-id="f439f-189">The initialization for these resources is put in the *SimpleText::CreateDeviceIndependentResources* method, which is called when initializing the class.</span></span>

1.  <span data-ttu-id="f439f-190">All'interno del metodo *SimpleText:: CreateDeviceIndependentResources* nel file di implementazione della classe (SimpleText. cpp), chiamare la funzione [**D2D1CreateFactory**](/windows/win32/api/d2d1/nf-d2d1-d2d1createfactory) per creare un'interfaccia [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) , ovvero l'interfaccia Factory radice per tutti gli oggetti [Direct2D](../direct2d/direct2d-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="f439f-190">Inside the *SimpleText::CreateDeviceIndependentResources* method in the class implementation file (SimpleText.cpp), call the [**D2D1CreateFactory**](/windows/win32/api/d2d1/nf-d2d1-d2d1createfactory) function to create an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) interface, which is the root factory interface for all [Direct2D](../direct2d/direct2d-portal.md) objects.</span></span> <span data-ttu-id="f439f-191">Si usa la stessa factory per creare un'istanza di altre risorse Direct2D.</span><span class="sxs-lookup"><span data-stu-id="f439f-191">You use the same factory to instantiate other Direct2D resources.</span></span>
    ```C++
    hr = D2D1CreateFactory(
        D2D1_FACTORY_TYPE_SINGLE_THREADED,
        &pD2DFactory_
        );
    
    ```

    

2.  <span data-ttu-id="f439f-192">Chiamare la funzione [**DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) per creare un'interfaccia [**IDWriteFactory archiviata nei**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) , che è l'interfaccia Factory radice per tutti gli oggetti [DirectWrite](direct-write-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="f439f-192">Call the [**DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) function to create an [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) interface, which is the root factory interface for all [DirectWrite](direct-write-portal.md) objects.</span></span> <span data-ttu-id="f439f-193">Si usa la stessa factory per creare un'istanza di altre risorse di DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="f439f-193">You use the same factory to instantiate other DirectWrite resources.</span></span>
    ```C++
    if (SUCCEEDED(hr))
    {
        hr = DWriteCreateFactory(
            DWRITE_FACTORY_TYPE_SHARED,
            __uuidof(IDWriteFactory),
            reinterpret_cast<IUnknown**>(&pDWriteFactory_)
            );
    }
    
    ```

    

3.  <span data-ttu-id="f439f-194">Inizializzare la stringa di testo e archiviarne la lunghezza.</span><span class="sxs-lookup"><span data-stu-id="f439f-194">Initialize the text string and store its length.</span></span>

    ```C++
    wszText_ = L"Hello World using  DirectWrite!";
    cTextLength_ = (UINT32) wcslen(wszText_);
    
    ```

    

4.  <span data-ttu-id="f439f-195">Creare un oggetto interfaccia [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) usando il metodo [**IDWriteFactory archiviata nei:: CreateTextFormat**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat) .</span><span class="sxs-lookup"><span data-stu-id="f439f-195">Create an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface object by using the [**IDWriteFactory::CreateTextFormat**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat) method.</span></span> <span data-ttu-id="f439f-196">**IDWriteTextFormat** specifica il tipo di carattere, il peso, l'estensione, lo stile e le impostazioni locali che verranno utilizzati per eseguire il rendering della stringa di testo.</span><span class="sxs-lookup"><span data-stu-id="f439f-196">The **IDWriteTextFormat** specifies the font, weight, stretch, style, and locale that will be used to render the text string.</span></span>
    ```C++
    if (SUCCEEDED(hr))
    {
        hr = pDWriteFactory_->CreateTextFormat(
            L"Gabriola",                // Font family name.
            NULL,                       // Font collection (NULL sets it to use the system font collection).
            DWRITE_FONT_WEIGHT_REGULAR,
            DWRITE_FONT_STYLE_NORMAL,
            DWRITE_FONT_STRETCH_NORMAL,
            72.0f,
            L"en-us",
            &pTextFormat_
            );
    }
    
    ```

    

5.  <span data-ttu-id="f439f-197">Centrare il testo orizzontalmente e verticalmente chiamando i metodi [**IDWriteTextFormat:: SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) e [**IDWriteTextFormat:: SetParagraphAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setparagraphalignment) .</span><span class="sxs-lookup"><span data-stu-id="f439f-197">Center the text horizontally and vertically by calling the [**IDWriteTextFormat::SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) and [**IDWriteTextFormat::SetParagraphAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setparagraphalignment) methods.</span></span>
    ```C++
    // Center align (horizontally) the text.
    if (SUCCEEDED(hr))
    {
        hr = pTextFormat_->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);
    }

    if (SUCCEEDED(hr))
    {
        hr = pTextFormat_->SetParagraphAlignment(DWRITE_PARAGRAPH_ALIGNMENT_CENTER);
    }
    
    ```

    

<span data-ttu-id="f439f-198">In questa parte sono state inizializzate le risorse indipendenti dal dispositivo utilizzate dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f439f-198">In this part, you initialized the device-independent resources that are used by your application.</span></span> <span data-ttu-id="f439f-199">Nella parte successiva si inizializzano le risorse dipendenti dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f439f-199">In the next part, you initialize the device-dependent resources.</span></span>

### <a name="part-3-create-device-dependent-resources"></a><span data-ttu-id="f439f-200">Parte 3: creare Device-Dependent risorse.</span><span class="sxs-lookup"><span data-stu-id="f439f-200">Part 3: Create Device-Dependent Resources.</span></span>

<span data-ttu-id="f439f-201">In questa parte viene creato un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) e un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) per il rendering del testo.</span><span class="sxs-lookup"><span data-stu-id="f439f-201">In this part, you create an [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) and an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) for rendering your text.</span></span>

<span data-ttu-id="f439f-202">Una destinazione di rendering è un oggetto Direct2D che consente di creare risorse di disegno ed eseguire il rendering dei comandi di disegno in un dispositivo di rendering.</span><span class="sxs-lookup"><span data-stu-id="f439f-202">A render target is a Direct2D object that creates drawing resources and renders drawing commands to a rendering device.</span></span> <span data-ttu-id="f439f-203">Un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) è una destinazione di rendering che esegue il rendering in un **HWND**.</span><span class="sxs-lookup"><span data-stu-id="f439f-203">An [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) is a render target that renders to an **HWND**.</span></span>

<span data-ttu-id="f439f-204">Una delle risorse di disegno che una destinazione di rendering può creare è un pennello per disegnare strutture, riempimenti e testo.</span><span class="sxs-lookup"><span data-stu-id="f439f-204">One of the drawing resources that a render target can create is a brush for painting outlines, fills, and text.</span></span> <span data-ttu-id="f439f-205">Un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) disegna con un colore a tinta unita.</span><span class="sxs-lookup"><span data-stu-id="f439f-205">An [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) paints with a solid color.</span></span>

<span data-ttu-id="f439f-206">Entrambe le interfacce [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) e [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) sono associate a un dispositivo di rendering quando vengono create e devono essere rilasciate e ricreate se il dispositivo diventa non valido.</span><span class="sxs-lookup"><span data-stu-id="f439f-206">Both the [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) and the [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) interfaces are bound to a rendering device when they are created and must be released and recreated if the device becomes invalid.</span></span>

1.  <span data-ttu-id="f439f-207">All'interno del metodo SimpleText:: CreateDeviceResources controllare se il puntatore della destinazione di rendering è **null**.</span><span class="sxs-lookup"><span data-stu-id="f439f-207">Inside the SimpleText::CreateDeviceResources method, check whether the render target pointer is **NULL**.</span></span> <span data-ttu-id="f439f-208">In caso contrario, recuperare le dimensioni dell'area di rendering e creare un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) di tale dimensione.</span><span class="sxs-lookup"><span data-stu-id="f439f-208">If it is, retrieve the size of the render area and create an [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) of that size.</span></span> <span data-ttu-id="f439f-209">Usare **ID2D1HwndRenderTarget** per creare un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).</span><span class="sxs-lookup"><span data-stu-id="f439f-209">Use the **ID2D1HwndRenderTarget** to create an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).</span></span>
    ```C++
    RECT rc;
    GetClientRect(hwnd_, &rc);

    D2D1_SIZE_U size = D2D1::SizeU(rc.right - rc.left, rc.bottom - rc.top);

    if (!pRT_)
    {
        // Create a Direct2D render target.
        hr = pD2DFactory_->CreateHwndRenderTarget(
                D2D1::RenderTargetProperties(),
                D2D1::HwndRenderTargetProperties(
                    hwnd_,
                    size
                    ),
                &pRT_
                );

        // Create a black brush.
        if (SUCCEEDED(hr))
        {
            hr = pRT_->CreateSolidColorBrush(
                D2D1::ColorF(D2D1::ColorF::Black),
                &pBlackBrush_
                );
        }
    }
    
    ```

    

2.  <span data-ttu-id="f439f-210">Nel metodo SimpleText::D iscardDeviceResources, rilasciare sia il pennello che la destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="f439f-210">In the SimpleText::DiscardDeviceResources method, release both the brush and render target.</span></span>
    ```C++
    SafeRelease(&pRT_);
    SafeRelease(&pBlackBrush_);
    
    ```

    

<span data-ttu-id="f439f-211">Ora che è stata creata una destinazione di rendering e un pennello, è possibile usarli per eseguire il rendering del testo.</span><span class="sxs-lookup"><span data-stu-id="f439f-211">Now that you have created a render target and a brush, you can use them to render your text.</span></span>

### <a name="part-4-draw-text-by-using-the-direct2d-drawtext-method"></a><span data-ttu-id="f439f-212">Parte 4: creare il testo usando il metodo DrawText Direct2D.</span><span class="sxs-lookup"><span data-stu-id="f439f-212">Part 4: Draw Text By Using the Direct2D DrawText Method.</span></span>

1.  <span data-ttu-id="f439f-213">Nel metodo SimpleText::D rawText della classe definire l'area per il layout del testo recuperando le dimensioni dell'area di rendering e creando un rettangolo [Direct2D](../direct2d/direct2d-portal.md) con le stesse dimensioni.</span><span class="sxs-lookup"><span data-stu-id="f439f-213">In the SimpleText::DrawText method of your class, define the area for the text layout by retrieving the dimensions of the rendering area, and create a [Direct2D](../direct2d/direct2d-portal.md) rectangle that has the same dimensions.</span></span>
    ```C++
    D2D1_RECT_F layoutRect = D2D1::RectF(
        static_cast<FLOAT>(rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.top) / dpiScaleY_,
        static_cast<FLOAT>(rc.right - rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.bottom - rc.top) / dpiScaleY_
        );
    
    ```

    

2.  <span data-ttu-id="f439f-214">Usare il metodo [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) e l'oggetto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) per eseguire il rendering del testo sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="f439f-214">Use the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method and the [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object to render text to the screen.</span></span> <span data-ttu-id="f439f-215">Il metodo **ID2D1RenderTarget::D rawtext** accetta i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="f439f-215">The **ID2D1RenderTarget::DrawText** method takes the following parameters:</span></span>
    -   <span data-ttu-id="f439f-216">Stringa di cui eseguire il rendering.</span><span class="sxs-lookup"><span data-stu-id="f439f-216">A string to render.</span></span>
    -   <span data-ttu-id="f439f-217">Puntatore a un'interfaccia [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) .</span><span class="sxs-lookup"><span data-stu-id="f439f-217">A pointer to an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface.</span></span>
    -   <span data-ttu-id="f439f-218">Rettangolo di layout [Direct2D](../direct2d/direct2d-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="f439f-218">A [Direct2D](../direct2d/direct2d-portal.md) layout rectangle.</span></span>
    -   <span data-ttu-id="f439f-219">Puntatore a un'interfaccia che espone [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush).</span><span class="sxs-lookup"><span data-stu-id="f439f-219">A pointer to an interface that exposes [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush).</span></span>

    ```C++
    pRT_->DrawText(
        wszText_,        // The string to render.
        cTextLength_,    // The string's length.
        pTextFormat_,    // The text format.
        layoutRect,       // The region of the window where the text will be rendered.
        pBlackBrush_     // The brush used to draw the text.
        );
    
    ```

    

### <a name="part-5-render-the-window-contents-using-direct2d"></a><span data-ttu-id="f439f-220">Parte 5: rendering del contenuto della finestra tramite Direct2D</span><span class="sxs-lookup"><span data-stu-id="f439f-220">Part 5: Render the Window Contents Using Direct2D</span></span>

<span data-ttu-id="f439f-221">Per eseguire il rendering del contenuto della finestra tramite [Direct2D](../direct2d/direct2d-portal.md) quando viene ricevuto un messaggio di disegno, procedere come segue:</span><span class="sxs-lookup"><span data-stu-id="f439f-221">To render the contents of the window by using [Direct2D](../direct2d/direct2d-portal.md) when a paint message is received, do the following:</span></span>

1.  <span data-ttu-id="f439f-222">Creare le risorse dipendenti dal dispositivo chiamando il metodo SimpleText:: CreateDeviceResources implementato nella parte 3.</span><span class="sxs-lookup"><span data-stu-id="f439f-222">Create the device dependent resources by calling the SimpleText::CreateDeviceResources method implemented in Part 3.</span></span>
2.  <span data-ttu-id="f439f-223">Chiamare il metodo [**ID2D1HwndRenderTarget:: BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) della destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="f439f-223">Call the [**ID2D1HwndRenderTarget::BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method of the render target.</span></span>
3.  <span data-ttu-id="f439f-224">Cancellare la destinazione di rendering chiamando il metodo [**ID2D1HwndRenderTarget:: Clear**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f)) .</span><span class="sxs-lookup"><span data-stu-id="f439f-224">Clear the render target by calling the [**ID2D1HwndRenderTarget::Clear**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f)) method.</span></span>
4.  <span data-ttu-id="f439f-225">Chiamare il metodo SimpleText::D rawText, implementato nella parte 4.</span><span class="sxs-lookup"><span data-stu-id="f439f-225">Call the SimpleText::DrawText method, implemented in Part 4.</span></span>
5.  <span data-ttu-id="f439f-226">Chiamare il metodo [**ID2D1HwndRenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) della destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="f439f-226">Call the [**ID2D1HwndRenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method of the render target.</span></span>
6.  <span data-ttu-id="f439f-227">Se necessario, rimuovere le risorse dipendenti dal dispositivo in modo che possano essere ricreate quando la finestra viene ridisegnato.</span><span class="sxs-lookup"><span data-stu-id="f439f-227">If it is necessary, discard the device-dependent resources so that they can be recreated when the window is redrawn.</span></span>


```C++
hr = CreateDeviceResources();

if (SUCCEEDED(hr))
{
    pRT_->BeginDraw();

    pRT_->SetTransform(D2D1::IdentityMatrix());

    pRT_->Clear(D2D1::ColorF(D2D1::ColorF::White));

    // Call the DrawText method of this class.
    hr = DrawText();

    if (SUCCEEDED(hr))
    {
        hr = pRT_->EndDraw(
            );
    }
}

if (FAILED(hr))
{
    DiscardDeviceResources();
}

```



<span data-ttu-id="f439f-228">La classe SimpleText è implementata in SimpleText. h e SimpleText. cpp.</span><span class="sxs-lookup"><span data-stu-id="f439f-228">The SimpleText class is implemented in SimpleText.h and SimpleText.cpp.</span></span>

## <a name="drawing-text-with-multiple-formats"></a><span data-ttu-id="f439f-229">Disegno di testo con più formati.</span><span class="sxs-lookup"><span data-stu-id="f439f-229">Drawing Text with Multiple Formats.</span></span>

<span data-ttu-id="f439f-230">Questa sezione illustra come usare [DirectWrite](direct-write-portal.md) e [Direct2D](../direct2d/direct2d-portal.md) per eseguire il rendering del testo con più formati, come illustrato nella schermata seguente.</span><span class="sxs-lookup"><span data-stu-id="f439f-230">This section shows how to use [DirectWrite](direct-write-portal.md) and [Direct2D](../direct2d/direct2d-portal.md) to render text with multiple formats, as shown in the following screen shot.</span></span>

![Screenshot di "Hello World using DirectWrite!", con alcune parti di stili, dimensioni e formati diversi](images/multiformattedcropped.png)

<span data-ttu-id="f439f-232">Il codice per questa sezione viene implementato come classe multiformattedtext nell' [esempio DWriteHelloWorld](/samples/browse/?redirectedfrom=MSDN-samples).</span><span class="sxs-lookup"><span data-stu-id="f439f-232">The code for this section is implemented as the MultiformattedText class in the [DWriteHelloWorld Sample](/samples/browse/?redirectedfrom=MSDN-samples).</span></span> <span data-ttu-id="f439f-233">Si basa sui passaggi della sezione precedente.</span><span class="sxs-lookup"><span data-stu-id="f439f-233">It is based on the steps from the previous section.</span></span>

<span data-ttu-id="f439f-234">Per creare testo multiformattato, è possibile usare l'interfaccia [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , oltre all'interfaccia [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) introdotta nella sezione precedente.</span><span class="sxs-lookup"><span data-stu-id="f439f-234">To create multi-formatted text, you use the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface in addition to the [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface introduced in the previous section.</span></span> <span data-ttu-id="f439f-235">L'interfaccia **IDWriteTextLayout** descrive la formattazione e il layout di un blocco di testo.</span><span class="sxs-lookup"><span data-stu-id="f439f-235">The **IDWriteTextLayout** interface describes the formatting and layout of a block of text.</span></span> <span data-ttu-id="f439f-236">Oltre alla formattazione predefinita specificata da un oggetto **IDWriteTextFormat** , è possibile modificare la formattazione di intervalli di testo specifici utilizzando **IDWriteTextLayout**.</span><span class="sxs-lookup"><span data-stu-id="f439f-236">In addition to default formatting specified by an **IDWriteTextFormat** object, the formatting for specific ranges of text can be changed by using **IDWriteTextLayout**.</span></span> <span data-ttu-id="f439f-237">Sono inclusi il nome della famiglia di caratteri, le dimensioni, il peso, lo stile, l'estensione, la barratura e la sottostruttura.</span><span class="sxs-lookup"><span data-stu-id="f439f-237">This includes font family name, size, weight, style, stretch, strikethrough, and underlining.</span></span>

<span data-ttu-id="f439f-238">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) fornisce anche metodi di hit testing.</span><span class="sxs-lookup"><span data-stu-id="f439f-238">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) also provides hit-testing methods.</span></span> <span data-ttu-id="f439f-239">Le metriche di hit testing restituite da questi metodi sono relative alla casella di layout specificata quando l'oggetto interfaccia **IDWriteTextLayout** viene creato tramite il metodo [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) dell'interfaccia [**IDWriteFactory archiviata nei**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) .</span><span class="sxs-lookup"><span data-stu-id="f439f-239">The hit-testing metrics returned by these methods are relative to the layout box specified when the **IDWriteTextLayout** interface object is created by using the [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) method of the [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) interface.</span></span>

<span data-ttu-id="f439f-240">L'interfaccia [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) viene utilizzata per aggiungere funzionalità tipografiche [OpenType](../intl/opentype-font-format.md) facoltative a un layout di testo, ad esempio ornati e set di testo stilistici alternativi.</span><span class="sxs-lookup"><span data-stu-id="f439f-240">The [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) interface is used to add optional [OpenType](../intl/opentype-font-format.md) typographic features to a text layout, such as swashes and alternative stylistic text sets.</span></span> <span data-ttu-id="f439f-241">Le funzionalità tipografiche possono essere aggiunte a un intervallo di testo specifico all'interno di un layout di testo chiamando il metodo [**AddFontFeature**](/windows/win32/api/dwrite/nf-dwrite-idwritetypography-addfontfeature) dell'interfaccia **IDWriteTypography** .</span><span class="sxs-lookup"><span data-stu-id="f439f-241">Typographic features can be added to a specific range of text within a text layout by calling the [**AddFontFeature**](/windows/win32/api/dwrite/nf-dwrite-idwritetypography-addfontfeature) method of the **IDWriteTypography** interface.</span></span> <span data-ttu-id="f439f-242">Questo metodo riceve una struttura della [**\_ \_ funzionalità del tipo di carattere DWrite**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_feature_tag) come parametro che contiene una costante di enumerazione dei tag della **funzionalità del tipo di \_ carattere \_ \_ DWrite** e un parametro di esecuzione **UInt32** .</span><span class="sxs-lookup"><span data-stu-id="f439f-242">This method receives a [**DWRITE\_FONT\_FEATURE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_feature_tag) structure as a parameter that contains a **DWRITE\_FONT\_FEATURE\_TAG** enumeration constant and a **UINT32** execution parameter.</span></span> <span data-ttu-id="f439f-243">Un elenco di funzionalità OpenType registrate è reperibile nel [Registro di sistema dei tag di layout OpenType](https://www.microsoft.com/typography/otspec/features_ae.htm) in Microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="f439f-243">A list of registered OpenType features can be found at the [OpenType Layout Tag Registry](https://www.microsoft.com/typography/otspec/features_ae.htm) on microsoft.com.</span></span> <span data-ttu-id="f439f-244">Per le costanti di enumerazione DirectWrite equivalenti, **vedere \_ \_ \_ tag della funzionalità del tipo di carattere DWrite**.</span><span class="sxs-lookup"><span data-stu-id="f439f-244">For the equivalent DirectWrite enumeration constants, see **DWRITE\_FONT\_FEATURE\_TAG**.</span></span>

### <a name="part-1-create-an-idwritetextlayout-interface"></a><span data-ttu-id="f439f-245">Parte 1: creare un'interfaccia IDWriteTextLayout.</span><span class="sxs-lookup"><span data-stu-id="f439f-245">Part 1: Create an IDWriteTextLayout Interface.</span></span>

1.  <span data-ttu-id="f439f-246">Dichiarare un puntatore a un'interfaccia [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) come membro della classe multiformattedtext.</span><span class="sxs-lookup"><span data-stu-id="f439f-246">Declare a pointer to an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface as a member of the MultiformattedText class.</span></span>
    ```C++
    IDWriteTextLayout* pTextLayout_;
    
    ```

    

2.  <span data-ttu-id="f439f-247">Alla fine del metodo multiformattedtext:: CreateDeviceIndependentResources, creare un oggetto interfaccia [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) chiamando il metodo [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) .</span><span class="sxs-lookup"><span data-stu-id="f439f-247">At the end of the MultiformattedText::CreateDeviceIndependentResources method, create an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface object by calling the [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) method.</span></span> <span data-ttu-id="f439f-248">L'interfaccia **IDWriteTextLayout** fornisce funzionalità di formattazione aggiuntive, ad esempio la possibilità di applicare formati diversi alle parti di testo selezionate.</span><span class="sxs-lookup"><span data-stu-id="f439f-248">The **IDWriteTextLayout** interface provides additional formatting features, such as the ability to apply different formats to selected portions of text.</span></span>
    ```C++
    // Create a text layout using the text format.
    if (SUCCEEDED(hr))
    {
        RECT rect;
        GetClientRect(hwnd_, &rect); 
        float width  = rect.right  / dpiScaleX_;
        float height = rect.bottom / dpiScaleY_;

        hr = pDWriteFactory_->CreateTextLayout(
            wszText_,      // The string to be laid out and formatted.
            cTextLength_,  // The length of the string.
            pTextFormat_,  // The text format to apply to the string (contains font information, etc).
            width,         // The width of the layout box.
            height,        // The height of the layout box.
            &pTextLayout_  // The IDWriteTextLayout interface pointer.
            );
    }
    
    ```

    

### <a name="part-2-applying-formatting-with-idwritetextlayout"></a><span data-ttu-id="f439f-249">Parte 2: applicazione della formattazione con IDWriteTextLayout.</span><span class="sxs-lookup"><span data-stu-id="f439f-249">Part 2: Applying Formatting with IDWriteTextLayout.</span></span>

<span data-ttu-id="f439f-250">La formattazione, ad esempio la dimensione del carattere, il peso e la sottostruttura, può essere applicata a sottostringhe del testo da visualizzare mediante l'interfaccia [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="f439f-250">Formatting, such as the font size, weight, and underlining, can be applied to substrings of the text to be displayed by using the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface.</span></span>

1.  <span data-ttu-id="f439f-251">Impostare la dimensione del carattere per la sottostringa "di" di "DirectWrite" su 100 dichiarando un [**\_ \_ intervallo di testo DWrite**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) e chiamando il metodo [**IDWriteTextLayout:: sefontsize**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setfontsize) .</span><span class="sxs-lookup"><span data-stu-id="f439f-251">Set the font size for the substring "Di" of "DirectWrite" to 100 by declaring a [**DWRITE\_TEXT\_RANGE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) and calling the [**IDWriteTextLayout::SetFontSize**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setfontsize) method.</span></span>
    ```C++
    // Format the "DirectWrite" substring to be of font size 100.
    if (SUCCEEDED(hr))
    {
        DWRITE_TEXT_RANGE textRange = {20,        // Start index where "DirectWrite" appears.
                                        6 };      // Length of the substring "Direct" in "DirectWrite".
        hr = pTextLayout_->SetFontSize(100.0f, textRange);
    }
    ```

    

2.  <span data-ttu-id="f439f-252">Sottolineare la sottostringa "DirectWrite" chiamando il metodo [**IDWriteTextLayout::**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline) SetValue.</span><span class="sxs-lookup"><span data-stu-id="f439f-252">Underline the substring "DirectWrite" by calling the [**IDWriteTextLayout::SetUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline) method.</span></span>
    ```C++
    // Format the word "DWrite" to be underlined.
    if (SUCCEEDED(hr))
    {
        
        DWRITE_TEXT_RANGE textRange = {20,      // Start index where "DirectWrite" appears.
                                       11 };    // Length of the substring "DirectWrite".
        hr = pTextLayout_->SetUnderline(TRUE, textRange);
    }
    ```

    

3.  <span data-ttu-id="f439f-253">Impostare lo spessore del carattere su grassetto per la sottostringa "DirectWrite" chiamando il metodo [**IDWriteTextLayout:: FontWeight**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setfontweight) .</span><span class="sxs-lookup"><span data-stu-id="f439f-253">Set the font weight to bold for the substring "DirectWrite" by calling the [**IDWriteTextLayout::SetFontWeight**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setfontweight) method.</span></span>
    ```C++
    if (SUCCEEDED(hr))
    {
        // Format the word "DWrite" to be bold.
        DWRITE_TEXT_RANGE textRange = {20,
                                       11 };
        hr = pTextLayout_->SetFontWeight(DWRITE_FONT_WEIGHT_BOLD, textRange);
    }
    ```

    

### <a name="part-3-adding-typographic-features-with-idwritetypography"></a><span data-ttu-id="f439f-254">Parte 3: aggiunta di funzionalità tipografiche con IDWriteTypography.</span><span class="sxs-lookup"><span data-stu-id="f439f-254">Part 3: Adding Typographic Features with IDWriteTypography.</span></span>

1.  <span data-ttu-id="f439f-255">Dichiarare e creare un oggetto interfaccia [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) chiamando il metodo [**IDWriteFactory archiviata nei:: CreateTypography**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtypography) .</span><span class="sxs-lookup"><span data-stu-id="f439f-255">Declare and create an [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) interface object by calling the [**IDWriteFactory::CreateTypography**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtypography) method.</span></span>
    ```C++
    // Declare a typography pointer.
    IDWriteTypography* pTypography = NULL;

    // Create a typography interface object.
    if (SUCCEEDED(hr))
    {
        hr = pDWriteFactory_->CreateTypography(&pTypography);
    }
    
    ```

    

2.  <span data-ttu-id="f439f-256">Aggiungere una funzionalità del tipo di carattere dichiarando un oggetto della [**\_ \_ funzionalità del tipo di carattere DWrite**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_feature) con il set stilistico 7 specificato e chiamando il metodo [**IDWriteTypography:: AddFontFeature**](/windows/win32/api/dwrite/nf-dwrite-idwritetypography-addfontfeature) .</span><span class="sxs-lookup"><span data-stu-id="f439f-256">Add a font feature by declaring a [**DWRITE\_FONT\_FEATURE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_feature) object that has the stylistic set 7 specified and calling the [**IDWriteTypography::AddFontFeature**](/windows/win32/api/dwrite/nf-dwrite-idwritetypography-addfontfeature) method.</span></span>
    ```C++
    // Set the stylistic set.
    DWRITE_FONT_FEATURE fontFeature = {DWRITE_FONT_FEATURE_TAG_STYLISTIC_SET_7,
                                       1};
    if (SUCCEEDED(hr))
    {
        hr = pTypography->AddFontFeature(fontFeature);
    }
    
    ```

    

3.  <span data-ttu-id="f439f-257">Impostare il layout del testo in modo da usare la funzionalità Typography sull'intera stringa dichiarando una variabile di [**\_ \_ intervallo di testo DWrite**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) e chiamando il metodo [**IDWriteTextLayout:: setypography**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-settypography) e passando l'intervallo di testo.</span><span class="sxs-lookup"><span data-stu-id="f439f-257">Set the text layout to use the typography over the whole string by declaring a [**DWRITE\_TEXT\_RANGE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) variable and calling the [**IDWriteTextLayout::SetTypography**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-settypography) method and passing in the text range.</span></span>
    ```C++
    if (SUCCEEDED(hr))
    {
        // Set the typography for the entire string.
        DWRITE_TEXT_RANGE textRange = {0,
                                       cTextLength_};
        hr = pTextLayout_->SetTypography(pTypography, textRange);
    }
    
    ```

    

4.  <span data-ttu-id="f439f-258">Impostare la nuova larghezza e l'altezza per l'oggetto layout di testo nel metodo multiformattedtext:: OnResize.</span><span class="sxs-lookup"><span data-stu-id="f439f-258">Set the new width and height for the text layout object in the MultiformattedText::OnResize method.</span></span>
    ```C++
    if (pTextLayout_)
    {
        pTextLayout_->SetMaxWidth(static_cast<FLOAT>(width / dpiScaleX_));
        pTextLayout_->SetMaxHeight(static_cast<FLOAT>(height / dpiScaleY_));
    }
    ```

    

### <a name="part-4-draw-text-using-the-direct2d-drawtextlayout-method"></a><span data-ttu-id="f439f-259">Parte 4: creare il testo usando il metodo DrawTextLayout di Direct2D.</span><span class="sxs-lookup"><span data-stu-id="f439f-259">Part 4: Draw Text Using the Direct2D DrawTextLayout Method.</span></span>

<span data-ttu-id="f439f-260">Per tracciare il testo con le impostazioni di layout del testo specificate dall'oggetto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , modificare il codice nel metodo multiformattedtext::D rawtext per usare [**IDWriteTextLayout::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout).</span><span class="sxs-lookup"><span data-stu-id="f439f-260">To draw the text with the text layout settings specified by the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object, change the code in the MultiformattedText::DrawText method to use [**IDWriteTextLayout::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout).</span></span>

1.  <span data-ttu-id="f439f-261">Delcare una variabile [**d2d1 \_ Point \_ 2F**](../direct2d/d2d1-point-2f.md) e la imposta sul punto in alto a sinistra della finestra.</span><span class="sxs-lookup"><span data-stu-id="f439f-261">Delcare a [**D2D1\_POINT\_2F**](../direct2d/d2d1-point-2f.md) variable and set it to the upper-left point of the window.</span></span>
    ```C++
    D2D1_POINT_2F origin = D2D1::Point2F(
        static_cast<FLOAT>(rc.left / dpiScaleX_),
        static_cast<FLOAT>(rc.top / dpiScaleY_)
        );
    
    ```

    

2.  <span data-ttu-id="f439f-262">Disegnare il testo sullo schermo chiamando il metodo [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) della destinazione di rendering [Direct2D](../direct2d/direct2d-portal.md) e passando il puntatore [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="f439f-262">Draw the text to the screen by calling the [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) method of the [Direct2D](../direct2d/direct2d-portal.md) render target and passing the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) pointer.</span></span>
    ```C++
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    
    ```

    

<span data-ttu-id="f439f-263">La classe multiformattedtext è implementata in multiformattedtext. h e multiformattedtext. cpp.</span><span class="sxs-lookup"><span data-stu-id="f439f-263">The MultiformattedText class is implemented in MultiformattedText.h and MultiformattedText.cpp.</span></span>

 

 