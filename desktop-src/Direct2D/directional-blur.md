---
title: Effetto sfocatura direzionale
description: L'effetto di sfocatura direzionale è simile alla sfocatura gaussiana, ad eccezione del fatto che è possibile inclinare la sfocatura in una direzione specifica.
ms.assetid: 59328FA4-5C27-4A81-AAB2-C5B25B3615C6
keywords:
- sfocatura direzionale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0e1c098d17929563cf69f4e61416fa0d93a88dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739855"
---
# <a name="directional-blur-effect"></a><span data-ttu-id="eaf1e-104">Effetto sfocatura direzionale</span><span class="sxs-lookup"><span data-stu-id="eaf1e-104">Directional blur effect</span></span>

<span data-ttu-id="eaf1e-105">L'effetto di sfocatura direzionale è simile alla [sfocatura gaussiana](gaussian-blur.md), ad eccezione del fatto che è possibile inclinare la sfocatura in una direzione specifica.</span><span class="sxs-lookup"><span data-stu-id="eaf1e-105">The directional blur effect is similar to [Gaussian blur](gaussian-blur.md), except you can skew the blur in a particular direction.</span></span> <span data-ttu-id="eaf1e-106">È possibile usare questo effetto per creare un'immagine come se fosse in movimento o per enfatizzare un'immagine animata.</span><span class="sxs-lookup"><span data-stu-id="eaf1e-106">You can use this effect to make an image look as if it is in motion or to emphasize an animated image.</span></span>

<span data-ttu-id="eaf1e-107">Il CLSID per questo effetto è CLSID \_ D2D1DirectionalBlur.</span><span class="sxs-lookup"><span data-stu-id="eaf1e-107">The CLSID for this effect is CLSID\_D2D1DirectionalBlur.</span></span>

-   [<span data-ttu-id="eaf1e-108">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="eaf1e-108">Example image</span></span>](#example-image)
-   [<span data-ttu-id="eaf1e-109">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="eaf1e-109">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="eaf1e-110">Modalità di ottimizzazione</span><span class="sxs-lookup"><span data-stu-id="eaf1e-110">Optimization modes</span></span>](#optimization-modes)
-   [<span data-ttu-id="eaf1e-111">Modalità bordo</span><span class="sxs-lookup"><span data-stu-id="eaf1e-111">Border modes</span></span>](#border-modes)
-   [<span data-ttu-id="eaf1e-112">Bitmap di output</span><span class="sxs-lookup"><span data-stu-id="eaf1e-112">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="eaf1e-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eaf1e-113">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="eaf1e-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eaf1e-114">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="eaf1e-115">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="eaf1e-115">Example image</span></span>



| <span data-ttu-id="eaf1e-116">Prima</span><span class="sxs-lookup"><span data-stu-id="eaf1e-116">Before</span></span>                                                          |
|-----------------------------------------------------------------|
| ![immagine prima dell'effetto.](images/default-before.jpg)      |
| <span data-ttu-id="eaf1e-118">After</span><span class="sxs-lookup"><span data-stu-id="eaf1e-118">After</span></span>                                                           |
| ![immagine dopo la trasformazione.](images/2-directionalblur.png) |



 


```C++
ComPtr<ID2D1Effect> directionalBlurEffect;
m_d2dContext->CreateEffect(CLSID_D2D1DirectionalBlur, &directionalBlurEffect);

directionalBlurEffect->SetInput(0, bitmap);
directionalBlurEffect->SetValue(D2D1_DIRECTIONALBLUR_PROP_STANDARD_DEVIATION, 7.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(directionalBlurEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="eaf1e-120">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="eaf1e-120">Effect properties</span></span>



| <span data-ttu-id="eaf1e-121">Nome visualizzato e enumerazione dell'indice</span><span class="sxs-lookup"><span data-stu-id="eaf1e-121">Display name and index enumeration</span></span>                                                       | <span data-ttu-id="eaf1e-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eaf1e-122">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eaf1e-123">StandardDeviation</span><span class="sxs-lookup"><span data-stu-id="eaf1e-123">StandardDeviation</span></span><br/> <span data-ttu-id="eaf1e-124">D2D1 \_ DIRECTIONALBLUR \_ prop \_ \_ deviazione standard</span><span class="sxs-lookup"><span data-stu-id="eaf1e-124">D2D1\_DIRECTIONALBLUR\_PROP\_STANDARD\_DEVIATION</span></span><br/> | <span data-ttu-id="eaf1e-125">Quantità di sfocatura da applicare all'immagine.</span><span class="sxs-lookup"><span data-stu-id="eaf1e-125">The amount of blur to be applied to the image.</span></span> <span data-ttu-id="eaf1e-126">È possibile calcolare il raggio di sfocatura del kernel moltiplicando la deviazione standard di 3.</span><span class="sxs-lookup"><span data-stu-id="eaf1e-126">You can compute the blur radius of the kernel by multiplying the standard deviation by 3.</span></span> <span data-ttu-id="eaf1e-127">Le unità della deviazione standard e del raggio di sfocatura sono dip.</span><span class="sxs-lookup"><span data-stu-id="eaf1e-127">The units of both the standard deviation and blur radius are DIPs.</span></span> <span data-ttu-id="eaf1e-128">Il valore 0 DIP Disabilita questo effetto.</span><span class="sxs-lookup"><span data-stu-id="eaf1e-128">A value of 0 DIPs disables this effect.</span></span> <span data-ttu-id="eaf1e-129">Il tipo è FLOAT.</span><span class="sxs-lookup"><span data-stu-id="eaf1e-129">The type is FLOAT.</span></span><br/> <span data-ttu-id="eaf1e-130">Il valore predefinito è 3.0 f.</span><span class="sxs-lookup"><span data-stu-id="eaf1e-130">The default value is 3.0f.</span></span><br/>                                                                            |
| <span data-ttu-id="eaf1e-131">Angle</span><span class="sxs-lookup"><span data-stu-id="eaf1e-131">Angle</span></span><br/> <span data-ttu-id="eaf1e-132">\_Angolo della \_ prop \_ DIRECTIONALBLUR d2d1</span><span class="sxs-lookup"><span data-stu-id="eaf1e-132">D2D1\_DIRECTIONALBLUR\_PROP\_ANGLE</span></span><br/>                           | <span data-ttu-id="eaf1e-133">Angolo della sfocatura rispetto all'asse x, in senso antiorario.</span><span class="sxs-lookup"><span data-stu-id="eaf1e-133">The angle of the blur relative to the x-axis, in the counterclockwise direction.</span></span> <span data-ttu-id="eaf1e-134">Le unità vengono specificate in gradi.</span><span class="sxs-lookup"><span data-stu-id="eaf1e-134">The units are specified in degrees.</span></span><br/> <span data-ttu-id="eaf1e-135">Il kernel di sfocatura viene innanzitutto generato utilizzando lo stesso processo dell'effetto [sfocatura gaussiana](gaussian-blur.md) .</span><span class="sxs-lookup"><span data-stu-id="eaf1e-135">The blur kernel is first generated using the same process as for the [Gaussian blur](gaussian-blur.md) effect.</span></span> <span data-ttu-id="eaf1e-136">I valori del kernel vengono quindi trasformati in base all'angolo di sfocatura.</span><span class="sxs-lookup"><span data-stu-id="eaf1e-136">The kernel values are then transformed according to the blur angle.</span></span><br/> <span data-ttu-id="eaf1e-137">Il tipo è FLOAT.</span><span class="sxs-lookup"><span data-stu-id="eaf1e-137">The type is FLOAT.</span></span><br/> <span data-ttu-id="eaf1e-138">Il valore predefinito è 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="eaf1e-138">The default value is 0.0f.</span></span><br/> |
| <span data-ttu-id="eaf1e-139">Optimization</span><span class="sxs-lookup"><span data-stu-id="eaf1e-139">Optimization</span></span><br/> <span data-ttu-id="eaf1e-140">\_Ottimizzazione della \_ prop \_ DIRECTIONALBLUR d2d1</span><span class="sxs-lookup"><span data-stu-id="eaf1e-140">D2D1\_DIRECTIONALBLUR\_PROP\_OPTIMIZATION</span></span><br/>             | <span data-ttu-id="eaf1e-141">Modalità di ottimizzazione.</span><span class="sxs-lookup"><span data-stu-id="eaf1e-141">The optimization mode.</span></span> <span data-ttu-id="eaf1e-142">Per altre informazioni, vedere [modalità di ottimizzazione](#optimization-modes) .</span><span class="sxs-lookup"><span data-stu-id="eaf1e-142">See [Optimization modes](#optimization-modes) for more info.</span></span><br/> <span data-ttu-id="eaf1e-143">Il tipo è D2D1 \_ DIRECTIONALBLUR \_ Optimization.</span><span class="sxs-lookup"><span data-stu-id="eaf1e-143">The type is D2D1\_DIRECTIONALBLUR\_OPTIMIZATION.</span></span><br/> <span data-ttu-id="eaf1e-144">Il valore predefinito è D2D1 \_ DIRECTIONALBLUR \_ Optimization \_ Balanced.</span><span class="sxs-lookup"><span data-stu-id="eaf1e-144">The default value is D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_BALANCED.</span></span> <br/>                                                                                                                                                         |
| <span data-ttu-id="eaf1e-145">BorderMode</span><span class="sxs-lookup"><span data-stu-id="eaf1e-145">BorderMode</span></span><br/> <span data-ttu-id="eaf1e-146">\_ \_ \_ Modalità bordo prop DIRECTIONALBLUR \_ d2d1</span><span class="sxs-lookup"><span data-stu-id="eaf1e-146">D2D1\_DIRECTIONALBLUR\_PROP\_BORDER\_MODE</span></span><br/>               | <span data-ttu-id="eaf1e-147">Modalità utilizzata per calcolare il bordo dell'immagine, soft o hard.</span><span class="sxs-lookup"><span data-stu-id="eaf1e-147">The mode used to calculate the border of the image, soft or hard.</span></span> <span data-ttu-id="eaf1e-148">Per altre informazioni, vedere [Border modes](#border-modes) .</span><span class="sxs-lookup"><span data-stu-id="eaf1e-148">See [Border modes](#border-modes) for more info.</span></span><br/> <span data-ttu-id="eaf1e-149">Il tipo è D2D1 \_ Border \_ mode.</span><span class="sxs-lookup"><span data-stu-id="eaf1e-149">The type is D2D1\_BORDER\_MODE.</span></span><br/> <span data-ttu-id="eaf1e-150">Il valore predefinito è D2D1 \_ Border \_ mode \_ .</span><span class="sxs-lookup"><span data-stu-id="eaf1e-150">The default value is D2D1\_BORDER\_MODE\_SOFT.</span></span><br/>                                                                                                                                                                 |



 

## <a name="optimization-modes"></a><span data-ttu-id="eaf1e-151">Modalità di ottimizzazione</span><span class="sxs-lookup"><span data-stu-id="eaf1e-151">Optimization modes</span></span>



| <span data-ttu-id="eaf1e-152">Nome</span><span class="sxs-lookup"><span data-stu-id="eaf1e-152">Name</span></span>                                          | <span data-ttu-id="eaf1e-153">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eaf1e-153">Description</span></span>                                                                                                                           |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eaf1e-154">\_Velocità di \_ ottimizzazione \_ DIRECTIONALBLUR di d2d1</span><span class="sxs-lookup"><span data-stu-id="eaf1e-154">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_SPEED</span></span>    | <span data-ttu-id="eaf1e-155">Applica le ottimizzazioni interne, ad esempio la pre-scalabilità a raggi relativamente piccoli.</span><span class="sxs-lookup"><span data-stu-id="eaf1e-155">Applies internal optimizations such as pre-scaling at relatively small radii.</span></span> <span data-ttu-id="eaf1e-156">Usa il filtro lineare.</span><span class="sxs-lookup"><span data-stu-id="eaf1e-156">Uses linear filtering.</span></span>                                  |
| <span data-ttu-id="eaf1e-157">\_Ottimizzazione d2d1 \_ DIRECTIONALBLUR \_</span><span class="sxs-lookup"><span data-stu-id="eaf1e-157">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_BALANCED</span></span> | <span data-ttu-id="eaf1e-158">Usa le stesse soglie di ottimizzazione della modalità velocità, ma usa il filtro trilineare.</span><span class="sxs-lookup"><span data-stu-id="eaf1e-158">Uses the same optimization thresholds as Speed mode, but uses trilinear filtering.</span></span>                                                    |
| <span data-ttu-id="eaf1e-159">\_ \_ Qualità ottimizzazione DIRECTIONALBLUR \_ d2d1</span><span class="sxs-lookup"><span data-stu-id="eaf1e-159">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_QUALITY</span></span>  | <span data-ttu-id="eaf1e-160">USA solo le ottimizzazioni interne con raggi di sfocatura grandi, in cui è meno probabile che le approssimazioni siano visibili.</span><span class="sxs-lookup"><span data-stu-id="eaf1e-160">Only uses internal optimizations with large blur radii, where approximations are less likely to be visible.</span></span> <span data-ttu-id="eaf1e-161">Usa il filtro trilineare.</span><span class="sxs-lookup"><span data-stu-id="eaf1e-161">Uses trilinear filtering.</span></span> |



 

## <a name="border-modes"></a><span data-ttu-id="eaf1e-162">Modalità bordo</span><span class="sxs-lookup"><span data-stu-id="eaf1e-162">Border modes</span></span>



| <span data-ttu-id="eaf1e-163">Nome</span><span class="sxs-lookup"><span data-stu-id="eaf1e-163">Name</span></span>                     | <span data-ttu-id="eaf1e-164">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eaf1e-164">Description</span></span>                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eaf1e-165">\_Modalità bordo \_ d2d1 \_ Soft</span><span class="sxs-lookup"><span data-stu-id="eaf1e-165">D2D1\_BORDER\_MODE\_SOFT</span></span> | <span data-ttu-id="eaf1e-166">L'effetto Ritaglia l'immagine con i pixel neri trasparenti quando applica il kernel di sfocatura, ottenendo un bordo flessibile.</span><span class="sxs-lookup"><span data-stu-id="eaf1e-166">The effect pads the image with transparent black pixels as it applies the blur kernel, resulting in a soft edge.</span></span> <br/>                                                                                             |
| <span data-ttu-id="eaf1e-167">\_Modalità bordo \_ d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="eaf1e-167">D2D1\_BORDER\_MODE\_HARD</span></span> | <span data-ttu-id="eaf1e-168">L'effetto fissa l'output alla dimensione dell'immagine di input.</span><span class="sxs-lookup"><span data-stu-id="eaf1e-168">The effect clamps the output to the size of the input image.</span></span> <span data-ttu-id="eaf1e-169">Quando l'effetto applica il kernel di sfocatura, estende l'immagine di input con una trasformazione del bordo di tipo mirror per i campioni all'esterno dei limiti di input.</span><span class="sxs-lookup"><span data-stu-id="eaf1e-169">When the effect applies the blur kernel, it extends the input image with a mirror-type border transform for samples outside of the input bounds.</span></span><br/> |



 

## <a name="output-bitmap"></a><span data-ttu-id="eaf1e-170">Bitmap di output</span><span class="sxs-lookup"><span data-stu-id="eaf1e-170">Output bitmap</span></span>

<span data-ttu-id="eaf1e-171">La dimensione della bitmap di output aumenta in base alla deviazione standard, all'angolo dell'effetto e alla modalità del bordo.</span><span class="sxs-lookup"><span data-stu-id="eaf1e-171">The size of the output bitmap increases based on the standard deviation, the angle of the effect, and the border mode.</span></span> <span data-ttu-id="eaf1e-172">Se la modalità bordo è impostata su D2D1 \_ Border \_ mode \_ , le dimensioni della bitmap di output aumentano in base alle dimensioni del kernel di sfocatura, rappresentate in pixel.</span><span class="sxs-lookup"><span data-stu-id="eaf1e-172">If the border mode is set to D2D1\_BORDER\_MODE\_SOFT the size of the output bitmap increases by the size of the blur kernel, represented in pixels.</span></span> <span data-ttu-id="eaf1e-173">Queste equazioni possono essere usate per calcolare le dimensioni della bitmap di output.</span><span class="sxs-lookup"><span data-stu-id="eaf1e-173">These equations can be used to calculate the size of the output bitmap.</span></span>



| <span data-ttu-id="eaf1e-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="eaf1e-174">Requirement</span></span> | <span data-ttu-id="eaf1e-175">Valore</span><span class="sxs-lookup"><span data-stu-id="eaf1e-175">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="eaf1e-176">Aumento dimensioni bitmap di output X</span><span class="sxs-lookup"><span data-stu-id="eaf1e-176">Output Bitmap Growth X</span></span> | <span data-ttu-id="eaf1e-177">StandardDeviation (DIP) \* 6 \* (((dpi utente)/96) \* cos (angolo))</span><span class="sxs-lookup"><span data-stu-id="eaf1e-177">StandardDeviation (DIPs) \* 6 \* ((User DPI) / 96) \* cos(Angle))</span></span> |
| <span data-ttu-id="eaf1e-178">Crescita bitmap di output Y</span><span class="sxs-lookup"><span data-stu-id="eaf1e-178">Output Bitmap Growth Y</span></span> | <span data-ttu-id="eaf1e-179">StandardDeviation (DIP) \* 6 \* (((dpi utente)/96) \* sin (angolo))</span><span class="sxs-lookup"><span data-stu-id="eaf1e-179">StandardDeviation (DIPs) \* 6 \* ((User DPI) / 96) \* sin(Angle))</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="eaf1e-180">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eaf1e-180">Requirements</span></span>



| <span data-ttu-id="eaf1e-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="eaf1e-181">Requirement</span></span> | <span data-ttu-id="eaf1e-182">Valore</span><span class="sxs-lookup"><span data-stu-id="eaf1e-182">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="eaf1e-183">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eaf1e-183">Minimum supported client</span></span> | <span data-ttu-id="eaf1e-184">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="eaf1e-184">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="eaf1e-185">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eaf1e-185">Minimum supported server</span></span> | <span data-ttu-id="eaf1e-186">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="eaf1e-186">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="eaf1e-187">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eaf1e-187">Header</span></span>                   | <span data-ttu-id="eaf1e-188">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="eaf1e-188">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="eaf1e-189">Libreria</span><span class="sxs-lookup"><span data-stu-id="eaf1e-189">Library</span></span>                  | <span data-ttu-id="eaf1e-190">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="eaf1e-190">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="eaf1e-191">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eaf1e-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eaf1e-192">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="eaf1e-192">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

