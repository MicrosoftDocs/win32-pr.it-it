---
description: Questo programma di esempio illustra come eseguire lo zoom e lo scorrimento dell'input penna.
ms.assetid: d3b5668a-29bf-4846-8ab0-1bda7b6160f9
title: Esempio di zoom di input penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f20253a3f56b2a03b5a6dad45ab9a8b72090b5ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525285"
---
# <a name="ink-zoom-sample"></a>Esempio di zoom di input penna

Questo programma di esempio illustra come eseguire lo zoom e lo scorrimento dell'input penna. In particolare, consente all'utente di eseguire lo zoom avanti e indietro dell'input penna in incrementi. Viene inoltre illustrato come eseguire lo zoom in una determinata area utilizzando un rettangolo di zoom. Infine, in questo esempio viene illustrato come raccogliere input penna con diverse proporzioni di zoom e come impostare lo scorrimento all'interno dell'area di disegno ingrandita.

Nell'esempio le trasformazioni oggetto e visualizzazione dell'oggetto [renderer](/previous-versions/ms828481(v=msdn.10)) vengono usate per eseguire lo zoom e lo scorrimento. La trasformazione visualizzazione si applica ai punti e alla larghezza della penna. La trasformazione oggetto si applica solo ai punti. L'utente può controllare quale trasformazione viene utilizzata modificando l'elemento larghezza penna scala nel menu modalità.

> [!Note]  
> È problematico eseguire alcune chiamate COM su determinati metodi di interfaccia (ad esempio,[**InkRenderer. SetViewTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setviewtransform) e [**InkRenderer. SetObjectTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setobjecttransform)) quando è stato inviato un messaggio. Quando vengono inviati, i messaggi devono essere sottoposti a marshalling nella coda dei messaggi. Per risolvere questo scenario, verificare se si sta gestendo un messaggio da POST chiamando [**InSendMesssageEx**](/windows/desktop/api/winuser/nf-winuser-insendmessageex) e inviare il messaggio a se stesso se il messaggio è stato inviato.

 

In questo esempio vengono usate le funzionalità seguenti:

-   Oggetto [InkCollector](/previous-versions/ms583683(v=vs.100))
-   Metodo [SetViewTransform](/previous-versions/ms828514(v=msdn.10)) dell'oggetto [renderer](/previous-versions/ms828481(v=msdn.10))
-   Metodo [SetObjectTransform](/previous-versions/ms828513(v=msdn.10)) dell'oggetto [renderer](/previous-versions/ms828481(v=msdn.10))

## <a name="initializing-the-form"></a>Inizializzazione del form

In primo luogo, l'esempio fa riferimento alle interfacce di automazione di Tablet PC, fornite in Windows Vista o Windows XP Tablet PC Edition Software Development Kit (SDK).


```C++
using Microsoft.Ink;
```



Nell'esempio vengono dichiarati un oggetto [InkCollector](/previous-versions/ms583683(v=vs.100)), `myInkCollector` , e alcuni membri privati per semplificare la scalabilità.


```C++
// Declare the Ink Collector object
private InkCollector myInkCollector = null;
...
// The starting and ending points of the zoom rectangle
private Rectangle zoomRectangle = Rectangle.Empty;

// The current zoom factor (1 = 100% zoom level)
private float zoomFactor = 1;

// Declare constants for the width and height of the 
// drawing area (in ink space coordinates).
private const int InkSpaceWidth = 50000;
private const int InkSpaceHeight = 50000;
...
// Declare constant for the pen width used by this application
private const float MediumInkWidth = 100;
```



Quindi, l'esempio crea e Abilita l'oggetto [InkCollector](/previous-versions/ms583683(v=vs.100)) nel gestore dell'evento [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) del form. Inoltre, la proprietà [Width](/previous-versions/ms837941(v=msdn.10)) della proprietà [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) dell'oggetto InkCollector è impostata. Infine, vengono definiti gli intervalli della barra di scorrimento e `UpdateZoomAndScroll` viene chiamato il metodo dell'applicazione.


```C++
private void InkZoom_Load(object sender, System.EventArgs e)
{
   // Create the pen used to draw the zoom rectangle
    blackPen = new Pen(Color.Black, 1);

    // Create the ink collector and associate it with the form
    myInkCollector = new InkCollector(pnlDrawingArea.Handle);

    // Set the pen width
    myInkCollector.DefaultDrawingAttributes.Width = MediumInkWidth;

    // Enable ink collection
    myInkCollector.Enabled = true;

    // Define ink space size - note that the scroll bars
    // map directly to ink space
    hScrollBar.Minimum = 0;
    hScrollBar.Maximum = InkSpaceWidth;
    vScrollBar.Minimum = 0;
    vScrollBar.Maximum = InkSpaceHeight;

    // Set the scroll bars to map to the current zoom level
    UpdateZoomAndScroll();
}
```



## <a name="updating-the-zoom-and-scroll-values"></a>Aggiornamento dei valori di zoom e scorrimento

L'area di disegno dell'agente di raccolta input penna è interessata da molti eventi. Nel `UpdateZoomAndScroll` metodo, una matrice di trasformazione viene utilizzata per la scalabilità e la conversione dell'agente di raccolta input penna nella finestra.

> [!Note]  
> Il metodo [SetViewTransform](/previous-versions/ms828514(v=msdn.10)) dell'oggetto [renderer](/previous-versions/ms828481(v=msdn.10)) applica la trasformazione ai tratti e alla larghezza della penna, mentre il metodo [SetObjectTransform](/previous-versions/ms828513(v=msdn.10)) applica solo la trasformazione ai tratti.

 

Infine, `UpdateScrollBars` viene chiamato il metodo dell'applicazione e il form è forzato ad aggiornarsi.


```C++
// Create a transformation matrix
Matrix m = new Matrix();

// Apply the current scale factor
m.Scale(zoomFactor,zoomFactor);

// Apply the current translation factor - note that since 
// the scroll bars map directly to ink space, their values
// can be used directly.
m.Translate(-hScrollBar.Value, -vScrollBar.Value);

// ...
if (miScalePenWidth.Checked)
{
    myInkCollector.Renderer.SetViewTransform(m);
}
else
{
    myInkCollector.Renderer.SetObjectTransform(m);
}

// Set the scroll bars to map to the current zoom level
UpdateScrollBars();

Refresh();
```



## <a name="managing-the-scroll-bars"></a>Gestione delle barre di scorrimento

Il `UpdateScrollBars` metodo configura le barre di scorrimento per funzionare correttamente con le dimensioni correnti della finestra, l'impostazione dello zoom e la posizione di scorrimento all'interno dell'oggetto [InkCollector](/previous-versions/ms583683(v=vs.100)). Questo metodo consente di calcolare i valori di modifica di grandi dimensioni e di piccole dimensioni per le barre di scorrimento verticali e orizzontali. Calcola inoltre il valore corrente delle barre di scorrimento e indica se devono essere visibili. Il metodo [PixelToInkSpace](/previous-versions/ms828505(v=msdn.10)) dell'oggetto [renderer](/previous-versions/ms828481(v=msdn.10)) gestisce la conversione da pixel allo spazio delle coordinate con zoom e gli account per qualsiasi ridimensionamento e scorrimento applicato tramite le trasformazioni di visualizzazione e oggetto.


```C++
// Create a point representing the top left of the drawing area (in pixels)
Point ptUpperLeft = new Point(0, 0);

// Create a point representing the size of a small change
Point ptSmallChange = new Point(SmallChangeSize, SmallChangeSize);

// Create a point representing the lower right of the drawing area (in pixels)
Point ptLowerRight = new Point(hScrollBar.Width, vScrollBar.Height);

using (Graphics g = CreateGraphics())
{
    // Convert each of the points to ink space
    myInkCollector.Renderer.PixelToInkSpace(g, ref ptUpperLeft);
    myInkCollector.Renderer.PixelToInkSpace(g, ref ptLowerRight);
    myInkCollector.Renderer.PixelToInkSpace(g, ref ptSmallChange);
}

// Set the SmallChange values (in ink space)
// Note that it is necessary to subract the upper-left point
// value to account for scrolling.
hScrollBar.SmallChange = ptSmallChange.X - ptUpperLeft.X;
vScrollBar.SmallChange = ptSmallChange.Y - ptUpperLeft.Y;

// Set the LargeChange values to the drawing area width (in ink space)
// Note that it is necessary to subract the upper-left point
// value to account for scrolling.
hScrollBar.LargeChange = ptLowerRight.X - ptUpperLeft.X;
vScrollBar.LargeChange = ptLowerRight.Y - ptUpperLeft.Y;

// If the scroll bars are not needed, hide them
hScrollBar.Visible = hScrollBar.LargeChange < hScrollBar.Maximum;
vScrollBar.Visible = vScrollBar.LargeChange < vScrollBar.Maximum;

// If the horizontal scroll bar value would run off of the drawing area, 
// adjust it
if(hScrollBar.Visible && (hScrollBar.Value + hScrollBar.LargeChange > hScrollBar.Maximum)) 
{
    hScrollBar.Value = hScrollBar.Maximum - hScrollBar.LargeChange;
}

// If the vertical scroll bar value would run off of the drawing area, 
// adjust it
if(vScrollBar.Visible && (vScrollBar.Value + vScrollBar.LargeChange > vScrollBar.Maximum))
{
    vScrollBar.Value = vScrollBar.Maximum - vScrollBar.LargeChange;
}
```



## <a name="zooming-to-a-rectangle"></a>Zoom su un rettangolo

I `pnlDrawingArea` gestori eventi Panel gestiscono il disegno del rettangolo nella finestra. Se il comando zoom a Rect è selezionato nel menu modalità, il gestore dell'evento [MouseUp](/previous-versions/ms567618(v=vs.100)) chiama il metodo dell'applicazione `ZoomToRectangle` . Il `ZoomToRectangle` metodo calcola la larghezza e l'altezza del rettangolo, controlla le condizioni di limite, aggiorna i valori della barra di scorrimento e il fattore di scala, quindi chiama il `UpdateZoomAndScroll` metodo dell'applicazione per applicare le nuove impostazioni.

## <a name="closing-the-form"></a>Chiusura del modulo

Il metodo [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) del modulo Elimina l'oggetto [InkCollector](/previous-versions/ms583683(v=vs.100)) .

 

 
