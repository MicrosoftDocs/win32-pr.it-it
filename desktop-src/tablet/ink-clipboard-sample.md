---
description: Questo programma illustra come copiare e incollare input penna in un'altra applicazione. Consente inoltre all'utente di copiare una selezione di tratti e incollare il risultato nell'oggetto input penna esistente.
ms.assetid: a0c42f1c-543d-44f8-83d9-fe810de410ff
title: Esempio di Appunti input penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73aa8acdf785321dc01706d4a4de50e0a2673a31250edbfa4316a27aecd0ce3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032329"
---
# <a name="ink-clipboard-sample"></a>Esempio di Appunti input penna

Questo programma illustra come copiare e incollare input penna in un'altra applicazione. Consente inoltre all'utente di copiare una selezione di tratti e incollare il risultato nell'oggetto input penna esistente.

Sono disponibili le modalità Appunti seguenti:

-   Formato serializzato input penna (ISF)
-   Metafile
-   Enhanced Metafile (EMF)
-   Bitmap
-   Input penna di testo
-   Disegnare l'input penna

L'input penna del testo e l'input penna dello sketch sono due tipi di controlli input penna usati rispettivamente come testo o disegno. È possibile incollare ISF, input penna di testo e disegnare l'input penna nell'input penna esistente.

Oltre agli Appunti, questo esempio illustra anche come selezionare i tratti con lo strumento lazo. L'utente può spostare i tratti selezionati e modificarne gli attributi di disegno. Questa funzionalità è un subset delle funzionalità di selezione già fornite dal controllo di sovrapposizione input penna. viene implementato qui a scopo illustrativo.

In questo esempio vengono usate le funzionalità seguenti:

-   Oggetto [InkCollector.](/previous-versions/ms583683(v=vs.100))
-   Supporto degli Appunti input penna.
-   Uso del lasso con il [metodo Microsoft.Ink.Ink.HitTest.](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90))

Questo esempio illustra come eseguire il rendering dell'input penna, copiarlo e quindi incollarlo in un'altra applicazione, ad esempio Microsoft Paint.

## <a name="collecting-ink-and-setting-up-the-form"></a>Raccolta di input penna e configurazione del modulo

Per prima cosa, fare riferimento alle interfacce di automazione di Tablet PC, installate con Microsoft Windows <entity type="reg"/> XP Tablet PC Edition Software Development Kit (SDK).


```C++
using Microsoft.Ink;
```



Successivamente, il modulo dichiara alcune costanti e campi che vengono notati più avanti in questo esempio.


```C++
// Declare constant for the size of the border around selected strokes
private const int SelectedInkWidthIncrease = 105;

// Declare constant for the size of a lasso point
private const int DotSize = 6;

// Declare constant for the spacing between lasso points
private const int DotSpacing = 7;

// Declare constant for the selection rectangle padding
private const int SelectionRectBuffer = 8;

// Declare constant for the lasso hit test percent (specifies how much
// of the stoke must fall within the lasso in order to be selected).
private const float LassoPercent = 50;
...
// Declare the InkCollector object
private InkCollector myInkCollector = null;

// The points in the selection lasso
private ArrayList lassoPoints = null;

// The array of rectangle selection handles
private PictureBox[] selectionHandles;

// The rectangle that bounds the selected strokes
private Rectangle selectionRect = Rectangle.Empty;

// The strokes that have been selected by the lasso
private Strokes selectedStrokes = null;
...
// Declare the colors used in the selection lasso
private Color dotEdgeColor = Color.White;
private Color dotColor = SystemColors.Highlight;
private Color connectorColor = Color.Black;

// Declare the pens used to draw the selection lasso
private Pen connectorPen = null;
private Pen dotEdgePen = null;
private Pen dotPen = null;
```



Infine, nel gestore dell'evento [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) del form viene inizializzato il form, viene creato un oggetto [InkCollector](/previous-versions/ms583683(v=vs.100)) per il form e viene abilitato l'agente di raccolta input penna.


```C++
// Create an ink collector and assign it to this form's window
myInkCollector = new InkCollector(this.Handle);

// Turn the ink collector on
myInkCollector.Enabled = true;
```



## <a name="handling-menu-events"></a>Gestione degli eventi di menu

I gestori eventi delle voci di menu aggiornano principalmente lo stato del form.

Il comando Cancella rimuove il rettangolo di selezione ed elimina i tratti dall'oggetto Ink dell'agente [di](/previous-versions/ms583670(v=vs.100)) raccolta input penna.

Il comando Esci disabilita l'agente di raccolta input penna prima di uscire dall'applicazione.

Il menu Modifica abilita i comandi Taglia e Copia in base allo stato di selezione del modulo e abilita il comando Incolla in base al contenuto degli Appunti, determinato dall'uso del metodo [CanPaste](/previous-versions/dotnet/netframework-3.5/ms571314(v=vs.90)) dell'oggetto [Ink.](/previous-versions/ms583670(v=vs.100))

Entrambi i comandi Taglia e Copia usano un metodo helper per copiare l'input penna negli Appunti. Il comando Taglia usa un metodo helper per eliminare i tratti selezionati.

Il comando Incolla controlla prima di tutto il [metodo](/previous-versions/ms583670(v=vs.100)) [CanPaste](/previous-versions/dotnet/netframework-3.5/ms571314(v=vs.90)) dell'oggetto Ink per verificare se l'oggetto negli Appunti può essere incollato. Il comando Incolla calcola quindi l'angolo superiore sinistro per l'area incollata, converte le coordinate dai pixel allo spazio input penna e incolla i tratti dagli Appunti all'agente di raccolta input penna. Infine, la casella di selezione viene aggiornata.


```C++
if (myInkCollector.Ink.CanPaste())
{
   // Compute the location where the ink should be pasted;
    // this location should be shifted from the origin
    // to account for the width of the selection rectangle's handle.
    Point offset = new Point(leftTopHandle.Width+1,leftTopHandle.Height+1);
    using (Graphics g = CreateGraphics())
    {
        myInkCollector.Renderer.PixelToInkSpace(g, ref offset);
    }
    // Use Ink API to paste the clipboard data into the Ink
    Strokes pastedStrokes = myInkCollector.Ink.ClipboardPaste(offset);

    // If the contents of the clipboard were a valid format 
    // (Ink Serialized Format or Embeddable OLE Object) and at
    // least one stroke was pasted into the ink, use a helper 
    // method to update the stroke selection.  Otherwise,
    // the result is null and this paste becomes a no-op.  
    if (null != pastedStrokes)
    {
        SetSelection(pastedStrokes);
    }
}
```



I comandi Seleziona e Input penna aggiornano la modalità applicazione e gli attributi di disegno predefiniti, cancellano la selezione corrente, aggiornano lo stato del menu e aggiornano il modulo. Altri gestori si basano sullo stato dell'applicazione per eseguire la funzione corretta, lasso o disposizione dell'input penna. Inoltre, il comando Seleziona aggiunge i gestori degli eventi [NewPackets](/previous-versions/ms567621(v=vs.100)) e [Stroke](/previous-versions/ms567622(v=vs.100)) all'agente di raccolta input penna e il comando Ink rimuove questi gestori eventi dall'agente di raccolta input penna.

I formati disponibili negli Appunti quando vengono copiati i tratti sono elencati nel menu Formato e l'utente seleziona il formato per copiare l'input penna da questo elenco. I tipi di formati disponibili includono Ink Serialized Format (ISF), metafile, metafile avanzato e bitmap. I formati di input penna di sketch e input penna di testo si escludono a vicenda e si basano sulla copia dell'input penna negli Appunti come oggetto OLE.

Il menu Stile consente all'utente di modificare le proprietà di colore e larghezza della penna e dei tratti selezionati.

Ad esempio, il comando Rosso imposta la [proprietà Color](/previous-versions/ms582103(v=vs.100)) della proprietà [DefaultDrawingAttributes](/previous-versions/ms571711(v=vs.100)) dell'agente di raccolta input penna sul colore rosso. Poiché la [proprietà DrawingAttributes](/previous-versions/ms581965(v=vs.100)) dell'oggetto [Cursor](/previous-versions/ms552104(v=vs.100)) non è stata impostata, qualsiasi nuovo input penna disegnato per l'agente di raccolta input penna eredita il colore di disegno predefinito. Inoltre, se sono attualmente selezionati tratti, viene aggiornata anche la proprietà Color degli attributi di disegno di ogni tratto.


```C++
private void SetColor(Color newColor)
{
    myInkCollector.DefaultDrawingAttributes.Color = newColor;

    // In addition to updating the ink collector, also update
    // the drawing attributes of all selected strokes.
    if (HasSelection())
    {
        foreach (Stroke s in selectedStrokes)
        {
            s.DrawingAttributes.Color = newColor;
        }
    }

    Refresh();
}
```



## <a name="handling-mouse-events"></a>Gestione degli eventi del mouse

Il [gestore dell'evento MouseMove](/previous-versions/ms567617(v=vs.100)) controlla la modalità dell'applicazione. Se la modalità è MoveInk e un pulsante del mouse è premuto, il gestore sposta i tratti usando il metodo Move della raccolta [Strokes](/previous-versions/ms552701(v=vs.100)) e aggiorna la casella di selezione. In caso contrario, il gestore verifica se il rettangolo di selezione contiene il cursore, abilita la raccolta input penna di conseguenza e imposta il cursore di conseguenza.

Il [gestore dell'evento MouseDown](/previous-versions/ms567616(v=vs.100)) controlla l'impostazione del cursore. Se il cursore è impostato su [SizeAll,](/dotnet/api/system.windows.forms.cursors.sizeall?view=netcore-3.1)il gestore imposta la modalità dell'applicazione su MoveInk e registra la posizione del cursore. In caso contrario, se è presente una selezione corrente, cancellarla.

Il [gestore dell'evento MouseUp](/previous-versions/ms567618(v=vs.100)) controlla la modalità dell'applicazione. Se la modalità è MoveInk, il gestore imposta la modalità dell'applicazione in base allo stato selezionato del comando Select.

[L'evento NewPackets](/previous-versions/ms567621(v=vs.100)) viene generato in modalità di selezione quando l'agente di raccolta input penna riceve nuovi dati del pacchetto. Se l'applicazione è in modalità di selezione, è necessario intercettare i nuovi pacchetti e usarli per disegnare il lasso di selezione.

La coordinata di ogni pacchetto viene convertita in pixel, vincolata all'area di disegno e aggiunta alla raccolta di punti del lazo. Viene quindi chiamato un metodo helper per disegnare il lasso nel form.

## <a name="handling-a-new-stroke"></a>Gestione di un nuovo tratto

[L'evento Stroke](/previous-versions/ms567622(v=vs.100)) viene generato in modalità di selezione quando viene disegnato un nuovo tratto. Se l'applicazione è in modalità di selezione, questo tratto corrisponde al lazo ed è necessario aggiornare le informazioni dei tratti selezionati.

Il gestore annulla l'evento [Stroke,](/previous-versions/ms567622(v=vs.100)) verifica la presenza di più di due punti di lazo, copia la raccolta Points in una matrice di oggetti [Point](/dotnet/api/system.drawing.point?view=netcore-3.1) e converte le coordinate dei punti nella matrice da pixel a spazio input penna. Il gestore usa quindi il metodo [HitTest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) dell'oggetto [Ink](/previous-versions/ms583670(v=vs.100)) per ottenere i tratti selezionati dai punti di lazo e aggiorna lo stato di selezione del form. Infine, il tratto che ha generato l'evento viene rimosso dalla raccolta di tratti selezionati, la raccolta Points lasso viene svuotata e un metodo helper disegna il rettangolo di selezione.


```C++
// This stroke corresponds to the lasso - 
// cancel it so that it is not added into the ink
e.Cancel = true;  

Strokes hitStrokes = null;

// If there are enough lasso points, perform a hit test
// to determine which strokes were selected. 
if (lassoPoints.Count > 2)
{

    // Convert the lasso points from pixels to ink space
    Point[] inkLassoPoints = (Point[])lassoPoints.ToArray(typeof(Point));
    using (Graphics g = CreateGraphics())
    {
        myInkCollector.Renderer.PixelToInkSpace(g, ref inkLassoPoints);
    }
    // Perform a hit test on this ink collector's ink to
    // determine which points were selected by the lasso stroke.
    //
    // Note that there is a slight inefficiency here since the
    // lasso stroke is part of the ink and, therefore, part of the
    // hit test - even though we don't need it.   It would have 
    // been more efficient to remove the stroke from the ink before 
    // calling HitTest.  However, it is not good practice to modify 
    // the stroke inside of its own event handler.
    hitStrokes = myInkCollector.Ink.HitTest(inkLassoPoints, LassoPercent);
    hitStrokes.Remove(e.Stroke);
}

// Reset the lasso points
lassoPoints.Clear();
lastDrawnLassoDot = Point.Empty;

// Use helper method to set the selection
SetSelection(hitStrokes);
```



## <a name="copying-ink-to-the-clipboard"></a>Copia dell'input penna negli Appunti

Il metodo helper CopyInkToClipboard crea un valore [InkClipboardFormats,](/previous-versions/ms583681(v=vs.100)) controlla lo stato del menu Formato per aggiornare i formati da inserire negli Appunti e usa il metodo [ClipboardCopy](/previous-versions/dotnet/netframework-3.5/ms571316(v=vs.90)) dell'oggetto [Ink](/previous-versions/ms583670(v=vs.100)) per copiare i tratti negli Appunti.


```C++
// Declare the ink clipboard formats to put on the clipboard
InkClipboardFormats formats = new InkClipboardFormats();

// Use selected format menu items to set the clipboard 
// formats
...

// If at least one format was selected, invoke the Ink
// API's ClipboardCopy method.  Note that selectedStrokes
// could be null, but that this is ok - if selectedStrokes
// is null, all of the ink is copied.
if (formats != InkClipboardFormats.None)
{
    myInkCollector.Ink.ClipboardCopy(selectedStrokes,formats,clipboardModes);
}
else
{
    MessageBox.Show("No clipboard formats selected");
}
```



## <a name="updating-a-selection"></a>Aggiornamento di una selezione

Il metodo helper SetSelection aggiorna le sequenze selezionate e, se la raccolta è **NULL** o **EMPTY,** il rettangolo di selezione viene impostato sul rettangolo vuoto. Se la raccolta [Strokes](/previous-versions/ms552701(v=vs.100)) selezionata non è vuota, il metodo SetSelection esegue i passaggi seguenti:

-   Determina il rettangolo di delimitazione usando [il metodo GetBoundingBox](/previous-versions/dotnet/netframework-3.5/ms571376(v=vs.90)) della raccolta strokes
-   Converte le coordinate del rettangolo dallo spazio input penna in pixel
-   Gonfia il rettangolo per fornire spazio visivo tra di esso e i tratti selezionati
-   Crea quadratini di selezione per la casella di selezione corrente

Infine, il metodo SetSelection imposta la visibilità dei punti di controllo di selezione e imposta la proprietà [AutoRedraw](/previous-versions/ms571706(v=vs.100)) dell'agente di raccolta input penna su **FALSE,** se i tratti sono selezionati.


```C++
// Tracks whether the rectangle that bounds the selected
// strokes should be displayed
bool isSelectionVisible = false;

// Update the selected strokes collection
selectedStrokes = strokes;

// If no strokes are selected, set the selection rectangle
// to empty
if (!HasSelection())
{
    selectionRect = Rectangle.Empty;
}
    // Otherwise, at least one stroke is selected and it is necessary
    // to display the selection rectangle.
else
{
    isSelectionVisible = true;

    // Retrieve the bounding box of the strokes
    selectionRect = selectedStrokes.GetBoundingBox();
    using (Graphics g = CreateGraphics())
    {
        InkSpaceToPixel(g, ref selectionRect);
    }

    // Pad the selection rectangle so that the selected ink 
    // doesn't overlap with the selection rectangle's handles.
    selectionRect.Inflate(SelectionRectBuffer, SelectionRectBuffer);

    // compute the center of the rectangle that bounds the 
    // selected strokes
    int xAvg = (selectionRect.Right+selectionRect.Left)/2;
    int yAvg = (selectionRect.Top+selectionRect.Bottom)/2;

    // Draw the resize handles
    // top left
    SetLocation(selectionHandles[0],selectionRect.Left, selectionRect.Top);
    // top
    SetLocation(selectionHandles[1],xAvg, selectionRect.Top);
    // top right 
    SetLocation(selectionHandles[2],selectionRect.Right, selectionRect.Top);

    // left 
    SetLocation(selectionHandles[3],selectionRect.Left, yAvg);
    // right
    SetLocation(selectionHandles[4],selectionRect.Right, yAvg);

    // bottom left
    SetLocation(selectionHandles[5],selectionRect.Left, selectionRect.Bottom);
    // bottom
    SetLocation(selectionHandles[6],xAvg, selectionRect.Bottom);
    // bottom right
    SetLocation(selectionHandles[7],selectionRect.Right, selectionRect.Bottom);
}

// Set the visibility of each selection handle in the 
// selection rectangle.  If there is no selection, all 
// handles should be hidden.  Otherwise, all handles should
// be visible.
foreach(PictureBox pb in selectionHandles)
{
    pb.Visible = isSelectionVisible;
}

// Turn off autoredrawing if there is a selection - otherwise,
// the selected ink is not displayed as selected.
myInkCollector.AutoRedraw = !isSelectionVisible;

// Since the selection has changed, repaint the screen.
Refresh();
```



## <a name="drawing-the-lasso"></a>Disegno del lasso

Il lazo viene disegnato come una serie di punti aperti che seguono il percorso del tratto lasso e una linea del connettore tratteggiata tra le due estremità. [L'evento NewPackets](/previous-versions/ms567621(v=vs.100)) viene generato durante la creazione del lasso e il gestore eventi passa le informazioni sul tratto al metodo DrawLasso.

Il metodo helper DrawLasso rimuove prima la linea del connettore precedente e quindi scorre i punti nel tratto. DrawLasso calcola quindi dove posizionare i punti lungo il tratto e li disegna. Infine, disegna una nuova linea del connettore.

## <a name="closing-the-form"></a>Chiusura del modulo

Il metodo [Dispose del](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) form elimina l'oggetto [InkCollector,](/previous-versions/ms583683(v=vs.100)) myInkCollector.

 

 
