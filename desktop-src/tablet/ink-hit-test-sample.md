---
description: Questo esempio illustra due metodi per trovare l'input penna, in base alla posizione dello schermo.
ms.assetid: fc581da4-0a7b-4c31-8f73-0784066fcc56
title: Esempio di hit test input penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 995bd6f14b4a0a014452ae9392fa744ab93f01f9047c79e5dc30652c243473db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713081"
---
# <a name="ink-hit-test-sample"></a>Esempio di hit test input penna

Questo esempio illustra due metodi per trovare l'input penna, in base alla posizione dello schermo.

In questo esempio vengono usate le funzionalità seguenti:

-   Uso di un agente di raccolta input penna
-   Esecuzione di un hit test
-   Individuazione del punto più vicino

## <a name="accessing-the-ink-api"></a>Accesso all'API Input penna

Per prima cosa, fare riferimento alle classi Tablet PC, disponibili in Windows Vista o Windows XP Tablet PC Edition Software Development Kit (SDK).


```C++
using Microsoft.Ink;
```



## <a name="handling-form-load-and-paint-events"></a>Gestione degli eventi di caricamento e Paint form

Gestore dell'evento Load del form:

-   Crea un [oggetto InkCollector,](/previous-versions/ms583683(v=vs.100)) ic, per il form.
-   Imposta la proprietà [CollectionMode](/previous-versions/ms836497(v=msdn.10)) dell'oggetto [InkCollector](/previous-versions/ms583683(v=vs.100)) per ignorare i movimenti.
-   Abilita [InkCollector.](/previous-versions/ms583683(v=vs.100))
-   Imposta la proprietà [AutoRedraw](/previous-versions/ms836495(v=msdn.10)) dell'oggetto [InkCollector](/previous-versions/ms583683(v=vs.100)) su **TRUE.**


```C++
// Create the InkCollector, and turn it on
ic = new InkCollector(Handle);  // attach it to the form's frame window

// default to ink-enabled mode
mode = ApplicationMode.Ink;
ic.CollectionMode = CollectionMode.InkOnly;

// turn the collector on
ic.Enabled = true;ic.AutoRedraw = true;
```



Il gestore dell'Paint del form controlla la modalità dell'applicazione:

-   In modalità HitTest disegna un cerchio intorno al cursore. La penna attiva viene impostata nel metodo handleHitTest dell'applicazione.
-   Nella modalità NearestPoint viene disegnata una linea rossa tra il cursore e il punto più vicino al cursore. Il punto più vicino viene calcolato nel metodo handleNearestPoint dell'applicazione.


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



Questo esempio ha un algoritmo di ridisegno molto semplice. Con la [proprietà AutoRedraw impostata](/previous-versions/ms836495(v=msdn.10)) su **TRUE,** l'agente di raccolta input penna si ridisegna quando il form viene ridisegnato. Per semplificare il ridisegno del form, l'applicazione tiene traccia di un rettangolo di selezione, la variabile membro invalidateRect, per l'area in cui viene aggiunto il disegno, che viene invalidato ogni volta che il form viene ridisegnato.

## <a name="handling-menu-events"></a>Gestione degli eventi di menu

Il comando Exit disabilita [InkCollector prima](/previous-versions/ms583683(v=vs.100)) di uscire dall'applicazione.

Il comando Input penna aggiorna la modalità applicazione e lo stato del menu, abilita l'agente di raccolta input penna e invalida l'area precedentemente disegnata del form.

Entrambi i comandi Hit Test e Punto più vicino modificano il cursore, aggiornano la modalità applicazione e lo stato del menu, disabilitano l'agente di raccolta input penna e invalidano l'area precedentemente disegnata del modulo.

The Clear! il comando disabilita [InkCollector](/previous-versions/ms583683(v=vs.100)) sostituendo la proprietà [Ink](/previous-versions/ms836505(v=msdn.10)) dell'oggetto InkCollector con un nuovo oggetto [Ink,](/previous-versions/ms571716(v=vs.100)) genera un evento di comando Ink e forza un aggiornamento sul controllo.

## <a name="handling-mouse-events"></a>Gestione degli eventi del mouse

Il [gestore dell'evento MouseMove](/previous-versions/ms567617(v=vs.100)) controlla la modalità dell'applicazione:

-   In modalità input penna non esegue alcuna operazione, consentendo la raccolta normale dell'input penna da parte dell'agente di raccolta input penna.
-   In modalità HitTest invia gli argomenti dell'evento al metodo handleHitTest dell'applicazione.
-   In modalità NearestPoint invia gli argomenti dell'evento al metodo handleNearestPoint dell'applicazione.

## <a name="performing-a-hit-test"></a>Esecuzione di un hit test

Il metodo handleHitTest dell'applicazione crea due punti, la posizione del cursore e un punto HitSize pixel distanti dal cursore, quindi converte questi due punti da pixel a coordinate dello spazio input penna.


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



[L'oggetto InkCollector](/previous-versions/ms583683(v=vs.100)) usa quindi il metodo [Microsoft.Ink.Ink.HitTest()](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) per trovare i tratti che si trovano all'interno di pt3. X - pt2. X unità dello spazio input penna del cursore, pt2.


```C++
Strokes strokes = ic.Ink.HitTest(pt2, (float)(pt3.X - pt2.X));
```



Il metodo handleHitTest imposta quindi il colore della penna in base al fatto che i tratti siano stati trovati, invalida l'area invalidateRect, calcola una nuova area in cui viene disegnato il cerchio dell'hit test e quindi invalida la nuova area.

## <a name="locating-the-nearest-point"></a>Individuazione del punto più vicino

Il metodo handleNearestPoint dell'applicazione crea due punti uguali alla posizione del cursore. Uno di questi punti, pt, viene convertito nello spazio input penna e usato nella chiamata al metodo NearestPoint dell'oggetto [Ink](/previous-versions/ms836505(v=msdn.10)) [di InkCollector.](/previous-versions/ms583683(v=vs.100)) Il metodo NearestPoint restituisce [l'oggetto Stroke](/previous-versions/ms827842(v=msdn.10)) più vicino al punto e imposta il parametro di output dell'indice a virgola mobile.


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



Se non sono presenti tratti, il metodo NearestPoint restituisce **NULL** e la posizione del cursore viene usata come punto più vicino. In caso contrario, viene calcolata la posizione sul tratto corrispondente all'indice a virgola mobile.

Le coordinate del punto più vicine vengono quindi convertite in pixel dallo spazio input penna, il metodo handleNearestPoint invalida quindi l'area invalidateRect, calcola una nuova area in cui viene disegnata la linea al punto più vicino e invalida anche la nuova area.

## <a name="closing-the-form"></a>Chiusura del modulo

Il metodo Dispose del form elimina [l'oggetto InkCollector.](/previous-versions/ms583683(v=vs.100))

 

 
