---
description: Questo esempio è basato sull'esempio di raccolta ink. Illustra come usare l'oggetto Divider per analizzare l'input penna.
ms.assetid: 3350b643-11b3-4474-8dd0-bc3eb1b7121e
title: Esempio di divisore input penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c74592606ba98ec913dd419deda1b2b766066e17545e95f18a14980f36dafde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452098"
---
# <a name="ink-divider-sample"></a>Esempio di divisore input penna

Questo esempio è basato su [Ink Collection Sample.](ink-collection-sample.md) Illustra come usare l'oggetto [Divider per](/previous-versions/ms839398(v=msdn.10)) analizzare l'input penna.

Per informazioni concettuali dettagliate su [Divider,](/previous-versions/ms839398(v=msdn.10))vedere [Oggetto Divider.](the-divider-object.md)

Quando il form viene aggiornato, l'esempio disegna un rettangolo di delimitazione intorno a ogni unità analizzata, suddiviso in parole, linee, paragrafi e disegni. Oltre a usare colori diversi, questi rettangoli vengono ingranditi di quantità diverse per garantire che nessuno dei rettangoli sia nascosto da altri. Nella tabella seguente vengono specificati il colore e la colorazione per ogni unità analizzata.



| unità analizzata        | Color              | Pixel Disassamento |
|----------------------|--------------------|-------------------|
| Word<br/>      | Green<br/>   | 1<br/>      |
| A linee<br/>      | Fucsia<br/> | 3<br/>      |
| Paragraph<br/> | Blu<br/>    | 5<br/>      |
| Disegno<br/>   | Red<br/>     | 1<br/>      |



 

## <a name="setting-up-the-form"></a>Impostazione del modulo

Quando il form viene caricato, viene creato un oggetto [Divider.](/previous-versions/ms839398(v=msdn.10)) Un [oggetto InkOverlay](/previous-versions/ms833057(v=msdn.10)) viene creato e associato a un pannello nel form. I gestori eventi vengono quindi associati all'oggetto InkOverlay per tenere traccia del momento in cui i tratti vengono aggiunti ed eliminati. Quindi, se sono disponibili riconoscitori, al divisore viene assegnato un oggetto [RecognizerContext](/previous-versions/ms828542(v=msdn.10)) per il riconoscitore predefinito. Viene quindi impostata la [proprietà LineHeight](/previous-versions/ms839409(v=msdn.10)) dell'oggetto Divider e la raccolta [Strokes](/previous-versions/ms827799(v=msdn.10)) dell'oggetto InkOverlay viene assegnata a Divider. Infine, l'oggetto InkOverlay è abilitato.


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



La raccolta [Strokes](/previous-versions/ms839422(v=msdn.10)) dell'oggetto [Divider](/previous-versions/ms839398(v=msdn.10)) deve essere mantenuta sincronizzata con la raccolta [Strokes](/previous-versions/ms827799(v=msdn.10)) dell'oggetto [InkOverlay](/previous-versions/ms833057(v=msdn.10)) (accessibile tramite la proprietà [Ink](/previous-versions/ms833110(v=msdn.10)) dell'oggetto InkOverlay). Per assicurarsi che ciò accada, il [gestore dell'evento Stroke](/previous-versions/ms835344(v=msdn.10)) per l'oggetto InkOverlay viene scritto come segue. Si noti che il gestore dell'evento verifica prima di tutto se [EditingMode](/previous-versions/ms833105(v=msdn.10)) è impostato su **Ink** per filtrare i tratti della gomma. Se l'utente ha richiesto l'analisi automatica del layout, l'applicazione chiama il metodo DivideInk del form e aggiorna l'area di disegno.


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



## <a name="dividing-the-ink"></a>Divisione dell'input penna

Quando l'utente fa clic su Dividi nel menu File, viene chiamato il [metodo Divide](/previous-versions/ms839461(v=msdn.10)) sull'oggetto [Divider.](/previous-versions/ms839398(v=msdn.10)) Se disponibile, viene usato il riconoscitore predefinito.


```C++
DivisionResult divResult = myInkDivider.Divide();
```



[L'oggetto DivisionResult risultante,](/previous-versions/ms839371(v=msdn.10)) a cui fa riferimento la variabile `divResult` , viene passato a una funzione di utilità, `getUnitBBBoxes()` . La funzione di utilità restituisce una matrice di rettangoli per qualsiasi tipo di divisione richiesto: segmenti, linee, paragrafi o disegni.


```C++
myWordBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Segment, 1);
myLineBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Line, 3);
myParagraphBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Paragraph, 5);
myDrawingBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Drawing, 1);
```



Infine, il pannello del form viene ridisegnato in modo da visualizzare i rettangoli di delimitazione.


```C++
DrawArea.Refresh();
```



## <a name="ink-analysis-results"></a>Risultati dell'analisi input penna

Nella funzione di utilità, l'oggetto [DivisionResult](/previous-versions/ms839371(v=msdn.10)) viene sottoposto a query per i risultati usando il metodo [ResultByType,](/previous-versions/ms839388(v=msdn.10)) in base al tipo di divisione richiesto dal chiamante. Il metodo ResultByType restituisce una [raccolta DivisionUnits.](/previous-versions/ms837954(v=msdn.10)) Ogni [DivisionUnit](/previous-versions/ms837976(v=msdn.10)) nella raccolta rappresenta un disegno, un singolo segmento di riconoscimento della grafia, una riga di grafia o un blocco di grafia, a seconda di ciò che è stato specificato quando è stata chiamata la funzione di utilità.


```C++
DivisionUnits units = divResult.ResultByType(divType);
```



Se è presente almeno un [oggetto DivisionUnit,](/previous-versions/ms837976(v=msdn.10))viene creata una matrice di rettangoli contenente un rettangolo di delimitazione per unità. I rettangoli vengono gonfiati in base a quantità diverse per ogni tipo di unità, mantenute nella variabile di gonfiamento, per evitare la sovrapposizione.


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



## <a name="redrawing-the-form"></a>Ridisegno del form

Quando il ridisegno viene forzato sopra, viene eseguito il codice seguente per disegnare i recinti di selezione per [ogni DivisionUnit](/previous-versions/ms837976(v=msdn.10)) sul form intorno all'input penna.


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



## <a name="closing-the-form"></a>Chiusura del modulo

Il metodo [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) del form elimina gli oggetti [InkOverlay,](/previous-versions/ms833057(v=msdn.10)) [Divider,](/previous-versions/ms839398(v=msdn.10)) [RecognizerContext](/previous-versions/ms828542(v=msdn.10)) e la raccolta [Strokes](/previous-versions/ms827799(v=msdn.10)) usata nell'esempio.

 

