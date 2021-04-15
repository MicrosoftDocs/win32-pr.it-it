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
# <a name="ink-erasing-sample"></a>Esempio di cancellazione di input penna

Questa applicazione si basa sull'esempio di [esempio della raccolta di input penna](ink-collection-sample.md) dimostrando l'eliminazione dei tratti di input penna. Nell'esempio viene fornito all'utente un menu con quattro modalità tra cui scegliere: abilitata per l'input penna, cancellazione a cuspide, cancellazione delle intersezioni e cancellazione dei tratti.

In modalità con input penna, l'oggetto [InkCollector](/previous-versions/ms836493(v=msdn.10)) raccoglie l'input penna come illustrato nell' [esempio di raccolta di input penna](ink-collection-sample.md).

In modalità di cancellazione, i segmenti di tratti di input penna esistenti che l'utente tocca con il cursore vengono cancellati. Inoltre, le cuspidi o le intersezioni possono essere contrassegnate con un cerchio rosso.

Le parti più interessanti di questo esempio si trovano nel `InkErase` `OnPaint` gestore eventi del form e nelle funzioni di cancellazione chiamate dal `OnMouseMove` gestore eventi del form.

## <a name="circling-the-cusps-and-intersections"></a>Cerchio delle cuspidi e delle intersezioni

Il `OnPaint` gestore eventi del form dipinge prima i tratti e, a seconda della modalità di applicazione, può trovare e contrassegnare tutte le cuspidi o le intersezioni con un piccolo cerchio rosso. Un cuspide contrassegna il punto in cui un tratto cambia direzione bruscamente. Un'intersezione contrassegna un punto in cui un tratto si interseca con se stesso o con un altro tratto.

L'evento [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) si verifica ogni volta che un controllo viene ridisegnato.

> [!Note]  
> L'esempio impone il ridisegnare il form ogni volta che viene cancellato un tratto o quando viene modificata la modalità dell'applicazione, usando il metodo [Refresh](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) del modulo.

 


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



In `PaintCusps` il codice scorre ogni cuspide in ogni tratto e disegna un cerchio rosso intorno. La proprietà [PolylineCusps](/previous-versions/ms827853(v=msdn.10)) del tratto restituisce gli indici dei punti all'interno di un Stoke che corrispondono a cuspidi. Si noti anche il metodo [InkSpaceToPixel](/previous-versions/ms828495(v=msdn.10)) dell'oggetto [renderer](/previous-versions/ms828481(v=msdn.10)) , che converte il punto in coordinate rilevanti per il metodo DrawEllipse.


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



In `PaintIntersections` il codice scorre ogni tratto per individuare le intersezioni con l'intero set di tratti. Si noti che al metodo [FindIntersections](/previous-versions/ms827856(v=msdn.10)) del tratto viene passata una raccolta [Strokes](/previous-versions/ms827799(v=msdn.10)) e viene restituita una matrice di valori di indice a virgola mobile che rappresentano le intersezioni. Il codice calcola quindi una coordinata X-Y per ogni intersezione e disegna un cerchio rosso intorno.


```C++
private void PaintIntersections(Graphics g, Strokes strokesToPaint)
{
    foreach (Stroke currentStroke in strokesToPaint)
    {
        float[] intersections =            currentStroke.FindIntersections(strokesToPaint);
    }
}
```



## <a name="handling-a-pen-that-has-two-ends"></a>Gestione di una penna con due estremità

Sono definiti tre gestori eventi per l'oggetto [InkCollector](/previous-versions/ms836493(v=msdn.10)) per gli eventi [CursorDown](/previous-versions/ms567611(v=vs.100)), [NewPackets](/previous-versions/ms567621(v=vs.100))e [Stroke](/previous-versions/ms567622(v=vs.100)) . Ogni gestore eventi controlla la proprietà [invertita](/previous-versions/ms839525(v=msdn.10)) dell'oggetto [cursore](/previous-versions/ms839521(v=msdn.10)) per vedere quale estremità della penna viene utilizzata. Quando la penna viene invertita:

-   Il `myInkCollector_CursorDown` metodo rende trasparente il tratto.
-   Il `myInkCollector_NewPackets` metodo cancella i tratti.
-   Il `myInkCollector_Stroke` metodo annulla l'evento. Gli eventi [NewPackets](/previous-versions/ms567621(v=vs.100)) vengono generati prima dell'evento [Stroke](/previous-versions/ms567622(v=vs.100)) .

## <a name="tracking-the-cursor"></a>Rilevamento del cursore

Se l'utente utilizza una penna o un mouse, vengono generati eventi [MouseMove](/previous-versions/ms567617(v=vs.100)) . Il gestore dell'evento MouseMove verifica innanzitutto per determinare se la modalità corrente è una modalità di cancellazione e se viene premuto un pulsante del mouse e ignora l'evento se questi Stati non sono presenti. Il gestore eventi converte quindi le coordinate dei pixel per il cursore in coordinate dello spazio di input penna usando il metodo [PixelToInkSpace](/previous-versions/ms828505(v=msdn.10)) dell'oggetto [renderer](/previous-versions/ms828481(v=msdn.10)) e chiama uno dei metodi di cancellazione del codice a seconda della modalità di cancellazione corrente.

## <a name="erasing-strokes"></a>Cancellazione di tratti

Il `EraseStrokes` metodo accetta la posizione del cursore nello spazio di input penna e genera una raccolta di tratti all'interno delle `HitTestRadius` unità. Il `currentStroke` parametro specifica un oggetto [Stroke](/previous-versions/ms827842(v=msdn.10)) che non deve essere eliminato. La raccolta Strokes viene quindi eliminata dall'agente di raccolta e il form viene ridisegnato.


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



## <a name="erasing-at-intersections"></a>Cancellazione all'intersezione

Il `EraseAtIntersections` metodo scorre ogni tratto che rientra nel raggio del test e genera una matrice di intersezioni tra tale tratto e tutti gli altri tratti della raccolta. Se non viene trovata alcuna intersezione, viene eliminato l'intero tratto; in caso contrario, viene individuato il punto più vicino sul tratto al punto di test e da questo, le intersezioni su entrambi i lati del punto si trovano, descrivendo il segmento da rimuovere.

Il metodo [Split](/previous-versions/ms828477(v=msdn.10)) dell'oggetto [Stroke](/previous-versions/ms827842(v=msdn.10)) viene usato per separare il segmento dal resto del tratto e quindi il segmento viene eliminato, lasciando intatto il resto del tratto. Come in `EraseStrokes` , il form viene ridisegnato prima che il metodo restituisca.


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



## <a name="erasing-at-cusps"></a>Cancellazione in corrispondenza di cuspidi

Per ogni tratto che rientra nel raggio di test, il `EraseAtCusps` metodo recupera la matrice di cuspidi dal metodo [PolylineCusps](/previous-versions/ms827853(v=msdn.10)) dell'oggetto [Stroke](/previous-versions/ms827842(v=msdn.10)) . Ogni estremità del tratto è anche un cuspide, pertanto se il tratto ha solo due cuspidi, viene eliminato l'intero tratto; in caso contrario, viene individuato il punto più vicino sul tratto al punto di test e da questo, le intersezioni su entrambi i lati del punto si trovano, descrivendo il segmento da rimuovere.

Il metodo [Split](/previous-versions/ms828477(v=msdn.10)) dell'oggetto [Stroke](/previous-versions/ms827842(v=msdn.10)) viene usato per separare il segmento dal resto del tratto e quindi il segmento viene eliminato, lasciando intatto il resto del tratto. Come in `EraseStrokes` , il form viene ridisegnato prima che il metodo restituisca.


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

Il metodo [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) del modulo Elimina l'oggetto [InkCollector](/previous-versions/ms836493(v=msdn.10)) , `myInkCollector` .

 

 
