---
description: "Questa applicazione si basa sull'esempio di esempio della raccolta di input penna dimostrando l'eliminazione dei tratti di input penna. Nell'esempio viene fornito all'utente un menu con quattro modalità tra cui scegliere: abilitata per l'input penna, cancellazione a cuspide, cancellazione delle intersezioni e cancellazione dei tratti."
ms.assetid: cec912ee-1645-47e1-8988-626719549e55
title: Esempio di cancellazione di input penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46040781d778f936815e57ba96b4ca516617d9a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525291"
---
# <a name="ink-erasing-sample"></a><span data-ttu-id="c6e91-104">Esempio di cancellazione di input penna</span><span class="sxs-lookup"><span data-stu-id="c6e91-104">Ink Erasing Sample</span></span>

<span data-ttu-id="c6e91-105">Questa applicazione si basa sull'esempio di [esempio della raccolta di input penna](ink-collection-sample.md) dimostrando l'eliminazione dei tratti di input penna.</span><span class="sxs-lookup"><span data-stu-id="c6e91-105">This application builds on the [Ink Collection Sample](ink-collection-sample.md) sample by demonstrating ink strokes deletion.</span></span> <span data-ttu-id="c6e91-106">Nell'esempio viene fornito all'utente un menu con quattro modalità tra cui scegliere: abilitata per l'input penna, cancellazione a cuspide, cancellazione delle intersezioni e cancellazione dei tratti.</span><span class="sxs-lookup"><span data-stu-id="c6e91-106">The sample provides the user with a menu that has four modes to choose from: ink-enabled, erasing at cusp, erasing at intersections, and erasing strokes.</span></span>

<span data-ttu-id="c6e91-107">In modalità con input penna, l'oggetto [InkCollector](/previous-versions/ms836493(v=msdn.10)) raccoglie l'input penna come illustrato nell' [esempio di raccolta di input penna](ink-collection-sample.md).</span><span class="sxs-lookup"><span data-stu-id="c6e91-107">In ink-enabled mode, the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object collects ink as shown in [Ink Collection Sample](ink-collection-sample.md).</span></span>

<span data-ttu-id="c6e91-108">In modalità di cancellazione, i segmenti di tratti di input penna esistenti che l'utente tocca con il cursore vengono cancellati.</span><span class="sxs-lookup"><span data-stu-id="c6e91-108">In an erasing mode, segments of existing ink strokes that the user touches with the cursor are erased.</span></span> <span data-ttu-id="c6e91-109">Inoltre, le cuspidi o le intersezioni possono essere contrassegnate con un cerchio rosso.</span><span class="sxs-lookup"><span data-stu-id="c6e91-109">Also, the cusps or intersections may be marked with a red circle.</span></span>

<span data-ttu-id="c6e91-110">Le parti più interessanti di questo esempio si trovano nel `InkErase` `OnPaint` gestore eventi del form e nelle funzioni di cancellazione chiamate dal `OnMouseMove` gestore eventi del form.</span><span class="sxs-lookup"><span data-stu-id="c6e91-110">The most interesting parts of this sample lie in the `InkErase` form's `OnPaint` event handler and in the erasing functions that are called from the form's `OnMouseMove` event handler.</span></span>

## <a name="circling-the-cusps-and-intersections"></a><span data-ttu-id="c6e91-111">Cerchio delle cuspidi e delle intersezioni</span><span class="sxs-lookup"><span data-stu-id="c6e91-111">Circling the Cusps and Intersections</span></span>

<span data-ttu-id="c6e91-112">Il `OnPaint` gestore eventi del form dipinge prima i tratti e, a seconda della modalità di applicazione, può trovare e contrassegnare tutte le cuspidi o le intersezioni con un piccolo cerchio rosso.</span><span class="sxs-lookup"><span data-stu-id="c6e91-112">The form's `OnPaint` event handler first paints the strokes, and depending on the application mode, may find and mark all of the cusps or intersections with a small red circle.</span></span> <span data-ttu-id="c6e91-113">Un cuspide contrassegna il punto in cui un tratto cambia direzione bruscamente.</span><span class="sxs-lookup"><span data-stu-id="c6e91-113">A cusp marks the point where a stroke changes direction abruptly.</span></span> <span data-ttu-id="c6e91-114">Un'intersezione contrassegna un punto in cui un tratto si interseca con se stesso o con un altro tratto.</span><span class="sxs-lookup"><span data-stu-id="c6e91-114">An intersection marks a point where one stroke intersects with itself or another stroke.</span></span>

<span data-ttu-id="c6e91-115">L'evento [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) si verifica ogni volta che un controllo viene ridisegnato.</span><span class="sxs-lookup"><span data-stu-id="c6e91-115">The [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) event occurs whenever a control is redrawn.</span></span>

> [!Note]  
> <span data-ttu-id="c6e91-116">L'esempio impone il ridisegnare il form ogni volta che viene cancellato un tratto o quando viene modificata la modalità dell'applicazione, usando il metodo [Refresh](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) del modulo.</span><span class="sxs-lookup"><span data-stu-id="c6e91-116">The sample forces the form to redraw itself whenever a stroke is erased, or when the application mode changes, using the form's [Refresh](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) method.</span></span>

 


```C++
private void InkErase_OnPaint(object sender, PaintEventArgs e)
{
    Strokes strokesToPaint = myInkCollector.Ink.Strokes;

    myInkCollector.Renderer.Draw(e.Graphics, strokesToPaint);

    switch (mode)
    {
        case ApplicationMode.CuspErase:
            PaintCusps(e.Graphics, strokesToPaint);
            break;
        case ApplicationMode.IntersectErase:
            PaintIntersections(e.Graphics, strokesToPaint);
            break;
    }
}
```



<span data-ttu-id="c6e91-117">In `PaintCusps` il codice scorre ogni cuspide in ogni tratto e disegna un cerchio rosso intorno.</span><span class="sxs-lookup"><span data-stu-id="c6e91-117">In `PaintCusps`, the code iterates through each cusp in each stroke, and draws a red circle around it.</span></span> <span data-ttu-id="c6e91-118">La proprietà [PolylineCusps](/previous-versions/ms827853(v=msdn.10)) del tratto restituisce gli indici dei punti all'interno di un Stoke che corrispondono a cuspidi.</span><span class="sxs-lookup"><span data-stu-id="c6e91-118">The stroke's [PolylineCusps](/previous-versions/ms827853(v=msdn.10)) property returns the indices of the points within a stoke that correspond to cusps.</span></span> <span data-ttu-id="c6e91-119">Si noti anche il metodo [InkSpaceToPixel](/previous-versions/ms828495(v=msdn.10)) dell'oggetto [renderer](/previous-versions/ms828481(v=msdn.10)) , che converte il punto in coordinate rilevanti per il metodo DrawEllipse.</span><span class="sxs-lookup"><span data-stu-id="c6e91-119">Also, note the [Renderer](/previous-versions/ms828481(v=msdn.10)) object's [InkSpaceToPixel](/previous-versions/ms828495(v=msdn.10)) method, which converts the point to coordinates relevant to the DrawEllipse method.</span></span>


```C++
private void PaintCusps(Graphics g, Strokes strokesToPaint)
{
    foreach (Stroke currentStroke in strokesToPaint)
    {
        int[] cusps = currentStroke.PolylineCusps;

        foreach (int i in cusps)
        {
            Point pt = currentStroke.GetPoint(i);

            // Convert the X, Y position to Window based pixel coordinates
            myInkCollector.Renderer.InkSpaceToPixel(g, ref pt);

            // Draw a red circle as the cusp position
            g.DrawEllipse(Pens.Red, pt.X-3, pt.Y-3, 6, 6);
        }
    }
}
```



<span data-ttu-id="c6e91-120">In `PaintIntersections` il codice scorre ogni tratto per individuare le intersezioni con l'intero set di tratti.</span><span class="sxs-lookup"><span data-stu-id="c6e91-120">In `PaintIntersections`, the code iterates through each stroke to find its intersections with the entire set of strokes.</span></span> <span data-ttu-id="c6e91-121">Si noti che al metodo [FindIntersections](/previous-versions/ms827856(v=msdn.10)) del tratto viene passata una raccolta [Strokes](/previous-versions/ms827799(v=msdn.10)) e viene restituita una matrice di valori di indice a virgola mobile che rappresentano le intersezioni.</span><span class="sxs-lookup"><span data-stu-id="c6e91-121">Note that the stroke's [FindIntersections](/previous-versions/ms827856(v=msdn.10)) method is passed a [Strokes](/previous-versions/ms827799(v=msdn.10)) collection and returns an array of floating point index values representing the intersections.</span></span> <span data-ttu-id="c6e91-122">Il codice calcola quindi una coordinata X-Y per ogni intersezione e disegna un cerchio rosso intorno.</span><span class="sxs-lookup"><span data-stu-id="c6e91-122">The code then calculates an X-Y coordinate for each intersection, and draws a red circle around it.</span></span>


```C++
private void PaintIntersections(Graphics g, Strokes strokesToPaint)
{
    foreach (Stroke currentStroke in strokesToPaint)
    {
        float[] intersections =            currentStroke.FindIntersections(strokesToPaint);
    }
}
```



## <a name="handling-a-pen-that-has-two-ends"></a><span data-ttu-id="c6e91-123">Gestione di una penna con due estremità</span><span class="sxs-lookup"><span data-stu-id="c6e91-123">Handling a Pen That Has Two Ends</span></span>

<span data-ttu-id="c6e91-124">Sono definiti tre gestori eventi per l'oggetto [InkCollector](/previous-versions/ms836493(v=msdn.10)) per gli eventi [CursorDown](/previous-versions/ms567611(v=vs.100)), [NewPackets](/previous-versions/ms567621(v=vs.100))e [Stroke](/previous-versions/ms567622(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="c6e91-124">Three event handlers are defined for the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object for the [CursorDown](/previous-versions/ms567611(v=vs.100)), [NewPackets](/previous-versions/ms567621(v=vs.100)), and [Stroke](/previous-versions/ms567622(v=vs.100)) events.</span></span> <span data-ttu-id="c6e91-125">Ogni gestore eventi controlla la proprietà [invertita](/previous-versions/ms839525(v=msdn.10)) dell'oggetto [cursore](/previous-versions/ms839521(v=msdn.10)) per vedere quale estremità della penna viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="c6e91-125">Each event handler checks the [Cursor](/previous-versions/ms839521(v=msdn.10)) object's [Inverted](/previous-versions/ms839525(v=msdn.10)) property to see which end of the pen is being used.</span></span> <span data-ttu-id="c6e91-126">Quando la penna viene invertita:</span><span class="sxs-lookup"><span data-stu-id="c6e91-126">When the pen is inverted:</span></span>

-   <span data-ttu-id="c6e91-127">Il `myInkCollector_CursorDown` metodo rende trasparente il tratto.</span><span class="sxs-lookup"><span data-stu-id="c6e91-127">The `myInkCollector_CursorDown` method makes the stroke transparent.</span></span>
-   <span data-ttu-id="c6e91-128">Il `myInkCollector_NewPackets` metodo cancella i tratti.</span><span class="sxs-lookup"><span data-stu-id="c6e91-128">The `myInkCollector_NewPackets` method erases strokes.</span></span>
-   <span data-ttu-id="c6e91-129">Il `myInkCollector_Stroke` metodo annulla l'evento.</span><span class="sxs-lookup"><span data-stu-id="c6e91-129">The `myInkCollector_Stroke` method cancels the event.</span></span> <span data-ttu-id="c6e91-130">Gli eventi [NewPackets](/previous-versions/ms567621(v=vs.100)) vengono generati prima dell'evento [Stroke](/previous-versions/ms567622(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="c6e91-130">[NewPackets](/previous-versions/ms567621(v=vs.100)) events are generated prior to the [Stroke](/previous-versions/ms567622(v=vs.100)) event.</span></span>

## <a name="tracking-the-cursor"></a><span data-ttu-id="c6e91-131">Rilevamento del cursore</span><span class="sxs-lookup"><span data-stu-id="c6e91-131">Tracking the Cursor</span></span>

<span data-ttu-id="c6e91-132">Se l'utente utilizza una penna o un mouse, vengono generati eventi [MouseMove](/previous-versions/ms567617(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="c6e91-132">Whether the user is using a pen or a mouse, [MouseMove](/previous-versions/ms567617(v=vs.100)) events are generated.</span></span> <span data-ttu-id="c6e91-133">Il gestore dell'evento MouseMove verifica innanzitutto per determinare se la modalità corrente è una modalità di cancellazione e se viene premuto un pulsante del mouse e ignora l'evento se questi Stati non sono presenti.</span><span class="sxs-lookup"><span data-stu-id="c6e91-133">The MouseMove event handler first checks to determine whether the current mode is an erase mode and if any mouse button is pressed, and ignores the event if these states are not present.</span></span> <span data-ttu-id="c6e91-134">Il gestore eventi converte quindi le coordinate dei pixel per il cursore in coordinate dello spazio di input penna usando il metodo [PixelToInkSpace](/previous-versions/ms828505(v=msdn.10)) dell'oggetto [renderer](/previous-versions/ms828481(v=msdn.10)) e chiama uno dei metodi di cancellazione del codice a seconda della modalità di cancellazione corrente.</span><span class="sxs-lookup"><span data-stu-id="c6e91-134">Then, the event handler converts the pixel coordinates for the cursor into ink space coordinates by using the [Renderer](/previous-versions/ms828481(v=msdn.10)) object's [PixelToInkSpace](/previous-versions/ms828505(v=msdn.10)) method, and calls one of the code's erase methods depending on the current erase mode.</span></span>

## <a name="erasing-strokes"></a><span data-ttu-id="c6e91-135">Cancellazione di tratti</span><span class="sxs-lookup"><span data-stu-id="c6e91-135">Erasing Strokes</span></span>

<span data-ttu-id="c6e91-136">Il `EraseStrokes` metodo accetta la posizione del cursore nello spazio di input penna e genera una raccolta di tratti all'interno delle `HitTestRadius` unità.</span><span class="sxs-lookup"><span data-stu-id="c6e91-136">The `EraseStrokes` method takes the cursor's location in ink space and generates a collection of strokes that are within `HitTestRadius` units.</span></span> <span data-ttu-id="c6e91-137">Il `currentStroke` parametro specifica un oggetto [Stroke](/previous-versions/ms827842(v=msdn.10)) che non deve essere eliminato.</span><span class="sxs-lookup"><span data-stu-id="c6e91-137">The `currentStroke` parameter specifies a [Stroke](/previous-versions/ms827842(v=msdn.10)) object that should not be deleted.</span></span> <span data-ttu-id="c6e91-138">La raccolta Strokes viene quindi eliminata dall'agente di raccolta e il form viene ridisegnato.</span><span class="sxs-lookup"><span data-stu-id="c6e91-138">Then the strokes collection is deleted from the collector, and the form is redrawn.</span></span>


```C++
private void EraseStrokes(Point pt, Stroke currentStroke)
{
    Strokes strokesHit = myInkCollector.Ink.HitTest(pt, HitTestRadius);

    if (null!=currentStroke && strokesHit.Contains(currentStroke))
    {
        strokesHit.Remove(currentStroke);
    }

    myInkCollector.Ink.DeleteStrokes(strokesHit);

    if (strokesHit.Count > 0)
    {
        this.Refresh();
    }
}
```



## <a name="erasing-at-intersections"></a><span data-ttu-id="c6e91-139">Cancellazione all'intersezione</span><span class="sxs-lookup"><span data-stu-id="c6e91-139">Erasing at Intersections</span></span>

<span data-ttu-id="c6e91-140">Il `EraseAtIntersections` metodo scorre ogni tratto che rientra nel raggio del test e genera una matrice di intersezioni tra tale tratto e tutti gli altri tratti della raccolta.</span><span class="sxs-lookup"><span data-stu-id="c6e91-140">The `EraseAtIntersections` method iterates over each stroke that falls within the test radius and generates an array of intersections between that stroke and all the other strokes in the collection.</span></span> <span data-ttu-id="c6e91-141">Se non viene trovata alcuna intersezione, viene eliminato l'intero tratto; in caso contrario, viene individuato il punto più vicino sul tratto al punto di test e da questo, le intersezioni su entrambi i lati del punto si trovano, descrivendo il segmento da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="c6e91-141">If no intersections are found, then that entire stroke is deleted; otherwise, the nearest point on the stroke to the test point is located, and from that, the intersections on either side of the point are located, describing the segment to be removed.</span></span>

<span data-ttu-id="c6e91-142">Il metodo [Split](/previous-versions/ms828477(v=msdn.10)) dell'oggetto [Stroke](/previous-versions/ms827842(v=msdn.10)) viene usato per separare il segmento dal resto del tratto e quindi il segmento viene eliminato, lasciando intatto il resto del tratto.</span><span class="sxs-lookup"><span data-stu-id="c6e91-142">The [Stroke](/previous-versions/ms827842(v=msdn.10)) object's [Split](/previous-versions/ms828477(v=msdn.10)) method is used to separate the segment from the rest of the stroke, and then the segment is deleted, leaving the rest of the stroke intact.</span></span> <span data-ttu-id="c6e91-143">Come in `EraseStrokes` , il form viene ridisegnato prima che il metodo restituisca.</span><span class="sxs-lookup"><span data-stu-id="c6e91-143">As in `EraseStrokes`, the form is redrawn before the method returns.</span></span>


```C++
private void EraseAtIntersections(Point pt)
{
    Strokes strokesHit = myInkCollector.Ink.HitTest(pt, HitTestRadius);

    foreach (Stroke currentStroke in strokesHit)
    {
        float[] intersections = currentStroke.FindIntersections(myInkCollector.Ink.Strokes);
        ...
        float findex = currentStroke.NearestPoint(pt);
        ...
        strokeToDelete = currentStroke.Split(intersections[i]);
        ...
    }
    ...
}
```



## <a name="erasing-at-cusps"></a><span data-ttu-id="c6e91-144">Cancellazione in corrispondenza di cuspidi</span><span class="sxs-lookup"><span data-stu-id="c6e91-144">Erasing at Cusps</span></span>

<span data-ttu-id="c6e91-145">Per ogni tratto che rientra nel raggio di test, il `EraseAtCusps` metodo recupera la matrice di cuspidi dal metodo [PolylineCusps](/previous-versions/ms827853(v=msdn.10)) dell'oggetto [Stroke](/previous-versions/ms827842(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="c6e91-145">For each stroke that falls within the test radius, the `EraseAtCusps` method retrieves the array of cusps from the [Stroke](/previous-versions/ms827842(v=msdn.10)) object's [PolylineCusps](/previous-versions/ms827853(v=msdn.10)) method.</span></span> <span data-ttu-id="c6e91-146">Ogni estremità del tratto è anche un cuspide, pertanto se il tratto ha solo due cuspidi, viene eliminato l'intero tratto; in caso contrario, viene individuato il punto più vicino sul tratto al punto di test e da questo, le intersezioni su entrambi i lati del punto si trovano, descrivendo il segmento da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="c6e91-146">Each end of the stroke is also a cusp, so if the stroke only has two cusps, then the entire stroke is deleted; otherwise, the nearest point on the stroke to the test point is located, and from that, the intersections on either side of the point are located, describing the segment to be removed.</span></span>

<span data-ttu-id="c6e91-147">Il metodo [Split](/previous-versions/ms828477(v=msdn.10)) dell'oggetto [Stroke](/previous-versions/ms827842(v=msdn.10)) viene usato per separare il segmento dal resto del tratto e quindi il segmento viene eliminato, lasciando intatto il resto del tratto.</span><span class="sxs-lookup"><span data-stu-id="c6e91-147">The [Stroke](/previous-versions/ms827842(v=msdn.10)) object's [Split](/previous-versions/ms828477(v=msdn.10)) method is used to separate the segment from the rest of the stroke, and then the segment is deleted, leaving the rest of the stroke intact.</span></span> <span data-ttu-id="c6e91-148">Come in `EraseStrokes` , il form viene ridisegnato prima che il metodo restituisca.</span><span class="sxs-lookup"><span data-stu-id="c6e91-148">As in `EraseStrokes`, the form is redrawn before the method returns.</span></span>


```C++
private void EraseAtCusps(Point pt)
{
    ...
    strokesHit = myInkCollector.Ink.HitTest(pt, HitTestRadius);
    
    foreach (Stroke currentStroke in strokesHit)
    {
        int[] cusps = currentStroke.PolylineCusps;
        ...
        float findex = currentStroke.NearestPoint(pt);
        ...
        strokeToDelete = currentStroke.Split(cusps[i]); 
        myInkCollector.Ink.DeleteStroke(strokeToDelete);
        ...
    }
    ...
}
```



## <a name="closing-the-form"></a><span data-ttu-id="c6e91-149">Chiusura del modulo</span><span class="sxs-lookup"><span data-stu-id="c6e91-149">Closing the Form</span></span>

<span data-ttu-id="c6e91-150">Il metodo [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) del modulo Elimina l'oggetto [InkCollector](/previous-versions/ms836493(v=msdn.10)) , `myInkCollector` .</span><span class="sxs-lookup"><span data-stu-id="c6e91-150">The form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method disposes the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object, `myInkCollector`.</span></span>

 

 
