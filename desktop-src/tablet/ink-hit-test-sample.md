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
# <a name="ink-hit-test-sample"></a>Esempio di hit test di input penna

In questo esempio vengono illustrati due metodi per trovare l'input penna, data una posizione dello schermo.

In questo esempio vengono usate le funzionalità seguenti:

-   Uso di un agente di raccolta input penna
-   Esecuzione di un hit test
-   Individuazione del punto più vicino

## <a name="accessing-the-ink-api"></a>Accesso all'API Ink

Per prima cosa, fare riferimento alle classi di Tablet PC, che si trovano in Windows Vista o Windows XP Tablet PC Edition Software Development Kit (SDK).


```C++
using Microsoft.Ink;
```



## <a name="handling-form-load-and-paint-events"></a>Gestione degli eventi di caricamento e disegno dei moduli

Gestore dell'evento Load del form:

-   Crea un oggetto [InkCollector](/previous-versions/ms583683(v=vs.100)) , IC, per il form.
-   Imposta la proprietà [CollectionMode](/previous-versions/ms836497(v=msdn.10)) dell'oggetto [InkCollector](/previous-versions/ms583683(v=vs.100)) per ignorare i movimenti.
-   Abilita l'oggetto [InkCollector](/previous-versions/ms583683(v=vs.100)).
-   Imposta la proprietà [AutoRedraw](/previous-versions/ms836495(v=msdn.10)) dell'oggetto [InkCollector](/previous-versions/ms583683(v=vs.100)) su **true**.


```C++
// Create the InkCollector, and turn it on
ic = new InkCollector(Handle);  // attach it to the form's frame window

// default to ink-enabled mode
mode = ApplicationMode.Ink;
ic.CollectionMode = CollectionMode.InkOnly;

// turn the collector on
ic.Enabled = true;ic.AutoRedraw = true;
```



Il gestore dell'evento Paint del modulo controlla la modalità dell'applicazione:

-   In modalità HitTest, disegna un cerchio intorno al cursore. Il puntatore attivo viene impostato nel metodo handleHitTest dell'applicazione.
-   In modalità NearestPoint, disegna una linea rossa tra il cursore e il punto più vicino al cursore. Il punto più vicino viene calcolato nel metodo handleNearestPoint dell'applicazione.


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



Questo esempio ha un algoritmo di ridisegno molto semplice. Con la proprietà [AutoRedraw](/previous-versions/ms836495(v=msdn.10)) impostata su **true**, l'agente di raccolta input penna si ridipinge quando il modulo viene ridisegnato. Per semplificare il ridisegno del form, l'applicazione tiene traccia di un rettangolo di delimitazione, della variabile membro invalidateRect, per l'area in cui viene aggiunto Paint, che viene invalidato ogni volta che viene ridisegnato il modulo.

## <a name="handling-menu-events"></a>Gestione degli eventi di menu

Il comando Exit Disabilita l'oggetto [InkCollector](/previous-versions/ms583683(v=vs.100)) prima di uscire dall'applicazione.

Il comando Ink aggiorna la modalità dell'applicazione e lo stato del menu, Abilita l'agente di raccolta input penna e invalida l'area precedentemente disegnata del modulo.

Entrambi i comandi hit test e punto più vicino cambiano il cursore, aggiornano la modalità dell'applicazione e lo stato del menu, disabilitano l'agente di raccolta input penna e invalidano l'area precedentemente disegnata del modulo.

Il chiaro! il comando Disabilita l'oggetto [InkCollector](/previous-versions/ms583683(v=vs.100)) durante la sostituzione della proprietà [Ink](/previous-versions/ms836505(v=msdn.10)) dell'oggetto InkCollector con un nuovo oggetto [Ink](/previous-versions/ms571716(v=vs.100)) , genera un evento di comando Ink e forza un aggiornamento sul controllo.

## <a name="handling-mouse-events"></a>Gestione degli eventi del mouse

Il gestore dell'evento [MouseMove](/previous-versions/ms567617(v=vs.100)) controlla la modalità dell'applicazione:

-   In modalità input penna, non esegue alcuna operazione, consentendo la raccolta di input penna normalmente da parte dell'agente di raccolta input penna.
-   In modalità HitTest invia gli argomenti dell'evento al metodo handleHitTest dell'applicazione.
-   In modalità NearestPoint invia gli argomenti dell'evento al metodo handleNearestPoint dell'applicazione.

## <a name="performing-a-hit-test"></a>Esecuzione di un hit test

Il metodo handleHitTest dell'applicazione crea due punti, la posizione del cursore e un punto HitSize pixel distanti dal cursore, quindi converte questi due punti da pixel a coordinate dello spazio di input penna.


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



Quindi, l'oggetto [InkCollector](/previous-versions/ms583683(v=vs.100)) usa il metodo [Microsoft. Ink. Ink. HitTest ()](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) per trovare tutti i tratti contenuti in PT3. X-pt2. X unità di spazio input penna del cursore, pt2.


```C++
Strokes strokes = ic.Ink.HitTest(pt2, (float)(pt3.X - pt2.X));
```



Il metodo handleHitTest imposta quindi il colore della penna in base al fatto che i tratti siano stati trovati, invalida l'area invalidateRect, calcola una nuova area in cui viene disegnato il cerchio dell'hit test e quindi invalida la nuova area.

## <a name="locating-the-nearest-point"></a>Individuazione del punto più vicino

Il metodo handleNearestPoint dell'applicazione crea due punti entrambi uguali alla posizione del cursore, uno di questi punti, PT, viene convertito nello spazio di input penna e utilizzato nella chiamata al metodo NearestPoint dell'oggetto [Ink](/previous-versions/ms836505(v=msdn.10)) di [InkCollector](/previous-versions/ms583683(v=vs.100)). Il metodo NearestPoint restituisce l'oggetto [Stroke](/previous-versions/ms827842(v=msdn.10)) più vicino al punto e imposta il parametro di output dell'indice a virgola mobile.


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



Se non sono presenti tratti, il metodo NearestPoint restituisce **null** e la posizione del cursore viene utilizzata come punto più vicino. In caso contrario, viene calcolata la posizione sul tratto che corrisponde all'indice a virgola mobile.

Le coordinate del punto più vicino vengono quindi convertite in pixel dallo spazio di input penna, il metodo handleNearestPoint invalida l'area invalidateRect, calcola una nuova area in cui viene disegnata la riga al punto più vicino e invalida anche la nuova area.

## <a name="closing-the-form"></a>Chiusura del modulo

Il metodo Dispose del modulo Elimina l'oggetto [InkCollector](/previous-versions/ms583683(v=vs.100)) .

 

 
