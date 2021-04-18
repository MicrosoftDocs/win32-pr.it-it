---
description: Nell'esempio di analisi dell'input penna di base viene illustrato come la classe InkAnalyzer divide l'input penna in diversi segmenti di Word e di disegno. Questo esempio è una versione aggiornata dell'esempio di divisore input penna.
ms.assetid: cb9a28d9-f8c6-478e-ae43-2d30106edc7b
title: Esempio di analisi dell'input penna di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e94ac73ca9049169c6e406059665a66e8eaa6f3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305697"
---
# <a name="basic-ink-analysis-sample"></a><span data-ttu-id="ea16f-103">Esempio di analisi dell'input penna di base</span><span class="sxs-lookup"><span data-stu-id="ea16f-103">Basic Ink Analysis Sample</span></span>

<span data-ttu-id="ea16f-104">Nell'esempio di analisi dell'input penna di base viene illustrato come la classe [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) divide l'input penna in diversi segmenti di Word e di disegno.</span><span class="sxs-lookup"><span data-stu-id="ea16f-104">The Basic Ink Analysis sample shows how the [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) class divides ink into various word and drawing segments.</span></span>

<span data-ttu-id="ea16f-105">Questo esempio è una versione aggiornata dell' [esempio di divisore input penna](ink-divider-sample.md).</span><span class="sxs-lookup"><span data-stu-id="ea16f-105">This sample is an updated version of the [Ink Divider Sample](ink-divider-sample.md).</span></span> <span data-ttu-id="ea16f-106">Mentre l'esempio di divisore di input penna usa la classe [divisore](/previous-versions/ms839398(v=msdn.10)) , in questo esempio viene usata l'API InkAnalysis più recente e preferita.</span><span class="sxs-lookup"><span data-stu-id="ea16f-106">Whereas the Ink Divider Sample uses the [Divider](/previous-versions/ms839398(v=msdn.10)) class, this sample uses the newer and preferred InkAnalysis API.</span></span> <span data-ttu-id="ea16f-107">L'API InkAnalysis combina l'oggetto [RecognizerContext](/previous-versions/ms828542(v=msdn.10)) e il divisore in un'unica API ed espande le funzionalità di entrambi.</span><span class="sxs-lookup"><span data-stu-id="ea16f-107">The InkAnalysis API combines the [RecognizerContext](/previous-versions/ms828542(v=msdn.10)) and Divider into one API and expands on the functionality of both.</span></span>

<span data-ttu-id="ea16f-108">Quando si aggiorna il modulo, l'esempio disegna un rettangolo intorno a ogni unità analizzata: parole, linee, paragrafi, aree di scrittura, disegni e punti elenco.</span><span class="sxs-lookup"><span data-stu-id="ea16f-108">When you update the form, the sample draws a rectangle around each analyzed unit: words, lines, paragraphs, writing regions, drawings and bullets.</span></span> <span data-ttu-id="ea16f-109">Il modulo usa colori diversi per le diverse unità.</span><span class="sxs-lookup"><span data-stu-id="ea16f-109">The form uses different colors for the different units.</span></span> <span data-ttu-id="ea16f-110">I rettangoli vengono inoltre ingranditi in base a importi diversi per garantire che nessun rettangolo sia nascosto da altri.</span><span class="sxs-lookup"><span data-stu-id="ea16f-110">The rectangles are also enlarged by different amounts to ensure that no one rectangle is obscured by any others.</span></span>

<span data-ttu-id="ea16f-111">Nella tabella seguente vengono specificati il colore e l'ingrandimento per ogni unità analizzata.</span><span class="sxs-lookup"><span data-stu-id="ea16f-111">The following table specifies the color and enlargement for each analyzed unit.</span></span>



| <span data-ttu-id="ea16f-112">Unità analizzata</span><span class="sxs-lookup"><span data-stu-id="ea16f-112">Analyzed unit</span></span>             | <span data-ttu-id="ea16f-113">Colore del rettangolo</span><span class="sxs-lookup"><span data-stu-id="ea16f-113">Color of rectangle</span></span> | <span data-ttu-id="ea16f-114">Ingrandimento rettangolo (pixel)</span><span class="sxs-lookup"><span data-stu-id="ea16f-114">Rectangle enlargement (pixels)</span></span> |
|---------------------------|--------------------|--------------------------------|
| <span data-ttu-id="ea16f-115">Word</span><span class="sxs-lookup"><span data-stu-id="ea16f-115">Word</span></span><br/>           | <span data-ttu-id="ea16f-116">Green</span><span class="sxs-lookup"><span data-stu-id="ea16f-116">Green</span></span><br/>   | <span data-ttu-id="ea16f-117">1</span><span class="sxs-lookup"><span data-stu-id="ea16f-117">1</span></span><br/>                   |
| <span data-ttu-id="ea16f-118">Linea</span><span class="sxs-lookup"><span data-stu-id="ea16f-118">Line</span></span><br/>           | <span data-ttu-id="ea16f-119">Fucsia</span><span class="sxs-lookup"><span data-stu-id="ea16f-119">Magenta</span></span><br/> | <span data-ttu-id="ea16f-120">3</span><span class="sxs-lookup"><span data-stu-id="ea16f-120">3</span></span><br/>                   |
| <span data-ttu-id="ea16f-121">Paragraph</span><span class="sxs-lookup"><span data-stu-id="ea16f-121">Paragraph</span></span><br/>      | <span data-ttu-id="ea16f-122">Blu</span><span class="sxs-lookup"><span data-stu-id="ea16f-122">Blue</span></span><br/>    | <span data-ttu-id="ea16f-123">5</span><span class="sxs-lookup"><span data-stu-id="ea16f-123">5</span></span><br/>                   |
| <span data-ttu-id="ea16f-124">Area di scrittura</span><span class="sxs-lookup"><span data-stu-id="ea16f-124">Writing region</span></span><br/> | <span data-ttu-id="ea16f-125">Giallo</span><span class="sxs-lookup"><span data-stu-id="ea16f-125">Yellow</span></span><br/>  | <span data-ttu-id="ea16f-126">7</span><span class="sxs-lookup"><span data-stu-id="ea16f-126">7</span></span><br/>                   |
| <span data-ttu-id="ea16f-127">Disegno</span><span class="sxs-lookup"><span data-stu-id="ea16f-127">Drawing</span></span><br/>        | <span data-ttu-id="ea16f-128">Red</span><span class="sxs-lookup"><span data-stu-id="ea16f-128">Red</span></span><br/>     | <span data-ttu-id="ea16f-129">1</span><span class="sxs-lookup"><span data-stu-id="ea16f-129">1</span></span><br/>                   |
| <span data-ttu-id="ea16f-130">Punto elenco</span><span class="sxs-lookup"><span data-stu-id="ea16f-130">Bullet</span></span><br/>         | <span data-ttu-id="ea16f-131">Orange</span><span class="sxs-lookup"><span data-stu-id="ea16f-131">Orange</span></span><br/>  | <span data-ttu-id="ea16f-132">1</span><span class="sxs-lookup"><span data-stu-id="ea16f-132">1</span></span><br/>                   |



 

<span data-ttu-id="ea16f-133">È possibile cancellare i tratti nel form.</span><span class="sxs-lookup"><span data-stu-id="ea16f-133">You can erase strokes in the form.</span></span> <span data-ttu-id="ea16f-134">Nell'applicazione di esempio, è possibile passare dall'input penna alla modalità di cancellazione e viceversa per modificare la funzione della penna.</span><span class="sxs-lookup"><span data-stu-id="ea16f-134">In the sample application, you can toggle between Ink and Erase mode to change the function of the pen.</span></span>


```C++
        private void miInk_Click(object sender, System.EventArgs e)
        {
            // Turn on the inking mode
            myInkOverlay.EditingMode = InkOverlayEditingMode.Ink;

            // Update the state of the Ink and Erase menu items
            miInk.Checked = true;
            miErase.Checked = false;

            // Update the UI
            this.Refresh();
        }

        private void miErase_Click(object sender, System.EventArgs e)
        {
            // Turn on the ink deletion mode
            myInkOverlay.EditingMode = InkOverlayEditingMode.Delete;

            // Update the state of the Ink and Erase menu items
            miInk.Checked = false;
            miErase.Checked = true;

            // Update the UI
            this.Refresh();
        }
```



<span data-ttu-id="ea16f-135">Quando si aggiungono o eliminano tratti, gli esempi aggiornano l' [oggetto InkAnalyzer](/previous-versions/ms583671(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="ea16f-135">When you add or delete strokes, the samples updates the [InkAnalyzer](/previous-versions/ms583671(v=vs.100)).</span></span>


```C++
        private void myInkOverlay_Stroke(object sender, InkCollectorStrokeEventArgs e)
        {
            // Filter out the eraser stroke.
            if (InkOverlayEditingMode.Ink == myInkOverlay.EditingMode)
            {

                // Add the new stroke to the InkAnalyzer's stroke collection
                myInkAnalyzer.AddStroke(e.Stroke);

                if (miAutomaticLayoutAnalysis.Checked)
                {
                    // Invoke an analysis operation on the background thread
                    myInkAnalyzer.BackgroundAnalyze();
                }
            }
        }

        void myInkOverlay_StrokeDeleting(object sender, InkOverlayStrokesDeletingEventArgs e)
        {
            // Remove the strokes to be deleted from the InkAnalyzer's stroke collection
            myInkAnalyzer.RemoveStrokes(e.StrokesToDelete);

            // If automatic layout analysis is turned on, analyze the ink on the background thread
            if ( miAutomaticLayoutAnalysis.Checked )
            {
                // Invoke an analysis operation on the background thread
                myInkAnalyzer.BackgroundAnalyze ( );
            }
        }
```



<span data-ttu-id="ea16f-136">Si noti che nel menu modalità l'analisi automatica del layout è attiva per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="ea16f-136">Notice that in the Mode menu, Automatic Layout Analysis is on by default.</span></span> <span data-ttu-id="ea16f-137">Se questa opzione è selezionata, i gestori eventi [Stroke](/previous-versions/ms835344(v=msdn.10)) e [StrokesDeleting](/previous-versions/ms835360(v=msdn.10)) dell'oggetto [InkOverlay](/previous-versions/ms833057(v=msdn.10)) chiamano il metodo [BackgroundAnalyze](/previous-versions/ms568972(v=vs.100)) ogni volta che viene creato o eliminato un tratto.</span><span class="sxs-lookup"><span data-stu-id="ea16f-137">With this option selected, the [InkOverlay](/previous-versions/ms833057(v=msdn.10)) object's [Stroke](/previous-versions/ms835344(v=msdn.10)) and [StrokesDeleting](/previous-versions/ms835360(v=msdn.10)) event handlers call the [BackgroundAnalyze](/previous-versions/ms568972(v=vs.100)) method every time a stroke is created or deleted.</span></span>

> [!Note]  
> <span data-ttu-id="ea16f-138">La chiamata al metodo [Analyze](/previous-versions/ms568971(v=vs.100)) dell'oggetto [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) con più di pochi tratti presenti crea un ritardo notevole in un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ea16f-138">Calling the [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) object's [Analyze](/previous-versions/ms568971(v=vs.100)) method with more than a few strokes present creates a noticeable delay in an application.</span></span> <span data-ttu-id="ea16f-139">Questo perché Analyze è un'operazione di analisi dell'input penna sincrona.</span><span class="sxs-lookup"><span data-stu-id="ea16f-139">This is because Analyze is a synchronous ink analysis operation.</span></span> <span data-ttu-id="ea16f-140">In pratica, chiamare il metodo Analyze solo quando è necessario il risultato.</span><span class="sxs-lookup"><span data-stu-id="ea16f-140">In practice, call the Analyze method only when you need the result.</span></span> <span data-ttu-id="ea16f-141">In caso contrario, utilizzare il metodo [BackgroundAnalyze](/previous-versions/ms568972(v=vs.100)) asincrono, come illustrato nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="ea16f-141">Otherwise use the asynchronous [BackgroundAnalyze](/previous-versions/ms568972(v=vs.100)) method, as shown in the sample.</span></span>

 

## <a name="handling-the-analysis-results"></a><span data-ttu-id="ea16f-142">Gestione dei risultati dell'analisi</span><span class="sxs-lookup"><span data-stu-id="ea16f-142">Handling the Analysis Results</span></span>

<span data-ttu-id="ea16f-143">Nell'esempio vengono create due matrici per mantenere i vari rettangoli, orizzontali o ruotati.</span><span class="sxs-lookup"><span data-stu-id="ea16f-143">The sample creates two arrays to hold the various rectangles, either horizontal or rotated.</span></span> <span data-ttu-id="ea16f-144">Utilizzare un rettangolo di delimitazione ruotato per ottenere l'angolo in cui viene scritta una riga di parole.</span><span class="sxs-lookup"><span data-stu-id="ea16f-144">Use a rotated bounding box to get the angle on which a line of words is written.</span></span> <span data-ttu-id="ea16f-145">Nell'esempio vengono illustrate le proprietà restituite dall' [oggetto InkAnalyzer](/previous-versions/ms583671(v=vs.100)) e viene visualizzato il rettangolo di selezione o il rettangolo di selezione ruotato (a seconda della selezione di menu).</span><span class="sxs-lookup"><span data-stu-id="ea16f-145">The sample shows the properties returned by the [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) and displays the bounding box or the rotated bounding box (depending on the menu selection).</span></span>


```C++
      private Rectangle[] GetHorizontalBBoxes(Guid nodeType, int inflate)
        {
            // Declare the array of rectangles to hold the result
            Rectangle[] analysisRects;

            // Get the division units from the division result of division type
            ContextNodeCollection nodes = myInkAnalyzer.FindNodesOfType(nodeType);

            // If there is at least one unit, we construct the rectangles
            if ((null != nodes) && (0 < nodes.Count))
            {
                // We need to convert rectangles from ink units to
                // pixel units. For that, we need Graphics object
                // to pass to InkRenderer.InkSpaceToPixel method
                using (Graphics g = drawArea.CreateGraphics())
                {
                    // Construct the rectangles
                    analysisRects = new Rectangle[nodes.Count];

                    // InkRenderer.InkSpaceToPixel takes Point as parameter. 
                    // Create two Point objects to point to (Top, Left) and
                    // (Width, Height) properties of rectangle. (Width, Height)
                    // is used instead of (Right, Bottom) because (Right, Bottom)
                    // are read-only properties on Rectangle
                    Point ptLocation = new Point();
                    Point ptSize = new Point();

                    // Index into the bounding boxes
                    int i = 0;

                    // Iterate through the collection of division units to obtain the bounding boxes
                    foreach (ContextNode node in nodes)
                    {
                        // Get the bounding box of the strokes of the division unit
                        analysisRects[i] = node.Location.GetBounds();

                        // The bounding box is in ink space unit. Convert them into pixel unit. 
                        ptLocation = analysisRects[i].Location;
                        ptSize.X = analysisRects[i].Width;
                        ptSize.Y = analysisRects[i].Height;

                        // Convert the Location from Ink Space to Pixel Space
                        myInkOverlay.Renderer.InkSpaceToPixel(g, ref ptLocation);

                        // Convert the Size from Ink Space to Pixel Space
                        myInkOverlay.Renderer.InkSpaceToPixel(g, ref ptSize);

                        // Assign the result back to the corresponding properties
                        analysisRects[i].Location = ptLocation;
                        analysisRects[i].Width = ptSize.X;
                        analysisRects[i].Height = ptSize.Y;

                        // Inflate the rectangle by inflate pixels in both directions
                        analysisRects[i].Inflate(inflate, inflate);

                        // Increment the index
                        ++i;
                    }

                } // Relinquish the Graphics object
            }
            else
            {
                // Otherwise we return null
                analysisRects = null;
            }

            // Return the Rectangle[] object
            return analysisRects;
        }

        private System.Collections.ArrayList GetRotatedBBoxes(Guid nodeType, int inflate)
        {
            //Find the correct collection of results nodes.
            ContextNodeCollection Nodes = myInkAnalyzer.FindNodesOfType(nodeType);

            // Declare the array list to hold the results; 
            // This array represents the four points of a rectangle, with the first point
            // copied again to complete the cycle of points.

            ArrayList polygonPoints = new ArrayList(Nodes.Count);

            // Cycle through each results node, get and convert the
            // rotated bounding box points
            foreach (ContextNode node in Nodes)
            {
                //Declare the point array
                Point[] rotatedBoundingBox = null;

                //Switch on the type of ContextNode to cast into the
                //appropriate type.  This is required to access the 
                //type specific property "RotatedBoundingBox" which
                //is not found on all ContextNode types.
                if (nodeType == ContextNodeType.InkWord)
                {
                    rotatedBoundingBox = ((InkWordNode)node).GetRotatedBoundingBox();
                }
                else if (nodeType == ContextNodeType.Line)
                {
                    rotatedBoundingBox = ((LineNode)node).GetRotatedBoundingBox();
                }
                else if (nodeType == ContextNodeType.Paragraph)
                {
                    rotatedBoundingBox = ((ParagraphNode)node).GetRotatedBoundingBox();
                }
                else if (nodeType == ContextNodeType.WritingRegion ||
                         nodeType == ContextNodeType.InkDrawing ||
                         nodeType == ContextNodeType.InkBullet )
                {

                    // Rotated Bounding Boxes are not a supported option for 
                    // Writing Regions or Drawings.  We return the axis aligned 
                    // bounding box instead
                    Rectangle rect = node.Location.GetBounds();

                    // We need to create a looped list of 4 points to be consistent
                    // with the way InkAnalysis represents rotated bounding boxes.  
                    rotatedBoundingBox = new Point[4];

                    rotatedBoundingBox[0] = new Point(rect.X, rect.Y);
                    rotatedBoundingBox[1] = new Point(rect.Right, rect.Y);
                    rotatedBoundingBox[2] = new Point(rect.Right, rect.Bottom);
                    rotatedBoundingBox[3] = new Point(rect.X, rect.Bottom);

                }


                if (null != rotatedBoundingBox)
                {
                    // We need to convert rectangles from ink units to
                    // pixel units. For that, we need Graphics object
                    // to pass to InkRenderer.InkSpaceToPixel method
                    using (Graphics g = drawArea.CreateGraphics())
                    {
                        // convert each of the points from ink space to pixel space
                        for (int i = 0; i < rotatedBoundingBox.Length; i++)
                        {
                            myInkOverlay.Renderer.InkSpaceToPixel(g, ref rotatedBoundingBox[i]);
                        }

                        //inflate the points by calling helper method
                        InflateHelperMethod(ref rotatedBoundingBox, inflate);

                        // increment the node portion of the polygonPoints array
                        polygonPoints.Add(rotatedBoundingBox);
                    }
                }
            }
            //Return the results
            return polygonPoints;
        }
```



<span data-ttu-id="ea16f-146">Il parser calcola [GetRotatedBoundingBox](/previous-versions/ms569544(v=vs.100)) durante l'analisi.</span><span class="sxs-lookup"><span data-stu-id="ea16f-146">The parser calculates [GetRotatedBoundingBox](/previous-versions/ms569544(v=vs.100)) during analysis.</span></span> <span data-ttu-id="ea16f-147">È possibile accedere alle informazioni dai rettangoli di delimitazione ruotati nell'applicazione per diversi motivi utili:</span><span class="sxs-lookup"><span data-stu-id="ea16f-147">You can access the information from the rotated bounding boxes in your application for a number of useful reasons:</span></span>

-   <span data-ttu-id="ea16f-148">Rilevare o creare i limiti di una singola riga, un paragrafo o un'altra unità.</span><span class="sxs-lookup"><span data-stu-id="ea16f-148">Detect or draw the bounds of a single line, paragraph, or other unit.</span></span>
-   <span data-ttu-id="ea16f-149">Determinare l'angolo in corrispondenza del quale viene scritta una riga o un paragrafo.</span><span class="sxs-lookup"><span data-stu-id="ea16f-149">Determine the angle at which a line or paragraph is written.</span></span>
-   <span data-ttu-id="ea16f-150">Implementare funzionalità come la selezione di una riga, un paragrafo o un'altra unità.</span><span class="sxs-lookup"><span data-stu-id="ea16f-150">Implement features such as selection for a line, paragraph, or other unit.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea16f-151">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ea16f-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea16f-152">Riconoscimento di base e analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="ea16f-152">Basic Recognition and Ink Analysis</span></span>](basic-recognition-and-ink-analysis.md)
</dt> <dt>

[<span data-ttu-id="ea16f-153">Esempio di modulo cartaceo analizzato</span><span class="sxs-lookup"><span data-stu-id="ea16f-153">Scanned Paper Form Sample</span></span>](scanned-paper-form-sample.md)
</dt> <dt>

[<span data-ttu-id="ea16f-154">Esempio di divisore input penna</span><span class="sxs-lookup"><span data-stu-id="ea16f-154">Ink Divider Sample</span></span>](ink-divider-sample.md)
</dt> </dl>

 

