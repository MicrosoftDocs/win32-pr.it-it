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
# <a name="ink-zoom-sample"></a><span data-ttu-id="93e31-103">Esempio di zoom di input penna</span><span class="sxs-lookup"><span data-stu-id="93e31-103">Ink Zoom Sample</span></span>

<span data-ttu-id="93e31-104">Questo programma di esempio illustra come eseguire lo zoom e lo scorrimento dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="93e31-104">This sample program demonstrates how to zoom and scroll ink.</span></span> <span data-ttu-id="93e31-105">In particolare, consente all'utente di eseguire lo zoom avanti e indietro dell'input penna in incrementi.</span><span class="sxs-lookup"><span data-stu-id="93e31-105">In particular, it enables the user to zoom in and out of ink in increments.</span></span> <span data-ttu-id="93e31-106">Viene inoltre illustrato come eseguire lo zoom in una determinata area utilizzando un rettangolo di zoom.</span><span class="sxs-lookup"><span data-stu-id="93e31-106">It also demonstrates how to zoom into a particular region using a zoom rectangle.</span></span> <span data-ttu-id="93e31-107">Infine, in questo esempio viene illustrato come raccogliere input penna con diverse proporzioni di zoom e come impostare lo scorrimento all'interno dell'area di disegno ingrandita.</span><span class="sxs-lookup"><span data-stu-id="93e31-107">Finally, this sample illustrates how to collect ink at different zoom ratios and how to set up scrolling within the zoomed drawing area.</span></span>

<span data-ttu-id="93e31-108">Nell'esempio le trasformazioni oggetto e visualizzazione dell'oggetto [renderer](/previous-versions/ms828481(v=msdn.10)) vengono usate per eseguire lo zoom e lo scorrimento.</span><span class="sxs-lookup"><span data-stu-id="93e31-108">In the sample, the [Renderer](/previous-versions/ms828481(v=msdn.10)) object's view and object transforms are used to perform zooming and scrolling.</span></span> <span data-ttu-id="93e31-109">La trasformazione visualizzazione si applica ai punti e alla larghezza della penna.</span><span class="sxs-lookup"><span data-stu-id="93e31-109">The view transform applies to the points and the pen width.</span></span> <span data-ttu-id="93e31-110">La trasformazione oggetto si applica solo ai punti.</span><span class="sxs-lookup"><span data-stu-id="93e31-110">The object transform applies only to the points.</span></span> <span data-ttu-id="93e31-111">L'utente può controllare quale trasformazione viene utilizzata modificando l'elemento larghezza penna scala nel menu modalità.</span><span class="sxs-lookup"><span data-stu-id="93e31-111">The user can control which transform is used by changing the Scale Pen Width item on the Mode menu.</span></span>

> [!Note]  
> <span data-ttu-id="93e31-112">È problematico eseguire alcune chiamate COM su determinati metodi di interfaccia (ad esempio,[**InkRenderer. SetViewTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setviewtransform) e [**InkRenderer. SetObjectTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setobjecttransform)) quando è stato inviato un messaggio.</span><span class="sxs-lookup"><span data-stu-id="93e31-112">It is problematic to perform some COM calls on certain interface methods ([**InkRenderer.SetViewTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setviewtransform) and [**InkRenderer.SetObjectTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setobjecttransform), for example) when a message has been SENT.</span></span> <span data-ttu-id="93e31-113">Quando vengono inviati, i messaggi devono essere sottoposti a marshalling nella coda dei messaggi.</span><span class="sxs-lookup"><span data-stu-id="93e31-113">When messages are SENT, they need to be marshalled to the POST message queue.</span></span> <span data-ttu-id="93e31-114">Per risolvere questo scenario, verificare se si sta gestendo un messaggio da POST chiamando [**InSendMesssageEx**](/windows/desktop/api/winuser/nf-winuser-insendmessageex) e inviare il messaggio a se stesso se il messaggio è stato inviato.</span><span class="sxs-lookup"><span data-stu-id="93e31-114">To address this scenario, test whether you are handling a message from POST by calling [**InSendMesssageEx**](/windows/desktop/api/winuser/nf-winuser-insendmessageex) and POST the message to yourself if the message was SENT.</span></span>

 

<span data-ttu-id="93e31-115">In questo esempio vengono usate le funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="93e31-115">The following features are used in this sample:</span></span>

-   <span data-ttu-id="93e31-116">Oggetto [InkCollector](/previous-versions/ms583683(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="93e31-116">The [InkCollector](/previous-versions/ms583683(v=vs.100)) object</span></span>
-   <span data-ttu-id="93e31-117">Metodo [SetViewTransform](/previous-versions/ms828514(v=msdn.10)) dell'oggetto [renderer](/previous-versions/ms828481(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="93e31-117">The [Renderer](/previous-versions/ms828481(v=msdn.10)) object's [SetViewTransform](/previous-versions/ms828514(v=msdn.10)) method</span></span>
-   <span data-ttu-id="93e31-118">Metodo [SetObjectTransform](/previous-versions/ms828513(v=msdn.10)) dell'oggetto [renderer](/previous-versions/ms828481(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="93e31-118">The [Renderer](/previous-versions/ms828481(v=msdn.10)) object's [SetObjectTransform](/previous-versions/ms828513(v=msdn.10)) method</span></span>

## <a name="initializing-the-form"></a><span data-ttu-id="93e31-119">Inizializzazione del form</span><span class="sxs-lookup"><span data-stu-id="93e31-119">Initializing the Form</span></span>

<span data-ttu-id="93e31-120">In primo luogo, l'esempio fa riferimento alle interfacce di automazione di Tablet PC, fornite in Windows Vista o Windows XP Tablet PC Edition Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="93e31-120">First, the sample references the Tablet PC Automation interfaces, which are provided in the Windows Vista or Windows XP Tablet PC Edition Software Development Kit (SDK).</span></span>


```C++
using Microsoft.Ink;
```



<span data-ttu-id="93e31-121">Nell'esempio vengono dichiarati un oggetto [InkCollector](/previous-versions/ms583683(v=vs.100)), `myInkCollector` , e alcuni membri privati per semplificare la scalabilità.</span><span class="sxs-lookup"><span data-stu-id="93e31-121">The sample declares an [InkCollector](/previous-versions/ms583683(v=vs.100)), `myInkCollector`, and some private members to help with scaling.</span></span>


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



<span data-ttu-id="93e31-122">Quindi, l'esempio crea e Abilita l'oggetto [InkCollector](/previous-versions/ms583683(v=vs.100)) nel gestore dell'evento [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) del form.</span><span class="sxs-lookup"><span data-stu-id="93e31-122">Then the sample creates and enables the [InkCollector](/previous-versions/ms583683(v=vs.100)) in the form's [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) event handler.</span></span> <span data-ttu-id="93e31-123">Inoltre, la proprietà [Width](/previous-versions/ms837941(v=msdn.10)) della proprietà [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) dell'oggetto InkCollector è impostata.</span><span class="sxs-lookup"><span data-stu-id="93e31-123">Also, the [Width](/previous-versions/ms837941(v=msdn.10)) property of the InkCollector object's [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) property is set.</span></span> <span data-ttu-id="93e31-124">Infine, vengono definiti gli intervalli della barra di scorrimento e `UpdateZoomAndScroll` viene chiamato il metodo dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="93e31-124">Finally, the scroll bar ranges are defined and the application's `UpdateZoomAndScroll` method is called.</span></span>


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



## <a name="updating-the-zoom-and-scroll-values"></a><span data-ttu-id="93e31-125">Aggiornamento dei valori di zoom e scorrimento</span><span class="sxs-lookup"><span data-stu-id="93e31-125">Updating the Zoom and Scroll Values</span></span>

<span data-ttu-id="93e31-126">L'area di disegno dell'agente di raccolta input penna è interessata da molti eventi.</span><span class="sxs-lookup"><span data-stu-id="93e31-126">The drawing area of the ink collector is affected by many events.</span></span> <span data-ttu-id="93e31-127">Nel `UpdateZoomAndScroll` metodo, una matrice di trasformazione viene utilizzata per la scalabilità e la conversione dell'agente di raccolta input penna nella finestra.</span><span class="sxs-lookup"><span data-stu-id="93e31-127">In the `UpdateZoomAndScroll` method, a transformation matrix is used to both scale and translate the ink collector within the window.</span></span>

> [!Note]  
> <span data-ttu-id="93e31-128">Il metodo [SetViewTransform](/previous-versions/ms828514(v=msdn.10)) dell'oggetto [renderer](/previous-versions/ms828481(v=msdn.10)) applica la trasformazione ai tratti e alla larghezza della penna, mentre il metodo [SetObjectTransform](/previous-versions/ms828513(v=msdn.10)) applica solo la trasformazione ai tratti.</span><span class="sxs-lookup"><span data-stu-id="93e31-128">The [Renderer](/previous-versions/ms828481(v=msdn.10)) object's [SetViewTransform](/previous-versions/ms828514(v=msdn.10)) method applies the transform to both the strokes and the pen width, while the [SetObjectTransform](/previous-versions/ms828513(v=msdn.10)) method only applies the transform to the strokes.</span></span>

 

<span data-ttu-id="93e31-129">Infine, `UpdateScrollBars` viene chiamato il metodo dell'applicazione e il form è forzato ad aggiornarsi.</span><span class="sxs-lookup"><span data-stu-id="93e31-129">Finally, the application's `UpdateScrollBars` method is called and the form is forced to refresh.</span></span>


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



## <a name="managing-the-scroll-bars"></a><span data-ttu-id="93e31-130">Gestione delle barre di scorrimento</span><span class="sxs-lookup"><span data-stu-id="93e31-130">Managing the Scroll Bars</span></span>

<span data-ttu-id="93e31-131">Il `UpdateScrollBars` metodo configura le barre di scorrimento per funzionare correttamente con le dimensioni correnti della finestra, l'impostazione dello zoom e la posizione di scorrimento all'interno dell'oggetto [InkCollector](/previous-versions/ms583683(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="93e31-131">The `UpdateScrollBars` method sets up the scroll bars to work correctly with the current window size, zoom setting, and scroll location within the [InkCollector](/previous-versions/ms583683(v=vs.100)).</span></span> <span data-ttu-id="93e31-132">Questo metodo consente di calcolare i valori di modifica di grandi dimensioni e di piccole dimensioni per le barre di scorrimento verticali e orizzontali.</span><span class="sxs-lookup"><span data-stu-id="93e31-132">This method calculates the large change and small change values for the vertical and horizontal scroll bars.</span></span> <span data-ttu-id="93e31-133">Calcola inoltre il valore corrente delle barre di scorrimento e indica se devono essere visibili.</span><span class="sxs-lookup"><span data-stu-id="93e31-133">It also calculates the current value of the scroll bars and whether they should be visible.</span></span> <span data-ttu-id="93e31-134">Il metodo [PixelToInkSpace](/previous-versions/ms828505(v=msdn.10)) dell'oggetto [renderer](/previous-versions/ms828481(v=msdn.10)) gestisce la conversione da pixel allo spazio delle coordinate con zoom e gli account per qualsiasi ridimensionamento e scorrimento applicato tramite le trasformazioni di visualizzazione e oggetto.</span><span class="sxs-lookup"><span data-stu-id="93e31-134">The [Renderer](/previous-versions/ms828481(v=msdn.10)) object's [PixelToInkSpace](/previous-versions/ms828505(v=msdn.10)) method handles the conversion from pixels to the zoomed coordinate space and accounts for any scaling and scrolling that is applied through the view and object transforms.</span></span>


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



## <a name="zooming-to-a-rectangle"></a><span data-ttu-id="93e31-135">Zoom su un rettangolo</span><span class="sxs-lookup"><span data-stu-id="93e31-135">Zooming to a Rectangle</span></span>

<span data-ttu-id="93e31-136">I `pnlDrawingArea` gestori eventi Panel gestiscono il disegno del rettangolo nella finestra.</span><span class="sxs-lookup"><span data-stu-id="93e31-136">The `pnlDrawingArea` panel event handlers manage drawing the rectangle to the window.</span></span> <span data-ttu-id="93e31-137">Se il comando zoom a Rect è selezionato nel menu modalità, il gestore dell'evento [MouseUp](/previous-versions/ms567618(v=vs.100)) chiama il metodo dell'applicazione `ZoomToRectangle` .</span><span class="sxs-lookup"><span data-stu-id="93e31-137">If the Zoom To Rect command is checked on the Mode menu, then the [MouseUp](/previous-versions/ms567618(v=vs.100)) event handler calls the application's `ZoomToRectangle` method.</span></span> <span data-ttu-id="93e31-138">Il `ZoomToRectangle` metodo calcola la larghezza e l'altezza del rettangolo, controlla le condizioni di limite, aggiorna i valori della barra di scorrimento e il fattore di scala, quindi chiama il `UpdateZoomAndScroll` metodo dell'applicazione per applicare le nuove impostazioni.</span><span class="sxs-lookup"><span data-stu-id="93e31-138">The `ZoomToRectangle` method calculates the width and height of the rectangle, checks for boundary conditions, updates the scroll bar values and the scale factor, and then calls the application's `UpdateZoomAndScroll` method to apply the new settings.</span></span>

## <a name="closing-the-form"></a><span data-ttu-id="93e31-139">Chiusura del modulo</span><span class="sxs-lookup"><span data-stu-id="93e31-139">Closing the Form</span></span>

<span data-ttu-id="93e31-140">Il metodo [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) del modulo Elimina l'oggetto [InkCollector](/previous-versions/ms583683(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="93e31-140">The form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method disposes the [InkCollector](/previous-versions/ms583683(v=vs.100)) object.</span></span>

 

 
