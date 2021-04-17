---
title: Panoramica delle realizzazioni di geometria
description: Questo argomento descrive come usare le realizzazioni di geometria Direct2D per migliorare le prestazioni di rendering della geometria dell'app in determinati scenari.
ms.assetid: E8C4C4E5-3102-4F53-847E-A4C2D12A6921
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b903e047ee58a803a7584aaca407281fc803e30
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299874"
---
# <a name="geometry-realizations-overview"></a>Panoramica delle realizzazioni di geometria

Questo argomento descrive come usare le realizzazioni di geometria [Direct2D](direct2d-portal.md) per migliorare le prestazioni di rendering della geometria dell'app in determinati scenari.

Contiene le sezioni seguenti:

-   [Che cosa sono le realizzazioni di geometria?](#what-are-geometry-realizations)
-   [Perché usare le realizzazioni di geometria?](#why-use-geometry-realizations)
-   [Quando usare le realizzazioni di geometria](#when-to-use-geometry-realizations)
-   [Creazione di realizzazioni di geometria](#creating-geometry-realizations)
-   [Creazione di realizzazioni di geometria](#drawing-geometry-realizations)
-   [Ridimensionamento delle realizzazioni di geometria](#scaling-geometry-realizations)
    -   [Uso delle realizzazioni di geometria nelle app che non si adattano](#using-geometry-realizations-in-apps-that-do-not-scale)
    -   [Uso delle realizzazioni di geometria nelle app che vengono ridimensionate in base a una piccola quantità](#using-geometry-realizations-in-apps-that-scale-by-a-small-amount)
    -   [Uso delle realizzazioni di geometria nelle app che si adattano a una grande quantità](#using-geometry-realizations-in-apps-that-scale-by-a-large-amount)
-   [Argomenti correlati](#related-topics)

## <a name="what-are-geometry-realizations"></a>Che cosa sono le realizzazioni di geometria?

Le realizzazioni di geometria, introdotte in Windows 8.1, sono un nuovo tipo di creazione primitiva che consente alle app [Direct2D](direct2d-portal.md) di migliorare in modo semplice le prestazioni di rendering della geometria in alcuni casi. Le realizzazioni di geometria sono rappresentate dall'interfaccia [**ID2D1GeometryRealization**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1geometryrealization) .

## <a name="why-use-geometry-realizations"></a>Perché usare le realizzazioni di geometria?

Quando [Direct2D](direct2d-portal.md) esegue il rendering di un oggetto [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) , deve convertire tale geometria in un form che l'hardware grafico riconosce tramite un processo denominato mosaico. In genere, Direct2D deve conteggiarla suddividerla la geometria ogni frame viene disegnato, anche se la geometria non cambia. Se l'app esegue il rendering della stessa geometria di ogni frame, la ripetizione dello schema ripetuto rappresenta un lavoro di calcolo sprecato. È più efficiente dal punto di vista del calcolo memorizzare nella cache lo schema a mosaico, o anche la rasterizzazione completa, della geometria e per richiamare la rappresentazione memorizzata nella cache di ogni fotogramma anziché tessellating ripetutamente.

Un modo comune per risolvere questo problema consiste nel memorizzare nella cache la rasterizzazione completa della geometria. In particolare, è normale creare una nuova bitmap, rasterizzare la geometria sulla bitmap e quindi creare la bitmap nella scena in base alle esigenze. Questo approccio è descritto nella sezione [rendering Geometry](improving-direct2d-performance.md) di miglioramento delle prestazioni delle app Direct2D. Sebbene questo approccio sia molto efficiente dal punto di vista del calcolo, presenta alcuni svantaggi:

-   La bitmap memorizzata nella cache è sensibile alle modifiche nella trasformazione applicata alla scena. Ad esempio, il ridimensionamento della rasterizzazione può comportare un notevole ridimensionamento degli artefatti. La mitigazione di questi elementi con algoritmi di scalabilità di alta qualità può risultare costosa dal punto di vista del calcolo.
-   La bitmap memorizzata nella cache utilizza una quantità significativa di memoria, soprattutto se è rasterizzata a una risoluzione elevata.

Le realizzazioni di geometria rappresentano una modalità alternativa per memorizzare nella cache la geometria che evita gli svantaggi precedenti. Le realizzazioni di geometria sono rappresentate non da pixel (come nel caso di una rasterizzazione completa), ma in base ai punti su un piano matematico. Per questo motivo sono meno sensibili rispetto alle rasterizzazioni complete per la scalabilità e altre manipolazioni e utilizzano una quantità significativamente inferiore di memoria.

## <a name="when-to-use-geometry-realizations"></a>Quando usare le realizzazioni di geometria

Provare a usare le realizzazioni di geometria quando l'app esegue il rendering di geometrie complesse le cui forme cambiano raramente, ma che possono essere soggette a trasformazioni mutevoli.

Si consideri, ad esempio, un'applicazione di mapping che mostra una mappa statica, ma che consente all'utente di eseguire lo zoom avanti e indietro. Questa app può trarre vantaggio dall'uso delle realizzazioni di geometria. Poiché le geometrie di cui è in corso il rendering rimangono statiche, è utile memorizzarle nella cache per salvare il lavoro a mosaico. Tuttavia, poiché le mappe vengono ridimensionate quando l'utente esegue lo zoom, la memorizzazione nella cache di una rasterizzazione completa non è ideale, a causa del ridimensionamento degli artefatti. La memorizzazione nella cache delle realizzazioni Geometry consente all'app di evitare il rimosaico del lavoro mantenendo al tempo stesso una qualità visiva elevata durante il ridimensionamento.

D'altra parte, si consideri un'App Caleidoscopica con geometria animata che cambia continuamente. Questa app probabilmente non trarrà vantaggio dall'uso delle realizzazioni di geometria. Poiché le forme cambiano da frame a frame, non è utile memorizzare nella cache i relativi tassellature. L'approccio migliore per questa app consiste nel creare direttamente gli oggetti [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) .

## <a name="creating-geometry-realizations"></a>Creazione di realizzazioni di geometria

È necessario creare un oggetto [**ID2D1GeometryRealization**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1geometryrealization) da un oggetto [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) esistente. Per creare una realizzazione di geometria, chiamare il metodo [**CreateFilledGeometryRealization**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-createfilledgeometryrealization) o il metodo [**CreateStrokedGeometryRealization**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-createstrokedgeometryrealization) e passare il **ID2D1Geometry** da realizzare.

-   [**CreateFilledGeometryRealization**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-createfilledgeometryrealization) crea una realizzazione della parte interna della forma, ovvero l'area che verrebbe disegnata chiamando [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry).
-   [**CreateStrokedGeometryRealization**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-createstrokedgeometryrealization) crea una realizzazione del tratto della forma, ovvero l'area che verrebbe disegnata chiamando [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry).

Entrambi i tipi di realizzazione della geometria sono rappresentati dall'interfaccia [**ID2D1GeometryRealization**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1geometryrealization) .

Quando si crea una realizzazione di geometria, [Direct2D](direct2d-portal.md) deve appiattire le curve della geometria fornita a approssimazioni poligonali. È necessario specificare un parametro di tolleranza flat per il metodo di creazione, specificando la distanza massima, in DIP (device independent pixel), tra la curva reale della geometria e la relativa approssimazione poligonale. Più basso è la tolleranza di flatità fornita, più alta è la fedeltà dell'oggetto di realizzazione Geometry risultante. Analogamente, garantire una maggiore tolleranza di appiattimento produce una realizzazione di geometria con minore fedeltà. Si noti che le realizzazioni di geometria con fedeltà più elevata sono più costose da creare rispetto a quelle più ridotte, ma possono essere ulteriormente ridimensionate prima di introdurre elementi visibili. Per istruzioni sull'uso delle tolleranze Flat, vedere [ridimensionamento delle realizzazioni Geometry](#scaling-geometry-realizations) di seguito.

> [!Note]  
> Gli oggetti di realizzazione Geometry sono associati a un particolare dispositivo di grafica: sono risorse dipendenti dal dispositivo.

 

## <a name="drawing-geometry-realizations"></a>Creazione di realizzazioni di geometria

Il disegno di realizzazioni di geometria è simile al disegno di altre primitive [Direct2D](direct2d-portal.md) , come le bitmap. A tale scopo, chiamare il metodo [**DrawGeometryRealization**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-drawgeometryrealization) e passargli l'oggetto di realizzazione Geometry da disegnare e il pennello da usare. Come per gli altri metodi di disegno Direct2D, è necessario chiamare **DrawGeometryRealization** tra le chiamate a [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) e [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).

## <a name="scaling-geometry-realizations"></a>Ridimensionamento delle realizzazioni di geometria

Le realizzazioni di geometria, come altre primitive [Direct2D](direct2d-portal.md) , rispettano il set di trasformazioni nel contesto di dispositivo. Sebbene le trasformazioni di traslazione e rotazione non abbiano effetto sulla qualità visiva delle realizzazioni di geometria, le trasformazioni di scala possono produrre artefatti visivi.

In particolare, l'applicazione di una scala sufficientemente grande a qualsiasi realizzazione di geometria può rivelare l'approssimazione poligonale delle curve reali. Nell'immagine viene illustrata una coppia di realizzazioni di geometria ellittica (riempimento e tratto) che sono state ridimensionate troppo a lungo. Gli artefatti di appiattimento curva sono visibili.

![coppia di realizzazioni di geometria ellittica (riempimento e tratto) che sono state ridimensionate troppo a lungo. gli artefatti di appiattimento curva sono visibili.](images/zoomed-in.png)

Le app sensibili alla qualità visiva devono adottare misure per garantire che ciò non avvenga. La modalità di gestione della scalabilità dipende dalle esigenze dell'app. Di seguito sono riportati diversi approcci consigliati per diversi tipi di app.

### <a name="using-geometry-realizations-in-apps-that-do-not-scale"></a>Uso delle realizzazioni di geometria nelle app che non si adattano

Se l'app non esegue alcun ridimensionamento sulle realizzazioni di geometria, è possibile creare le realizzazioni solo una volta, usando una singola tolleranza di Flat. (Le trasformazioni senza scalabilità non influiscono sulla qualità visiva delle realizzazioni di geometria sottoposte a rendering). Usare la funzione [**ComputeFlatteningTolerance**](/previous-versions/windows/desktop/legacy/dn280327(v=vs.85)) per calcolare la tolleranza di appiattimento appropriata per il valore dpi:


```C++
    float dpiX, dpiY;
    deviceContext->GetDpi(&dpiX, &dpiY);

    float flatteningTolerance = D2D1::ComputeFlatteningTolerance(
        D2D1::Matrix3x2F::Identity(),   // apply no additional scaling transform
        dpiX,                           // horizontal DPI
        dpiY                            // vertical DPI
        );
```



### <a name="using-geometry-realizations-in-apps-that-scale-by-a-small-amount"></a>Uso delle realizzazioni di geometria nelle app che vengono ridimensionate in base a una piccola quantità

Se l'app è in grado di ridimensionare una realizzazione di geometria solo con una piccola quantità (ad esempio, fino a 2x o 3x), potrebbe essere appropriato semplicemente creare la realizzazione della geometria una sola volta, con una tolleranza di Flat proporzionale inferiore rispetto a quella predefinita. In questo modo si crea una realizzazione con maggiore fedeltà che può essere scalata significativamente prima di generare artefatti di ridimensionamento. il compromesso è che il disegno della realizzazione con maggiore fedeltà richiede un maggior lavoro.

Si supponga, ad esempio, di sapere che l'app non ridimensiona mai una realizzazione di geometria più di 2x. L'app può creare la realizzazione geometrica usando una tolleranza flat che è la metà del valore predefinito e ridimensionare semplicemente la realizzazione in base alle esigenze, fino a 2x. Usare la funzione [**ComputeFlatteningTolerance**](/previous-versions/windows/desktop/legacy/dn280327(v=vs.85)) per calcolare la tolleranza di Flat appropriata passando 2,0 come parametro *maxZoomFactor* :


```C++
    float dpiX, dpiY;
    deviceContext->GetDpi(&dpiX, &dpiY);
    
    float flatteningTolerance = D2D1::ComputeFlatteningTolerance(
        D2D1::Matrix3x2F::Identity(),   // apply no additional scaling transform
        dpiX,                           // horizontal DPI
        dpiY,                           // vertical DPI
        2.0f                            // realization can be scaled by an additional 2x
        );
```



### <a name="using-geometry-realizations-in-apps-that-scale-by-a-large-amount"></a>Uso delle realizzazioni di geometria nelle app che si adattano a una grande quantità

Se l'app è in grado di aumentare o ridurre le prestazioni di una geometria in base a grandi quantità (ad esempio, per 10 volte o più), la gestione del ridimensionamento in modo appropriato è più complessa.

Per la maggior parte di queste app, l'approccio consigliato consiste nel ricreare la realizzazione di geometria con una riduzione graduale delle tolleranze Man mano che la scena viene ridimensionata, in modo da mantenere la fedeltà visiva ed evitare la scalabilità degli artefatti. Analogamente, man mano che la scena viene ridimensionata, l'app deve ricreare le realizzazioni di geometria con tolleranze progressivamente più elevate, in modo da evitare un inutile rendering dei dettagli che non sono visibili. L'app non deve ricreare le realizzazioni di geometria ogni volta che la scala viene modificata, perché in questo modo si vanifica lo scopo della memorizzazione nella cache del lavoro a mosaico. Al contrario, l'app deve ricreare le realizzazioni di geometria con minore frequenza, ad esempio dopo ogni aumento o riduzione della dimensione di 2x.

Ogni volta che la scala cambia in un'app in risposta all'interazione dell'utente, l'app potrebbe confrontare la nuova scala con la scala in cui sono state create le realizzazioni di geometria (archiviate, ad esempio, in un membro **\_ lastScale m** ). Se i due valori sono vicini (in questo caso, all'interno di un fattore 2), non viene eseguita alcuna azione ulteriore. Tuttavia, se i due valori non sono vicini, le realizzazioni di geometria vengono ricreate. La funzione [**ComputeFlatteningTolerance**](/previous-versions/windows/desktop/legacy/dn280327(v=vs.85)) viene usata per calcolare una tolleranza appiattita appropriata per la nuova scala e **m \_ lastScale** viene aggiornato alla nuova scala.

Inoltre, l'app crea sempre le realizzazioni usando una tolleranza inferiore rispetto a quella usata normalmente per la nuova scala, passando il valore 2 come parametro *maxZoomFactor* a [**ComputeFlatteningTolerance**](/previous-versions/windows/desktop/legacy/dn280327(v=vs.85)). In questo modo è possibile aumentare la scalabilità delle nuove realizzazioni geometriche con un fattore aggiuntivo pari a 2 senza influire sulla scalabilità degli artefatti.

> [!Note]  
> L'approccio descritto qui potrebbe non essere appropriato per tutte le app. Se, ad esempio, l'app consente di ridimensionare la scena in modo molto rapido, ad esempio se contiene un dispositivo di scorrimento "zoom", che può essere spostato da 100% a 1 milione% nell'intervallo di pochi frame, questo approccio può comportare un lavoro in eccesso ricreando le realizzazioni Geometry ogni frame. Un approccio alternativo consiste nel ricreare le realizzazioni di geometria solo dopo che ogni modifica della scala della scena è stata completata (ad esempio, dopo che l'utente ha completato un movimento di tocco).

 

## <a name="related-topics"></a>Argomenti correlati

[Panoramica delle geometrie](direct2d-geometries-overview.md)

[Miglioramento delle prestazioni delle app Direct2D](improving-direct2d-performance.md)

[Linee guida generali per il rendering di contenuto statico complesso](improving-direct2d-performance.md)

[**ID2D1DeviceContext1**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1devicecontext1)

[**ID2D1GeometryRealization**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1geometryrealization)

[**ComputeFlatteningTolerance (funzione)**](/previous-versions/windows/desktop/legacy/dn280327(v=vs.85))