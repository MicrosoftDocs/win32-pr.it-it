---
title: Come creare un pennello sfumatura radiale
description: Viene illustrato come creare un pennello a sfumatura radiale tramite Direct2D.
ms.assetid: 663743c9-16e9-4e3a-90b2-883ef0b8d5cf
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: fe3509a80f80132f4a5e5d65f62476be1cac61d1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104223939"
---
# <a name="how-to-create-a-radial-gradient-brush"></a>Come creare un pennello sfumatura radiale

Per creare un pennello a sfumatura radiale, usare il metodo [**ID2DRenderTarget:: CreateRadialGradientBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush)) e specificare le proprietà del pennello sfumatura radiale e la raccolta di arresti sfumatura. Alcuni overload consentono di specificare le proprietà del pennello. Il codice seguente illustra come creare un pennello a sfumatura radiale per riempire un cerchio e un pennello nero a tinta unita per disegnare il contorno del cerchio.

Il codice produce l'output illustrato nella figura seguente.

![illustrazione di un cerchio riempito con un pennello a sfumatura radiale](images/brushes-ovw-radials.png)

1.  Dichiarare una variabile di tipo [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush).
    ```C++
        ID2D1RadialGradientBrush *m_pRadialGradientBrush;
    ```

    

2.  Creare una matrice di strutture di [**\_ \_ arresto sfumatura d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop) da inserire nella raccolta di arresti sfumatura. La struttura di **\_ \_ arresto sfumatura d2d1** contiene la posizione e il colore di un cursore sfumatura. La posizione indica la posizione relativa del cursore sfumatura nel pennello. Il valore è compreso nell'intervallo \[ 0,0 f, 1.0 f \] , come illustrato nel codice seguente.

    ```C++
    // Create an array of gradient stops to put in the gradient stop
    // collection that will be used in the gradient brush.
    ID2D1GradientStopCollection *pGradientStops = NULL;

    D2D1_GRADIENT_STOP gradientStops[2];
    gradientStops[0].color = D2D1::ColorF(D2D1::ColorF::Yellow, 1);
    gradientStops[0].position = 0.0f;
    gradientStops[1].color = D2D1::ColorF(D2D1::ColorF::ForestGreen, 1);
    gradientStops[1].position = 1.0f;
    // Create the ID2D1GradientStopCollection from a previously
    // declared array of D2D1_GRADIENT_STOP structs.
    hr = m_pRenderTarget->CreateGradientStopCollection(
        gradientStops,
        2,
        D2D1_GAMMA_2_2,
        D2D1_EXTEND_MODE_CLAMP,
        &pGradientStops
        );
    ```

    

3.  Usare il metodo [**ID2D1RenderTarget:: CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) per creare la raccolta [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) da una matrice dichiarata in precedenza di strutture di [**\_ \_ arresto sfumatura d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop) . Quindi, usare [**CreateRadialGradientBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush)) per creare un pennello a sfumatura radiale.

    > [!Note]  
    > A partire da Windows 8, è possibile usare il metodo [**ID2D1DeviceContext:: CreateGradientStopCollection**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-creategradientstopcollection) per creare una raccolta [**ID2D1GradientStopCollection1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1gradientstopcollection1) anziché il metodo [**ID2D1RenderTarget:: CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) . Questa interfaccia aggiunge sfumature di colore elevato e l'interpolazione delle sfumature nei colori unidirezionali o prmultiplied. Per ulteriori informazioni, vedere la pagina **ID2DDeviceContext:: CreateGradientStopCollection** .

     

    ```C++
    // The center of the gradient is in the center of the box.
    // The gradient origin offset was set to zero(0, 0) or center in this case.
    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateRadialGradientBrush(
            D2D1::RadialGradientBrushProperties(
                D2D1::Point2F(75, 75),
                D2D1::Point2F(0, 0),
                75,
                75),
            pGradientStops,
            &m_pRadialGradientBrush
            );
    }
    ```

    

    ```C++
    m_pRenderTarget->FillEllipse(ellipse, m_pRadialGradientBrush);
    m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 1, NULL);
    ```

    

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento Direct2D](reference.md)
</dt> </dl>

 

 