---
title: Come applicare effetti alle primitive
description: Questo argomento illustra come applicare una serie di effetti a Direct2D e DirectWrite primitive.
ms.assetid: 9782C22E-5D4C-494D-A0B1-19474C2CA900
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c17cbf1efe17d1c23c90382f3b95fb41e33946a93935b0be02fc5b41f314a8c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569596"
---
# <a name="how-to-apply-effects-to-primitives"></a>Come applicare effetti alle primitive

Questo argomento illustra come applicare una serie di effetti a [Direct2D](./direct2d-portal.md) [e DirectWrite](direct2d-and-directwrite.md) primitive.

È possibile usare [l'API effetti Direct2D](effects-overview.md) per applicare i grafici degli effetti alle primitive sottoposte a rendering [da Direct2D](./direct2d-portal.md) a un'immagine. L'esempio include due rettangoli arrotondati e il testo "Direct2D". Usare Direct2D per disegnare i rettangoli [e DirectWrite](direct2d-and-directwrite.md) per disegnare il testo.

![rettangoli con il testo "direct2d" all'interno di .](images/direct2d-rounded.png)

Usando [gli effetti Direct2D,](effects-overview.md)è possibile fare in modo che questa immagine sia simile all'immagine successiva. Applicare gli [sfocatura gaussiana,](gaussian-blur.md) [Point Specular Lighting,](specular-lighting.md) [Arithmetic Composite](arithmetic-composite.md)e [Composite](composite.md) alle primitive 2D per creare l'immagine qui.

![rettangoli con il testo "direct2d" all'interno di dopo l'applicazione di diversi effetti.](images/direct2d-svg.png)

Dopo aver eseguito il rendering dei rettangoli e del testo su una superficie intermedia, è possibile usarlo come input per gli [**oggetti ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) nel grafico dell'immagine.

In questo esempio, impostare l'immagine originale come input sull'effetto [sfocatura gaussiana](gaussian-blur.md) e quindi impostare l'output della sfocatura come input per l'effetto [Point Specular Lighting](specular-lighting.md). Il risultato di questo effetto viene quindi composito con l'immagine originale due volte per ottenere l'immagine finale di cui viene eseguito il rendering nella finestra.

Ecco un diagramma del grafo dell'immagine.

![diagramma grafico degli effetti.](images/effect-graph.png)

Questo grafico degli effetti è costituito da [**quattro oggetti ID2D1Effect,**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) ognuno dei quali rappresenta un effetto incorporato diverso. È possibile creare e connettere gli effetti personalizzati nello stesso modo, dopo averli registrati usando [**ID1D1Factory1::RegisterEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring). Il codice crea gli effetti, imposta le proprietà e connette il grafico degli effetti illustrato in precedenza.

1.  Creare [l'effetto sfocatura gaussiana](gaussian-blur.md) usando il [**metodo ID2D1DeviceContext::CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) e specificando il CLSID appropriato. I CLSID per gli effetti predefiniti sono definiti in d2d1effects.h. È quindi possibile impostare la deviazione standard della sfocatura usando il [**metodo ID2D1Effect::SetValue.**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32))

    ```C++
    // Create the Gaussian Blur Effect
    DX::ThrowIfFailed(
        m_d2dContext->CreateEffect(CLSID_D2D1GaussianBlur, &gaussianBlurEffect)
        );

    // Set the blur amount
    DX::ThrowIfFailed(
        gaussianBlurEffect->SetValue(D2D1_GAUSSIANBLUR_PROP_STANDARD_DEVIATION, sc_gaussianBlurStDev)
        );
    ```

    

    [L'effetto sfocatura gaussiana](gaussian-blur.md) sfoca tutti i canali dell'immagine, incluso il canale alfa.

2.  Creare [l'effetto di illuminazione speculare](point-specular.md) e impostare le proprietà. La posizione della luce è un vettore di 3 valori a virgola mobile, quindi è necessario dichiararla come variabile separata e passarla al [**metodo SetValue.**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32))

    ```C++
    // Create the Specular Lighting Effect
    DX::ThrowIfFailed(
        m_d2dContext->CreateEffect(CLSID_D2D1PointSpecular, &specularLightingEffect)
        );

    DX::ThrowIfFailed(
        specularLightingEffect->SetValue(D2D1_POINTSPECULAR_PROP_LIGHT_POSITION, sc_specularLightPosition)
        );

    DX::ThrowIfFailed(
        specularLightingEffect->SetValue(D2D1_POINTSPECULAR_PROP_SPECULAR_EXPONENT, sc_specularExponent)
        );

    DX::ThrowIfFailed(
        specularLightingEffect->SetValue(D2D1_POINTSPECULAR_PROP_SURFACE_SCALE, sc_specularSurfaceScale)
        );

    DX::ThrowIfFailed(
        specularLightingEffect->SetValue(D2D1_POINTSPECULAR_PROP_SPECULAR_CONSTANT, sc_specularConstant)
        );
    ```

    

    [L'effetto di illuminazione speculare](point-specular.md) usa il canale alfa dell'input per creare una mappa dell'altezza per l'illuminazione.

3.  Esistono due diversi effetti compositi che è possibile usare l'effetto [composito](composite.md) e il composito [aritmetico](arithmetic-composite.md). Questo grafico degli effetti usa entrambi.

    Creare [l'effetto composito](composite.md) e impostare la modalità su D2D1 COMPOSITE MODE SOURCE IN, che restituisce l'intersezione delle immagini \_ di origine e di \_ \_ \_ destinazione.

    L'effetto composito [aritmetico](arithmetic-composite.md) compone le due immagini di input in base a una formula definita dal World Wide Web Consortium (W3C) per lo standard Scalable Vector Graphics (SVG). Creare un composto aritmetico e impostare i coefficienti per la formula.

    ```C++
    // Create the Composite Effects
    DX::ThrowIfFailed(
        m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect)
        );

    DX::ThrowIfFailed(
        compositeEffect->SetValue(D2D1_COMPOSITE_PROP_MODE, D2D1_COMPOSITE_MODE_SOURCE_IN)
        );

    DX::ThrowIfFailed(
        m_d2dContext->CreateEffect(CLSID_D2D1ArithmeticComposite, &m_arithmeticCompositeEffect)
        );

    DX::ThrowIfFailed(
        m_arithmeticCompositeEffect->SetValue(D2D1_ARITHMETICCOMPOSITE_PROP_COEFFICIENTS, sc_arithmeticCoefficients)
        );
    ```

    

    I coefficienti per [l'effetto composito aritmetico](arithmetic-composite.md) sono mostrati qui.

    ```C++
    D2D1_VECTOR_4F sc_arithmeticCoefficients   = D2D1::Vector4F(0.0f, 1.0f, 1.0f, 0.0f);
    ```

    

    In questo grafico degli effetti, entrambi gli effetti compositi accettano l'output degli altri effetti e la superficie intermedia come input e li compositi.

4.  Infine, si connettono gli effetti per formare il grafico impostando gli input per le immagini e le bitmap appropriate.

    Il primo effetto, [la sfocatura gaussiana,](gaussian-blur.md)riceve l'input dalla superficie intermedia su cui è stato eseguito il rendering delle primitive. L'input viene impostato usando il [**metodo ID2D1Effect::SetInput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) e specificando l'indice di un [**oggetto ID2D1Image.**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) Gli effetti di sfocatura gaussiana [e illuminazione speculare](point-specular.md) hanno un solo input. L'effetto di illuminazione speculare usa il canale alfa sfocato della sfocatura gaussiana

    Gli [effetti compositi](composite.md) [e compositi aritmetici](arithmetic-composite.md) hanno più input. Per assicurarsi che le immagini siano riunite nell'ordine corretto, è necessario specificare l'indice corretto per ogni immagine di input.

    ```C++
    // Connect the graph.
    // Apply a blur effect to the original image.
    gaussianBlurEffect->SetInput(0, m_inputImage.Get());

    // Apply a specular lighting effect to the result.
    specularLightingEffect->SetInputEffect(0, gaussianBlurEffect.Get());

    // Compose the original bitmap under the output from lighting and blur.
    compositeEffect->SetInput(0, m_inputImage.Get());
    compositeEffect->SetInputEffect(1, specularLightingEffect.Get());

    // Compose the original bitmap under the output from lighting and blur.
    m_arithmeticCompositeEffect->SetInput(0, m_inputImage.Get());
    m_arithmeticCompositeEffect->SetInputEffect(1, compositeEffect.Get());
    ```

    

5.  Passare [l'oggetto effetto](arithmetic-composite.md) composito aritmetico nel metodo [**ID2DDeviceContext::D rawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) e elabora e disegna l'output del grafico.

    ```C++
        // Draw the output of the effects graph.
        m_d2dContext->DrawImage(
            m_arithmeticCompositeEffect.Get(),
            D2D1::Point2F(
                (size.width - sc_inputBitmapSize.width) / 2,
                (size.height - sc_inputBitmapSize.height) / 2 + sc_offset
                )
            );
    ```

    

 

 