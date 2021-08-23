---
title: Come creare un pennello sfumatura radiale
description: Illustra come creare un pennello sfumatura radiale usando Direct2D.
ms.assetid: 663743c9-16e9-4e3a-90b2-883ef0b8d5cf
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 1932dc6506c625332d61f4e549ae2dd169060731bfbea344f64c3aa826540ae0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569267"
---
# <a name="how-to-create-a-radial-gradient-brush"></a>Come creare un pennello sfumatura radiale

Per creare un pennello sfumatura radiale, usa il [**metodo ID2DRenderTarget::CreateRadialGradientBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush)) e specifica le proprietà del pennello sfumatura radiale e la raccolta dei cursori sfumatura. Alcuni overload consentono di specificare le proprietà del pennello. Il codice seguente illustra come creare un pennello sfumato radiale per riempire un cerchio e un pennello nero a tinta unita per disegnare il contorno del cerchio.

Il codice produce l'output illustrato nella figura seguente.

![illustrazione di un cerchio riempito con un pennello sfumato radiale](images/brushes-ovw-radials.png)

1.  Dichiarare una variabile di tipo [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush).
    ```C++
        ID2D1RadialGradientBrush *m_pRadialGradientBrush;
    ```

    

2.  Creare una matrice di strutture [**\_ GRADIENT \_ STOP D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop) da inserire nella raccolta dei cursori sfumatura. La **struttura GRADIENT \_ \_ STOP D2D1** contiene la posizione e il colore di un cursore sfumatura. La posizione indica la posizione relativa del cursore sfumatura nel pennello. Il valore è compreso nell'intervallo \[ 0,0f, 1,0f, \] come illustrato nel codice seguente.

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

    

3.  Usare il metodo [**ID2D1RenderTarget::CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) per creare la raccolta [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) da una matrice dichiarata in precedenza di strutture [**GRADIENT \_ \_ STOP D2D1.**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop) Usa quindi [**CreateRadialGradientBrush per**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush)) creare un pennello sfumatura radiale.

    > [!Note]  
    > A partire da Windows 8, è possibile usare il metodo [**ID2D1DeviceContext::CreateGradientStopCollection**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-creategradientstopcollection) per creare una raccolta [**ID2D1GradientStopCollection1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1gradientstopcollection1) anziché il metodo [**ID2D1RenderTarget::CreateGradientStopCollection.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) Questa interfaccia aggiunge sfumature di colore elevato e l'interpolazione delle sfumature in colori rette o prmoltimentati. Per altre informazioni, vedere la pagina **ID2DDeviceContext::CreateGradientStopCollection.**

     

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

[Informazioni di riferimento su Direct2D](reference.md)
</dt> </dl>

 

 