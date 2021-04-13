---
title: Come applicare effetti alle primitive
description: In questo argomento viene illustrato come applicare una serie di effetti alle primitive Direct2D e DirectWrite.
ms.assetid: 9782C22E-5D4C-494D-A0B1-19474C2CA900
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aafb171c20c567d1fbd6385d23cc3b2925efc154
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399444"
---
# <a name="how-to-apply-effects-to-primitives"></a>Come applicare effetti alle primitive

In questo argomento viene illustrato come applicare una serie di effetti alle primitive [Direct2D](./direct2d-portal.md) e [DirectWrite](direct2d-and-directwrite.md) .

È possibile usare l' [API di effetti Direct2D](effects-overview.md) per applicare grafici effetti alle primitive di cui è stato eseguito il rendering da [Direct2D](./direct2d-portal.md) a un'immagine. Nell'esempio seguente sono presenti due rettangoli arrotondati e il testo "Direct2D". Utilizzare Direct2D per creare i rettangoli e [DirectWrite](direct2d-and-directwrite.md) per creare il testo.

![rettangoli con il testo "Direct2D" all'interno di.](images/direct2d-rounded.png)

Utilizzando [gli effetti Direct2D](effects-overview.md), è possibile rendere questa immagine simile all'immagine successiva. Applicare gli effetti [sfocatura gaussiana](gaussian-blur.md), [illuminazione speculare](specular-lighting.md), [composito](arithmetic-composite.md)e [composito](composite.md) alle primitive 2D per creare l'immagine in questo punto.

![i rettangoli con il testo "Direct2D" all'interno di dopo diversi effetti vengono applicati.](images/direct2d-svg.png)

Dopo aver eseguito il rendering dei rettangoli e del testo in una superficie intermedia, è possibile usarlo come input per gli oggetti [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) nel grafico dell'immagine.

In questo esempio, impostare l'immagine originale come input per l' [effetto sfocatura gaussiana](gaussian-blur.md) e quindi impostare l'output della sfocatura come input per l'effetto di [illuminazione speculare del punto](specular-lighting.md). Il risultato di questo effetto viene quindi composto con l'immagine originale due volte per ottenere l'immagine finale di cui viene eseguito il rendering nella finestra.

Di seguito è riportato un diagramma del grafico immagine.

![diagramma grafico effetto.](images/effect-graph.png)

Questo grafico degli effetti è costituito da quattro oggetti [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) , ognuno dei quali rappresenta un effetto predefinito diverso. È possibile creare e connettere gli effetti personalizzati nello stesso modo, dopo averli registrati usando [**ID1D1Factory1:: RegisterEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring). Il codice qui crea gli effetti, imposta le proprietà e connette il grafico di effetto illustrato in precedenza.

1.  Creare l'effetto di [sfocatura gaussiana](gaussian-blur.md) usando il metodo [**ID2D1DeviceContext:: CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) e specificando il CLSID appropriato. I CLSID per gli effetti predefiniti sono definiti in d2d1effects. h. Si imposta quindi la deviazione standard della sfocatura usando il metodo [**ID2D1Effect:: SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) .

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

    

    L'effetto di [sfocatura gaussiana](gaussian-blur.md) offusca tutti i canali dell'immagine, incluso il canale alfa.

2.  Creare l'effetto di [illuminazione speculare](point-specular.md) e impostare le proprietà. La posizione della luce è un vettore di 3 valori a virgola mobile, pertanto è necessario dichiararlo come variabile separata e passarlo al metodo [**SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) .

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

    

    L'effetto di [illuminazione speculare](point-specular.md) usa il canale alfa dell'input per creare una mappa di altezza per l'illuminazione.

3.  Esistono due diversi effetti compositi che è possibile utilizzare l'effetto [composito](composite.md) e la [composizione aritmetica](arithmetic-composite.md). Questo effetto grafico usa entrambi.

    Creare l'effetto [composito](composite.md) e impostare la modalità sull' \_ \_ origine in modalità composita d2d1 \_ \_ in, che restituisce l'intersezione delle immagini di origine e di destinazione.

    L'effetto [composito aritmetico](arithmetic-composite.md) compone le due immagini di input in base a una formula definita dal World Wide Web Consortium (W3C) per lo standard svg (Scalable Vector Graphics). Creare una composizione aritmetica e impostare i coefficienti per la formula.

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

    

    Di seguito sono riportati i coefficienti per l'effetto [composito aritmetico](arithmetic-composite.md) .

    ```C++
    D2D1_VECTOR_4F sc_arithmeticCoefficients   = D2D1::Vector4F(0.0f, 1.0f, 1.0f, 0.0f);
    ```

    

    In questo grafico, entrambi gli effetti compositi accettano l'output degli altri effetti e della superficie intermedia come input e li compositi.

4.  Infine, è possibile connettere gli effetti per formare il grafo impostando gli input sulle immagini e le bitmap corrette.

    Il primo effetto, ovvero la [sfocatura gaussiana](gaussian-blur.md), riceve l'input dalla superficie intermedia in cui sono state sottoposte a rendering le primitive. È possibile impostare l'input usando il metodo [**ID2D1Effect:: seinput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) e specificando l'indice di un oggetto [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) . La sfocatura gaussiana e gli effetti di [illuminazione speculare](point-specular.md) hanno solo un input singolo. L'effetto di illuminazione speculare usa il canale alfa sfocato della sfocatura gaussiana

    Gli [effetti compositi e](composite.md) [composti aritmetici](arithmetic-composite.md) hanno più input. Per assicurarsi che le immagini siano riunite nell'ordine corretto, è necessario specificare l'indice corretto per ogni immagine di input.

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

    

5.  Passare l'oggetto effetto [composito aritmetico](arithmetic-composite.md) al metodo [**ID2DDeviceContext::D rawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) ed elaborare e disegnare l'output del grafo.

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

    

 

 