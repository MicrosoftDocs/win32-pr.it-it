---
description: Questo esempio è basato sull'esempio di raccolta di input penna. Mostra come usare l'oggetto divisore per analizzare l'input penna.
ms.assetid: 3350b643-11b3-4474-8dd0-bc3eb1b7121e
title: Esempio di divisore input penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a272d6a5530938e6fecfeefc9f46ffdd0835d045
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484380"
---
# <a name="ink-divider-sample"></a><span data-ttu-id="bc124-104">Esempio di divisore input penna</span><span class="sxs-lookup"><span data-stu-id="bc124-104">Ink Divider Sample</span></span>

<span data-ttu-id="bc124-105">Questo esempio è basato sull' [esempio di raccolta di input penna](ink-collection-sample.md).</span><span class="sxs-lookup"><span data-stu-id="bc124-105">This sample is based on the [Ink Collection Sample](ink-collection-sample.md).</span></span> <span data-ttu-id="bc124-106">Mostra come usare l'oggetto [divisore](/previous-versions/ms839398(v=msdn.10)) per analizzare l'input penna.</span><span class="sxs-lookup"><span data-stu-id="bc124-106">It shows how to use the [Divider](/previous-versions/ms839398(v=msdn.10)) object to analyze ink input.</span></span>

<span data-ttu-id="bc124-107">Per informazioni concettuali dettagliate sul [divisore](/previous-versions/ms839398(v=msdn.10)), vedere [l'oggetto divisore](the-divider-object.md).</span><span class="sxs-lookup"><span data-stu-id="bc124-107">For detailed conceptual information about [Divider](/previous-versions/ms839398(v=msdn.10)), see [The Divider Object](the-divider-object.md).</span></span>

<span data-ttu-id="bc124-108">Quando il modulo viene aggiornato, l'esempio disegna un rettangolo di delimitazione intorno a ogni unità analizzata, suddiviso in parole, linee, paragrafi e disegni.</span><span class="sxs-lookup"><span data-stu-id="bc124-108">When the form is updated, the sample draws a bounding rectangle around each analyzed unit, broken into words, lines, paragraphs, and drawings.</span></span> <span data-ttu-id="bc124-109">Oltre a usare colori diversi, questi rettangoli vengono ingranditi in base a importi diversi per garantire che nessuno dei rettangoli venga oscurato da altri.</span><span class="sxs-lookup"><span data-stu-id="bc124-109">Besides using different colors, these rectangles are enlarged by different amounts to ensure that none of the rectangles is obscured by others.</span></span> <span data-ttu-id="bc124-110">Nella tabella seguente vengono specificati il colore e l'ingrandimento per ogni unità analizzata.</span><span class="sxs-lookup"><span data-stu-id="bc124-110">The following table specifies the color and enlargement for each analyzed unit.</span></span>



| <span data-ttu-id="bc124-111">Unità analizzata</span><span class="sxs-lookup"><span data-stu-id="bc124-111">analyzed Unit</span></span>        | <span data-ttu-id="bc124-112">Colore</span><span class="sxs-lookup"><span data-stu-id="bc124-112">Color</span></span>              | <span data-ttu-id="bc124-113">Ingrandimento pixel</span><span class="sxs-lookup"><span data-stu-id="bc124-113">Pixel Enlargement</span></span> |
|----------------------|--------------------|-------------------|
| <span data-ttu-id="bc124-114">Word</span><span class="sxs-lookup"><span data-stu-id="bc124-114">Word</span></span><br/>      | <span data-ttu-id="bc124-115">Green</span><span class="sxs-lookup"><span data-stu-id="bc124-115">Green</span></span><br/>   | <span data-ttu-id="bc124-116">1</span><span class="sxs-lookup"><span data-stu-id="bc124-116">1</span></span><br/>      |
| <span data-ttu-id="bc124-117">Linea</span><span class="sxs-lookup"><span data-stu-id="bc124-117">Line</span></span><br/>      | <span data-ttu-id="bc124-118">Fucsia</span><span class="sxs-lookup"><span data-stu-id="bc124-118">Magenta</span></span><br/> | <span data-ttu-id="bc124-119">3</span><span class="sxs-lookup"><span data-stu-id="bc124-119">3</span></span><br/>      |
| <span data-ttu-id="bc124-120">Paragraph</span><span class="sxs-lookup"><span data-stu-id="bc124-120">Paragraph</span></span><br/> | <span data-ttu-id="bc124-121">Blu</span><span class="sxs-lookup"><span data-stu-id="bc124-121">Blue</span></span><br/>    | <span data-ttu-id="bc124-122">5</span><span class="sxs-lookup"><span data-stu-id="bc124-122">5</span></span><br/>      |
| <span data-ttu-id="bc124-123">Disegno</span><span class="sxs-lookup"><span data-stu-id="bc124-123">Drawing</span></span><br/>   | <span data-ttu-id="bc124-124">Red</span><span class="sxs-lookup"><span data-stu-id="bc124-124">Red</span></span><br/>     | <span data-ttu-id="bc124-125">1</span><span class="sxs-lookup"><span data-stu-id="bc124-125">1</span></span><br/>      |



 

## <a name="setting-up-the-form"></a><span data-ttu-id="bc124-126">Impostazione del modulo</span><span class="sxs-lookup"><span data-stu-id="bc124-126">Setting Up the Form</span></span>

<span data-ttu-id="bc124-127">Quando il form viene caricato, viene creato un oggetto [divisore](/previous-versions/ms839398(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="bc124-127">When the form loads, a [Divider](/previous-versions/ms839398(v=msdn.10)) object is created.</span></span> <span data-ttu-id="bc124-128">Un oggetto [InkOverlay](/previous-versions/ms833057(v=msdn.10)) viene creato e associato a un pannello nel form.</span><span class="sxs-lookup"><span data-stu-id="bc124-128">An [InkOverlay](/previous-versions/ms833057(v=msdn.10)) object is created and associated with a panel on the form.</span></span> <span data-ttu-id="bc124-129">I gestori di eventi vengono quindi collegati all'oggetto InkOverlay per tenere traccia del momento in cui i tratti vengono aggiunti ed eliminati.</span><span class="sxs-lookup"><span data-stu-id="bc124-129">Then event handlers are attached to the InkOverlay object to track when strokes are added and deleted.</span></span> <span data-ttu-id="bc124-130">Quindi, se sono disponibili i riconoscitori, al divisore viene assegnato un oggetto [RecognizerContext](/previous-versions/ms828542(v=msdn.10)) per il riconoscimento predefinito.</span><span class="sxs-lookup"><span data-stu-id="bc124-130">Then if recognizers are available, a [RecognizerContext](/previous-versions/ms828542(v=msdn.10)) object for the default recognizer is assigned to the Divider.</span></span> <span data-ttu-id="bc124-131">Viene quindi impostata la proprietà [LineHeight](/previous-versions/ms839409(v=msdn.10)) dell'oggetto divisore e la raccolta [Strokes](/previous-versions/ms827799(v=msdn.10)) dall'oggetto InkOverlay viene assegnata al divisore.</span><span class="sxs-lookup"><span data-stu-id="bc124-131">Then the Divider object's [LineHeight](/previous-versions/ms839409(v=msdn.10)) property is set and the [Strokes](/previous-versions/ms827799(v=msdn.10)) collection from the InkOverlay object is assigned to the Divider.</span></span> <span data-ttu-id="bc124-132">Infine, l'oggetto InkOverlay è abilitato.</span><span class="sxs-lookup"><span data-stu-id="bc124-132">Finally, the InkOverlay object is enabled.</span></span>


```C++
// Create the ink overlay and associate it with the form
myInkOverlay = new Microsoft.Ink.InkOverlay(DrawArea.Handle);

// Set the erasing mode to stroke erase.
myInkOverlay.EraserMode = InkOverlayEraserMode.StrokeErase;

// Hook event handler for the Stroke event to myInkOverlay_Stroke.
// This is necessary since the application needs to pass the strokes 
// to the ink divider.
myInkOverlay.Stroke += new InkCollectorStrokeEventHandler(myInkOverlay_Stroke); 

// Hook the event handler for StrokeDeleting event to myInkOverlay_StrokeDeleting.
// This is necessary as the application needs to remove the strokes from 
// ink divider object as well.
myInkOverlay.StrokesDeleting += new InkOverlayStrokesDeletingEventHandler(myInkOverlay_StrokeDeleting);

// Hook the event handler for StrokeDeleted event to myInkOverlay_StrokeDeleted.
// This is necessary to update the layout analysis result when automatic layout analysis
// option is selected.
myInkOverlay.StrokesDeleted += new InkOverlayStrokesDeletedEventHandler(myInkOverlay_StrokeDeleted);

// Create the ink divider object
myInkDivider = new Divider();

// Add a default recognizer context to the divider object
// without adding the recognizer context, the divider would
// not use a recognizer to do its word segmentation and would
// have less accurate results.
// Adding the recognizer context slows down the call to 
// myInkDivider.Divide though.
// It is possible that there is no recognizer installed on the
// machine for this language. In that case the divider does
// not use a recognizer to improve its accuracy.
// Get the default recognizer if any
try
{
    Recognizers recognizers = new Recognizers();
     myInkDivider.RecognizerContext = recognizers.GetDefaultRecognizer().CreateRecognizerContext();
}
catch (InvalidOperationException)
{
     //We are in the case where no default recognizers can be found
}

    // The LineHeight property helps the InkDivider distinguish between 
    // drawing and handwriting. The value should be the expected height 
    // of the user's handwriting in ink space units (0.01mm).
    // Here we set the LineHeight to 840, which is about 1/3 of an inch.
    myInkDivider.LineHeight = 840;

// Assign ink overlay's strokes collection to the ink divider
// This strokes collection is updated in the event handler
myInkDivider.Strokes = myInkOverlay.Ink.Strokes;

// Enable ink collection
myInkOverlay.Enabled = true;
```



<span data-ttu-id="bc124-133">La raccolta [Strokes](/previous-versions/ms839422(v=msdn.10)) dell'oggetto [divisore](/previous-versions/ms839398(v=msdn.10)) deve essere mantenuta sincronizzata con la raccolta [Strokes](/previous-versions/ms827799(v=msdn.10)) dell'oggetto [InkOverlay](/previous-versions/ms833057(v=msdn.10)) (a cui si accede tramite la proprietà [Ink](/previous-versions/ms833110(v=msdn.10)) dell'oggetto InkOverlay).</span><span class="sxs-lookup"><span data-stu-id="bc124-133">The [Divider](/previous-versions/ms839398(v=msdn.10)) object's [Strokes](/previous-versions/ms839422(v=msdn.10)) collection must be kept in sync with the [InkOverlay](/previous-versions/ms833057(v=msdn.10)) object's [Strokes](/previous-versions/ms827799(v=msdn.10)) collection (accessed through the InkOverlay object's [Ink](/previous-versions/ms833110(v=msdn.10)) property).</span></span> <span data-ttu-id="bc124-134">Per assicurarsi che ciò avvenga, il gestore dell'evento [Stroke](/previous-versions/ms835344(v=msdn.10)) per l'oggetto InkOverlay viene scritto nel modo seguente.</span><span class="sxs-lookup"><span data-stu-id="bc124-134">To ensure that this happens, the [Stroke](/previous-versions/ms835344(v=msdn.10)) event handler for the InkOverlay object is written as follows.</span></span> <span data-ttu-id="bc124-135">Si noti che il gestore dell'evento verifica prima di tutto se [EditingMode](/previous-versions/ms833105(v=msdn.10)) è impostato su **input penna** per filtrare i tratti di gomma.</span><span class="sxs-lookup"><span data-stu-id="bc124-135">Note that the event handler first tests to see if the [EditingMode](/previous-versions/ms833105(v=msdn.10)) is set to **Ink** to filter out eraser strokes.</span></span> <span data-ttu-id="bc124-136">Se l'utente ha richiesto l'analisi automatica del layout, l'applicazione chiama il metodo DivideInk del form e aggiorna l'area di disegno.</span><span class="sxs-lookup"><span data-stu-id="bc124-136">If the user has requested automatic layout analysis, then the application calls the form's DivideInk method and refreshes the drawing area.</span></span>


```C++
private void myInkOverlay_Stroke(object sender, InkCollectorStrokeEventArgs e )
{
    // Filter out the eraser stroke.
    if(InkOverlayEditingMode.Ink == myInkOverlay.EditingMode)
    {
        // Add the new stroke to the ink divider's strokes collection
        myInkDivider.Strokes.Add(e.Stroke);
        
        if(miAutomaticLayoutAnalysis.Checked)
        {
            // Call DivideInk
            DivideInk();

            // Repaint the screen to reflect the change
            DrawArea.Refresh();
        }
    }
}
```



## <a name="dividing-the-ink"></a><span data-ttu-id="bc124-137">Divisione dell'input penna</span><span class="sxs-lookup"><span data-stu-id="bc124-137">Dividing the Ink</span></span>

<span data-ttu-id="bc124-138">Quando l'utente fa clic su divide nel menu file, il metodo [divide](/previous-versions/ms839461(v=msdn.10)) viene chiamato sull'oggetto [divisore](/previous-versions/ms839398(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="bc124-138">When the user clicks Divide on the File menu, the [Divide](/previous-versions/ms839461(v=msdn.10)) method is called on the [Divider](/previous-versions/ms839398(v=msdn.10)) object.</span></span> <span data-ttu-id="bc124-139">Viene utilizzato il riconoscimento predefinito, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="bc124-139">The default recognizer is used, if available.</span></span>


```C++
DivisionResult divResult = myInkDivider.Divide();
```



<span data-ttu-id="bc124-140">L'oggetto [DivisionResult](/previous-versions/ms839371(v=msdn.10)) risultante, a cui fa riferimento la variabile `divResult` , viene passato a una funzione di utilità `getUnitBBBoxes()` .</span><span class="sxs-lookup"><span data-stu-id="bc124-140">The resulting [DivisionResult](/previous-versions/ms839371(v=msdn.10)) object, referenced by the variable `divResult`, is passed to a utility function, `getUnitBBBoxes()`.</span></span> <span data-ttu-id="bc124-141">La funzione di utilità restituisce una matrice di rettangoli per qualsiasi tipo di divisione richiesto: segmenti, linee, paragrafi o disegni.</span><span class="sxs-lookup"><span data-stu-id="bc124-141">The utility function returns an array of rectangles for whatever division type is requested: segments, lines, paragraphs, or drawings.</span></span>


```C++
myWordBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Segment, 1);
myLineBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Line, 3);
myParagraphBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Paragraph, 5);
myDrawingBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Drawing, 1);
```



<span data-ttu-id="bc124-142">Infine, è necessario ricreare il pannello del modulo in modo che vengano visualizzati i rettangoli di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="bc124-142">Finally, the form panel is forced to redraw so that the bounding rectangles appear.</span></span>


```C++
DrawArea.Refresh();
```



## <a name="ink-analysis-results"></a><span data-ttu-id="bc124-143">Risultati analisi input penna</span><span class="sxs-lookup"><span data-stu-id="bc124-143">Ink Analysis Results</span></span>

<span data-ttu-id="bc124-144">Nella funzione di utilità, l'oggetto [DivisionResult](/previous-versions/ms839371(v=msdn.10)) viene sottoposto a query per i risultati tramite il metodo [ResultByType](/previous-versions/ms839388(v=msdn.10)) , in base al tipo di divisione richiesto dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="bc124-144">In the utility function, the [DivisionResult](/previous-versions/ms839371(v=msdn.10)) object is queried for its results by using the [ResultByType](/previous-versions/ms839388(v=msdn.10)) method, based on the division type requested by the caller.</span></span> <span data-ttu-id="bc124-145">Il metodo ResultByType restituisce una raccolta [DivisionUnits](/previous-versions/ms837954(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="bc124-145">The ResultByType method returns a [DivisionUnits](/previous-versions/ms837954(v=msdn.10)) collection.</span></span> <span data-ttu-id="bc124-146">Ogni [DivisionUnit](/previous-versions/ms837976(v=msdn.10)) della raccolta rappresenta un disegno, un singolo segmento di riconoscimento della grafia, una riga di grafia o un blocco di grafia, a seconda di quanto specificato quando è stata chiamata la funzione di utilità.</span><span class="sxs-lookup"><span data-stu-id="bc124-146">Each [DivisionUnit](/previous-versions/ms837976(v=msdn.10)) in the collection represents a drawing, a single recognition segment of handwriting, a line of handwriting, or a block of handwriting, depending upon what was specified when the utility function was called.</span></span>


```C++
DivisionUnits units = divResult.ResultByType(divType);
```



<span data-ttu-id="bc124-147">Se è presente almeno un [DivisionUnit](/previous-versions/ms837976(v=msdn.10)), viene creata una matrice di rettangoli contenente un rettangolo di delimitazione per unità.</span><span class="sxs-lookup"><span data-stu-id="bc124-147">If there is at least one [DivisionUnit](/previous-versions/ms837976(v=msdn.10)), an array of rectangles is created containing one bounding rectangle per unit.</span></span> <span data-ttu-id="bc124-148">I rettangoli sono inflat da importi diversi per ogni tipo di unità, contenuto nella variabile inflat, per evitare la sovrapposizione.</span><span class="sxs-lookup"><span data-stu-id="bc124-148">(The rectangles are inflated by differing amounts for each type of unit, held in the inflate variable, to prevent overlapping.)</span></span>


```C++
// If there is at least one unit, we construct the rectangles
if((null != units) && (0 < units.Count))
{
    // We need to convert rectangles from ink units to
    // pixel units. For that, we need Graphics object
    // to pass to InkRenderer.InkSpaceToPixel method
    using (Graphics g = DrawArea.CreateGraphics())
    {

    // InkSpace to Pixel Space conversion setup done here. 
    // Not shown for brevity.

        // Iterate through the collection of division units to obtain the bounding boxes
        foreach(DivisionUnit unit in units)
        {
            // Get the bounding box of the strokes of the division unit
            divRects[i] = unit.Strokes.GetBoundingBox();

            // Div unit rect Ink space to Pixel space conversion done here. 
            // Not shown for brevity.

            // Inflate the rectangle by inflate pixels in both directions
            divRects[i].Inflate(inflate, inflate);

            // Increment the index
            ++i;
        }

    } // Relinquish the Graphics object
}
```



## <a name="redrawing-the-form"></a><span data-ttu-id="bc124-149">Ridisegno del modulo</span><span class="sxs-lookup"><span data-stu-id="bc124-149">Redrawing the Form</span></span>

<span data-ttu-id="bc124-150">Quando il ridisegno è forzato sopra, viene eseguito il codice seguente per disegnare i rettangoli di delimitazione per ogni [DivisionUnit](/previous-versions/ms837976(v=msdn.10)) sul form intorno all'input penna.</span><span class="sxs-lookup"><span data-stu-id="bc124-150">When the redraw is forced above, the following code executes to paint the bounding boxes for each [DivisionUnit](/previous-versions/ms837976(v=msdn.10)) on the form around the ink.</span></span>


```C++
private void DrawArea_Paint(object sender, System.Windows.Forms.PaintEventArgs e)
        {
            // Create the Pen used to draw bounding boxes.
            // First set of bounding boxes drawn here are 
            // the bounding boxes of paragraphs.
            // These boxes are drawn with Blue pen.
            Pen penBox = new Pen(Color.Blue, 2);

            // First, draw the bounding boxes for Paragraphs
            if(null != myParagraphBoundingBoxes)
            {
                // Draw bounding boxes for Paragraphs
                e.Graphics.DrawRectangles(penBox, myParagraphBoundingBoxes);
            }

            // Next, draw the bounding boxes for Lines
            if(null != myLineBoundingBoxes)
            {
                // Color is Magenta pen
                penBox.Color = Color.Magenta;
                // Draw the bounding boxes for Lines
                e.Graphics.DrawRectangles(penBox, myLineBoundingBoxes);
            }
            
            // Then, draw the bounding boxes for Words
            if(null != myWordBoundingBoxes)
            {
                // Color is Green
                penBox.Color = Color.Green;
                // Draw bounding boxes for Words
                e.Graphics.DrawRectangles(penBox, myWordBoundingBoxes);
            }
            
            // Finally, draw the boxes for Drawings
            if(null != myDrawingBoundingBoxes)
            {
                // Color is Red pen
                penBox.Color = Color.Red;
                // Draw bounding boxes for Drawings
                e.Graphics.DrawRectangles(penBox, myDrawingBoundingBoxes);
            }
        }
```



## <a name="closing-the-form"></a><span data-ttu-id="bc124-151">Chiusura del modulo</span><span class="sxs-lookup"><span data-stu-id="bc124-151">Closing the Form</span></span>

<span data-ttu-id="bc124-152">Il metodo [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) del modulo Elimina gli oggetti [InkOverlay](/previous-versions/ms833057(v=msdn.10)), [divisore](/previous-versions/ms839398(v=msdn.10)), [RecognizerContext](/previous-versions/ms828542(v=msdn.10)) e la raccolta [Strokes](/previous-versions/ms827799(v=msdn.10)) utilizzata nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="bc124-152">The form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method disposes the [InkOverlay](/previous-versions/ms833057(v=msdn.10)), [Divider](/previous-versions/ms839398(v=msdn.10)), [RecognizerContext](/previous-versions/ms828542(v=msdn.10)) objects and the [Strokes](/previous-versions/ms827799(v=msdn.10)) collection used in the sample.</span></span>

 

