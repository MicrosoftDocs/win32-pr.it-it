---
title: Effetto sfocatura gaussiana
description: Utilizzare l'effetto di sfocatura gaussiana per creare una sfocatura basata sulla funzione gaussiana sull'intera immagine di input.
ms.assetid: 6B8C9A0A-81D6-4CC2-B30B-995D4C2E59FC
keywords:
- Sfocatura gaussiana
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfbe8b309a498315e389be45d382eca3ee1b98ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104570870"
---
# <a name="gaussian-blur-effect"></a><span data-ttu-id="61822-104">Effetto sfocatura gaussiana</span><span class="sxs-lookup"><span data-stu-id="61822-104">Gaussian blur effect</span></span>

<span data-ttu-id="61822-105">Utilizzare l'effetto di sfocatura gaussiana per creare una sfocatura basata sulla funzione gaussiana sull'intera immagine di input.</span><span class="sxs-lookup"><span data-stu-id="61822-105">Use the Gaussian blur effect to create a blur based on the Gaussian function over the entire input image.</span></span>

<span data-ttu-id="61822-106">È possibile utilizzare questo effetto per creare bagliori e ombreggiature e utilizzare l'effetto [composito](composite.md) per applicare il risultato all'immagine originale.</span><span class="sxs-lookup"><span data-stu-id="61822-106">You can use this effect to create glows and drop shadows and use the [composite](composite.md) effect to apply the result to the original image.</span></span> <span data-ttu-id="61822-107">È utile nell'elaborazione di foto per filtri come evidenziazioni e ombre.</span><span class="sxs-lookup"><span data-stu-id="61822-107">It is useful in photo processing for filters like highlights and shadows.</span></span> <span data-ttu-id="61822-108">È possibile usare l'output di questo effetto per l'input in effetti di illuminazione, ad esempio l' [illuminazione speculare](specular-lighting.md) o gli effetti di [illuminazione diffusa](diffuse-lighting.md) , perché il canale alfa è sfocato e gli effetti di illuminazione usano il canale alfa per determinare la geometria della superficie come mappa di altezza.</span><span class="sxs-lookup"><span data-stu-id="61822-108">You can use the output of this effect for input into lighting effects, like the [Specular Lighting](specular-lighting.md) or [Diffuse Lighting](diffuse-lighting.md) effects, because the alpha channel is blurred, too and lighting effects use the alpha channel to determine surface geometry as a height map.</span></span>

<span data-ttu-id="61822-109">Questo effetto viene usato dall'effetto di [ombreggiatura](drop-shadow.md) incorporato.</span><span class="sxs-lookup"><span data-stu-id="61822-109">This effect is used by the built-in [Shadow](drop-shadow.md) effect.</span></span>

<span data-ttu-id="61822-110">Il CLSID per questo effetto è CLSID \_ D2D1GaussianBlur.</span><span class="sxs-lookup"><span data-stu-id="61822-110">The CLSID for this effect is CLSID\_D2D1GaussianBlur.</span></span>

-   [<span data-ttu-id="61822-111">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="61822-111">Example image</span></span>](#example-image)
-   [<span data-ttu-id="61822-112">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="61822-112">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="61822-113">Modalità di ottimizzazione</span><span class="sxs-lookup"><span data-stu-id="61822-113">Optimization modes</span></span>](#optimization-modes)
-   [<span data-ttu-id="61822-114">Modalità bordo</span><span class="sxs-lookup"><span data-stu-id="61822-114">Border modes</span></span>](#border-modes)
-   [<span data-ttu-id="61822-115">Bitmap di output</span><span class="sxs-lookup"><span data-stu-id="61822-115">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="61822-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="61822-116">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="61822-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="61822-117">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="61822-118">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="61822-118">Example image</span></span>



| <span data-ttu-id="61822-119">Prima</span><span class="sxs-lookup"><span data-stu-id="61822-119">Before</span></span>                                                       |
|--------------------------------------------------------------|
| ![immagine prima dell'effetto.](images/default-before.jpg)   |
| <span data-ttu-id="61822-121">After</span><span class="sxs-lookup"><span data-stu-id="61822-121">After</span></span>                                                        |
| ![immagine dopo la trasformazione.](images/1-gaussianblur.png) |



 


```C++
ComPtr<ID2D1Effect> gaussianBlurEffect;
m_d2dContext->CreateEffect(CLSID_D2D1GaussianBlur, &gaussianBlurEffect);

gaussianBlurEffect->SetInput(0, bitmap);
gaussianBlurEffect->SetValue(D2D1_GAUSSIANBLUR_PROP_STANDARD_DEVIATION, 3.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(gaussianBlurEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="61822-123">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="61822-123">Effect properties</span></span>



| <span data-ttu-id="61822-124">Nome visualizzato e enumerazione dell'indice</span><span class="sxs-lookup"><span data-stu-id="61822-124">Display name and index enumeration</span></span>                                                    | <span data-ttu-id="61822-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="61822-125">Description</span></span>                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61822-126">StandardDeviation</span><span class="sxs-lookup"><span data-stu-id="61822-126">StandardDeviation</span></span><br/> <span data-ttu-id="61822-127">D2D1 \_ GAUSSIANBLUR \_ prop \_ \_ deviazione standard</span><span class="sxs-lookup"><span data-stu-id="61822-127">D2D1\_GAUSSIANBLUR\_PROP\_STANDARD\_DEVIATION</span></span><br/> | <span data-ttu-id="61822-128">Quantità di sfocatura da applicare all'immagine.</span><span class="sxs-lookup"><span data-stu-id="61822-128">The amount of blur to be applied to the image.</span></span> <span data-ttu-id="61822-129">È possibile calcolare il raggio di sfocatura del kernel moltiplicando la deviazione standard di 3.</span><span class="sxs-lookup"><span data-stu-id="61822-129">You can compute the blur radius of the kernel by multiplying the standard deviation by 3.</span></span> <span data-ttu-id="61822-130">Le unità della deviazione standard e del raggio di sfocatura sono dip.</span><span class="sxs-lookup"><span data-stu-id="61822-130">The units of both the standard deviation and blur radius are DIPs.</span></span> <span data-ttu-id="61822-131">Il valore zero DIP Disabilita interamente questo effetto.</span><span class="sxs-lookup"><span data-stu-id="61822-131">A value of zero DIPs disables this effect entirely.</span></span> <span data-ttu-id="61822-132">Il tipo è FLOAT.</span><span class="sxs-lookup"><span data-stu-id="61822-132">The type is FLOAT.</span></span><br/> <span data-ttu-id="61822-133">Il valore predefinito è 3.0 f.</span><span class="sxs-lookup"><span data-stu-id="61822-133">The default value is 3.0f.</span></span><br/> |
| <span data-ttu-id="61822-134">Optimization</span><span class="sxs-lookup"><span data-stu-id="61822-134">Optimization</span></span><br/> <span data-ttu-id="61822-135">\_Ottimizzazione della \_ prop \_ GAUSSIANBLUR d2d1</span><span class="sxs-lookup"><span data-stu-id="61822-135">D2D1\_GAUSSIANBLUR\_PROP\_OPTIMIZATION</span></span><br/>             | <span data-ttu-id="61822-136">Modalità di ottimizzazione.</span><span class="sxs-lookup"><span data-stu-id="61822-136">The optimization mode.</span></span> <span data-ttu-id="61822-137">Per altre informazioni, vedere [modalità di ottimizzazione](#optimization-modes) .</span><span class="sxs-lookup"><span data-stu-id="61822-137">See [Optimization modes](#optimization-modes) for more info.</span></span> <span data-ttu-id="61822-138">Il tipo è D2D1 \_ GAUSSIANBLUR \_ Optimization.</span><span class="sxs-lookup"><span data-stu-id="61822-138">The type is D2D1\_GAUSSIANBLUR\_OPTIMIZATION.</span></span><br/> <span data-ttu-id="61822-139">Il valore predefinito è D2D1 \_ GAUSSIANBLUR \_ Optimization \_ Balanced.</span><span class="sxs-lookup"><span data-stu-id="61822-139">The default value is D2D1\_GAUSSIANBLUR\_OPTIMIZATION\_BALANCED.</span></span><br/>                                                                                                            |
| <span data-ttu-id="61822-140">BorderMode</span><span class="sxs-lookup"><span data-stu-id="61822-140">BorderMode</span></span><br/> <span data-ttu-id="61822-141">\_ \_ \_ Modalità bordo prop GAUSSIANBLUR \_ d2d1</span><span class="sxs-lookup"><span data-stu-id="61822-141">D2D1\_GAUSSIANBLUR\_PROP\_BORDER\_MODE</span></span><br/>               | <span data-ttu-id="61822-142">Modalità utilizzata per calcolare il bordo dell'immagine, soft o hard.</span><span class="sxs-lookup"><span data-stu-id="61822-142">The mode used to calculate the border of the image, soft or hard.</span></span> <span data-ttu-id="61822-143">Per altre informazioni, vedere [Border modes](#border-modes) .</span><span class="sxs-lookup"><span data-stu-id="61822-143">See [Border modes](#border-modes) for more info.</span></span> <br/> <span data-ttu-id="61822-144">Il tipo è D2D1 \_ GAUSSIANBLUR \_ Border \_ mode.</span><span class="sxs-lookup"><span data-stu-id="61822-144">The type is D2D1\_GAUSSIANBLUR\_BORDER\_MODE.</span></span><br/> <span data-ttu-id="61822-145">Il valore predefinito è D2D1 \_ Border \_ mode \_ .</span><span class="sxs-lookup"><span data-stu-id="61822-145">The default value is D2D1\_BORDER\_MODE\_SOFT.</span></span><br/>                                                                                   |



 

## <a name="optimization-modes"></a><span data-ttu-id="61822-146">Modalità di ottimizzazione</span><span class="sxs-lookup"><span data-stu-id="61822-146">Optimization modes</span></span>



| <span data-ttu-id="61822-147">Nome</span><span class="sxs-lookup"><span data-stu-id="61822-147">Name</span></span>                                          | <span data-ttu-id="61822-148">Descrizione</span><span class="sxs-lookup"><span data-stu-id="61822-148">Description</span></span>                                                                                                                           |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61822-149">\_Velocità di \_ ottimizzazione \_ DIRECTIONALBLUR di d2d1</span><span class="sxs-lookup"><span data-stu-id="61822-149">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_SPEED</span></span>    | <span data-ttu-id="61822-150">Applica le ottimizzazioni interne, ad esempio la pre-scalabilità a raggi relativamente piccoli.</span><span class="sxs-lookup"><span data-stu-id="61822-150">Applies internal optimizations such as pre-scaling at relatively small radii.</span></span> <span data-ttu-id="61822-151">Usa il filtro lineare.</span><span class="sxs-lookup"><span data-stu-id="61822-151">Uses linear filtering.</span></span>                                  |
| <span data-ttu-id="61822-152">\_Ottimizzazione d2d1 \_ DIRECTIONALBLUR \_</span><span class="sxs-lookup"><span data-stu-id="61822-152">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_BALANCED</span></span> | <span data-ttu-id="61822-153">Usa le stesse soglie di ottimizzazione della modalità velocità, ma usa il filtro trilineare.</span><span class="sxs-lookup"><span data-stu-id="61822-153">Uses the same optimization thresholds as Speed mode, but uses trilinear filtering.</span></span>                                                    |
| <span data-ttu-id="61822-154">\_ \_ Qualità ottimizzazione DIRECTIONALBLUR \_ d2d1</span><span class="sxs-lookup"><span data-stu-id="61822-154">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_QUALITY</span></span>  | <span data-ttu-id="61822-155">USA solo le ottimizzazioni interne con raggi di sfocatura grandi, in cui è meno probabile che le approssimazioni siano visibili.</span><span class="sxs-lookup"><span data-stu-id="61822-155">Only uses internal optimizations with large blur radii, where approximations are less likely to be visible.</span></span> <span data-ttu-id="61822-156">Usa il filtro trilineare.</span><span class="sxs-lookup"><span data-stu-id="61822-156">Uses trilinear filtering.</span></span> |



 

## <a name="border-modes"></a><span data-ttu-id="61822-157">Modalità bordo</span><span class="sxs-lookup"><span data-stu-id="61822-157">Border modes</span></span>



| <span data-ttu-id="61822-158">Nome</span><span class="sxs-lookup"><span data-stu-id="61822-158">Name</span></span>                     | <span data-ttu-id="61822-159">Descrizione</span><span class="sxs-lookup"><span data-stu-id="61822-159">Description</span></span>                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61822-160">\_Modalità bordo \_ d2d1 \_ Soft</span><span class="sxs-lookup"><span data-stu-id="61822-160">D2D1\_BORDER\_MODE\_SOFT</span></span> | <span data-ttu-id="61822-161">L'effetto Ritaglia l'immagine con i pixel neri trasparenti quando applica il kernel di sfocatura, ottenendo un bordo flessibile.</span><span class="sxs-lookup"><span data-stu-id="61822-161">The effect pads the image with transparent black pixels as it applies the blur kernel, resulting in a soft edge.</span></span> <br/>                                                                                             |
| <span data-ttu-id="61822-162">\_Modalità bordo \_ d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="61822-162">D2D1\_BORDER\_MODE\_HARD</span></span> | <span data-ttu-id="61822-163">L'effetto fissa l'output alla dimensione dell'immagine di input.</span><span class="sxs-lookup"><span data-stu-id="61822-163">The effect clamps the output to the size of the input image.</span></span> <span data-ttu-id="61822-164">Quando l'effetto applica il kernel di sfocatura, estende l'immagine di input con una trasformazione del bordo di tipo mirror per i campioni all'esterno dei limiti di input.</span><span class="sxs-lookup"><span data-stu-id="61822-164">When the effect applies the blur kernel, it extends the input image with a mirror-type border transform for samples outside of the input bounds.</span></span><br/> |



 

## <a name="output-bitmap"></a><span data-ttu-id="61822-165">Bitmap di output</span><span class="sxs-lookup"><span data-stu-id="61822-165">Output bitmap</span></span>

<span data-ttu-id="61822-166">L'output di questo effetto può essere maggiore della bitmap di input in base al raggio di sfocatura e alla modalità bordo.</span><span class="sxs-lookup"><span data-stu-id="61822-166">The output of this effect can be larger than the input bitmap based on the blur radius and the border mode.</span></span> <span data-ttu-id="61822-167">Se la modalità bordo è impostata su D2D1 \_ bordo \_ modalità \_ soft il ize della bitmap di output aumenta in base alle dimensioni del kernel di sfocatura, rappresentato in pixel.</span><span class="sxs-lookup"><span data-stu-id="61822-167">If the border mode is set to D2D1\_BORDER\_MODE\_SOFT the s ize of the output bitmap increases by the size of the blur kernel, represented in pixels.</span></span> <span data-ttu-id="61822-168">Questa tabella fornisce un'equazione che è possibile usare per calcolare la bitmap di output.</span><span class="sxs-lookup"><span data-stu-id="61822-168">This table provides an equation that you can use to compute the output bitmap.</span></span>

`Output bitmap growth (X and Y) = StandardDeviation  (DIPs)*6*((User DPI)/96)`

<span data-ttu-id="61822-169">Quindi, se le dimensioni dell'immagine aumentano di 10 pixel in ogni direzione, l'angolo superiore sinistro dell'immagine si troverà in corrispondenza di (-5,-5) mentre la parte inferiore destra si trova in corrispondenza di (105, 105).</span><span class="sxs-lookup"><span data-stu-id="61822-169">So, if the image size increases by 10 pixels in each direction the upper left corner of the image will be located at (-5, -5) while the lower right will be at (105, 105).</span></span>

## <a name="requirements"></a><span data-ttu-id="61822-170">Requisiti</span><span class="sxs-lookup"><span data-stu-id="61822-170">Requirements</span></span>



| <span data-ttu-id="61822-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="61822-171">Requirement</span></span> | <span data-ttu-id="61822-172">Valore</span><span class="sxs-lookup"><span data-stu-id="61822-172">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="61822-173">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="61822-173">Minimum supported client</span></span> | <span data-ttu-id="61822-174">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="61822-174">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="61822-175">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="61822-175">Minimum supported server</span></span> | <span data-ttu-id="61822-176">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="61822-176">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="61822-177">Intestazione</span><span class="sxs-lookup"><span data-stu-id="61822-177">Header</span></span>                   | <span data-ttu-id="61822-178">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="61822-178">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="61822-179">Libreria</span><span class="sxs-lookup"><span data-stu-id="61822-179">Library</span></span>                  | <span data-ttu-id="61822-180">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="61822-180">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="61822-181">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="61822-181">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61822-182">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="61822-182">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

