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
# <a name="how-to-apply-effects-to-primitives"></a><span data-ttu-id="1596a-103">Come applicare effetti alle primitive</span><span class="sxs-lookup"><span data-stu-id="1596a-103">How to Apply Effects to Primitives</span></span>

<span data-ttu-id="1596a-104">In questo argomento viene illustrato come applicare una serie di effetti alle primitive [Direct2D](./direct2d-portal.md) e [DirectWrite](direct2d-and-directwrite.md) .</span><span class="sxs-lookup"><span data-stu-id="1596a-104">This topic shows how to apply a series of effect to [Direct2D](./direct2d-portal.md) and [DirectWrite](direct2d-and-directwrite.md) primitives.</span></span>

<span data-ttu-id="1596a-105">È possibile usare l' [API di effetti Direct2D](effects-overview.md) per applicare grafici effetti alle primitive di cui è stato eseguito il rendering da [Direct2D](./direct2d-portal.md) a un'immagine.</span><span class="sxs-lookup"><span data-stu-id="1596a-105">You can use the [Direct2D effects API](effects-overview.md) to apply effect graphs to primitives rendered by [Direct2D](./direct2d-portal.md) to an image.</span></span> <span data-ttu-id="1596a-106">Nell'esempio seguente sono presenti due rettangoli arrotondati e il testo "Direct2D".</span><span class="sxs-lookup"><span data-stu-id="1596a-106">The example here has two rounded rectangles and the text "Direct2D".</span></span> <span data-ttu-id="1596a-107">Utilizzare Direct2D per creare i rettangoli e [DirectWrite](direct2d-and-directwrite.md) per creare il testo.</span><span class="sxs-lookup"><span data-stu-id="1596a-107">Use Direct2D to draw the rectangles and [DirectWrite](direct2d-and-directwrite.md) to draw the text.</span></span>

![rettangoli con il testo "Direct2D" all'interno di.](images/direct2d-rounded.png)

<span data-ttu-id="1596a-109">Utilizzando [gli effetti Direct2D](effects-overview.md), è possibile rendere questa immagine simile all'immagine successiva.</span><span class="sxs-lookup"><span data-stu-id="1596a-109">Using [Direct2D effects](effects-overview.md), you can make this image look like the next image.</span></span> <span data-ttu-id="1596a-110">Applicare gli effetti [sfocatura gaussiana](gaussian-blur.md), [illuminazione speculare](specular-lighting.md), [composito](arithmetic-composite.md)e [composito](composite.md) alle primitive 2D per creare l'immagine in questo punto.</span><span class="sxs-lookup"><span data-stu-id="1596a-110">Apply the [Gaussian Blur](gaussian-blur.md), [Point Specular Lighting](specular-lighting.md), [Arithmetic Composite](arithmetic-composite.md), and [Composite](composite.md) effects to the 2D primitives to create the image here.</span></span>

![i rettangoli con il testo "Direct2D" all'interno di dopo diversi effetti vengono applicati.](images/direct2d-svg.png)

<span data-ttu-id="1596a-112">Dopo aver eseguito il rendering dei rettangoli e del testo in una superficie intermedia, è possibile usarlo come input per gli oggetti [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) nel grafico dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="1596a-112">After you render the rectangles and text to a intermediate surface, you can use this as input for [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) objects in the image graph.</span></span>

<span data-ttu-id="1596a-113">In questo esempio, impostare l'immagine originale come input per l' [effetto sfocatura gaussiana](gaussian-blur.md) e quindi impostare l'output della sfocatura come input per l'effetto di [illuminazione speculare del punto](specular-lighting.md).</span><span class="sxs-lookup"><span data-stu-id="1596a-113">In this example, set the original image as the input to the [Gaussian Blur effect](gaussian-blur.md) and then set the output of the blur as the input for the [Point Specular Lighting effect](specular-lighting.md).</span></span> <span data-ttu-id="1596a-114">Il risultato di questo effetto viene quindi composto con l'immagine originale due volte per ottenere l'immagine finale di cui viene eseguito il rendering nella finestra.</span><span class="sxs-lookup"><span data-stu-id="1596a-114">The result of this effect is then composited with the original image twice to get the final image that is rendered to the window.</span></span>

<span data-ttu-id="1596a-115">Di seguito è riportato un diagramma del grafico immagine.</span><span class="sxs-lookup"><span data-stu-id="1596a-115">Here is a diagram of the image graph.</span></span>

![diagramma grafico effetto.](images/effect-graph.png)

<span data-ttu-id="1596a-117">Questo grafico degli effetti è costituito da quattro oggetti [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) , ognuno dei quali rappresenta un effetto predefinito diverso.</span><span class="sxs-lookup"><span data-stu-id="1596a-117">This effect graph consists of four [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) objects, each representing a different built-in effect.</span></span> <span data-ttu-id="1596a-118">È possibile creare e connettere gli effetti personalizzati nello stesso modo, dopo averli registrati usando [**ID1D1Factory1:: RegisterEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring).</span><span class="sxs-lookup"><span data-stu-id="1596a-118">You can create and connect custom effects in the same way, after you register them using [**ID1D1Factory1::RegisterEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring).</span></span> <span data-ttu-id="1596a-119">Il codice qui crea gli effetti, imposta le proprietà e connette il grafico di effetto illustrato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="1596a-119">The code here creates the effects, sets the properties, and connects the effect graph shown earlier.</span></span>

1.  <span data-ttu-id="1596a-120">Creare l'effetto di [sfocatura gaussiana](gaussian-blur.md) usando il metodo [**ID2D1DeviceContext:: CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) e specificando il CLSID appropriato.</span><span class="sxs-lookup"><span data-stu-id="1596a-120">Create the [Gaussian blur](gaussian-blur.md) effect using the [**ID2D1DeviceContext::CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) method and specifying the proper CLSID.</span></span> <span data-ttu-id="1596a-121">I CLSID per gli effetti predefiniti sono definiti in d2d1effects. h.</span><span class="sxs-lookup"><span data-stu-id="1596a-121">The CLSIDs for the built-in effects are defined in d2d1effects.h.</span></span> <span data-ttu-id="1596a-122">Si imposta quindi la deviazione standard della sfocatura usando il metodo [**ID2D1Effect:: SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) .</span><span class="sxs-lookup"><span data-stu-id="1596a-122">You then set the standard deviation of the blur using the [**ID2D1Effect::SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) method.</span></span>

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

    

    <span data-ttu-id="1596a-123">L'effetto di [sfocatura gaussiana](gaussian-blur.md) offusca tutti i canali dell'immagine, incluso il canale alfa.</span><span class="sxs-lookup"><span data-stu-id="1596a-123">The [Gaussian blur](gaussian-blur.md) effect blurs all of the channels of the image, including the alpha channel.</span></span>

2.  <span data-ttu-id="1596a-124">Creare l'effetto di [illuminazione speculare](point-specular.md) e impostare le proprietà.</span><span class="sxs-lookup"><span data-stu-id="1596a-124">Create the [specular lighting](point-specular.md) effect and set the properties.</span></span> <span data-ttu-id="1596a-125">La posizione della luce è un vettore di 3 valori a virgola mobile, pertanto è necessario dichiararlo come variabile separata e passarlo al metodo [**SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) .</span><span class="sxs-lookup"><span data-stu-id="1596a-125">The position of the light is a vector of 3 floating point values, so you must declare it as a separate variable and pass it to the [**SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) method.</span></span>

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

    

    <span data-ttu-id="1596a-126">L'effetto di [illuminazione speculare](point-specular.md) usa il canale alfa dell'input per creare una mappa di altezza per l'illuminazione.</span><span class="sxs-lookup"><span data-stu-id="1596a-126">The [specular lighting](point-specular.md) effect uses the alpha channel of the input to create a height map for the lighting.</span></span>

3.  <span data-ttu-id="1596a-127">Esistono due diversi effetti compositi che è possibile utilizzare l'effetto [composito](composite.md) e la [composizione aritmetica](arithmetic-composite.md).</span><span class="sxs-lookup"><span data-stu-id="1596a-127">There are two different composite effects that you can use the [composite](composite.md) effect and the [arithmetic composite](arithmetic-composite.md).</span></span> <span data-ttu-id="1596a-128">Questo effetto grafico usa entrambi.</span><span class="sxs-lookup"><span data-stu-id="1596a-128">This effect graph uses both.</span></span>

    <span data-ttu-id="1596a-129">Creare l'effetto [composito](composite.md) e impostare la modalità sull' \_ \_ origine in modalità composita d2d1 \_ \_ in, che restituisce l'intersezione delle immagini di origine e di destinazione.</span><span class="sxs-lookup"><span data-stu-id="1596a-129">Create the [composite](composite.md) effect and set the mode to D2D1\_COMPOSITE\_MODE\_SOURCE\_IN, which outputs the intersection of the source and destination images.</span></span>

    <span data-ttu-id="1596a-130">L'effetto [composito aritmetico](arithmetic-composite.md) compone le due immagini di input in base a una formula definita dal World Wide Web Consortium (W3C) per lo standard svg (Scalable Vector Graphics).</span><span class="sxs-lookup"><span data-stu-id="1596a-130">The [arithmetic composite](arithmetic-composite.md) effect composes the two input images based on a formula defined by the World Wide Web Consortium (W3C) for the Scalable Vector Graphics (SVG) standard.</span></span> <span data-ttu-id="1596a-131">Creare una composizione aritmetica e impostare i coefficienti per la formula.</span><span class="sxs-lookup"><span data-stu-id="1596a-131">Create arithmetic composite and set the coefficients for the formula.</span></span>

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

    

    <span data-ttu-id="1596a-132">Di seguito sono riportati i coefficienti per l'effetto [composito aritmetico](arithmetic-composite.md) .</span><span class="sxs-lookup"><span data-stu-id="1596a-132">The coefficients for the [arithmetic composite](arithmetic-composite.md) effect are shown here.</span></span>

    ```C++
    D2D1_VECTOR_4F sc_arithmeticCoefficients   = D2D1::Vector4F(0.0f, 1.0f, 1.0f, 0.0f);
    ```

    

    <span data-ttu-id="1596a-133">In questo grafico, entrambi gli effetti compositi accettano l'output degli altri effetti e della superficie intermedia come input e li compositi.</span><span class="sxs-lookup"><span data-stu-id="1596a-133">In this effect graph, both of the composite effects take the output of the other effects and the intermediate surface as inputs and composites them.</span></span>

4.  <span data-ttu-id="1596a-134">Infine, è possibile connettere gli effetti per formare il grafo impostando gli input sulle immagini e le bitmap corrette.</span><span class="sxs-lookup"><span data-stu-id="1596a-134">Finally, you connect the effects to form the graph by setting the inputs to the proper images and bitmaps.</span></span>

    <span data-ttu-id="1596a-135">Il primo effetto, ovvero la [sfocatura gaussiana](gaussian-blur.md), riceve l'input dalla superficie intermedia in cui sono state sottoposte a rendering le primitive.</span><span class="sxs-lookup"><span data-stu-id="1596a-135">The first effect, [Gaussian blur](gaussian-blur.md), receives its input from the intermediate surface that you rendered the primitives to.</span></span> <span data-ttu-id="1596a-136">È possibile impostare l'input usando il metodo [**ID2D1Effect:: seinput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) e specificando l'indice di un oggetto [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) .</span><span class="sxs-lookup"><span data-stu-id="1596a-136">You set the input using the [**ID2D1Effect::SetInput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) method and specifying the index of an [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) object.</span></span> <span data-ttu-id="1596a-137">La sfocatura gaussiana e gli effetti di [illuminazione speculare](point-specular.md) hanno solo un input singolo.</span><span class="sxs-lookup"><span data-stu-id="1596a-137">The Gaussian blur and [specular lighting](point-specular.md) effects have only a single input.</span></span> <span data-ttu-id="1596a-138">L'effetto di illuminazione speculare usa il canale alfa sfocato della sfocatura gaussiana</span><span class="sxs-lookup"><span data-stu-id="1596a-138">The specular lighting effect uses the blurred alpha channel of the Gaussian blur</span></span>

    <span data-ttu-id="1596a-139">Gli [effetti compositi e](composite.md) [composti aritmetici](arithmetic-composite.md) hanno più input.</span><span class="sxs-lookup"><span data-stu-id="1596a-139">The [composite](composite.md) and [arithmetic composite](arithmetic-composite.md) effects have multiple inputs.</span></span> <span data-ttu-id="1596a-140">Per assicurarsi che le immagini siano riunite nell'ordine corretto, è necessario specificare l'indice corretto per ogni immagine di input.</span><span class="sxs-lookup"><span data-stu-id="1596a-140">To make sure the images are put together in the right order, you must specify the correct index for each input image.</span></span>

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

    

5.  <span data-ttu-id="1596a-141">Passare l'oggetto effetto [composito aritmetico](arithmetic-composite.md) al metodo [**ID2DDeviceContext::D rawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) ed elaborare e disegnare l'output del grafo.</span><span class="sxs-lookup"><span data-stu-id="1596a-141">Pass the [arithmetic composite](arithmetic-composite.md) effect object into the [**ID2DDeviceContext::DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) method and it processes and draws the output of the graph.</span></span>

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

    

 

 