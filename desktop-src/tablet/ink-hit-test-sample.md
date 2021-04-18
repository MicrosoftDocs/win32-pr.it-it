---
description: In questo esempio vengono illustrati due metodi per trovare l'input penna, data una posizione dello schermo.
ms.assetid: fc581da4-0a7b-4c31-8f73-0784066fcc56
title: Esempio di hit test di input penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d25e6cbc0ed471384bea0cc1977dd38d3ae4830
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306747"
---
# <a name="ink-hit-test-sample"></a><span data-ttu-id="f141d-103">Esempio di hit test di input penna</span><span class="sxs-lookup"><span data-stu-id="f141d-103">Ink Hit Test Sample</span></span>

<span data-ttu-id="f141d-104">In questo esempio vengono illustrati due metodi per trovare l'input penna, data una posizione dello schermo.</span><span class="sxs-lookup"><span data-stu-id="f141d-104">This sample illustrates two methods to find ink, given a screen location.</span></span>

<span data-ttu-id="f141d-105">In questo esempio vengono usate le funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="f141d-105">The following features are used in this sample:</span></span>

-   <span data-ttu-id="f141d-106">Uso di un agente di raccolta input penna</span><span class="sxs-lookup"><span data-stu-id="f141d-106">Using an ink collector</span></span>
-   <span data-ttu-id="f141d-107">Esecuzione di un hit test</span><span class="sxs-lookup"><span data-stu-id="f141d-107">Performing a hit test</span></span>
-   <span data-ttu-id="f141d-108">Individuazione del punto più vicino</span><span class="sxs-lookup"><span data-stu-id="f141d-108">Locating the nearest point</span></span>

## <a name="accessing-the-ink-api"></a><span data-ttu-id="f141d-109">Accesso all'API Ink</span><span class="sxs-lookup"><span data-stu-id="f141d-109">Accessing the Ink API</span></span>

<span data-ttu-id="f141d-110">Per prima cosa, fare riferimento alle classi di Tablet PC, che si trovano in Windows Vista o Windows XP Tablet PC Edition Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="f141d-110">First, reference the Tablet PC classes, located in the Windows Vista or Windows XP Tablet PC Edition Software Development Kit (SDK).</span></span>


```C++
using Microsoft.Ink;
```



## <a name="handling-form-load-and-paint-events"></a><span data-ttu-id="f141d-111">Gestione degli eventi di caricamento e disegno dei moduli</span><span class="sxs-lookup"><span data-stu-id="f141d-111">Handling Form Load and Paint Events</span></span>

<span data-ttu-id="f141d-112">Gestore dell'evento Load del form:</span><span class="sxs-lookup"><span data-stu-id="f141d-112">The form's Load event handler:</span></span>

-   <span data-ttu-id="f141d-113">Crea un oggetto [InkCollector](/previous-versions/ms583683(v=vs.100)) , IC, per il form.</span><span class="sxs-lookup"><span data-stu-id="f141d-113">Creates an [InkCollector](/previous-versions/ms583683(v=vs.100)) object, ic, for the form.</span></span>
-   <span data-ttu-id="f141d-114">Imposta la proprietà [CollectionMode](/previous-versions/ms836497(v=msdn.10)) dell'oggetto [InkCollector](/previous-versions/ms583683(v=vs.100)) per ignorare i movimenti.</span><span class="sxs-lookup"><span data-stu-id="f141d-114">Sets the [InkCollector](/previous-versions/ms583683(v=vs.100)) object's [CollectionMode](/previous-versions/ms836497(v=msdn.10)) property to ignore gestures.</span></span>
-   <span data-ttu-id="f141d-115">Abilita l'oggetto [InkCollector](/previous-versions/ms583683(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="f141d-115">Enables the [InkCollector](/previous-versions/ms583683(v=vs.100)).</span></span>
-   <span data-ttu-id="f141d-116">Imposta la proprietà [AutoRedraw](/previous-versions/ms836495(v=msdn.10)) dell'oggetto [InkCollector](/previous-versions/ms583683(v=vs.100)) su **true**.</span><span class="sxs-lookup"><span data-stu-id="f141d-116">Sets the [InkCollector](/previous-versions/ms583683(v=vs.100)) object's [AutoRedraw](/previous-versions/ms836495(v=msdn.10)) property to **TRUE**.</span></span>


```C++
// Create the InkCollector, and turn it on
ic = new InkCollector(Handle);  // attach it to the form's frame window

// default to ink-enabled mode
mode = ApplicationMode.Ink;
ic.CollectionMode = CollectionMode.InkOnly;

// turn the collector on
ic.Enabled = true;ic.AutoRedraw = true;
```



<span data-ttu-id="f141d-117">Il gestore dell'evento Paint del modulo controlla la modalità dell'applicazione:</span><span class="sxs-lookup"><span data-stu-id="f141d-117">The form's Paint event handler checks the application mode:</span></span>

-   <span data-ttu-id="f141d-118">In modalità HitTest, disegna un cerchio intorno al cursore.</span><span class="sxs-lookup"><span data-stu-id="f141d-118">In the HitTest mode, it paints a circle around the cursor.</span></span> <span data-ttu-id="f141d-119">Il puntatore attivo viene impostato nel metodo handleHitTest dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f141d-119">The active pen is set in the application's handleHitTest method.</span></span>
-   <span data-ttu-id="f141d-120">In modalità NearestPoint, disegna una linea rossa tra il cursore e il punto più vicino al cursore.</span><span class="sxs-lookup"><span data-stu-id="f141d-120">In the NearestPoint mode, it paints a red line between the cursor and the point nearest the cursor.</span></span> <span data-ttu-id="f141d-121">Il punto più vicino viene calcolato nel metodo handleNearestPoint dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f141d-121">The nearest point is calculated in the application's handleNearestPoint method.</span></span>


```C++
if( mode == ApplicationMode.HitTest)
{
    e.Graphics.DrawEllipse(activepen, penPt.X - HitSize/2, penPt.Y - HitSize/2, HitSize, HitSize);
}
else if( mode == ApplicationMode.NearestPoint )
{
    e.Graphics.DrawLine(redPen, penPt, nearestPt);
}
```



<span data-ttu-id="f141d-122">Questo esempio ha un algoritmo di ridisegno molto semplice.</span><span class="sxs-lookup"><span data-stu-id="f141d-122">This sample has a very straightforward repaint algorithm.</span></span> <span data-ttu-id="f141d-123">Con la proprietà [AutoRedraw](/previous-versions/ms836495(v=msdn.10)) impostata su **true**, l'agente di raccolta input penna si ridipinge quando il modulo viene ridisegnato.</span><span class="sxs-lookup"><span data-stu-id="f141d-123">With its [AutoRedraw](/previous-versions/ms836495(v=msdn.10)) property set to **TRUE**, the ink collector repaints itself when the form is redrawn.</span></span> <span data-ttu-id="f141d-124">Per semplificare il ridisegno del form, l'applicazione tiene traccia di un rettangolo di delimitazione, della variabile membro invalidateRect, per l'area in cui viene aggiunto Paint, che viene invalidato ogni volta che viene ridisegnato il modulo.</span><span class="sxs-lookup"><span data-stu-id="f141d-124">To simplify redrawing the form, the application tracks a bounding box, the invalidateRect member variable, for the area where paint is added, which is invalidated each time the form is redrawn.</span></span>

## <a name="handling-menu-events"></a><span data-ttu-id="f141d-125">Gestione degli eventi di menu</span><span class="sxs-lookup"><span data-stu-id="f141d-125">Handling Menu Events</span></span>

<span data-ttu-id="f141d-126">Il comando Exit Disabilita l'oggetto [InkCollector](/previous-versions/ms583683(v=vs.100)) prima di uscire dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f141d-126">The Exit command disables the [InkCollector](/previous-versions/ms583683(v=vs.100)) before exiting the application.</span></span>

<span data-ttu-id="f141d-127">Il comando Ink aggiorna la modalità dell'applicazione e lo stato del menu, Abilita l'agente di raccolta input penna e invalida l'area precedentemente disegnata del modulo.</span><span class="sxs-lookup"><span data-stu-id="f141d-127">The Ink command updates the application mode and menu status, enables the ink collector, and invalidates the previously painted region of the form.</span></span>

<span data-ttu-id="f141d-128">Entrambi i comandi hit test e punto più vicino cambiano il cursore, aggiornano la modalità dell'applicazione e lo stato del menu, disabilitano l'agente di raccolta input penna e invalidano l'area precedentemente disegnata del modulo.</span><span class="sxs-lookup"><span data-stu-id="f141d-128">Both the Hit Test and Nearest Point commands change the cursor, update the application mode and menu status, disable the ink collector, and invalidate the previously painted region of the form.</span></span>

<span data-ttu-id="f141d-129">Il chiaro!</span><span class="sxs-lookup"><span data-stu-id="f141d-129">The Clear!</span></span> <span data-ttu-id="f141d-130">il comando Disabilita l'oggetto [InkCollector](/previous-versions/ms583683(v=vs.100)) durante la sostituzione della proprietà [Ink](/previous-versions/ms836505(v=msdn.10)) dell'oggetto InkCollector con un nuovo oggetto [Ink](/previous-versions/ms571716(v=vs.100)) , genera un evento di comando Ink e forza un aggiornamento sul controllo.</span><span class="sxs-lookup"><span data-stu-id="f141d-130">command disables the [InkCollector](/previous-versions/ms583683(v=vs.100)) while replacing InkCollector object's [Ink](/previous-versions/ms836505(v=msdn.10)) property with a new [Ink](/previous-versions/ms571716(v=vs.100)) object, generates an Ink command event, and forces a refresh on the control.</span></span>

## <a name="handling-mouse-events"></a><span data-ttu-id="f141d-131">Gestione degli eventi del mouse</span><span class="sxs-lookup"><span data-stu-id="f141d-131">Handling Mouse Events</span></span>

<span data-ttu-id="f141d-132">Il gestore dell'evento [MouseMove](/previous-versions/ms567617(v=vs.100)) controlla la modalità dell'applicazione:</span><span class="sxs-lookup"><span data-stu-id="f141d-132">The [MouseMove](/previous-versions/ms567617(v=vs.100)) event handler checks the application mode:</span></span>

-   <span data-ttu-id="f141d-133">In modalità input penna, non esegue alcuna operazione, consentendo la raccolta di input penna normalmente da parte dell'agente di raccolta input penna.</span><span class="sxs-lookup"><span data-stu-id="f141d-133">In Ink mode, it does nothing, allowing ink to be collected normally by the ink collector.</span></span>
-   <span data-ttu-id="f141d-134">In modalità HitTest invia gli argomenti dell'evento al metodo handleHitTest dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f141d-134">In HitTest mode, it sends the event arguments to the application's handleHitTest method.</span></span>
-   <span data-ttu-id="f141d-135">In modalità NearestPoint invia gli argomenti dell'evento al metodo handleNearestPoint dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f141d-135">In NearestPoint mode, it sends the event arguments to the application's handleNearestPoint method.</span></span>

## <a name="performing-a-hit-test"></a><span data-ttu-id="f141d-136">Esecuzione di un hit test</span><span class="sxs-lookup"><span data-stu-id="f141d-136">Performing a Hit Test</span></span>

<span data-ttu-id="f141d-137">Il metodo handleHitTest dell'applicazione crea due punti, la posizione del cursore e un punto HitSize pixel distanti dal cursore, quindi converte questi due punti da pixel a coordinate dello spazio di input penna.</span><span class="sxs-lookup"><span data-stu-id="f141d-137">The application's handleHitTest method creates two points, the cursor location and a point HitSize pixels distant from the cursor, and then converts these two points from pixels to ink space coordinates.</span></span>


```C++
penPt = new Point(e.X, e.Y);
Point pt2 = new Point(e.X, e.Y);
Point pt3 = new Point(e.X + HitSize/2, e.Y);

using (Graphics g = CreateGraphics())
{
    ic.Renderer.PixelToInkSpace(g, ref pt1);
    ic.Renderer.PixelToInkSpace(g, ref pt2);
}
```



<span data-ttu-id="f141d-138">Quindi, l'oggetto [InkCollector](/previous-versions/ms583683(v=vs.100)) usa il metodo [Microsoft. Ink. Ink. HitTest ()](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) per trovare tutti i tratti contenuti in PT3. X-pt2. X unità di spazio input penna del cursore, pt2.</span><span class="sxs-lookup"><span data-stu-id="f141d-138">Then, the [InkCollector](/previous-versions/ms583683(v=vs.100)) object uses the [Microsoft.Ink.Ink.HitTest()](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) method to find any strokes that are within pt3.X - pt2.X ink space units of the cursor, pt2.</span></span>


```C++
Strokes strokes = ic.Ink.HitTest(pt2, (float)(pt3.X - pt2.X));
```



<span data-ttu-id="f141d-139">Il metodo handleHitTest imposta quindi il colore della penna in base al fatto che i tratti siano stati trovati, invalida l'area invalidateRect, calcola una nuova area in cui viene disegnato il cerchio dell'hit test e quindi invalida la nuova area.</span><span class="sxs-lookup"><span data-stu-id="f141d-139">The handleHitTest method then sets the pen color based on whether strokes were found, invalidates the invalidateRect region, calculates a new region that the hit test circle is drawn in, and then invalidates the new region.</span></span>

## <a name="locating-the-nearest-point"></a><span data-ttu-id="f141d-140">Individuazione del punto più vicino</span><span class="sxs-lookup"><span data-stu-id="f141d-140">Locating the Nearest Point</span></span>

<span data-ttu-id="f141d-141">Il metodo handleNearestPoint dell'applicazione crea due punti entrambi uguali alla posizione del cursore, uno di questi punti, PT, viene convertito nello spazio di input penna e utilizzato nella chiamata al metodo NearestPoint dell'oggetto [Ink](/previous-versions/ms836505(v=msdn.10)) di [InkCollector](/previous-versions/ms583683(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="f141d-141">The application's handleNearestPoint method creates two points both equal to the cursor's location, one of these points, pt, is converted to ink space and used in the call to the NearestPoint method of the [InkCollector](/previous-versions/ms583683(v=vs.100))'s [Ink](/previous-versions/ms836505(v=msdn.10)) object.</span></span> <span data-ttu-id="f141d-142">Il metodo NearestPoint restituisce l'oggetto [Stroke](/previous-versions/ms827842(v=msdn.10)) più vicino al punto e imposta il parametro di output dell'indice a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="f141d-142">The NearestPoint method returns the [Stroke](/previous-versions/ms827842(v=msdn.10)) object closest to the point, and sets the floating point index output parameter.</span></span>


```C++
using (Graphics g = CreateGraphics())
{

   // Remeber pen location
    Point inkPenPt = new Point(e.X, e.Y);

    // Convert the pen location into a location in ink space
    ic.Renderer.PixelToInkSpace(g, ref inkPenPt);

    // ...

    float fIndex;
    Stroke stroke = ic.Ink.NearestPoint(inkPenPt, out fIndex);
```



<span data-ttu-id="f141d-143">Se non sono presenti tratti, il metodo NearestPoint restituisce **null** e la posizione del cursore viene utilizzata come punto più vicino.</span><span class="sxs-lookup"><span data-stu-id="f141d-143">If no strokes are present, the NearestPoint method returns **NULL**, and the cursor location is used as the nearest point.</span></span> <span data-ttu-id="f141d-144">In caso contrario, viene calcolata la posizione sul tratto che corrisponde all'indice a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="f141d-144">Otherwise, the location on the stroke that corresponds to the floating point index is calculated.</span></span>

<span data-ttu-id="f141d-145">Le coordinate del punto più vicino vengono quindi convertite in pixel dallo spazio di input penna, il metodo handleNearestPoint invalida l'area invalidateRect, calcola una nuova area in cui viene disegnata la riga al punto più vicino e invalida anche la nuova area.</span><span class="sxs-lookup"><span data-stu-id="f141d-145">The nearest point coordinates are then converted to pixels from ink space, The handleNearestPoint method then invalidates the invalidateRect region, calculates a new region the line to the nearest point is drawn in, and invalidates the new region, too.</span></span>

## <a name="closing-the-form"></a><span data-ttu-id="f141d-146">Chiusura del modulo</span><span class="sxs-lookup"><span data-stu-id="f141d-146">Closing the Form</span></span>

<span data-ttu-id="f141d-147">Il metodo Dispose del modulo Elimina l'oggetto [InkCollector](/previous-versions/ms583683(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="f141d-147">The form's Dispose method disposes the [InkCollector](/previous-versions/ms583683(v=vs.100)) object.</span></span>

 

 
