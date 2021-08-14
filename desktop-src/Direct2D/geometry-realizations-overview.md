---
title: Panoramica delle realizzazioni di geometria
description: Questo argomento descrive come usare le realizzazioni di geometrie Direct2D per migliorare le prestazioni di rendering della geometria dell'app in determinati scenari.
ms.assetid: E8C4C4E5-3102-4F53-847E-A4C2D12A6921
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5108537e9ea9b38bebaab590178d990b44e611e56e82690e9d91ad9b56c19372
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119260136"
---
# <a name="geometry-realizations-overview"></a>Panoramica delle realizzazioni di geometria

Questo argomento descrive come usare le realizzazioni di geometrie [Direct2D](direct2d-portal.md) per migliorare le prestazioni di rendering della geometria dell'app in determinati scenari.

Contiene le sezioni seguenti:

-   [Che cosa sono le realizzazioni geometriche?](#what-are-geometry-realizations)
-   [Perché usare le realizzazioni geometriche?](#why-use-geometry-realizations)
-   [Quando usare le realizzazioni geometriche](#when-to-use-geometry-realizations)
-   [Creazione di realizzazioni geometriche](#creating-geometry-realizations)
-   [Disegno di realizzazioni geometriche](#drawing-geometry-realizations)
-   [Ridimensionamento delle realizzazioni geometry](#scaling-geometry-realizations)
    -   [Uso di realizzazioni geometry nelle app che non vengono ridimensionate](#using-geometry-realizations-in-apps-that-do-not-scale)
    -   [Uso di realizzazioni geometry nelle app che vengono ridimensionate di una piccola quantità](#using-geometry-realizations-in-apps-that-scale-by-a-small-amount)
    -   [Uso di realizzazioni geometriche nelle app che vengono ridimensionate di una grande quantità](#using-geometry-realizations-in-apps-that-scale-by-a-large-amount)
-   [Argomenti correlati](#related-topics)

## <a name="what-are-geometry-realizations"></a>Che cosa sono le realizzazioni geometriche?

Le realizzazioni geometry, introdotte in Windows 8.1, sono un nuovo tipo di primitiva di disegno che consente alle app [Direct2D](direct2d-portal.md) di migliorare facilmente le prestazioni di rendering della geometria in determinati casi. Le realizzazioni geometry sono rappresentate [**dall'interfaccia ID2D1GeometryRealization.**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1geometryrealization)

## <a name="why-use-geometry-realizations"></a>Perché usare le realizzazioni geometriche?

Quando [Direct2D esegue](direct2d-portal.md) il rendering di un [**oggetto ID2D1Geometry,**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) deve convertire tale geometria in un formato che l'hardware grafico comprende tramite un processo denominato a tessellazione. In genere, Direct2D deve eseguire la tessellatura della geometria ogni fotogramma disegnato, anche se la geometria non cambia. Se l'app esegue il rendering della stessa geometria per ogni fotogramma, la ripetizione della ripetizione della tessellazione rappresenta uno sforzo di calcolo sprecato. È più efficiente dal punto di vista computazionale memorizzare nella cache la struttura a tessellazione, o anche la rasterizzazione completa, della geometria e disegnare la rappresentazione memorizzata nella cache di ogni fotogramma anziché ripetere ripetutamente la ripetizione.

Un modo comune che gli sviluppatori risolvono questo problema è memorizzare nella cache la rasterizzazione completa della geometria. In particolare, è comune creare una nuova bitmap, rasterizzare la geometria in tale bitmap e quindi disegnare tale bitmap sulla scena in base alle esigenze. Questo approccio è descritto nella [sezione Rendering geometry](improving-direct2d-performance.md) di Miglioramento delle prestazioni delle app Direct2D. Sebbene questo approccio sia molto efficiente dal punto di vista del calcolo, presenta alcuni svantaggi:

-   La bitmap memorizzata nella cache è sensibile alle modifiche nella trasformazione applicata alla scena. Ad esempio, il ridimensionamento della rasterizzazione può comportare un notevole ridimensionamento degli artefatti. La mitigazione di questi artefatti con algoritmi di scalabilità di alta qualità può essere costosa dal punto di vista del calcolo.
-   La bitmap memorizzata nella cache utilizza una quantità significativa di memoria, soprattutto se viene rasterizzata a una risoluzione elevata.

Le realizzazioni geometry offrono un modo alternativo per memorizzare nella cache la geometria, evitando gli svantaggi precedenti. Le realizzazioni geometry non sono rappresentate da pixel (come nel caso di una rasterizzazione completa), ma da punti su un piano matematico. Per questo motivo sono meno sensibili delle rasterizzazioni complete al ridimensionamento e ad altre manipolazioni e consumano una quantità di memoria significativamente inferiore.

## <a name="when-to-use-geometry-realizations"></a>Quando usare le realizzazioni geometriche

È consigliabile usare le realizzazioni geometriche quando l'app esegue il rendering di geometrie complesse le cui forme cambiano raramente, ma che possono essere soggette a trasformazioni mutevoli.

Si consideri, ad esempio, un'applicazione di mapping che mostra una mappa statica, ma che consente all'utente di eseguire lo zoom avanti e indietro. Questa app può trarre vantaggio dall'uso di realizzazioni geometriche. Poiché le geometrie di cui viene eseguito il rendering rimangono statiche, è utile memorizzarle nella cache per salvare il lavoro a tassellamento. Tuttavia, poiché le mappe vengono ridimensionate quando l'utente esegue lo zoom, la memorizzazione nella cache di una rasterizzazione completa non è ideale, a causa del ridimensionamento degli artefatti. Caching realizzazioni geometriche consentirebbe all'app di evitare il lavoro di ricorsività mantenendo un'elevata qualità visiva durante il ridimensionamento.

D'altra parte, si consideri un'app caleidoscopio con geometria animata che cambia continuamente. Questa app probabilmente non trarrebbe vantaggio dall'uso di realizzazioni geometriche. Poiché le forme stesse cambiano da frame a frame, non è utile memorizzare nella cache le loro tessellazioni. L'approccio migliore per questa app consiste nel disegnare [**direttamente oggetti ID2D1Geometry.**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)

## <a name="creating-geometry-realizations"></a>Creazione di realizzazioni geometriche

È necessario creare un oggetto [**ID2D1GeometryRealization**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1geometryrealization) da un [**oggetto ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) esistente. Per creare una realizzazione geometrica, chiamare il [**metodo CreateFilledGeometryRealization**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-createfilledgeometryrealization) o [**CreateStrokedGeometryRealization**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-createstrokedgeometryrealization) e passare **id2D1Geometry** da realizzare.

-   [**CreateFilledGeometryRealization**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-createfilledgeometryrealization) crea una realizzazione dell'interno della forma: l'area che verrà disegnata chiamando [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry).
-   [**CreateStrokedGeometryRealization**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-createstrokedgeometryrealization) crea una realizzazione del tratto della forma: l'area che verrebbe disegnata chiamando [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry).

Entrambi i tipi di realizzazione della geometria sono rappresentati [**dall'interfaccia ID2D1GeometryRealization.**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1geometryrealization)

Quando si crea una realizzazione geometrica, [Direct2D](direct2d-portal.md) deve appiattire le curve nella geometria fornita in approssimazioni poligonali. È necessario fornire un parametro di tolleranza di appiattimento al metodo di creazione, che specifica la distanza massima, in DIP (Device Independent Pixel), tra la curva vera della geometria e l'approssimazione poligonale. Più bassa è la tolleranza di appiattimento specificata, maggiore è la fedeltà dell'oggetto di realizzazione della geometria risultante. Analogamente, fornire una tolleranza di appiattimento più elevata produce una realizzazione della geometria a bassa fedeltà. Si noti che le realizzazioni di geometrie con maggiore fedeltà sono più costose da disegnare rispetto a quelle a bassa fedeltà, ma possono essere ulteriormente ridimensionate prima di introdurre artefatti visibili. Per indicazioni sull'uso delle tolleranze di appiattimento, vedere [Scalare le realizzazioni geometriche di](#scaling-geometry-realizations) seguito.

> [!Note]  
> Gli oggetti di realizzazione geometry sono associati a un particolare dispositivo grafico: sono risorse dipendenti dal dispositivo.

 

## <a name="drawing-geometry-realizations"></a>Disegno di realizzazioni geometriche

Il disegno di realizzazioni geometriche è simile al disegno di altre primitive [Direct2D,](direct2d-portal.md) ad esempio bitmap. A tale scopo, chiamare il [**metodo DrawGeometryRealization**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-drawgeometryrealization) e passarlo all'oggetto di realizzazione della geometria da disegnare e al pennello da usare. Come per altri metodi di disegno Direct2D, è necessario chiamare **DrawGeometryRealization** tra le chiamate a [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) [**ed EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).

## <a name="scaling-geometry-realizations"></a>Ridimensionamento delle realizzazioni geometry

Le realizzazioni geometry, come altre primitive [Direct2D,](direct2d-portal.md) rispettano la trasformazione impostata nel contesto di dispositivo. Anche se le trasformazioni di traslazione e rotazione non hanno alcun effetto sulla qualità visiva delle realizzazioni geometriche, le trasformazioni di scala possono produrre artefatti visivi.

In particolare, l'applicazione di una scala sufficiente a qualsiasi realizzazione geometrica può rivelare l'approssimazione poligonale delle curve vere. L'immagine mostra una coppia di realizzazioni geometriche ellittiche (riempimento e tratto) che sono state ridimensionate troppo in alto. Gli artefatti di appiattimento della curva sono visibili.

![una coppia di realizzazioni geometriche ellittiche (riempimento e tratto) che sono state ridimensionate troppo in alto. Gli artefatti di appiattimento della curva sono visibili.](images/zoomed-in.png)

Le app sensibili alla qualità dell'oggetto visivo devono adottare misure per assicurarsi che ciò non avvenga. La modalità di gestione del ridimensionamento dipende dalle esigenze dell'app. Di seguito sono riportati diversi approcci consigliati per diversi tipi di app.

### <a name="using-geometry-realizations-in-apps-that-do-not-scale"></a>Uso di realizzazioni geometry nelle app che non vengono ridimensionate

Se l'app non esegue alcuna scalabilità sulle realizzazioni geometry, è possibile creare le realizzazioni una sola volta, usando una singola tolleranza di appiattimento. Le trasformazioni non ridimensionate non influiscono sulla qualità visiva delle realizzazioni geometriche sottoposte a rendering. Usare la [**funzione ComputeFlatteningTolerance**](/previous-versions/windows/desktop/legacy/dn280327(v=vs.85)) per calcolare la tolleranza di appiattimento appropriata per il valore DPI:


```C++
    float dpiX, dpiY;
    deviceContext->GetDpi(&dpiX, &dpiY);

    float flatteningTolerance = D2D1::ComputeFlatteningTolerance(
        D2D1::Matrix3x2F::Identity(),   // apply no additional scaling transform
        dpiX,                           // horizontal DPI
        dpiY                            // vertical DPI
        );
```



### <a name="using-geometry-realizations-in-apps-that-scale-by-a-small-amount"></a>Uso di realizzazioni geometry nelle app che vengono ridimensionate di una piccola quantità

Se l'app può aumentare la realizzazione di una geometria solo di una piccola quantità (ad esempio, fino a 2x o 3 volte), può essere opportuno creare semplicemente la realizzazione della geometria una sola volta, con una tolleranza di appiattimento proporzionalmente inferiore rispetto all'impostazione predefinita. In questo modo si crea una realizzazione con maggiore fedeltà che può essere ridotta in modo significativo prima di incorrere in artefatti di ridimensionamento; il compromesso è che il disegno della realizzazione con maggiore fedeltà richiede più lavoro.

Si supponga, ad esempio, di sapere che l'app non ridimensiona mai una realizzazione geometrica di più di 2x. L'app può creare la realizzazione della geometria usando una tolleranza di appiattimento pari alla metà del valore predefinito e ridimensionare semplicemente la realizzazione in base alle esigenze, fino a 2x. Usare la [**funzione ComputeFlatteningTolerance**](/previous-versions/windows/desktop/legacy/dn280327(v=vs.85)) per calcolare la tolleranza di appiattimento appropriata passando 2.0 come *parametro maxZoomFactor:*


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



### <a name="using-geometry-realizations-in-apps-that-scale-by-a-large-amount"></a>Uso di realizzazioni geometriche nelle app che vengono ridimensionate di una grande quantità

Se l'app può aumentare o ridurre la realizzazione di una geometria di grandi quantità (ad esempio, di 10 o più), la gestione appropriata del ridimensionamento è più complessa.

Per la maggior parte di queste app, l'approccio consigliato consiste nel ricreare la realizzazione della geometria a tolleranze di appiattimento progressivamente inferiori quando la scena viene ridimensionata, in modo da mantenere la fedeltà visiva ed evitare il ridimensionamento degli artefatti. Analogamente, quando la scena viene ridotta, l'app deve ricreare le realizzazioni geometriche a tolleranze di appiattimento progressivamente più elevate, per evitare di eseguire il rendering ingente di dettagli non visibili. L'app non deve ricreare le realizzazioni geometriche ogni volta che cambia la scala, perché questa operazione non consente di memorizzare nella cache il lavoro a tessellazione. Al contrario, l'app deve ricreare le realizzazioni geometriche meno frequentemente, ad esempio dopo un aumento o una riduzione di scala di 2 volte.

Ogni volta che la scala cambia in un'app in risposta all'interazione dell'utente, l'app può confrontare la nuova scala con la scala in cui sono state create le realizzazioni geometry (archiviate, ad esempio, in un membro **m \_ lastScale).** Se i due valori sono vicini (in questo caso, entro un fattore 2), non vengono intraprese altre azioni. Tuttavia, se i due valori non sono vicini, le realizzazioni geometry vengono ri-create. La [**funzione ComputeFlatteningTolerance**](/previous-versions/windows/desktop/legacy/dn280327(v=vs.85)) viene usata per calcolare una tolleranza di flattening appropriata per la nuova scala e **m \_ lastScale** viene aggiornata alla nuova scala.

Inoltre, l'app crea sempre realizzazioni usando una tolleranza inferiore a quella normalmente usata per la nuova scala, passando il valore 2 come parametro *maxZoomFactor* a [**ComputeFlatteningTolerance**](/previous-versions/windows/desktop/legacy/dn280327(v=vs.85)). In questo modo le nuove realizzazioni geometry possono essere ridimensionate di un fattore aggiuntivo di 2 senza incorrere in artefatti di ridimensionamento.

> [!Note]  
> L'approccio descritto qui potrebbe non essere appropriato per tutte le app. Ad esempio, se l'app consente di ridimensionare la scena con fattori molto grandi molto rapidamente (ad esempio, se contiene un dispositivo di scorrimento "zoom" che può essere spostato dal 100% al 1.000.000% nell'intervallo di pochi fotogrammi), questo approccio può comportare un lavoro in eccesso ricreando le realizzazioni geometriche ogni fotogramma. Un approccio alternativo consiste nel ricreare le realizzazioni geometriche solo dopo il completamento di ogni modifica della scala della scena (ad esempio, dopo che l'utente ha completato un movimento di avvicinamento delle dita).

 

## <a name="related-topics"></a>Argomenti correlati

[Panoramica delle geometrie](direct2d-geometries-overview.md)

[Miglioramento delle prestazioni delle app Direct2D](improving-direct2d-performance.md)

[Linee guida generali per il rendering di contenuto statico complesso](improving-direct2d-performance.md)

[**ID2D1DeviceContext1**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1devicecontext1)

[**ID2D1GeometryRealization**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1geometryrealization)

[**Funzione ComputeFlatteningTolerance**](/previous-versions/windows/desktop/legacy/dn280327(v=vs.85))