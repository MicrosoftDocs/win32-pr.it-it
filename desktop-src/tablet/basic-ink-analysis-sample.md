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
# <a name="basic-ink-analysis-sample"></a>Esempio di analisi dell'input penna di base

Nell'esempio di analisi dell'input penna di base viene illustrato come la classe [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) divide l'input penna in diversi segmenti di Word e di disegno.

Questo esempio è una versione aggiornata dell' [esempio di divisore input penna](ink-divider-sample.md). Mentre l'esempio di divisore di input penna usa la classe [divisore](/previous-versions/ms839398(v=msdn.10)) , in questo esempio viene usata l'API InkAnalysis più recente e preferita. L'API InkAnalysis combina l'oggetto [RecognizerContext](/previous-versions/ms828542(v=msdn.10)) e il divisore in un'unica API ed espande le funzionalità di entrambi.

Quando si aggiorna il modulo, l'esempio disegna un rettangolo intorno a ogni unità analizzata: parole, linee, paragrafi, aree di scrittura, disegni e punti elenco. Il modulo usa colori diversi per le diverse unità. I rettangoli vengono inoltre ingranditi in base a importi diversi per garantire che nessun rettangolo sia nascosto da altri.

Nella tabella seguente vengono specificati il colore e l'ingrandimento per ogni unità analizzata.



| Unità analizzata             | Colore del rettangolo | Ingrandimento rettangolo (pixel) |
|---------------------------|--------------------|--------------------------------|
| Word<br/>           | Green<br/>   | 1<br/>                   |
| Linea<br/>           | Fucsia<br/> | 3<br/>                   |
| Paragraph<br/>      | Blu<br/>    | 5<br/>                   |
| Area di scrittura<br/> | Giallo<br/>  | 7<br/>                   |
| Disegno<br/>        | Red<br/>     | 1<br/>                   |
| Punto elenco<br/>         | Orange<br/>  | 1<br/>                   |



 

È possibile cancellare i tratti nel form. Nell'applicazione di esempio, è possibile passare dall'input penna alla modalità di cancellazione e viceversa per modificare la funzione della penna.


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



Quando si aggiungono o eliminano tratti, gli esempi aggiornano l' [oggetto InkAnalyzer](/previous-versions/ms583671(v=vs.100)).


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



Si noti che nel menu modalità l'analisi automatica del layout è attiva per impostazione predefinita. Se questa opzione è selezionata, i gestori eventi [Stroke](/previous-versions/ms835344(v=msdn.10)) e [StrokesDeleting](/previous-versions/ms835360(v=msdn.10)) dell'oggetto [InkOverlay](/previous-versions/ms833057(v=msdn.10)) chiamano il metodo [BackgroundAnalyze](/previous-versions/ms568972(v=vs.100)) ogni volta che viene creato o eliminato un tratto.

> [!Note]  
> La chiamata al metodo [Analyze](/previous-versions/ms568971(v=vs.100)) dell'oggetto [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) con più di pochi tratti presenti crea un ritardo notevole in un'applicazione. Questo perché Analyze è un'operazione di analisi dell'input penna sincrona. In pratica, chiamare il metodo Analyze solo quando è necessario il risultato. In caso contrario, utilizzare il metodo [BackgroundAnalyze](/previous-versions/ms568972(v=vs.100)) asincrono, come illustrato nell'esempio.

 

## <a name="handling-the-analysis-results"></a>Gestione dei risultati dell'analisi

Nell'esempio vengono create due matrici per mantenere i vari rettangoli, orizzontali o ruotati. Utilizzare un rettangolo di delimitazione ruotato per ottenere l'angolo in cui viene scritta una riga di parole. Nell'esempio vengono illustrate le proprietà restituite dall' [oggetto InkAnalyzer](/previous-versions/ms583671(v=vs.100)) e viene visualizzato il rettangolo di selezione o il rettangolo di selezione ruotato (a seconda della selezione di menu).


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



Il parser calcola [GetRotatedBoundingBox](/previous-versions/ms569544(v=vs.100)) durante l'analisi. È possibile accedere alle informazioni dai rettangoli di delimitazione ruotati nell'applicazione per diversi motivi utili:

-   Rilevare o creare i limiti di una singola riga, un paragrafo o un'altra unità.
-   Determinare l'angolo in corrispondenza del quale viene scritta una riga o un paragrafo.
-   Implementare funzionalità come la selezione di una riga, un paragrafo o un'altra unità.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riconoscimento di base e analisi dell'input penna](basic-recognition-and-ink-analysis.md)
</dt> <dt>

[Esempio di modulo cartaceo analizzato](scanned-paper-form-sample.md)
</dt> <dt>

[Esempio di divisore input penna](ink-divider-sample.md)
</dt> </dl>

 

