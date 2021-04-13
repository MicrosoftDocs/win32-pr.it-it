---
description: Questo programma illustra come copiare e incollare input penna in un'altra applicazione. Consente inoltre all'utente di copiare una selezione di tratti e incollare il risultato nell'oggetto Ink esistente.
ms.assetid: a0c42f1c-543d-44f8-83d9-fe810de410ff
title: Esempio di appunti Ink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95c5da0bc0ba9a7e3a1b4e1a5c52784f10fb2023
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525969"
---
# <a name="ink-clipboard-sample"></a>Esempio di appunti Ink

Questo programma illustra come copiare e incollare input penna in un'altra applicazione. Consente inoltre all'utente di copiare una selezione di tratti e incollare il risultato nell'oggetto Ink esistente.

Sono disponibili le modalità degli Appunti seguenti:

-   Formato ISF (Ink Serialized Format)
-   Metafile
-   Enhanced Metafile (EMF)
-   Bitmap
-   Input penna
-   Disegna input penna

Input penna e sketch input penna sono due tipi di controlli input penna utilizzati rispettivamente come testo o come disegno. È possibile incollare ISF, input penna e sketch Ink nell'input penna esistente.

Oltre agli Appunti, questo esempio illustra anche come selezionare i tratti con lo strumento lazo. L'utente può spostare i tratti selezionati e modificarne gli attributi di disegno. Questa funzionalità è un subset della funzionalità di selezione già fornita dal controllo overlay dell'input penna. viene implementato qui a scopo illustrativo.

In questo esempio vengono usate le funzionalità seguenti:

-   Oggetto [InkCollector](/previous-versions/ms583683(v=vs.100)) .
-   Supporto degli Appunti di input penna.
-   Uso del lazo con il metodo [Microsoft. Ink. Ink. HitTest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) .

In questo esempio viene illustrato come eseguire il rendering dell'input penna, copiare l'input penna e quindi incollare l'input penna in un'altra applicazione, ad esempio Microsoft Paint.

## <a name="collecting-ink-and-setting-up-the-form"></a>Raccolta di input penna e configurazione del modulo

Per prima cosa, fare riferimento alle interfacce di automazione di Tablet PC, installate con Microsoft Windows <entity type="reg"/> XP Tablet PC Edition Software Development Kit (SDK).


```C++
using Microsoft.Ink;
```



Successivamente, il form dichiara alcune costanti e i campi che sono indicati più avanti in questo esempio.


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



Infine, nel gestore dell'evento [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) del form, il form viene inizializzato, viene creato un oggetto [InkCollector](/previous-versions/ms583683(v=vs.100)) per il form e l'agente di raccolta input penna è abilitato.


```C++
// Create an ink collector and assign it to this form's window
myInkCollector = new InkCollector(this.Handle);

// Turn the ink collector on
myInkCollector.Enabled = true;
```



## <a name="handling-menu-events"></a>Gestione degli eventi di menu

I gestori eventi delle voci di menu aggiornano principalmente lo stato del modulo.

Il comando Clear rimuove il rettangolo di selezione ed Elimina i tratti dall'oggetto [Ink](/previous-versions/ms583670(v=vs.100)) dell'agente di raccolta input penna.

Il comando Exit Disabilita l'agente di raccolta input penna prima di uscire dall'applicazione.

Il menu modifica Abilita i comandi taglia e copia in base allo stato di selezione del form e Abilita il comando Incolla in base al contenuto degli Appunti, determinato tramite il metodo [CanPaste](/previous-versions/dotnet/netframework-3.5/ms571314(v=vs.90)) dell'oggetto [Ink](/previous-versions/ms583670(v=vs.100)) .

I comandi taglia e copia usano entrambi un metodo helper per copiare l'input penna negli Appunti. Il comando Taglia USA un metodo helper per eliminare i tratti selezionati.

Il comando Incolla controlla prima di tutto il metodo [CanPaste](/previous-versions/dotnet/netframework-3.5/ms571314(v=vs.90)) dell'oggetto [Ink](/previous-versions/ms583670(v=vs.100)) per verificare se l'oggetto negli Appunti può essere incollato. Il comando Incolla quindi calcola l'angolo superiore sinistro per l'area di Incolla, converte le coordinate da pixel a spazio di input penna e incolla i tratti dagli Appunti nell'agente di raccolta input penna. Infine, viene aggiornata la casella di selezione.


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



I comandi SELECT e Ink aggiornano la modalità dell'applicazione e gli attributi di disegno predefiniti, cancellano la selezione corrente, aggiornano lo stato del menu e aggiornano il modulo. Gli altri gestori si basano sullo stato dell'applicazione per eseguire la funzione corretta, ovvero il lazo o la disinstallazione dell'input penna. Inoltre, il comando SELECT aggiunge i gestori eventi [NewPackets](/previous-versions/ms567621(v=vs.100)) e [Stroke](/previous-versions/ms567622(v=vs.100)) all'agente di raccolta input penna e il comando Ink rimuove i gestori eventi dall'agente di raccolta input penna.

I formati disponibili negli Appunti quando vengono copiati i tratti sono elencati nel menu formato e l'utente seleziona il formato per la copia dell'input penna da questo elenco. I tipi di formati disponibili includono il formato ISF (Ink Serialized Format), metafile, Enhanced Metafile e bitmap. I formati di sketch Ink e Text Ink si escludono a vicenda e si basano sull'input penna copiato negli Appunti come oggetto OLE.

Il menu stile consente all'utente di modificare le proprietà relative al colore e alla larghezza della penna e dei tratti selezionati.

Ad esempio, il comando rosso imposta la proprietà [color](/previous-versions/ms582103(v=vs.100)) della proprietà [DefaultDrawingAttributes](/previous-versions/ms571711(v=vs.100)) dell'agente di raccolta input penna sul colore rosso. Poiché la proprietà [DrawingAttributes](/previous-versions/ms581965(v=vs.100)) dell'oggetto [cursore](/previous-versions/ms552104(v=vs.100)) non è stata impostata, qualsiasi nuovo input penna creato nell'agente di raccolta input penna eredita il colore predefinito del disegno. Inoltre, se sono attualmente selezionati tratti, viene aggiornata anche la proprietà Color degli attributi di disegno di ciascun tratto.


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

Il gestore dell'evento [MouseMove](/previous-versions/ms567617(v=vs.100)) controlla la modalità dell'applicazione. Se la modalità è MoveInk e un pulsante del mouse è inattivo, il gestore sposta i tratti usando il metodo Move della raccolta [Strokes](/previous-versions/ms552701(v=vs.100)) e aggiorna la casella di selezione. In caso contrario, il gestore verifica per determinare se il rettangolo di selezione contiene il cursore, Abilita la raccolta di input penna di conseguenza e imposta di conseguenza il cursore.

Il gestore eventi [MouseDown](/previous-versions/ms567616(v=vs.100)) controlla l'impostazione del cursore. Se il cursore è impostato su [SizeAll](/dotnet/api/system.windows.forms.cursors.sizeall?view=netcore-3.1), il gestore imposta la modalità dell'applicazione su MoveInk e registra la posizione del cursore. In caso contrario, se è presente una selezione corrente, deselezionarla.

Il gestore dell'evento [MouseUp](/previous-versions/ms567618(v=vs.100)) controlla la modalità dell'applicazione. Se la modalità è MoveInk, il gestore imposta la modalità dell'applicazione in base allo stato selezionato del comando SELECT.

L'evento [NewPackets](/previous-versions/ms567621(v=vs.100)) viene generato in modalità di selezione quando l'agente di raccolta input penna riceve nuovi dati del pacchetto. Se l'applicazione è in modalità di selezione, è necessario intercettare i nuovi pacchetti e usarli per creare il lazo di selezione.

La coordinata di ogni pacchetto viene convertita in pixel, vincolata all'area di disegno e aggiunta alla raccolta di punti del lazo. Viene quindi chiamato un metodo helper per creare il lazo sul form.

## <a name="handling-a-new-stroke"></a>Gestione di un nuovo tratto

Quando viene disegnato un nuovo tratto, l'evento [Stroke](/previous-versions/ms567622(v=vs.100)) viene generato in modalità di selezione. Se l'applicazione è in modalità di selezione, questo tratto corrisponde al lazo ed è necessario aggiornare le informazioni sui tratti selezionati.

Il gestore Annulla l'evento [Stroke](/previous-versions/ms567622(v=vs.100)) , verifica la presenza di più di due punti lazo, copia la raccolta Points in una matrice di oggetti [Point](/dotnet/api/system.drawing.point?view=netcore-3.1) e converte le coordinate dei punti della matrice da pixel a spazio di input penna. Quindi, il gestore usa il metodo [HitTest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) dell'oggetto [Ink](/previous-versions/ms583670(v=vs.100)) per ottenere i tratti selezionati dai punti di lazo e aggiorna lo stato di selezione del form. Infine, il tratto che ha generato l'evento viene rimosso dalla raccolta dei tratti selezionati, la raccolta di punti lazo viene svuotata e un metodo helper disegna il rettangolo di selezione.


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

Il metodo helper CopyInkToClipboard crea un valore [InkClipboardFormats](/previous-versions/ms583681(v=vs.100)) , controlla lo stato del menu formato per aggiornare i formati da inserire negli Appunti e usa il metodo [ClipboardCopy](/previous-versions/dotnet/netframework-3.5/ms571316(v=vs.90)) dell'oggetto [Ink](/previous-versions/ms583670(v=vs.100)) per copiare i tratti negli Appunti.


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

Il metodo helper seselectation aggiorna il selectedStrokes archiviato e, se la raccolta è **null** o **vuota**, il rettangolo di selezione viene impostato sul rettangolo vuoto. Se la raccolta [Strokes](/previous-versions/ms552701(v=vs.100)) selezionata non è vuota, il metodo di selezione esegue i passaggi seguenti:

-   Determina il rettangolo di delimitazione usando il metodo [GetBoundingBox](/previous-versions/dotnet/netframework-3.5/ms571376(v=vs.90)) della raccolta Strokes
-   Converte le coordinate del rettangolo dallo spazio dell'input penna ai pixel
-   Ingrandisce il rettangolo per fornire uno spazio visivo tra l'oggetto e i tratti selezionati.
-   Crea gli handle di selezione per la casella di selezione corrente

Infine, il metodo seselectation imposta la visibilità degli handle di selezione e imposta la proprietà [AutoRedraw](/previous-versions/ms571706(v=vs.100)) dell'agente di raccolta input penna su **false**, se i tratti sono selezionati.


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



## <a name="drawing-the-lasso"></a>Disegno del lazo

Il lazo viene disegnato come una serie di punti aperti che seguono il percorso del tratto del lazo e una linea del connettore tratteggiata tra le due estremità. L'evento [NewPackets](/previous-versions/ms567621(v=vs.100)) viene generato durante il disegno del lazo e il gestore dell'evento passa le informazioni sul tratto al metodo DrawLasso.

Il metodo helper DrawLasso rimuove prima di tutto la vecchia riga del connettore e quindi scorre i punti del tratto. Quindi, DrawLasso calcola dove posizionare i punti lungo il tratto e li disegna. Infine, viene disegnata una nuova linea di connessione.

## <a name="closing-the-form"></a>Chiusura del modulo

Il metodo [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) del modulo Elimina l'oggetto [InkCollector](/previous-versions/ms583683(v=vs.100)) , ovvero InkCollector.

 

 
