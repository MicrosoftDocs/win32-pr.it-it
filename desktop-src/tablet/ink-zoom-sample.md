---
description: Questo programma di esempio illustra come fare zoom e scorrere l'input penna.
ms.assetid: d3b5668a-29bf-4846-8ab0-1bda7b6160f9
title: Esempio di zoom input penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d786fe502e1510a44df39049e845f05694a1befae0d4a21bcfa2ba2bd2b19b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939441"
---
# <a name="ink-zoom-sample"></a>Esempio di zoom input penna

Questo programma di esempio illustra come fare zoom e scorrere l'input penna. In particolare, consente all'utente di eseguire lo zoom avanti e indietro dell'input penna in incrementi. Illustra anche come eseguire lo zoom avanti in una determinata area usando un rettangolo di zoom. Infine, questo esempio illustra come raccogliere input penna con proporzioni di zoom diverse e come configurare lo scorrimento all'interno dell'area di disegno ingrandita.

Nell'esempio le trasformazioni di visualizzazione e oggetto dell'oggetto [Renderer](/previous-versions/ms828481(v=msdn.10)) vengono usate per eseguire lo zoom e lo scorrimento. La trasformazione della visualizzazione si applica ai punti e alla larghezza della penna. La trasformazione dell'oggetto si applica solo ai punti. L'utente può controllare quale trasformazione viene usata modificando la voce Ridimensiona larghezza penna nel menu Modalità.

> [!Note]  
> È problematico eseguire alcune chiamate COM su determinati metodi di interfaccia ([**InkRenderer.SetViewTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setviewtransform) e [**InkRenderer.SetObjectTransform,**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setobjecttransform)ad esempio) quando un messaggio è stato inviato. Quando i messaggi vengono inviati, è necessario eseguire il marshalling nella coda di messaggi POST. Per risolvere questo scenario, verificare se si sta gestendo un messaggio da POST chiamando [**InSendMesssageEx**](/windows/desktop/api/winuser/nf-winuser-insendmessageex) e POST per se il messaggio è stato inviato.

 

In questo esempio vengono usate le funzionalità seguenti:

-   Oggetto [InkCollector](/previous-versions/ms583683(v=vs.100))
-   Metodo [SetViewTransform dell'oggetto](/previous-versions/ms828514(v=msdn.10)) [Renderer](/previous-versions/ms828481(v=msdn.10))
-   Metodo [SetObjectTransform dell'oggetto](/previous-versions/ms828513(v=msdn.10)) [Renderer](/previous-versions/ms828481(v=msdn.10))

## <a name="initializing-the-form"></a>Inizializzazione del form

In primo luogo, l'esempio fa riferimento alle interfacce di automazione di Tablet PC, disponibili in Windows Vista o Windows XP Tablet PC Edition Software Development Kit (SDK).


```C++
using Microsoft.Ink;
```



L'esempio dichiara un [InkCollector](/previous-versions/ms583683(v=vs.100)), e alcuni membri privati per `myInkCollector` facilitare il ridimensionamento.


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



L'esempio crea e abilita [InkCollector](/previous-versions/ms583683(v=vs.100)) nel gestore dell'evento [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) del form. Viene inoltre [impostata](/previous-versions/ms837941(v=msdn.10)) la proprietà Width della proprietà [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) dell'oggetto InkCollector. Infine, vengono definiti gli intervalli della barra di scorrimento e viene chiamato `UpdateZoomAndScroll` il metodo dell'applicazione.


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

L'area di disegno dell'agente di raccolta input penna è interessata da molti eventi. Nel metodo viene usata una matrice di trasformazione per ridimensionare e traslare l'agente di raccolta `UpdateZoomAndScroll` input penna all'interno della finestra.

> [!Note]  
> Il metodo [SetViewTransform](/previous-versions/ms828514(v=msdn.10)) dell'oggetto [Renderer](/previous-versions/ms828481(v=msdn.10)) applica la trasformazione sia ai tratti che alla larghezza della penna, mentre il metodo [SetObjectTransform](/previous-versions/ms828513(v=msdn.10)) applica la trasformazione solo ai tratti.

 

Infine, viene chiamato il `UpdateScrollBars` metodo dell'applicazione e viene forzato l'aggiornamento del form.


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

Il metodo configura le barre di scorrimento in modo che funzionino correttamente con le dimensioni della finestra corrente, l'impostazione dello zoom e la posizione di scorrimento `UpdateScrollBars` all'interno di [InkCollector.](/previous-versions/ms583683(v=vs.100)) Questo metodo calcola i valori delle modifiche di grandi dimensioni e di piccole dimensioni per le barre di scorrimento verticale e orizzontale. Calcola inoltre il valore corrente delle barre di scorrimento e indica se devono essere visibili. Il metodo [PixelToInkSpace](/previous-versions/ms828505(v=msdn.10)) dell'oggetto [Renderer](/previous-versions/ms828481(v=msdn.10)) gestisce la conversione dai pixel allo spazio delle coordinate ingrandito e rappresenta qualsiasi ridimensionamento e scorrimento applicato nelle trasformazioni di visualizzazione e oggetto.


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

I `pnlDrawingArea` gestori eventi del pannello gestiscono il disegno del rettangolo nella finestra. Se il comando Zoom su rect è selezionato nel menu Modalità, il gestore [dell'evento MouseUp](/previous-versions/ms567618(v=vs.100)) chiama il metodo dell'applicazione. `ZoomToRectangle` Il metodo calcola la larghezza e l'altezza del rettangolo, verifica le condizioni limite, aggiorna i valori della barra di scorrimento e il fattore di scala e quindi chiama il metodo dell'applicazione per applicare le `ZoomToRectangle` `UpdateZoomAndScroll` nuove impostazioni.

## <a name="closing-the-form"></a>Chiusura del modulo

Il metodo [Dispose del](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) form elimina l'oggetto [InkCollector.](/previous-versions/ms583683(v=vs.100))

 

 
