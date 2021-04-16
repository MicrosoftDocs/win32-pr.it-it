---
title: Come creare e riempire una forma di base
description: In questo argomento viene descritto come creare una forma di base.
ms.assetid: 8a68fc3f-118c-447b-856c-05417ae4ef29
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 6b6b5a6fb08ac962475c2f0aa2812b4c3ae5da03
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104558238"
---
# <a name="how-to-draw-and-fill-a-basic-shape"></a>Come creare e riempire una forma di base

In questo argomento viene descritto come creare una forma di base. L'interfaccia [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) fornisce metodi per la struttura e il riempimento di ellissi, rettangoli e linee. Negli esempi seguenti viene illustrato come creare e creare un'ellisse.

In questo argomento sono incluse le sezioni seguenti:

-   [Disegnare il contorno di un'ellisse con un tratto a tinta unita](#draw-the-outline-of-an-ellipse-with-a-solid-stroke)
-   [Disegnare un'ellisse con un tratto tratteggiato](#draw-an-ellipse-with-a-dashed-stroke)
-   [Creare e riempire un'ellisse](#draw-and-fill-an-ellipse)
-   [Disegno di forme più complesse](#drawing-more-complex-shapes)
-   [Argomenti correlati](#related-topics)

## <a name="draw-the-outline-of-an-ellipse-with-a-solid-stroke"></a>Disegnare il contorno di un'ellisse con un tratto a tinta unita

Per disegnare la struttura di un'ellisse, è necessario definire un pennello, ad esempio [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) o [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), per disegnare il contorno e un' [**\_ ellisse d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) per descrivere la posizione e le dimensioni dell'ellisse, quindi passare questi oggetti al metodo [**ID2D1RenderTarget::D rawellipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) . L'esempio seguente crea un pennello tinta unita nero e lo archivia nel \_ membro della classe m spBlackBrush.


```C++
hr = m_pRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF::Black),
    &m_pBlackBrush
    );
```



L'esempio seguente definisce un' [**\_ ellisse d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) e la USA con il pennello definito nell'esempio precedente per disegnare il contorno di un'ellisse. Questo esempio produce l'output illustrato nella figura seguente.

![illustrazione di un'ellisse con un tratto a tinta unita](images/drawandfillellipseexample-1.png)


```C++
D2D1_ELLIPSE ellipse = D2D1::Ellipse(
    D2D1::Point2F(100.f, 100.f),
    75.f,
    50.f
    );

m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f);
```



## <a name="draw-an-ellipse-with-a-dashed-stroke"></a>Disegnare un'ellisse con un tratto tratteggiato

Nell'esempio precedente è stato usato un tratto normale. È possibile modificare l'aspetto di un tratto in diversi modi creando un [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle). **ID2D1StrokeStyle** consente di specificare la forma all'inizio e alla fine di un tratto, se dispone di uno schema di tratteggio e così via. Nell'esempio seguente viene creato un **ID2D1StrokeStyle** che descrive un tratto tratteggiato. Questo esempio usa un modello Dash predefinito, [**d2d1 Dash \_ \_ Style \_ Dash \_ \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_dash_style), ma è anche possibile specificarne uno personalizzato.


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



Nell'esempio seguente viene usato lo stile del tratto con il metodo [**DrawEllipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) . Questo esempio produce l'output illustrato nella figura seguente.

![illustrazione di un'ellisse con tratto tratteggiato](images/drawandfillellipseexample-2.png)


```C++
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f, m_pStrokeStyle);
```



## <a name="draw-and-fill-an-ellipse"></a>Creare e riempire un'ellisse

Per disegnare l'area interna di un'ellisse, usare il metodo [**FillEllipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) . Nell'esempio seguente viene usato il metodo [**DrawEllipse**]/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse (constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) per delineare l'ellisse, quindi viene usato il metodo **FillEllipse** per disegnare l'interno. Questo esempio produce l'output illustrato nella figura seguente.

![illustrazione di un'ellisse con un tratto tratteggiato e quindi riempito con un colore grigio a tinta unita](images/drawandfillellipseexample-3.png)


```C++
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f, m_pStrokeStyle);
m_pRenderTarget->FillEllipse(ellipse, m_pSilverBrush);
```



Nell'esempio successivo viene prima riempito l'ellisse, quindi ne viene disegnato il contorno. Questo esempio produce l'output illustrato nella figura seguente.

![illustrazione di un'ellisse riempita con un colore grigio a tinta unita e quindi delineata con un tratto tratteggiato](images/drawandfillellipseexample-4.png)


```C++
m_pRenderTarget->FillEllipse(ellipse, m_pSilverBrush);
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f, m_pStrokeStyle);
```



Il codice è stato omesso da questi esempi.

## <a name="drawing-more-complex-shapes"></a>Disegno di forme più complesse

Per creare forme più complesse, è necessario definire gli oggetti ID2D1Geometry e usarli con i metodi [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) e [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) . Per altre informazioni, vedere [Cenni preliminari sulle geometrie](direct2d-geometries-overview.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica delle geometrie](direct2d-geometries-overview.md)
</dt> <dt>

[Panoramica dei pennelli](direct2d-brushes-overview.md)
</dt> </dl>

 

 