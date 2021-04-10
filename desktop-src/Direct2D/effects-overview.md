---
title: Effetti (Direct2D)
description: Panoramica degli effetti Direct2D.
ms.assetid: 1446BDA9-AD4C-472C-8F1D-82ABC1880E13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dd29a4b2968e91bd0d516a74ec01538f69821bb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047111"
---
# <a name="effects"></a><span data-ttu-id="f3a32-103">Effetti</span><span class="sxs-lookup"><span data-stu-id="f3a32-103">Effects</span></span>

## <a name="what-are-direct2d-effects"></a><span data-ttu-id="f3a32-104">Che cosa sono gli effetti Direct2D?</span><span class="sxs-lookup"><span data-stu-id="f3a32-104">What are Direct2D effects?</span></span>

<span data-ttu-id="f3a32-105">È possibile utilizzare Direct2D per applicare uno o più effetti di alta qualità a un'immagine o a un set di immagini.</span><span class="sxs-lookup"><span data-stu-id="f3a32-105">You can use Direct2D to apply one or more high quality effects to an image or a set of images.</span></span> <span data-ttu-id="f3a32-106">Le API degli effetti sono basate su [Direct3D 11](/windows/desktop/direct3d11/direct3d-11-features) e sfruttano le funzionalità GPU per l'elaborazione delle immagini.</span><span class="sxs-lookup"><span data-stu-id="f3a32-106">The effects APIs are built on [Direct3D 11](/windows/desktop/direct3d11/direct3d-11-features) and take advantage of GPU features for image processing.</span></span> <span data-ttu-id="f3a32-107">È possibile concatenare gli effetti in un grafico effetto e comporre o fondere l'output degli effetti.</span><span class="sxs-lookup"><span data-stu-id="f3a32-107">You can chain effects in an effect graph and compose or blend the output of effects.</span></span>

<span data-ttu-id="f3a32-108">Un effetto Direct2D esegue un'attività di creazione di immagini, ad esempio la modifica della luminosità, la desaturazione di un'immagine o la creazione di un'ombreggiatura.</span><span class="sxs-lookup"><span data-stu-id="f3a32-108">A Direct2D effect performs an imaging task, like changing brightness, de-saturating an image, or creating a drop shadow.</span></span> <span data-ttu-id="f3a32-109">Gli effetti possono accettare zero o più immagini di input, esporre più proprietà che controllano l'operazione e generare un'unica immagine di output.</span><span class="sxs-lookup"><span data-stu-id="f3a32-109">Effects can accept zero or more input images, expose multiple properties that control their operation, and generate a single output image.</span></span>

<span data-ttu-id="f3a32-110">Ogni effetto crea un grafo di trasformazione interno costituito da trasformazioni singole.</span><span class="sxs-lookup"><span data-stu-id="f3a32-110">Each effect creates an internal transform graph made up of individual transforms.</span></span> <span data-ttu-id="f3a32-111">Ogni trasformazione rappresenta una singola operazione di immagine.</span><span class="sxs-lookup"><span data-stu-id="f3a32-111">Each transform represents a single image operation.</span></span> <span data-ttu-id="f3a32-112">Lo scopo principale di una trasformazione è quello di ospitare gli shader eseguiti per ogni pixel di output.</span><span class="sxs-lookup"><span data-stu-id="f3a32-112">The main purpose of a transform is to house the shaders that are executed for each output pixel.</span></span> <span data-ttu-id="f3a32-113">Questi shader possono includere pixel shader, vertex shader, la fase Blend di una GPU e compute shader.</span><span class="sxs-lookup"><span data-stu-id="f3a32-113">These shaders can include pixel shaders, vertex shaders, the blend stage of a GPU, and compute shaders.</span></span>

<span data-ttu-id="f3a32-114">Gli effetti [](./direct2d-portal.md) [predefiniti](built-in-effects.md) di Direct2D e gli effetti personalizzati che è possibile apportare usando l' [API degli effetti personalizzati](custom-effects.md) funzionano in questo modo.</span><span class="sxs-lookup"><span data-stu-id="f3a32-114">Both the [Direct2D](./direct2d-portal.md) [built-in effects](built-in-effects.md) and custom effects you can make using the [custom effects API](custom-effects.md) work this way.</span></span>

<span data-ttu-id="f3a32-115">Sono disponibili diversi [effetti predefiniti](built-in-effects.md) da categorie come quelle riportate di seguito.</span><span class="sxs-lookup"><span data-stu-id="f3a32-115">There are a range of [built-in effects](built-in-effects.md) from categories like the ones here.</span></span> <span data-ttu-id="f3a32-116">Per un elenco completo, vedere la sezione [effetti predefiniti](built-in-effects.md) .</span><span class="sxs-lookup"><span data-stu-id="f3a32-116">See the [Built-in Effects](built-in-effects.md) section for a full list.</span></span>

-   [<span data-ttu-id="f3a32-117">Filtro</span><span class="sxs-lookup"><span data-stu-id="f3a32-117">Filtering</span></span>](built-in-effects.md)
-   [<span data-ttu-id="f3a32-118">Composizione e fusione</span><span class="sxs-lookup"><span data-stu-id="f3a32-118">Composition and Blending</span></span>](built-in-effects.md)
-   [<span data-ttu-id="f3a32-119">Trasparenza</span><span class="sxs-lookup"><span data-stu-id="f3a32-119">Transparency</span></span>](built-in-effects.md)
-   [<span data-ttu-id="f3a32-120">Colore</span><span class="sxs-lookup"><span data-stu-id="f3a32-120">Color</span></span>](built-in-effects.md)
-   [<span data-ttu-id="f3a32-121">Illuminazione e stilizzazione</span><span class="sxs-lookup"><span data-stu-id="f3a32-121">Lighting and Stylizing</span></span>](built-in-effects.md)
-   [<span data-ttu-id="f3a32-122">Trasformazione e scalabilità</span><span class="sxs-lookup"><span data-stu-id="f3a32-122">Transforming and Scaling</span></span>](built-in-effects.md)
-   [<span data-ttu-id="f3a32-123">recenti</span><span class="sxs-lookup"><span data-stu-id="f3a32-123">Sources</span></span>](built-in-effects.md)

<span data-ttu-id="f3a32-124">È possibile applicare effetti a qualsiasi bitmap, incluse le immagini caricate da [Windows Imaging Component (WIC)](/windows/desktop/wic/-wic-api), primitive disegnate da [Direct2D](./direct2d-portal.md), testo da [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal)o scene sottoposte a rendering da [Direct3D](/windows/desktop/direct3d10/d3d10-graphics).</span><span class="sxs-lookup"><span data-stu-id="f3a32-124">You can apply effects to any bitmap, including: images loaded by the [Windows Imaging Component (WIC)](/windows/desktop/wic/-wic-api), primitives drawn by [Direct2D](./direct2d-portal.md), text from [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal), or scenes rendered by [Direct3D](/windows/desktop/direct3d10/d3d10-graphics).</span></span>

<span data-ttu-id="f3a32-125">Con gli effetti Direct2D è possibile scrivere gli effetti che è possibile usare per le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="f3a32-125">With Direct2D effects you can write your own effects that you can use for your applications.</span></span> <span data-ttu-id="f3a32-126">Un Framework di effetto personalizzato consente di usare le funzionalità GPU come pixel shader, vertex shader e l'unità di fusione.</span><span class="sxs-lookup"><span data-stu-id="f3a32-126">A custom effect framework allows you to use GPU features such as pixel shaders, vertex shaders, and the blending unit.</span></span> <span data-ttu-id="f3a32-127">È anche possibile includere altri effetti predefiniti o personalizzati nell'effetto personalizzato.</span><span class="sxs-lookup"><span data-stu-id="f3a32-127">You can also include other built-in or custom effects in your custom effect.</span></span> <span data-ttu-id="f3a32-128">Il Framework per la creazione di effetti personalizzati è identico a quello usato per creare gli effetti predefiniti di [Direct2D](./direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="f3a32-128">The framework for building custom effects is the same one that was used to create the built-in effects of [Direct2D](./direct2d-portal.md).</span></span> <span data-ttu-id="f3a32-129">L' [API autore dell'effetto Direct2D](custom-effects.md) fornisce un set di interfacce per la creazione e la registrazione di effetti.</span><span class="sxs-lookup"><span data-stu-id="f3a32-129">The [Direct2D effect author API](custom-effects.md) provides a set of interfaces to create and register effects.</span></span>

### <a name="more-effects-topics"></a><span data-ttu-id="f3a32-130">Argomenti per altri effetti</span><span class="sxs-lookup"><span data-stu-id="f3a32-130">More effects topics</span></span>

<span data-ttu-id="f3a32-131">Nella parte restante di questo argomento vengono illustrate le nozioni di base degli effetti Direct2D, ad esempio l'applicazione di un effetto a un'immagine.</span><span class="sxs-lookup"><span data-stu-id="f3a32-131">The rest of this topic explains the basics of Direct2D effects, like applying an effect to an image.</span></span> <span data-ttu-id="f3a32-132">La tabella contiene collegamenti ad argomenti aggiuntivi sugli effetti.</span><span class="sxs-lookup"><span data-stu-id="f3a32-132">The table here has links to additional topics about effects.</span></span>

| <span data-ttu-id="f3a32-133">Argomento</span><span class="sxs-lookup"><span data-stu-id="f3a32-133">Topic</span></span>                                                                                                                    | <span data-ttu-id="f3a32-134">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f3a32-134">Description</span></span>                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f3a32-135">Collegamento Effect shader</span><span class="sxs-lookup"><span data-stu-id="f3a32-135">Effect Shader Linking</span></span>](effect-shader-linking.md)<br/>                                                            | <span data-ttu-id="f3a32-136">Direct2D usa un'ottimizzazione denominata Effect shader linking che combina il rendering del grafico a più effetti passa in un singolo passaggio.</span><span class="sxs-lookup"><span data-stu-id="f3a32-136">Direct2D uses an optimization called effect shader linking which combines multiple effect graph rendering passes into a single pass.</span></span><br/>                                               |
| [<span data-ttu-id="f3a32-137">Effetti personalizzati</span><span class="sxs-lookup"><span data-stu-id="f3a32-137">Custom effects</span></span>](custom-effects.md)<br/>                                                                          | <span data-ttu-id="f3a32-138">Viene illustrato come scrivere effetti personalizzati usando HLSL standard.</span><span class="sxs-lookup"><span data-stu-id="f3a32-138">Shows you how to write your own custom effects using standard HLSL.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="f3a32-139">Come caricare un'immagine in effetti Direct2D usando il Filepicker</span><span class="sxs-lookup"><span data-stu-id="f3a32-139">How to load an image into Direct2D Effects using the FilePicker</span></span>](load-a-id2d1image-using-the-filepicker.md)<br/> | <span data-ttu-id="f3a32-140">Mostra come usare [**Windows:: Storage::P ickers:: FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) per caricare un'immagine in effetti Direct2D.</span><span class="sxs-lookup"><span data-stu-id="f3a32-140">Shows how to use the [**Windows::Storage::Pickers::FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) to load an image into Direct2D effects.</span></span><br/>                                      |
| [<span data-ttu-id="f3a32-141">Come salvare il contenuto Direct2D in un file di immagine</span><span class="sxs-lookup"><span data-stu-id="f3a32-141">How to save Direct2D content to an image file</span></span>](save-direct2d-content-to-an-image-file.md)<br/>                   | <span data-ttu-id="f3a32-142">Questo argomento illustra come usare [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) per salvare il contenuto sotto forma di [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) in un file di immagine codificato, ad esempio JPEG.</span><span class="sxs-lookup"><span data-stu-id="f3a32-142">This topic shows how to use [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) to save content in the form of an [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) to an encoded image file such as JPEG.</span></span><br/> |
| [<span data-ttu-id="f3a32-143">Come applicare effetti alle primitive</span><span class="sxs-lookup"><span data-stu-id="f3a32-143">How to Apply Effects to Primitives</span></span>](how-to-apply-effects-to-primitives.md)<br/>                                  | <span data-ttu-id="f3a32-144">In questo argomento viene illustrato come applicare una serie di effetti alle primitive [Direct2D](./direct2d-portal.md) e [DirectWrite](direct2d-and-directwrite.md) .</span><span class="sxs-lookup"><span data-stu-id="f3a32-144">This topic shows how to apply a series of effect to [Direct2D](./direct2d-portal.md) and [DirectWrite](direct2d-and-directwrite.md) primitives.</span></span><br/>                           |
| [<span data-ttu-id="f3a32-145">Controllo della precisione e ritaglio numerico nei grafici effettivi</span><span class="sxs-lookup"><span data-stu-id="f3a32-145">Controlling Precision and Numerical Clipping in Effect Graphs</span></span>](precision-and-clipping-in-effect-graphs.md)<br/>  | <span data-ttu-id="f3a32-146">Le applicazioni che eseguono il rendering degli effetti utilizzando Direct2D devono prestare attenzione a raggiungere il livello di qualità e prevedibilità desiderato rispetto alla precisione numerica.</span><span class="sxs-lookup"><span data-stu-id="f3a32-146">Applications that render effects using Direct2D must take care to achieve the desired level of quality and predictability with respect to numerical precision.</span></span> <br/>                    |

## <a name="applying-an-effect-to-an-image"></a><span data-ttu-id="f3a32-147">Applicazione di un effetto a un'immagine</span><span class="sxs-lookup"><span data-stu-id="f3a32-147">Applying an effect to an image</span></span>

<span data-ttu-id="f3a32-148">È possibile usare l'API di effetti Direct2D per applicare le trasformazioni alle immagini.</span><span class="sxs-lookup"><span data-stu-id="f3a32-148">You can use the Direct2D effects API to apply transforms to images.</span></span>

> [!Note]  
> <span data-ttu-id="f3a32-149">In questo esempio si presuppone che siano già stati creati gli oggetti [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) e [IWICBitmapSource](/windows/desktop/wic/-wic-imp-iwicbitmapsource) .</span><span class="sxs-lookup"><span data-stu-id="f3a32-149">This example assumes that you already have [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) and [IWICBitmapSource](/windows/desktop/wic/-wic-imp-iwicbitmapsource) objects created.</span></span> <span data-ttu-id="f3a32-150">Per ulteriori informazioni sulla creazione di questi oggetti [, vedere come caricare un'immagine in effetti Direct2D utilizzando il FilePicker e i](load-a-id2d1image-using-the-filepicker.md) [dispositivi e i contesti di dispositivo](devices-and-device-contexts.md).</span><span class="sxs-lookup"><span data-stu-id="f3a32-150">For more information on creating these objects see [How to load an image into Direct2D effects using the FilePicker](load-a-id2d1image-using-the-filepicker.md) and [Devices and Device Contexts](devices-and-device-contexts.md).</span></span>

 

1.  <span data-ttu-id="f3a32-151">Dichiarare una variabile [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) e quindi creare un effetto di [origine bitmap](bitmap-source.md) usando il metodo [**ID2DDeviceContext:: CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) .</span><span class="sxs-lookup"><span data-stu-id="f3a32-151">Declare an [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) variable and then create a [bitmap source](bitmap-source.md) effect using the [**ID2DDeviceContext::CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) method.</span></span>

    ```C++
        ComPtr<ID2D1Effect> bitmapSourceEffect;

        DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1BitmapSource, &bitmapSourceEffect));
    ```

    

2.  <span data-ttu-id="f3a32-152">Impostare la proprietà BitmapSource sull'origine bitmap WIC utilizzando [**ID2D1Effect:: SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)).</span><span class="sxs-lookup"><span data-stu-id="f3a32-152">Set the BitmapSource property to the WIC bitmap source using the [**ID2D1Effect::SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)).</span></span>

    ```C++
            DX::ThrowIfFailed(m_bitmapSourceEffect->SetValue(D2D1_BITMAPSOURCE_PROP_WIC_BITMAP_SOURCE, m_wicBitmapSource.Get()));
    ```

    

3.  <span data-ttu-id="f3a32-153">Dichiarare una variabile [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) , quindi creare l'effetto di [sfocatura gaussiana](gaussian-blur.md) .</span><span class="sxs-lookup"><span data-stu-id="f3a32-153">Declare an [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) variable and then create the [gaussian blur](gaussian-blur.md) effect.</span></span>

    ```C++
        ComPtr<ID2D1Effect> gaussianBlurEffect;

        DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1GaussianBlur, &gaussianBlurEffect));
    ```

    

4.  <span data-ttu-id="f3a32-154">Impostare l'input per la ricezione dell'immagine dall'effetto origine bitmap.</span><span class="sxs-lookup"><span data-stu-id="f3a32-154">Set the input to receive the image from the bitmap source effect.</span></span> <span data-ttu-id="f3a32-155">Impostare la quantità di sfocatura per il metodo [**SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) e la proprietà della deviazione standard.</span><span class="sxs-lookup"><span data-stu-id="f3a32-155">Set the blur amount the [**SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) method and the standard deviation property.</span></span>

    ```C++
        gaussianBlurEffect->SetInputEffect(0, bitmapSourceEffect.Get());

        DX::ThrowIfFailed(gaussianBlurEffect->SetValue(D2D1_GAUSSIANBLUR_PROP_STANDARD_DEVIATION, 6.0f));
    ```

    

5.  <span data-ttu-id="f3a32-156">Usare il contesto di dispositivo per tracciare l'output dell'immagine risultante.</span><span class="sxs-lookup"><span data-stu-id="f3a32-156">Use the device context to draw the resulting image output.</span></span>

    ```C++
        m_d2dContext->BeginDraw();

        m_d2dContext->Clear(D2D1::ColorF(D2D1::ColorF::CornflowerBlue));

        // Draw the blurred image.
        m_d2dContext->DrawImage(gaussianBlurEffect.Get());

        HRESULT hr = m_d2dContext->EndDraw();
    ```

    

    <span data-ttu-id="f3a32-157">Il metodo [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) deve essere chiamato tra le chiamate a [**ID2DDeviceContext:: BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) e [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) come ad altre operazioni di rendering Direct2D.</span><span class="sxs-lookup"><span data-stu-id="f3a32-157">The [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) method must be called between the [**ID2DDeviceContext::BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) and [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) calls like other Direct2D render operations.</span></span> <span data-ttu-id="f3a32-158">**DrawImage** può utilizzare un'immagine o l'output di un effetto ed eseguirne il rendering nell'area di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f3a32-158">**DrawImage** can take an image or the output of an effect and render it to the target surface.</span></span>

## <a name="spatial-transforms"></a><span data-ttu-id="f3a32-159">Trasformazioni spaziali</span><span class="sxs-lookup"><span data-stu-id="f3a32-159">Spatial Transforms</span></span>

<span data-ttu-id="f3a32-160">Direct2D fornisce effetti predefiniti che consentono di trasformare immagini nello spazio 2D e 3D, nonché di ridimensionare.</span><span class="sxs-lookup"><span data-stu-id="f3a32-160">Direct2D provides built-in effects that can transform images in 2D and 3D space, as well as scaling.</span></span> <span data-ttu-id="f3a32-161">Gli effetti di ridimensionamento e trasformazione offrono diversi livelli di qualità, ad esempio: Neighbor più vicino, lineare, cubico, lineare multiplo, anisotropico e cubi di alta qualità.</span><span class="sxs-lookup"><span data-stu-id="f3a32-161">The scale and transform effects offer various quality levels like: nearest neighbor, linear, cubic, multi-sample linear, anisotropic, and high quality cubic.</span></span>

> [!Note]  
> <span data-ttu-id="f3a32-162">La modalità anisotropico genera mipmap durante il ridimensionamento. Tuttavia, se si imposta la proprietà **memorizzato nella cache** su true per gli effetti che sono input della trasformazione, il mipmap non verrà generato ogni volta per immagini sufficientemente piccole.</span><span class="sxs-lookup"><span data-stu-id="f3a32-162">Anisotropic mode generates mipmaps when scaling, however, if you set the **Cached** property to true on the effects that are input to the transform the mipmaps won't be generated every time for sufficiently small images.</span></span>

 


```C++
ComPtr<ID2D1Effect> affineTransformEffect;
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D12DAffineTransform, &affineTransformEffect));

affineTransformEffect->SetInput(0, bitmap.Get());

D2D1_MATRIX_3X2_F matrix = D2D1::Matrix3x2F(0.9f, -0.1f,  0.1f, 0.9f, 8.0f, 45.0f);
DX::ThrowIfFailed(affineTransformEffect->SetValue(D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX, matrix));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(affineTransformEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="f3a32-163">Questo utilizzo dell'effetto di trasformazione affine 2D ruota leggermente la bitmap in senso antiorario.</span><span class="sxs-lookup"><span data-stu-id="f3a32-163">This use of the 2D affine transform effect rotates the bitmap counterclockwise slightly.</span></span>



| <span data-ttu-id="f3a32-164">Prima</span><span class="sxs-lookup"><span data-stu-id="f3a32-164">Before</span></span>                                                            |
|-------------------------------------------------------------------|
| ![effetto affine 2D prima dell'immagine.](images/default-before.jpg)      |
| <span data-ttu-id="f3a32-166">After</span><span class="sxs-lookup"><span data-stu-id="f3a32-166">After</span></span>                                                             |
| ![effetto affine 2D dopo l'immagine.](images/21-2daffinetransform.png) |



 

## <a name="compositing-images"></a><span data-ttu-id="f3a32-168">Composizione di immagini</span><span class="sxs-lookup"><span data-stu-id="f3a32-168">Compositing images</span></span>

<span data-ttu-id="f3a32-169">Alcuni effetti accettano più input e li compostano in un'immagine risultante.</span><span class="sxs-lookup"><span data-stu-id="f3a32-169">Some effects accept multiple inputs and composite them into one resulting image.</span></span>

<span data-ttu-id="f3a32-170">Gli effetti compositi incorporati e aritmetici composte forniscono varie modalità. per altre informazioni, vedere l'argomento [composito](composite.md) .</span><span class="sxs-lookup"><span data-stu-id="f3a32-170">The built-in composite and arithmetic composite effects provide various modes, for more info see the [composite](composite.md) topic.</span></span> <span data-ttu-id="f3a32-171">Per l'effetto [Blend](blend.md) sono disponibili diverse modalità con accelerazione GPU.</span><span class="sxs-lookup"><span data-stu-id="f3a32-171">The [blend](blend.md) effect has a variety of GPU accelerated modes available.</span></span>


```C++
ComPtr<ID2D1Effect> compositeEffect;
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect));

compositeEffect->SetInput(0, bitmap.Get());
compositeEffect->SetInput(1, bitmapTwo.Get());

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="f3a32-172">L'effetto composito combina le immagini in modi diversi in base alla modalità specificata.</span><span class="sxs-lookup"><span data-stu-id="f3a32-172">The composite effect combines images in various different ways according to the mode you specify.</span></span>

## <a name="pixel-adjustments"></a><span data-ttu-id="f3a32-173">Regolazioni pixel</span><span class="sxs-lookup"><span data-stu-id="f3a32-173">Pixel adjustments</span></span>

<span data-ttu-id="f3a32-174">Sono disponibili alcuni effetti Direct2D predefiniti che consentono di modificare i dati in pixel.</span><span class="sxs-lookup"><span data-stu-id="f3a32-174">There are a few built-in Direct2D effects that allow you to alter the pixel data.</span></span> <span data-ttu-id="f3a32-175">È ad esempio possibile utilizzare l'effetto matrice colori per modificare il colore di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="f3a32-175">For example, the color matrix effect can be used to change the color of an image.</span></span>


```C++
ComPtr<ID2D1Effect> colorMatrixEffect;
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1ColorMatrix, &colorMatrixEffect));

colorMatrixEffect->SetInput(0, bitmap.Get());

D2D1_MATRIX_5X4_F matrix = D2D1::Matrix5x4F(0, 0, 1, 0,   0, 1, 0, 0,   1, 0, 0, 0,   0, 0, 0, 1,   0, 0, 0, 0);
DX::ThrowIfFailed(colorMatrixEffect->SetValue(D2D1_COLORMATRIX_PROP_COLOR_MATRIX, matrix));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(colorMatrixEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="f3a32-176">Questo codice acquisisce l'immagine e modifica il colore come illustrato nelle immagini di esempio.</span><span class="sxs-lookup"><span data-stu-id="f3a32-176">This code takes the image and alters the color as shown in the example images here.</span></span>



| <span data-ttu-id="f3a32-177">Prima</span><span class="sxs-lookup"><span data-stu-id="f3a32-177">Before</span></span>                                                          |
|-----------------------------------------------------------------|
| ![effetto della matrice di colori prima dell'immagine.](images/default-before.jpg) |
| <span data-ttu-id="f3a32-179">After</span><span class="sxs-lookup"><span data-stu-id="f3a32-179">After</span></span>                                                           |
| ![effetto matrice colore dopo l'immagine.](images/15-colormatrix.png)  |



 

<span data-ttu-id="f3a32-181">Per altre informazioni, vedere la sezione [effetti sul colore predefinito](how-to-create-a-solid-color-brush.md) .</span><span class="sxs-lookup"><span data-stu-id="f3a32-181">See the [color built-in effects](how-to-create-a-solid-color-brush.md) section for more info.</span></span>

## <a name="building-effect-graphs"></a><span data-ttu-id="f3a32-182">Creazione di grafici degli effetti</span><span class="sxs-lookup"><span data-stu-id="f3a32-182">Building effect graphs</span></span>

<span data-ttu-id="f3a32-183">È possibile concatenare gli effetti per trasformare le immagini.</span><span class="sxs-lookup"><span data-stu-id="f3a32-183">You can chain effects together to transform images.</span></span> <span data-ttu-id="f3a32-184">Ad esempio, il codice qui applica un'ombreggiatura e una trasformazione 2D, quindi compone i risultati insieme.</span><span class="sxs-lookup"><span data-stu-id="f3a32-184">For example, the code here applies a shadow and a 2D transform, then composites the results together.</span></span>


```C++
ComPtr<ID2D1Effect> shadowEffect;
ComPtr<ID2D1Effect> affineTransformEffect;
ComPtr<ID2D1Effect> compositeEffect;

DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1Shadow, &shadowEffect));
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D12DAffineTransform, &affineTransformEffect));
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect));

shadowEffect->SetInput(0, bitmap.Get());
affineTransformEffect->SetInputEffect(0, shadowEffect.Get());

D2D1_MATRIX_3X2_F matrix = D2D1::Matrix3x2F::Translation(20, 20));

affineTransformEffect->SetValue(D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX, matrix);

compositeEffect->SetInputEffect(0, affineTransformEffect.Get());
compositeEffect->SetInput(1, bitmap.Get());

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="f3a32-185">Risultato:</span><span class="sxs-lookup"><span data-stu-id="f3a32-185">Here is the result.</span></span>

![output effetto ombreggiatura.](images/effect-overview-shadow.png)

<span data-ttu-id="f3a32-187">Gli effetti accettano gli oggetti [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) come input.</span><span class="sxs-lookup"><span data-stu-id="f3a32-187">Effects take [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) objects as input.</span></span> <span data-ttu-id="f3a32-188">È possibile usare un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) perché l'interfaccia è derivata da **ID2D1Image**.</span><span class="sxs-lookup"><span data-stu-id="f3a32-188">You can use an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) because the interface is derived from **ID2D1Image**.</span></span> <span data-ttu-id="f3a32-189">È anche possibile usare [**ID2D1Effect:: GetOutput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-getoutput) per ottenere l'output di un oggetto [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) come **ID2D1Image** o usare il metodo **SetInputEffect** , che converte l'output.</span><span class="sxs-lookup"><span data-stu-id="f3a32-189">You can also use the [**ID2D1Effect::GetOutput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-getoutput) to get the output of an [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) object as an **ID2D1Image** or use the **SetInputEffect** method, which converts the output for you.</span></span> <span data-ttu-id="f3a32-190">Nella maggior parte dei casi un grafico effetto è costituito da oggetti **ID2D1Effect** direttamente concatenati, che semplifica l'applicazione di più effetti a un'immagine per la creazione di oggetti visivi accattivanti.</span><span class="sxs-lookup"><span data-stu-id="f3a32-190">In most cases an effect graph consists of **ID2D1Effect** objects directly chained together, which makes it easy to apply multiple effects to an image to create compelling visuals.</span></span>

<span data-ttu-id="f3a32-191">Per altre informazioni [, vedere come applicare effetti alle primitive](how-to-apply-effects-to-primitives.md) .</span><span class="sxs-lookup"><span data-stu-id="f3a32-191">See [How to apply effects to primitives](how-to-apply-effects-to-primitives.md) for more info.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f3a32-192">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f3a32-192">Related topics</span></span>

[<span data-ttu-id="f3a32-193">Esempio di effetti immagine di base Direct2D</span><span class="sxs-lookup"><span data-stu-id="f3a32-193">Direct2D basic image effects sample</span></span>](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20basic%20image%20effects%20sample)

[<span data-ttu-id="f3a32-194">Effetti predefiniti</span><span class="sxs-lookup"><span data-stu-id="f3a32-194">Built-in Effects</span></span>](built-in-effects.md)