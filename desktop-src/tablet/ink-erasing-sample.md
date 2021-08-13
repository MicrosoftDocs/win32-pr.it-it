---
description: "Questa applicazione si basa sull'esempio di raccolta Ink illustrando l'eliminazione dei tratti input penna. L'esempio fornisce all'utente un menu che offre quattro modalità tra cui scegliere: abilitata per l'input penna, cancellazione in corrispondenza del punto di cancellazione, cancellazione in corrispondenza delle intersezioni e cancellazione dei tratti."
ms.assetid: cec912ee-1645-47e1-8988-626719549e55
title: Esempio di cancellazione input penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b56885835a2d42c3f4c050938658cfc7cdf5a5d5463309ae2f0a6d8021c817e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452079"
---
# <a name="ink-erasing-sample"></a>Esempio di cancellazione input penna

Questa applicazione si basa sull'esempio [di raccolta Ink](ink-collection-sample.md) illustrando l'eliminazione dei tratti input penna. L'esempio fornisce all'utente un menu che offre quattro modalità tra cui scegliere: abilitata per l'input penna, cancellazione in corrispondenza del punto di cancellazione, cancellazione in corrispondenza delle intersezioni e cancellazione dei tratti.

In modalità abilitata per l'input penna, [l'oggetto InkCollector](/previous-versions/ms836493(v=msdn.10)) raccoglie l'input penna come illustrato in [Ink Collection Sample](ink-collection-sample.md).

In modalità di cancellazione, i segmenti dei tratti input penna esistenti che l'utente tocca con il cursore vengono cancellati. Inoltre, i punti di intersezione o i punti di intersezione possono essere contrassegnati con un cerchio rosso.

Le parti più interessanti di questo esempio si trovano nel gestore eventi del form e nelle funzioni di cancellazione chiamate dal gestore eventi `InkErase` `OnPaint` del `OnMouseMove` form.

## <a name="circling-the-cusps-and-intersections"></a>Circling the Cusps and Intersections

Il gestore eventi del form disegna prima i tratti e, a seconda della modalità dell'applicazione, può trovare e contrassegnare tutti i punti di sospensione o le intersezioni con un piccolo `OnPaint` cerchio rosso. Un oggetto cusp contrassegna il punto in cui un tratto cambia improvvisamente direzione. Un'intersezione contrassegna un punto in cui un tratto si interseca con se stesso o con un altro tratto.

[L Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) evento si verifica ogni volta che un controllo viene ridisegnato.

> [!Note]  
> L'esempio forza il form a ridisegnarsi ogni volta che un tratto viene cancellato o quando cambia la modalità dell'applicazione, usando il metodo [Refresh del](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) form.

 


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



In il codice scorre ogni cuspide in ogni tratto e disegna `PaintCusps` un cerchio rosso intorno a esso. La proprietà [PolylineCusps del](/previous-versions/ms827853(v=msdn.10)) tratto restituisce gli indici dei punti all'interno di uno stoke che corrispondono a cusps. Si noti anche il metodo [InkSpaceToPixel](/previous-versions/ms828495(v=msdn.10)) dell'oggetto [Renderer,](/previous-versions/ms828481(v=msdn.10)) che converte il punto in coordinate rilevanti per il metodo DrawEllipse.


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



In il codice scorre ogni tratto per trovare le intersezioni con `PaintIntersections` l'intero set di tratti. Si noti che al metodo [FindIntersections](/previous-versions/ms827856(v=msdn.10)) del tratto viene passata una raccolta [Strokes](/previous-versions/ms827799(v=msdn.10)) e restituisce una matrice di valori di indice a virgola mobile che rappresentano le intersezioni. Il codice calcola quindi una coordinata X-Y per ogni intersezione e disegna un cerchio rosso intorno ad essa.


```C++
private void PaintIntersections(Graphics g, Strokes strokesToPaint)
{
    foreach (Stroke currentStroke in strokesToPaint)
    {
        float[] intersections =            currentStroke.FindIntersections(strokesToPaint);
    }
}
```



## <a name="handling-a-pen-that-has-two-ends"></a>Gestione di un oggetto Pen con due estremità

Vengono definiti tre gestori eventi per [l'oggetto InkCollector](/previous-versions/ms836493(v=msdn.10)) per gli eventi [CursorDown,](/previous-versions/ms567611(v=vs.100)) [NewPackets](/previous-versions/ms567621(v=vs.100)) [e Stroke.](/previous-versions/ms567622(v=vs.100)) Ogni gestore eventi controlla la proprietà [Inverted](/previous-versions/ms839525(v=msdn.10)) dell'oggetto [Cursor](/previous-versions/ms839521(v=msdn.10)) per vedere quale estremità della penna viene usata. Quando la penna è invertita:

-   Il `myInkCollector_CursorDown` metodo rende trasparente il tratto.
-   Il `myInkCollector_NewPackets` metodo cancella i tratti.
-   Il `myInkCollector_Stroke` metodo annulla l'evento . [Gli eventi NewPackets](/previous-versions/ms567621(v=vs.100)) vengono generati prima [dell'evento Stroke.](/previous-versions/ms567622(v=vs.100))

## <a name="tracking-the-cursor"></a>Rilevamento del cursore

Se l'utente usa una penna o un mouse, vengono [generati eventi MouseMove.](/previous-versions/ms567617(v=vs.100)) Il gestore dell'evento MouseMove verifica innanzitutto se la modalità corrente è una modalità di cancellazione e se viene premuto un pulsante del mouse e ignora l'evento se questi stati non sono presenti. Il gestore eventi converte quindi le coordinate in pixel per il cursore in coordinate dello spazio input penna usando il metodo [PixelToInkSpace](/previous-versions/ms828505(v=msdn.10)) dell'oggetto [Renderer](/previous-versions/ms828481(v=msdn.10)) e chiama uno dei metodi di cancellazione del codice a seconda della modalità di cancellazione corrente.

## <a name="erasing-strokes"></a>Cancellazione di tratti

Il `EraseStrokes` metodo accetta la posizione del cursore nello spazio input penna e genera una raccolta di tratti all'interno di `HitTestRadius` unità. Il `currentStroke` parametro specifica un oggetto [Stroke](/previous-versions/ms827842(v=msdn.10)) che non deve essere eliminato. La raccolta di tratti viene quindi eliminata dall'agente di raccolta e il form viene ridisegnato.


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



## <a name="erasing-at-intersections"></a>Cancellazione in corrispondenza delle intersezioni

Il metodo esegue l'iterazione su ogni tratto che rientra nel raggio del test e genera una matrice di intersezioni tra tale tratto e tutti gli altri `EraseAtIntersections` tratti nella raccolta. Se non vengono trovate intersezioni, l'intero tratto viene eliminato; In caso contrario, viene individuato il punto più vicino sul tratto al punto di test e da tale punto si trovano le intersezioni su entrambi i lati del punto, che descrivono il segmento da rimuovere.

Il [metodo Split](/previous-versions/ms827842(v=msdn.10)) dell'oggetto [Stroke](/previous-versions/ms828477(v=msdn.10)) viene usato per separare il segmento dal resto del tratto e quindi viene eliminato, lasciando intatto il resto del tratto. Come in `EraseStrokes` , il form viene ridisegnato prima che il metodo venga restituito.


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



## <a name="erasing-at-cusps"></a>Cancellazione in Cusps

Per ogni tratto che rientra nel raggio del test, il metodo recupera la matrice di segnali dal metodo `EraseAtCusps` [PolylineCusps](/previous-versions/ms827853(v=msdn.10)) dell'oggetto [Stroke.](/previous-versions/ms827842(v=msdn.10)) Ogni estremità del tratto è anche un cuspide, quindi se il tratto ha solo due puntine, viene eliminato l'intero tratto; In caso contrario, viene individuato il punto più vicino sul tratto al punto di test e da tale punto si trovano le intersezioni su entrambi i lati del punto, che descrivono il segmento da rimuovere.

Il [metodo Split](/previous-versions/ms827842(v=msdn.10)) dell'oggetto [Stroke](/previous-versions/ms828477(v=msdn.10)) viene usato per separare il segmento dal resto del tratto e quindi viene eliminato, lasciando intatto il resto del tratto. Come in `EraseStrokes` , il form viene ridisegnato prima che il metodo venga restituito.


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



## <a name="closing-the-form"></a>Chiusura del modulo

Il metodo [Dispose del](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) form elimina l'oggetto [InkCollector,](/previous-versions/ms836493(v=msdn.10)) `myInkCollector` .

 

 
