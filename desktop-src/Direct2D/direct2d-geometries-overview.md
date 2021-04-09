---
title: 'Panoramica delle geometrie '
description: Vengono descritte le nozioni di base delle geometrie Direct2D, ovvero gli oggetti che è possibile utilizzare per rappresentare, modificare e analizzare le forme.
ms.assetid: f5870d4b-dd30-4034-884e-1c398a6865c6
keywords:
- Direct2D, Cenni preliminari sulle geometrie
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: cb97b0737bfad391fb9ba2501793a970fcbd9886
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "103734570"
---
# <a name="geometries-overview"></a>Panoramica delle geometrie 

In questa panoramica viene descritto come creare e utilizzare oggetti [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) per definire e modificare le cifre 2D. Include le sezioni seguenti:

## <a name="what-is-a-direct2d-geometry"></a>Che cos'è una geometria Direct2D?

Una geometria Direct2D è un oggetto [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) . Questo oggetto può essere una geometria semplice ([**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry), [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry)o [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry)), una geometria del percorso ([**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry)) o una geometria composita ([**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) e [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry)).

Le geometrie Direct2D consentono di descrivere le cifre bidimensionali e offrono molti utilizzi, ad esempio la definizione di aree di hit test, aree di ritaglio e persino percorsi di animazione.

Le geometrie Direct2D sono risorse non modificabili e indipendenti dal dispositivo create da [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory). In genere, è necessario creare geometrie una volta e mantenerle per la durata dell'applicazione o fino a quando non è necessario modificarle. Per altre informazioni sulle risorse indipendenti dal dispositivo e dipendenti dal dispositivo, vedere [Panoramica delle risorse](resources-and-resource-domains.md).

Le sezioni seguenti descrivono i diversi tipi di geometrie.

## <a name="simple-geometries"></a>Geometrie semplici

Le geometrie semplici includono oggetti [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry), [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry)e [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) e possono essere usati per creare figure geometriche di base, ad esempio rettangoli, rettangoli arrotondati, cerchi e ellissi.

Per creare una geometria semplice, usare uno dei metodi [**ID2D1Factory:: create<*GeometryType*>Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) . Questi metodi creano un oggetto del tipo specificato. Per creare, ad esempio, un rettangolo, chiamare [**ID2D1Factory:: CreateRectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry)), che restituisce un oggetto [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) ; per creare un rettangolo arrotondato, chiamare [**ID2D1Factory:: CreateRoundedRectangleGeometry**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createroundedrectanglegeometry(constd2d1_rounded_rect__id2d1roundedrectanglegeometry)), che restituisce un oggetto [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry) e così via.

Nell'esempio di codice seguente viene chiamato il metodo [**CreateEllipseGeometry**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createellipsegeometry(constd2d1_ellipse__id2d1ellipsegeometry)) , passando una struttura ellisse con il *centro* impostato su (100, 100), *x-RADIUS* a 100 e *y-RADIUS* a 50. Chiama quindi [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry), passando la geometria dei puntini di sospensione restituita, un puntatore a una [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)nera e una larghezza del tratto di 5. La figura seguente mostra l'output dell'esempio di codice.

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



Per disegnare la struttura di qualsiasi geometria, usare il metodo [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) . Per disegnare l'interno, usare il metodo [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) .

## <a name="path-geometries"></a>Geometrie percorso

Le geometrie del percorso sono rappresentate dall'interfaccia [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) . Questi oggetti possono essere usati per descrivere figure geometriche complesse costituite da segmenti come archi, curve e linee. Nella figura seguente viene illustrato un disegno creato utilizzando la geometria del percorso.

![illustrazione di un fiume, delle montagne e del sole](images/path-geo-mnts.png)

Per altre informazioni ed esempi, vedere [Cenni preliminari sulle geometrie del percorso](path-geometries-overview.md).

## <a name="composite-geometries"></a>Geometrie composite

Una geometria composita è una geometria raggruppata o combinata con un altro oggetto Geometry o con una trasformazione. Le geometrie composite includono oggetti [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry) e [**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) .

### <a name="geometry-groups"></a>Gruppi di geometria

I gruppi Geometry rappresentano un modo pratico per raggruppare contemporaneamente più geometrie, in modo che tutte le cifre di diverse geometrie vengano concatenate in una sola. Per creare un oggetto [**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) , chiamare il metodo [**CreateGeometryGroup**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup) sull'oggetto [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) , passando il *FillMode* con i valori possibili della [**modalità di \_ riempimento \_ d2d1 \_ alternativa**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode) (alternativa) e **la \_ \_ modalità di \_ riempimento d2d1**, una matrice di oggetti Geometry da aggiungere al gruppo Geometry e il numero di elementi in questa matrice.

Nell'esempio di codice riportato di seguito viene innanzitutto dichiarata una matrice di oggetti Geometry. Questi oggetti sono quattro cerchi concentrici con i raggi seguenti: 25, 50, 75 e 100. Chiamare quindi il metodo [**CreateGeometryGroup**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup) sull'oggetto [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) , passando in [**\_ \_ modalità di riempimento \_ d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode), una matrice di oggetti Geometry da aggiungere al gruppo Geometry e il numero di elementi in questa matrice.


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

Nella figura seguente sono illustrati i risultati del rendering delle due geometrie di gruppo dall'esempio.

![illustrazione di due set di quattro cerchi concentrici, uno con anelli alternati pieni e uno con tutti gli anelli riempiti](images/create-geometry-group.png)

### <a name="transformed-geometries"></a>Geometrie trasformate

Esistono diversi modi per trasformare una geometria. È possibile utilizzare il metodo [**setransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)) di una destinazione di rendering per trasformare tutti gli elementi che la destinazione di rendering disegna oppure è possibile associare una trasformazione direttamente a una geometria utilizzando il metodo [**CreateTransformedGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f_id2d1transformedgeometry)) per creare un [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)).

Il metodo da usare dipende dall'effetto desiderato. Quando si usa la destinazione di rendering per trasformare ed eseguire il rendering di una geometria, la trasformazione influiscono su tutti gli elementi relativi alla geometria, inclusa la larghezza di qualsiasi tratto applicato. D'altra parte, quando si usa un [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry), la trasformazione influiscono solo sulle coordinate che descrivono la forma. La trasformazione non influirà sullo spessore del tratto quando viene disegnata la geometria.

> [!Note]  
> A partire da Windows 8, la trasformazione globale non influisce sullo spessore del tratto dei tratti con [**\_ tipo di trasformazione Stroke d2d1 di \_ \_ tipo \_ fixed**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type)o [**d2d1 \_ Stroke \_ Transform \_ \_**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type). È consigliabile usare questi tipi di trasformazione per ottenere tratti di trasformazione indipendenti

 

Nell'esempio seguente viene creato un [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry), quindi viene disegnato senza trasformarlo. Produce l'output mostrato nella figura seguente.

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



Nell'esempio seguente viene usata la destinazione di rendering per ridimensionare la geometria in base a un fattore 3, quindi viene disegnata. Nella figura seguente viene illustrato il risultato della creazione del rettangolo senza la trasformazione e con la trasformazione. Si noti che il tratto è più spessa dopo la trasformazione, anche se lo spessore del tratto è 1.

![illustrazione di un rettangolo più piccolo all'interno di un rettangolo più grande con un tratto più spessa](images/transformedgeometry2-step2.png)


```C++
// Transform the render target, then draw the rectangle geometry again.
m_pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Scale(
        D2D1::SizeF(3.f, 3.f),
        D2D1::Point2F(175.f, 175.f))
    );

m_pRenderTarget->DrawGeometry(m_pRectangleGeometry, m_pBlackBrush, 1);
```



Nell'esempio seguente viene usato il metodo [**CreateTransformedGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry)) per ridimensionare la geometria per un fattore 3, quindi viene disegnata. Produce l'output mostrato nella figura seguente. Si noti che, anche se il rettangolo è più grande, il relativo tratto non è aumentato.

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

Quando si chiama il metodo [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) , è possibile usare un oggetto [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) come maschera geometrica. La maschera geometrica specifica l'area del livello composito nella destinazione di rendering. Per altre informazioni, vedere la sezione maschere geometriche della [Panoramica dei livelli](direct2d-layers-overview.md).

## <a name="geometric-operations"></a>Operazioni geometriche

L'interfaccia [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) fornisce diverse operazioni geometriche che è possibile usare per modificare e misurare le cifre geometriche. Ad esempio, è possibile usarli per calcolare e restituire i limiti, confrontare per vedere in che modo una geometria è correlata a livello spaziale a un'altra (utile per l'hit test), calcolare le aree e le lunghezze e altro ancora. Nella tabella seguente vengono descritte le operazioni geometriche comuni.



| Operazione                                                   | Metodo                                                                                                                                                                     |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Combina                                                     | [**CombineWithGeometry**](id2d1geometry-combinewithgeometry.md)                                                                                                           |
| Limiti/limiti estesi/recupera limiti, aggiornamento area dirty | [**Ampliamento**](id2d1geometry-widen.md), [**GetBounds**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gdimetafile-getbounds), [**GetWidenedBounds**](id2d1geometry-getwidenedbounds.md)                             |
| Hit Testing                                                 | [**FillContainsPoint**](id2d1geometry-fillcontainspoint.md), [ **StrokeContainsPoint**](id2d1geometry-strokecontainspoint.md)                                             |
| Stroke                                                      | [**StrokeContainsPoint**](id2d1geometry-strokecontainspoint.md)                                                                                                           |
| Confronto                                                  | [**CompareWithGeometry**](id2d1geometry-comparewithgeometry.md)                                                                                                           |
| Semplificazione (rimuove archi e curve di Bézier quadratiche)   | [**Semplificare**](id2d1geometry-simplify.md)                                                                                                                                 |
| Suddivisione a mosaico                                                | [**Conteggiarla suddividerla**](id2d1geometry-tessellate.md)                                                                                                                             |
| Struttura (Rimuovi intersezione)                               | [**Riquadro**](id2d1geometry-outline.md)                                                                                                                                   |
| Calcolare l'area o la lunghezza di una geometria                  | [**ComputeArea**](id2d1geometry-computearea.md), [**ComputeLength**](id2d1geometry-computelength.md), [**ComputePointAtLength**](id2d1geometry-computepointatlength.md) |



 

> [!Note]  
> A partire da Windows 8, è possibile usare il metodo [**ComputePointAndSegmentAtLength**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1pathgeometry1-computepointandsegmentatlength(float_uint32_constd2d1_matrix_3x2_f_float_d2d1_point_description)) in [**ID2D1PathGeometry1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1pathgeometry1) per calcolare l'area o la lunghezza di una geometria.

 

### <a name="combining-geometries"></a>Combinazione di geometrie

Per combinare una geometria con un'altra, chiamare il metodo [**ID2D1Geometry:: CombineWithGeometry**](id2d1geometry-combinewithgeometry.md) . Quando si combinano le geometrie, è possibile specificare uno dei quattro modi per eseguire l'operazione di combinazione, ovvero Unione [**d2d1 \_ \_ modalità \_ combinata**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (Unione), [**\_ modalità combinata d2d1 \_ \_ Intersect**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (Intersect), [**d2d1 \_ Combine \_ mode \_ Xor**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (XOR) e [**d2d1 \_ Combine \_ mode \_ Escludi**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (Escludi). Nell'esempio di codice seguente vengono illustrati due cerchi combinati tramite la modalità di Unione delle unioni, in cui il primo cerchio ha il punto centrale di (75, 75) e il raggio di 50 e il secondo cerchio ha il punto centrale di (125, 75) e il raggio di 50.


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



Nella figura seguente vengono illustrati due cerchi combinati con una modalità di combinazione di Union.

![illustrazione di due cerchi sovrapposti combinati in un'Unione](images/combine-mode-union.png)

Per illustrazioni di tutte le modalità di combinazione, vedere [**l' \_ enumerazione della \_ modalità di combinazione d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode).

### <a name="widen"></a>Ampliare

Il metodo [**Wide**](id2d1geometry-widen.md) genera una nuova geometria il cui riempimento equivale a tracciare la geometria esistente e quindi scrive il risultato nell'oggetto [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) specificato. Nell'esempio di codice seguente viene chiamato [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) sull'oggetto [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) . Se l' **apertura** ha esito positivo, viene chiamato **Wide** nell'oggetto Geometry.


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



### <a name="tessellate"></a>Conteggiarla suddividerla

Il metodo [**conteggiarla suddividerla**](id2d1geometry-tessellate.md) crea un set di triangoli con ferita in senso orario che coprono la geometria dopo che è stata trasformata utilizzando la matrice specificata e appiattita utilizzando la tolleranza specificata. Nell'esempio di codice seguente viene usato **conteggiarla suddividerla** per creare un elenco di triangoli che rappresentano *pPathGeometry*. I triangoli vengono archiviati in un [**ID2D1Mesh**](/windows/win32/api/d2d1/nn-d2d1-id2d1mesh), *pMesh*, quindi trasferiti a un membro di classe, *m \_ pStrokeMesh*, per un uso successivo durante il rendering.


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

Il metodo [**FillContainsPoint**](id2d1geometry-fillcontainspoint.md) indica se l'area riempita dalla geometria contiene il punto specificato. È possibile utilizzare questo metodo per eseguire l'hit testing. Nell'esempio di codice seguente viene chiamato **FillContainsPoint** su un oggetto [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) , passando un punto in (0, 0) e una matrice di [**identità**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-isidentity) .


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



Il metodo [**StrokeContainsPoint**](id2d1geometry-strokecontainspoint.md) determina se il tratto della geometria contiene il punto specificato. È possibile utilizzare questo metodo per eseguire l'hit testing. Nell'esempio di codice seguente viene usato **StrokeContainsPoint**.


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

Il metodo [**semplifica**](id2d1geometry-simplify.md) rimuove archi e curve di Bézier quadratiche da una geometria specificata. La geometria risultante contiene quindi solo le linee e, facoltativamente, le curve di Bézier cubiche. Nell'esempio di codice seguente viene usato il comando **semplificato** per trasformare una geometria con curve di Bezier in una geometria che contiene solo segmenti di linea.


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

Il metodo [**ComputeLength**](id2d1geometry-computelength.md) calcola la lunghezza della geometria specificata se ogni segmento è stato registrato in una riga. Questo include il segmento di chiusura implicito se la geometria viene chiusa. Nell'esempio di codice seguente viene usato **ComputeLength** per calcolare la lunghezza di un cerchio specificato (**m \_ pCircleGeometry1**).


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



Il metodo [**ComputeArea**](id2d1geometry-computearea.md) calcola l'area della geometria specificata. Nell'esempio di codice seguente viene usato **ComputeArea** per calcolare l'area di un cerchio specificato (**m \_ pCircleGeometry1**).


```C++
float area;

// Compute the area of circle1
hr = m_pCircleGeometry1->ComputeArea(
    D2D1::IdentityMatrix(),
    &area
    );
```



### <a name="comparewithgeometry"></a>CompareWithGeometry

Il metodo [**CompareWithGeometry**](id2d1geometry-comparewithgeometry.md) descrive l'intersezione tra la geometria che chiama questo metodo e la geometria specificata. I valori possibili per l'intersezione includono la relazione di geometria d2d1 (disgiunta), la **\_ relazione di geometria d2d1 \_ \_ è \_ contenuta** (is contained), la relazione di geometria **d2d1 \_ \_ \_ contiene** (Contains) e **d2d1 \_ Geometry \_ Relation \_** (sovrapposizioni). [**\_ \_ \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_relation) "disgiunto" significa che due riempimenti di geometria non si intersecano affatto. "è contenuto" significa che la geometria è completamente contenuta dalla geometria specificata. "Contains" significa che la geometria contiene completamente la geometria specificata e "sovrapposizione" significa che le due geometrie si sovrappongono, ma nessuna delle due contiene completamente l'altra.

Nell'esempio di codice riportato di seguito viene illustrato come confrontare due cerchi con lo stesso raggio di 50 ma con offset di 50.


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

Il metodo di [**struttura**](id2d1geometry-outline.md) calcola il contorno della geometria (una versione della geometria in cui nessuna figura si interseca se stessa o qualsiasi altra figura) e scrive il risultato in un [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink). Nell'esempio di codice seguente viene usato il **contorno** per costruire una geometria equivalente senza alcuna intersezione automatica. Usa la tolleranza di Flat predefinita.


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

Il metodo [**GetBounds**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gdimetafile-getbounds) recupera i limiti della geometria. Nell'esempio di codice seguente viene usato **GetBounds** per recuperare i limiti di un cerchio specificato **( \_ m pCircleGeometry1**).


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



Il metodo [**GetWidenedBounds**](id2d1geometry-getwidenedbounds.md) recupera i limiti della geometria dopo che è stato ampliato dalla larghezza e dallo stile del tratto specificato e trasformato dalla matrice specificata. Nell'esempio di codice seguente viene usato **GetWidenedBounds** per recuperare i limiti di un cerchio specificato (**m \_ pCircleGeometry1**) dopo che è stato ampliato in base alla larghezza del tratto specificata.


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

Il metodo [**ComputePointAtLength**](id2d1geometry-computepointatlength.md) calcola il vettore punto e tangente alla distanza specificata lungo la geometria. Nell'esempio di codice seguente viene usato **ComputePointAtLength**.


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

[Cenni preliminari sulle geometrie del percorso](path-geometries-overview.md)
</dt> <dt>

[Riferimento Direct2D](reference.md)
</dt> </dl>

 

 