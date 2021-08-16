---
title: 'Panoramica delle geometrie '
description: Descrive le nozioni di base delle geometrie Direct2D, oggetti che è possibile usare per rappresentare, modificare e analizzare le forme.
ms.assetid: f5870d4b-dd30-4034-884e-1c398a6865c6
keywords:
- Direct2D, panoramica delle geometrie
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: d3f8cd7420325fd876897d538ea9e01a5c0adb64b2d0c55437514773904d6013
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117825843"
---
# <a name="geometries-overview"></a>Panoramica delle geometrie 

Questa panoramica descrive come creare e usare oggetti [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) per definire e modificare figure 2D. Include le sezioni seguenti:

## <a name="what-is-a-direct2d-geometry"></a>Che cos'è una geometria Direct2D?

Una geometria Direct2D è un [**oggetto ID2D1Geometry.**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) Questo oggetto può essere una geometria semplice ([**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry), [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry)o [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry)), una geometria del percorso ([**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry)) o una geometria composita ([**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) e [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry)).

Le geometrie Direct2D consentono di descrivere figure bidimensionali e offrono molti usi, ad esempio la definizione di aree di hit test, aree di ritaglio e persino tracciati di animazione.

Le geometrie Direct2D sono risorse non modificabili e indipendenti dal dispositivo create da [**ID2D1Factory.**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) In genere, è consigliabile creare le geometrie una sola volta e mantenerle per tutta la durata dell'applicazione o fino a quando non devono essere modificate. Per altre informazioni sulle risorse indipendenti dal dispositivo e dipendenti dal dispositivo, vedere Panoramica [delle risorse.](resources-and-resource-domains.md)

Le sezioni seguenti descrivono i diversi tipi di geometrie.

## <a name="simple-geometries"></a>Geometrie semplici

Le geometrie semplici includono gli oggetti [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry), [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry)e [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) e possono essere usate per creare figure geometriche di base, ad esempio rettangoli, rettangoli arrotondati, cerchi ed ellissi.

Per creare una geometria semplice, usare uno dei metodi [**ID2D1Factory::Create<*geometryType*>Geometry.**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) Questi metodi creano un oggetto del tipo specificato. Ad esempio, per creare un rettangolo, chiamare [**ID2D1Factory::CreateRectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry)), che restituisce un [**oggetto ID2D1RectangleGeometry;**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) Per creare un rettangolo arrotondato, chiamare [**ID2D1Factory::CreateRoundedRectangleGeometry**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createroundedrectanglegeometry(constd2d1_rounded_rect__id2d1roundedrectanglegeometry)), che restituisce un oggetto [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry) e così via.

L'esempio di codice seguente chiama il metodo [**CreateEllipseGeometry,**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createellipsegeometry(constd2d1_ellipse__id2d1ellipsegeometry)) passando una struttura *ellisse* con il centro impostato su (100, 100), il raggio *x* su 100 e il raggio y su 50.  Chiama quindi [**DrawGeometry,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry)passando la geometria ellisse restituita, un puntatore a un oggetto [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)nero e uno spessore del tratto di 5. La figura seguente mostra l'output dell'esempio di codice.

![illustrazione di un'ellisse](images/geometry-ovw-drawstep6.png)


```C++
ID2D1EllipseGeometry *m_pEllipseGeometry;
```




```C++
if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory->CreateEllipseGeometry(
        D2D1::Ellipse(D2D1::Point2F(100.f, 60.f), 100.f, 50.f),
        &m_pEllipseGeometry
        );
}
```




```C++
m_pRenderTarget->DrawGeometry(m_pEllipseGeometry, m_pBlackBrush, 5);
```



Per disegnare il contorno di qualsiasi geometria, usare il [**metodo DrawGeometry.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) Per disegnare l'interno, usare [**il metodo FillGeometry.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry)

## <a name="path-geometries"></a>Geometrie di percorso

Le geometrie di percorso sono rappresentate [**dall'interfaccia ID2D1PathGeometry.**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) Questi oggetti possono essere usati per descrivere figure geometriche complesse composte da segmenti quali archi, curve e linee. La figura seguente mostra un disegno creato usando la geometria del tracciato.

![illustrazione di un river, del letto e del sole](images/path-geo-mnts.png)

Per altre informazioni ed esempi, vedere [Cenni preliminari sulle geometrie dei percorsi.](path-geometries-overview.md)

## <a name="composite-geometries"></a>Geometrie composite

Una geometria composita è una geometria raggruppata o combinata con un altro oggetto geometry o con una trasformazione. Le geometrie composite [**includono gli oggetti ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry) [**e ID2D1GeometryGroup.**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup)

### <a name="geometry-groups"></a>Gruppi di geometria

I gruppi di geometrie sono un modo pratico per raggruppare più geometrie contemporaneamente, in modo che tutte le figure di diverse geometrie distinte siano concatenate in una sola. Per creare un oggetto [**ID2D1GeometryGroup,**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) chiamare il metodo [**CreateGeometryGroup**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup) sull'oggetto [**ID2D1Factory,**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) passando fillMode con i valori possibili [**di D2D1 \_ FILL MODE \_ \_ ALTERNATE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode) (alternate) e **D2D1 \_ FILL MODE \_ \_ WINDING,** una matrice di oggetti *geometry* da aggiungere al gruppo geometry e il numero di elementi in questa matrice.

Nell'esempio di codice seguente viene prima dichiarata una matrice di oggetti geometry. Questi oggetti sono quattro cerchi concentrici con i raggi seguenti: 25, 50, 75 e 100. Chiamare quindi [**CreateGeometryGroup**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup) sull'oggetto [**ID2D1Factory,**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) passando [**D2D1 \_ FILL MODE \_ \_ ALTERNATE,**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode)una matrice di oggetti geometry da aggiungere al gruppo geometry e il numero di elementi in questa matrice.


```C++
ID2D1Geometry *ppGeometries[] =
{
    m_pEllipseGeometry1,
    m_pEllipseGeometry2,
    m_pEllipseGeometry3,
    m_pEllipseGeometry4
};

hr = m_pD2DFactory->CreateGeometryGroup(
    D2D1_FILL_MODE_ALTERNATE,
    ppGeometries,
    ARRAYSIZE(ppGeometries),
    &m_pGeoGroup_AlternateFill
    );

if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory->CreateGeometryGroup(
        D2D1_FILL_MODE_WINDING,
        ppGeometries,
        ARRAYSIZE(ppGeometries),
        &m_pGeoGroup_WindingFill
        );
}
```

La figura seguente mostra i risultati del rendering delle due geometrie di gruppo dell'esempio.

![illustrazione di due set di quattro cerchi concentrici, uno con anelli alternati riempiti e uno con tutti gli anelli riempiti](images/create-geometry-group.png)

### <a name="transformed-geometries"></a>Geometrie trasformate

Esistono diversi modi per trasformare una geometria. Puoi usare il metodo [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)) di una destinazione di rendering per trasformare tutto ciò che disegna la destinazione di rendering oppure puoi associare una trasformazione direttamente a una geometria usando il metodo [**CreateTransformedGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f_id2d1transformedgeometry)) per creare un oggetto [**ID2D1TransformedGeometry.**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85))

Il metodo da usare dipende dall'effetto desiderato. Quando si usa la destinazione di rendering per trasformare e quindi eseguire il rendering di una geometria, la trasformazione influisce su tutto ciò che riguarda la geometria, inclusa la larghezza di qualsiasi tratto applicato. D'altra parte, quando si usa [**id2D1TransformedGeometry,**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry)la trasformazione influisce solo sulle coordinate che descrivono la forma. La trasformazione non influisce lo spessore del tratto quando viene disegnata la geometria.

> [!Note]  
> A partire Windows 8 la trasformazione del mondo non influirà sugli spessori dei tratti con TIPO DI TRASFORMAZIONE TRATTO [**D2D1 \_ \_ \_ \_ FIXED**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type)o [**D2D1 \_ STROKE TRANSFORM TYPE \_ \_ \_ HAIRLINE**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type). È consigliabile usare questi tipi di trasformazione per ottenere tratti indipendenti dalla trasformazione

 

L'esempio seguente crea un [**id2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry)e quindi lo disegna senza trasformarlo. Produce l'output illustrato nella figura seguente.

![illustrazione di un rettangolo](images/transformedgeometry2-step1.png)


```C++
hr = m_pD2DFactory->CreateRectangleGeometry(
    D2D1::RectF(150.f, 150.f, 200.f, 200.f),
    &m_pRectangleGeometry
    );
```




```C++
// Draw the untransformed rectangle geometry.
m_pRenderTarget->DrawGeometry(m_pRectangleGeometry, m_pBlackBrush, 1);
```



L'esempio seguente usa la destinazione di rendering per ridimensionare la geometria di un fattore di 3, quindi la disegna. La figura seguente mostra il risultato del disegno del rettangolo senza la trasformazione e con la trasformazione . Si noti che il tratto è più spesso dopo la trasformazione, anche se lo spessore del tratto è 1.

![illustrazione di un rettangolo più piccolo all'interno di un rettangolo più grande con tratto più spesso](images/transformedgeometry2-step2.png)


```C++
// Transform the render target, then draw the rectangle geometry again.
m_pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Scale(
        D2D1::SizeF(3.f, 3.f),
        D2D1::Point2F(175.f, 175.f))
    );

m_pRenderTarget->DrawGeometry(m_pRectangleGeometry, m_pBlackBrush, 1);
```



L'esempio seguente usa [**il metodo CreateTransformedGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry)) per ridimensionare la geometria di un fattore di 3 e quindi la disegna. Produce l'output illustrato nella figura seguente. Si noti che, anche se il rettangolo è più grande, il tratto non è aumentato.

![illustrazione di un rettangolo più piccolo all'interno di un rettangolo più grande con lo stesso spessore del tratto](images/transformedgeometry2-step3.png)


```C++
 // Create a geometry that is a scaled version
 // of m_pRectangleGeometry.
 // The new geometry is scaled by a factory of 3
 // from the center of the geometry, (35, 35).

 hr = m_pD2DFactory->CreateTransformedGeometry(
     m_pRectangleGeometry,
     D2D1::Matrix3x2F::Scale(
         D2D1::SizeF(3.f, 3.f),
         D2D1::Point2F(175.f, 175.f)),
     &m_pTransformedGeometry
     );
```




```C++
// Replace the previous render target transform.
m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

// Draw the transformed geometry.
m_pRenderTarget->DrawGeometry(m_pTransformedGeometry, m_pBlackBrush, 1);
```



## <a name="geometries-as-masks"></a>Geometrie come maschere

È possibile usare un [**oggetto ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) come maschera geometrica quando si chiama il [**metodo PushLayer.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) La maschera geometrica specifica l'area del livello composito nella destinazione di rendering. Per altre informazioni, vedere la sezione Geometric Masks (Maschere geometriche) di [Panoramica dei livelli.](direct2d-layers-overview.md)

## <a name="geometric-operations"></a>Operazioni geometriche

[**L'interfaccia ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) fornisce diverse operazioni geometriche che è possibile usare per modificare e misurare le figure geometriche. Ad esempio, è possibile usarli per calcolare e restituire i limiti, confrontare per vedere in che modo una geometria è correlata a livello spaziale a un'altra (utile per l'hit testing), calcolare le aree e le lunghezze e altro ancora. Nella tabella seguente vengono descritte le operazioni geometriche comuni.



| Operazione                                                   | Metodo                                                                                                                                                                     |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Combina                                                     | [**CombineWithGeometry**](id2d1geometry-combinewithgeometry.md)                                                                                                           |
| Limiti/Limiti ampi/Recupera limiti, aggiornamento dell'area dirty | [**Widen,**](id2d1geometry-widen.md) [**GetBounds,**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gdimetafile-getbounds) [**GetWidenedBounds**](id2d1geometry-getwidenedbounds.md)                             |
| Hit Testing                                                 | [**FillContainsPoint**](id2d1geometry-fillcontainspoint.md), [ **StrokeContainsPoint**](id2d1geometry-strokecontainspoint.md)                                             |
| Stroke                                                      | [**StrokeContainsPoint**](id2d1geometry-strokecontainspoint.md)                                                                                                           |
| Confronto                                                  | [**CompareWithGeometry**](id2d1geometry-comparewithgeometry.md)                                                                                                           |
| Semplificazione (rimuove gli archi e le curve di Bézier quadratica)   | [**Semplificare**](id2d1geometry-simplify.md)                                                                                                                                 |
| Suddivisione a mosaico                                                | [**A tessellate**](id2d1geometry-tessellate.md)                                                                                                                             |
| Contorno (rimozione dell'intersezione)                               | [**Riquadro**](id2d1geometry-outline.md)                                                                                                                                   |
| Calcolare l'area o la lunghezza di una geometria                  | [**ComputeArea**](id2d1geometry-computearea.md), [**ComputeLength**](id2d1geometry-computelength.md), [**ComputePointAtLength**](id2d1geometry-computepointatlength.md) |



 

> [!Note]  
> A partire da Windows 8, è possibile usare il metodo [**ComputePointAndSegmentAtLength**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1pathgeometry1-computepointandsegmentatlength(float_uint32_constd2d1_matrix_3x2_f_float_d2d1_point_description)) in [**ID2D1PathGeometry1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1pathgeometry1) per calcolare l'area o la lunghezza di una geometria.

 

### <a name="combining-geometries"></a>Combinazione di geometrie

Per combinare una geometria con un'altra, chiamare il [**metodo ID2D1Geometry::CombineWithGeometry.**](id2d1geometry-combinewithgeometry.md) Quando si combinano le geometrie, si specifica uno dei quattro modi per eseguire l'operazione di combinazione: [**D2D1 \_ COMBINE \_ MODE \_ UNION**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (union), [**D2D1 \_ COMBINE MODE \_ \_ INTERSECT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (intersect), [**D2D1 \_ COMBINE MODE \_ \_ XOR**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (xor) e [**D2D1 \_ COMBINE MODE EXCLUDE \_ \_ (exclude).**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) L'esempio di codice seguente mostra due cerchi combinati usando la modalità unione, in cui il primo cerchio ha il punto centrale (75, 75) e il raggio di 50 e il secondo cerchio ha il punto centrale (125, 75) e il raggio di 50.


```C++
HRESULT hr = S_OK;
ID2D1GeometrySink *pGeometrySink = NULL;

// Create the first ellipse geometry to merge.
const D2D1_ELLIPSE circle1 = D2D1::Ellipse(
    D2D1::Point2F(75.0f, 75.0f),
    50.0f,
    50.0f
    );

hr = m_pD2DFactory->CreateEllipseGeometry(
    circle1,
    &m_pCircleGeometry1
    );

if (SUCCEEDED(hr))
{
    // Create the second ellipse geometry to merge.
    const D2D1_ELLIPSE circle2 = D2D1::Ellipse(
        D2D1::Point2F(125.0f, 75.0f),
        50.0f,
        50.0f
        );

    hr = m_pD2DFactory->CreateEllipseGeometry(circle2, &m_pCircleGeometry2);
}


if (SUCCEEDED(hr))
{
    //
    // Use D2D1_COMBINE_MODE_UNION to combine the geometries.
    //
    hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometryUnion);

    if (SUCCEEDED(hr))
    {
        hr = m_pPathGeometryUnion->Open(&pGeometrySink);

        if (SUCCEEDED(hr))
        {
            hr = m_pCircleGeometry1->CombineWithGeometry(
                m_pCircleGeometry2,
                D2D1_COMBINE_MODE_UNION,
                NULL,
                NULL,
                pGeometrySink
                );
        }

        if (SUCCEEDED(hr))
        {
            hr = pGeometrySink->Close();
        }

        SafeRelease(&pGeometrySink);
    }
}
```



La figura seguente mostra due cerchi combinati con una modalità di combinazione di unione.

![illustrazione di due cerchi sovrapposti combinati in un'unione](images/combine-mode-union.png)

Per illustrazioni di tutte le modalità di combinazione, vedere [**l'enumerazione \_ COMBINE \_ MODE D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode).

### <a name="widen"></a>Ampliare

Il [**metodo Widen**](id2d1geometry-widen.md) genera una nuova geometria il cui riempimento equivale a riempire la geometria esistente e quindi scrive il risultato nell'oggetto [**ID2D1SimplifiedGeometrySink specificato.**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) L'esempio di codice seguente [**chiama Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) sull'oggetto [**ID2D1PathGeometry.**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) Se **Open** ha esito positivo, chiama **Widen** sull'oggetto geometry.


```C++
ID2D1GeometrySink *pGeometrySink = NULL;
hr = pPathGeometry->Open(&pGeometrySink);
if (SUCCEEDED(hr))
{
    hr = pGeometry->Widen(
            strokeWidth,
            pIStrokeStyle,
            pWorldTransform,
            pGeometrySink
            );
```



### <a name="tessellate"></a>Tessellate

Il [**metodo Tessellate**](id2d1geometry-tessellate.md) crea un set di triangoli in senso orario che coprono la geometria dopo che è stata trasformata usando la matrice specificata e appiattita usando la tolleranza specificata. L'esempio di codice seguente **usa Tessellate** per creare un elenco di triangoli che rappresentano *pPathGeometry*. I triangoli vengono archiviati in [**id2D1Mesh**](/windows/win32/api/d2d1/nn-d2d1-id2d1mesh), *pMesh* e quindi trasferiti a un membro della classe, *m \_ pStrokeMesh*, per un uso successivo durante il rendering.


```C++
ID2D1Mesh *pMesh = NULL;
hr = m_pRT->CreateMesh(&pMesh);
if (SUCCEEDED(hr))
{
    ID2D1TessellationSink *pSink = NULL;
    hr = pMesh->Open(&pSink);
    if (SUCCEEDED(hr))
    {
        hr = pPathGeometry->Tessellate(
                NULL, // world transform (already handled in Widen)
                pSink
                );
        if (SUCCEEDED(hr))
        {
            hr = pSink->Close();
            if (SUCCEEDED(hr))
            {
                SafeReplace(&m_pStrokeMesh, pMesh);
            }
        }
        pSink->Release();
    }
    pMesh->Release();
}
```



### <a name="fillcontainspoint-and-strokecontainspoint"></a>FillContainsPoint e StrokeContainsPoint

Il [**metodo FillContainsPoint**](id2d1geometry-fillcontainspoint.md) indica se l'area riempita dalla geometria contiene il punto specificato. È possibile usare questo metodo per eseguire l'hit testing. L'esempio di codice seguente chiama **FillContainsPoint** su un [**oggetto ID2D1EllipseGeometry,**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) passando un punto in corrispondenza di (0,0) e una matrice [**Identity.**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-isidentity)


```C++
BOOL containsPoint1;
hr = m_pCircleGeometry1->FillContainsPoint(
    D2D1::Point2F(0,0),
    D2D1::Matrix3x2F::Identity(),
    &containsPoint1
    );

if (SUCCEEDED(hr))
{
    // Process containsPoint.
}
```



Il [**metodo StrokeContainsPoint**](id2d1geometry-strokecontainspoint.md) determina se il tratto della geometria contiene il punto specificato. È possibile usare questo metodo per eseguire l'hit testing. Nell'esempio di codice seguente **viene utilizzato StrokeContainsPoint**.


```C++
BOOL containsPoint;

hr = m_pCircleGeometry1->StrokeContainsPoint(
    D2D1::Point2F(0,0),
    10,     // stroke width
    NULL,   // stroke style
    NULL,   // world transform
    &containsPoint
    );

if (SUCCEEDED(hr))
{
    // Process containsPoint.
}
```



### <a name="simplify"></a>Semplificare 

Il [**metodo Simplify**](id2d1geometry-simplify.md) rimuove archi e curve di Bézier quadratica da una geometria specificata. La geometria risultante contiene quindi solo linee e, facoltativamente, curve di Bézier cubiche. L'esempio di codice seguente usa **Simplify** per trasformare una geometria con curve di Bézier in una geometria che contiene solo segmenti di linea.


```C++
HRESULT D2DFlatten(
    ID2D1Geometry *pGeometry,
    float flatteningTolerance,
    ID2D1Geometry **ppGeometry
    )
{
    HRESULT hr;
    ID2D1Factory *pFactory = NULL;
    pGeometry->GetFactory(&pFactory);

    ID2D1PathGeometry *pPathGeometry = NULL;
    hr = pFactory->CreatePathGeometry(&pPathGeometry);

    if (SUCCEEDED(hr))
    {
        ID2D1GeometrySink *pSink = NULL;
        hr = pPathGeometry->Open(&pSink);

        if (SUCCEEDED(hr))
        {
            hr = pGeometry->Simplify(
                    D2D1_GEOMETRY_SIMPLIFICATION_OPTION_LINES,
                    NULL, // world transform
                    flatteningTolerance,
                    pSink
                    );

            if (SUCCEEDED(hr))
            {
                hr = pSink->Close();

                if (SUCCEEDED(hr))
                {
                    *ppGeometry = pPathGeometry;
                    (*ppGeometry)->AddRef();
                }
            }
            pSink->Release();
        }
        pPathGeometry->Release();
    }

    pFactory->Release();

    return hr;
}
```



### <a name="computelength-and-computearea"></a>ComputeLength e ComputeArea

Il [**metodo ComputeLength**](id2d1geometry-computelength.md) calcola la lunghezza della geometria specificata se ogni segmento è stato scollegato in una linea. Include il segmento di chiusura implicito se la geometria è chiusa. L'esempio di codice seguente usa **ComputeLength** per calcolare la lunghezza di un cerchio specificato (**m \_ pCircleGeometry1**).


```C++
float length;

// Compute the area of circle1
hr = m_pCircleGeometry1->ComputeLength(
    D2D1::IdentityMatrix(),
    &length
    );

if (SUCCEEDED(hr))
{
    // Process the length of the geometry.
}
```



Il [**metodo ComputeArea**](id2d1geometry-computearea.md) calcola l'area della geometria specificata. L'esempio di codice seguente **usa ComputeArea** per calcolare l'area di un cerchio specificato (**m \_ pCircleGeometry1**).


```C++
float area;

// Compute the area of circle1
hr = m_pCircleGeometry1->ComputeArea(
    D2D1::IdentityMatrix(),
    &area
    );
```



### <a name="comparewithgeometry"></a>CompareWithGeometry

Il [**metodo CompareWithGeometry**](id2d1geometry-comparewithgeometry.md) descrive l'intersezione tra la geometria che chiama questo metodo e la geometria specificata. I valori possibili per l'intersezione includono [**D2D1 \_ GEOMETRY \_ RELATION \_ DISJOINT (disjoint),**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_relation) **D2D1 \_ GEOMETRY \_ RELATION IS \_ \_ CONTAINED** (è contenuto), **D2D1 \_ GEOMETRY RELATION CONTAINS \_ \_ (contains)** e **D2D1 \_ GEOMETRY RELATION \_ \_ OVERLAP** (sovrapposizione). "disgiunto" significa che due riempimenti geometrici non si intersecano affatto. "è contenuto" significa che la geometria è completamente contenuta nella geometria specificata. "contains" significa che la geometria contiene completamente la geometria specificata e "sovrapposizione" significa che le due geometrie si sovrappongono, ma nessuna contiene completamente l'altra.

Nell'esempio di codice seguente viene illustrato come confrontare due cerchi con lo stesso raggio di 50 ma con offset di 50.


```C++
HRESULT hr = S_OK;
ID2D1GeometrySink *pGeometrySink = NULL;

// Create the first ellipse geometry to merge.
const D2D1_ELLIPSE circle1 = D2D1::Ellipse(
    D2D1::Point2F(75.0f, 75.0f),
    50.0f,
    50.0f
    );

hr = m_pD2DFactory->CreateEllipseGeometry(
    circle1,
    &m_pCircleGeometry1
    );

if (SUCCEEDED(hr))
{
    // Create the second ellipse geometry to merge.
    const D2D1_ELLIPSE circle2 = D2D1::Ellipse(
        D2D1::Point2F(125.0f, 75.0f),
        50.0f,
        50.0f
        );

    hr = m_pD2DFactory->CreateEllipseGeometry(circle2, &m_pCircleGeometry2);
}

```




```C++
D2D1_GEOMETRY_RELATION result = D2D1_GEOMETRY_RELATION_UNKNOWN;

// Compare circle1 with circle2
hr = m_pCircleGeometry1->CompareWithGeometry(
    m_pCircleGeometry2,
    D2D1::IdentityMatrix(),
    0.1f,
    &result
    );

if (SUCCEEDED(hr))
{
    static const WCHAR szGeometryRelation[] = L"Two circles overlap.";
    m_pRenderTarget->SetTransform(D2D1::IdentityMatrix());
    if (result == D2D1_GEOMETRY_RELATION_OVERLAP)
    {
        m_pRenderTarget->DrawText(
            szGeometryRelation,
            ARRAYSIZE(szGeometryRelation) - 1,
            m_pTextFormat,
            D2D1::RectF(25.0f, 160.0f, 200.0f, 300.0f),
            m_pTextBrush
            );
    }
}
```



### <a name="outline"></a>Riquadro

Il [**metodo Outline**](id2d1geometry-outline.md) calcola la struttura della geometria (una versione della geometria in cui nessuna figura si incrocia o qualsiasi altra figura) e scrive il risultato in [**id2D1SimplifiedGeometrySink.**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) Nell'esempio di codice seguente **viene utilizzato Outline** per costruire una geometria equivalente senza auto-intersezioni. Usa la tolleranza di appiattimento predefinita.


```C++
HRESULT D2DOutline(
    ID2D1Geometry *pGeometry,
    ID2D1Geometry **ppGeometry
    )
{
    HRESULT hr;
    ID2D1Factory *pFactory = NULL;
    pGeometry->GetFactory(&pFactory);

    ID2D1PathGeometry *pPathGeometry = NULL;
    hr = pFactory->CreatePathGeometry(&pPathGeometry);

    if (SUCCEEDED(hr))
    {
        ID2D1GeometrySink *pSink = NULL;
        hr = pPathGeometry->Open(&pSink);

        if (SUCCEEDED(hr))
        {
            hr = pGeometry->Outline(NULL, pSink);

            if (SUCCEEDED(hr))
            {
                hr = pSink->Close();

                if (SUCCEEDED(hr))
                {
                    *ppGeometry = pPathGeometry;
                    (*ppGeometry)->AddRef();
                }
            }
            pSink->Release();
        }
        pPathGeometry->Release();
    }

    pFactory->Release();

    return hr;
}
```



### <a name="getbounds-and-getwidenedbounds"></a>GetBounds e GetWidenedBounds

Il [**metodo GetBounds**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gdimetafile-getbounds) recupera i limiti della geometria. Nell'esempio di codice seguente viene utilizzato **GetBounds** per recuperare i limiti di un cerchio specificato (**m \_ pCircleGeometry1**).


```C++
D2D1_RECT_F bounds;

hr = m_pCircleGeometry1->GetBounds(
      D2D1::IdentityMatrix(),
      &bounds
     );

if (SUCCEEDED(hr))
{
    // Retrieve the bounds.
}
```



Il [**metodo GetWidenedBounds**](id2d1geometry-getwidenedbounds.md) recupera i limiti della geometria dopo che è stata ampliata in base alla larghezza e allo stile del tratto specificati e trasformata dalla matrice specificata. L'esempio di codice seguente usa **GetWidenedBounds** per recuperare i limiti di un cerchio specificato (**m \_ pCircleGeometry1**) dopo che è stato ampliato in base alla larghezza del tratto specificata.


```C++
float dashes[] = {1.f, 1.f, 2.f, 3.f, 5.f};

m_pD2DFactory->CreateStrokeStyle(
    D2D1::StrokeStyleProperties(
        D2D1_CAP_STYLE_FLAT,
        D2D1_CAP_STYLE_FLAT,
        D2D1_CAP_STYLE_ROUND,
        D2D1_LINE_JOIN_ROUND,   // lineJoin
        10.f,   //miterLimit
        D2D1_DASH_STYLE_CUSTOM,
        0.f     //dashOffset
        ),
     dashes,
     ARRAYSIZE(dashes)-1,
     &m_pStrokeStyle
     );
```




```C++
D2D1_RECT_F bounds1;
hr = m_pCircleGeometry1->GetWidenedBounds(
      5.0,
      m_pStrokeStyle,
      D2D1::IdentityMatrix(),
      &bounds1
     );
if (SUCCEEDED(hr))
{
    // Retrieve the widened bounds.
}
```



### <a name="computepointatlength"></a>ComputePointAtLength

Il [**metodo ComputePointAtLength**](id2d1geometry-computepointatlength.md) calcola il punto e il vettore tangente alla distanza specificata lungo la geometria. Nell'esempio di codice seguente viene **utilizzato ComputePointAtLength**.


```C++
D2D1_POINT_2F point;
D2D1_POINT_2F tangent;

hr = m_pCircleGeometry1->ComputePointAtLength(
    10, 
    NULL, 
    &point, 
    &tangent); 
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica delle geometrie dei percorsi](path-geometries-overview.md)
</dt> <dt>

[Informazioni di riferimento su Direct2D](reference.md)
</dt> </dl>

 

 