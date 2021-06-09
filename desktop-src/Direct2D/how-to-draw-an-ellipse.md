---
title: Come disegnare e riempire una forma di base
description: Questo argomento descrive come disegnare una forma di base.
ms.assetid: 8a68fc3f-118c-447b-856c-05417ae4ef29
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 93d8f3a3ddeb06c9168971789dff3ac8c9222d22
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827000"
---
# <a name="how-to-draw-and-fill-a-basic-shape"></a>Come disegnare e riempire una forma di base

Questo argomento descrive come disegnare una forma di base. [**L'interfaccia ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) fornisce metodi per la struttura e il riempimento di ellissi, rettangoli e linee. Gli esempi seguenti illustrano come creare e disegnare un ellisse.

In questo argomento sono incluse le sezioni seguenti:

-   [Disegnare il contorno di un'ellisse con un tratto a tinta unita](#draw-the-outline-of-an-ellipse-with-a-solid-stroke)
-   [Disegnare un'ellisse con un tratto tratteggiato](#draw-an-ellipse-with-a-dashed-stroke)
-   [Disegnare e riempire un'ellisse](#draw-and-fill-an-ellipse)
-   [Disegno di forme più complesse](#drawing-more-complex-shapes)
-   [Argomenti correlati](#related-topics)

## <a name="draw-the-outline-of-an-ellipse-with-a-solid-stroke"></a>Disegnare il contorno di un'ellisse con un tratto a tinta unita

Per disegnare il contorno di un'ellisse, si definisce un pennello (ad esempio [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) o [**ID2D1LinearGradientBrush)**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)per disegnare il contorno e [**un oggetto D2D1 \_ ELLIPSE**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) per descrivere la posizione e le dimensioni dell'ellisse, quindi passare questi oggetti al metodo [**ID2D1RenderTarget::D rawEllipse.**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) L'esempio seguente crea un pennello a tinta unita nero e lo archivia nel membro della classe \_ m spBlackBrush.


```C++
hr = m_pRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF::Black),
    &m_pBlackBrush
    );
```



L'esempio successivo definisce un [**oggetto D2D1 \_ ELLIPSE**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) e lo usa con il pennello definito nell'esempio precedente per disegnare il contorno di un'ellisse. Questo esempio produce l'output illustrato nella figura seguente.

![Illustrazione di un'ellisse con un tratto a tinta unita](images/drawandfillellipseexample-1.png)


```C++
D2D1_ELLIPSE ellipse = D2D1::Ellipse(
    D2D1::Point2F(100.f, 100.f),
    75.f,
    50.f
    );

m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f);
```



## <a name="draw-an-ellipse-with-a-dashed-stroke"></a>Disegnare un'ellisse con un tratto tratteggiato

Nell'esempio precedente è stato usato un tratto normale. È possibile modificare l'aspetto di un tratto in diversi modi creando un [**oggetto ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle). **ID2D1StrokeStyle** consente di specificare la forma all'inizio e alla fine di un tratto, se ha un motivo tratteggiato e così via. Nell'esempio seguente viene creato **un oggetto ID2D1StrokeStyle** che descrive un tratto tratteggiato. In questo esempio viene utilizzato un modello di tratteggio predefinito, [**D2D1 \_ DASH STYLE DASH DOT \_ \_ \_ \_ DOT,**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_dash_style)ma è anche possibile specificarne uno personalizzato.


```C++
D2D1_STROKE_STYLE_PROPERTIES strokeStyleProperties = D2D1::StrokeStyleProperties(
    D2D1_CAP_STYLE_FLAT,  // The start cap.
    D2D1_CAP_STYLE_FLAT,  // The end cap.
    D2D1_CAP_STYLE_TRIANGLE, // The dash cap.
    D2D1_LINE_JOIN_MITER, // The line join.
    10.0f, // The miter limit.
    D2D1_DASH_STYLE_DASH_DOT_DOT, // The dash style.
    0.0f // The dash offset.
    );

hr = m_pDirect2dFactory->CreateStrokeStyle(strokeStyleProperties, NULL, 0, &m_pStrokeStyle);

```



L'esempio successivo usa lo stile del tratto con [**il metodo DrawEllipse.**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) Questo esempio produce l'output illustrato nella figura seguente.

![Illustrazione di un'ellisse con un tratto tratteggiato](images/drawandfillellipseexample-2.png)


```C++
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f, m_pStrokeStyle);
```



## <a name="draw-and-fill-an-ellipse"></a>Disegnare e riempire un'ellisse

Per disegnare l'interno di un'ellisse, usare il [**metodo FillEllipse.**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) Nell'esempio seguente viene utilizzato il [**metodo DrawEllipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) per delineare l'ellisse, quindi viene utilizzato il **metodo FillEllipse** per disegnare l'interno. Questo esempio produce l'output illustrato nella figura seguente.

![illustrazione di un'ellisse con un tratto tratteggiato e quindi riempita con un colore grigio a tinta unita](images/drawandfillellipseexample-3.png)


```C++
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f, m_pStrokeStyle);
m_pRenderTarget->FillEllipse(ellipse, m_pSilverBrush);
```



L'esempio successivo riempie prima l'ellisse e quindi ne disegna il contorno. Questo esempio produce l'output illustrato nella figura seguente.

![illustrazione di un'ellisse riempita con un colore grigio a tinta unita e quindi delineata con un tratto tratteggiato](images/drawandfillellipseexample-4.png)


```C++
m_pRenderTarget->FillEllipse(ellipse, m_pSilverBrush);
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f, m_pStrokeStyle);
```



Il codice è stato omesso da questi esempi.

## <a name="drawing-more-complex-shapes"></a>Disegno di forme più complesse

Per disegnare forme più complesse, definire oggetti ID2D1Geometry e usarli con i [**metodi DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) e [**FillGeometry.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) Per altre informazioni, vedere [Cenni preliminari sulle geometrie.](direct2d-geometries-overview.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica delle geometrie](direct2d-geometries-overview.md)
</dt> <dt>

[Panoramica dei pennelli](direct2d-brushes-overview.md)
</dt> </dl>

 

 
