---
title: Come creare un pennello a sfumatura lineare
description: Illustra come creare un pennello sfumato lineare usando Direct2D.
ms.assetid: 3cf5acc6-2f17-49d4-aca5-a84a846d1749
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 0c9223eb561ecc391014bc4a89c86a634181bec6d1e3917866aeef2723f1510a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119259536"
---
# <a name="how-to-create-a-linear-gradient-brush"></a>Come creare un pennello a sfumatura lineare

Per creare un pennello a sfumatura lineare, usare il [**metodo CreateLinearGradientBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) e specificare le proprietà del pennello sfumatura lineare e la raccolta delle interruzioni sfumature. Alcuni overload consentono di specificare le proprietà del pennello. Il codice seguente illustra come creare un pennello sfumato lineare per riempire un quadrato e un pennello nero a tinta unita per disegnare il contorno del quadrato.

Il codice produce l'output illustrato nella figura seguente.

![Illustrazione di un quadrato riempito con un pennello sfumato lineare](images/brushes-ovw-lineargradient.png)

1.  Dichiarare una variabile di tipo [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).
    ```C++
        ID2D1LinearGradientBrush *m_pLinearGradientBrush;
    ```

    

2.  Usare il [**metodo ID2D1RenderTarget::CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_id2d1gradientstopcollection)) per creare la raccolta [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) con una matrice dichiarata di strutture [**D2D1 \_ GRADIENT \_ STOP,**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop) come illustrato nel codice seguente.
    > [!Note]  
    > A partire da Windows 8, è possibile usare il [**metodo ID2D1DeviceContext::CreateGradientStopCollection**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-creategradientstopcollection) per creare una raccolta [**ID2D1GradientStopCollection1.**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1gradientstopcollection1) Questa interfaccia aggiunge sfumature di colore elevato e l'interpolazione delle sfumature in colori rette o prmultipli. Per altre informazioni, vedere la **pagina ID2DDeviceContext::CreateGradientStopCollection.**

     

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

    

3.  Usare [**ID2D1RenderTarget::CreateLinearGradientBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) per creare un pennello sfumato lineare, riempire il quadrato con il pennello e disegnare il quadrato con il pennello di colore nero.
    ```C++
    // The line that determines the direction of the gradient starts at
    // the upper-left corner of the square and ends at the lower-right corner.

    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateLinearGradientBrush(
            D2D1::LinearGradientBrushProperties(
                D2D1::Point2F(0, 0),
                D2D1::Point2F(150, 150)),
            pGradientStops,
            &m_pLinearGradientBrush
            );
    }
    ```

    

    ```C++
    m_pRenderTarget->FillRectangle(&rcBrushRect, m_pLinearGradientBrush);
    m_pRenderTarget->DrawRectangle(&rcBrushRect, m_pBlackBrush, 1, NULL);
    ```

    

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su Direct2D](reference.md)
</dt> </dl>

 

 
