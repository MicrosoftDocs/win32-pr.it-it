---
title: Effetto ombreggiatura
description: Usare l'effetto ombreggiatura per generare un'ombreggiatura dal canale alfa di un'immagine.
ms.assetid: 53525584-10CF-46C2-9400-C4FB225D4693
keywords:
- effetto ombreggiatura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c42fd8755078dd79f2b01b623b1839785beb3c3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340412"
---
# <a name="shadow-effect"></a><span data-ttu-id="84c88-104">Effetto ombreggiatura</span><span class="sxs-lookup"><span data-stu-id="84c88-104">Shadow effect</span></span>

<span data-ttu-id="84c88-105">Usare l'effetto ombreggiatura per generare un'ombreggiatura dal canale alfa di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="84c88-105">Use the shadow effect to generate a shadow from the alpha channel of an image.</span></span> <span data-ttu-id="84c88-106">L'ombreggiatura è più opaca per i valori alfa più elevati e più trasparente per i valori alfa inferiori.</span><span class="sxs-lookup"><span data-stu-id="84c88-106">The shadow is more opaque for higher alpha values and more transparent for lower alpha values.</span></span> <span data-ttu-id="84c88-107">È possibile impostare la quantità di sfocatura e il colore dell'ombreggiatura.</span><span class="sxs-lookup"><span data-stu-id="84c88-107">You can set the amount of blur and the color of the shadow.</span></span>

-   [<span data-ttu-id="84c88-108">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="84c88-108">Example image</span></span>](#example-image)
-   [<span data-ttu-id="84c88-109">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="84c88-109">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="84c88-110">Modalità di ottimizzazione</span><span class="sxs-lookup"><span data-stu-id="84c88-110">Optimization modes</span></span>](#optimization-modes)
-   [<span data-ttu-id="84c88-111">Bitmap di output</span><span class="sxs-lookup"><span data-stu-id="84c88-111">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="84c88-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="84c88-112">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="84c88-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="84c88-113">Related topics</span></span>](#related-topics)

<span data-ttu-id="84c88-114">Il CLSID per questo effetto è CLSID \_ D2D1Shadow.</span><span class="sxs-lookup"><span data-stu-id="84c88-114">The CLSID for this effect is CLSID\_D2D1Shadow.</span></span>

## <a name="example-image"></a><span data-ttu-id="84c88-115">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="84c88-115">Example image</span></span>

<span data-ttu-id="84c88-116">Nell'esempio riportato di seguito viene illustrato l'output dell'effetto di ombreggiatura convertito verso il basso e verso destra con l'immagine di origine composita nel percorso originale.</span><span class="sxs-lookup"><span data-stu-id="84c88-116">The example here shows the output of the shadow effect translated down and right with the source image composited over it in the original location.</span></span> <span data-ttu-id="84c88-117">L'effetto di ombreggiatura restituisce solo l'ombreggiatura.</span><span class="sxs-lookup"><span data-stu-id="84c88-117">The shadow effect only outputs the shadow.</span></span>



| <span data-ttu-id="84c88-118">Prima</span><span class="sxs-lookup"><span data-stu-id="84c88-118">Before</span></span>                                                  |
|---------------------------------------------------------|
| ![immagine prima dell'effetto.](images/8-crop.png)      |
| <span data-ttu-id="84c88-120">After</span><span class="sxs-lookup"><span data-stu-id="84c88-120">After</span></span>                                                   |
| ![immagine dopo la trasformazione.](images/25-shadow.png) |



 


```C++
ComPtr<ID2D1Effect> shadowEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Shadow, &shadowEffect);

shadowEffect->SetInput(0, bitmap);

// Shadow is composited on top of a white surface to show opacity.
ComPtr<ID2D1Effect> floodEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Flood, &floodEffect);

floodEffect->SetValue(D2D1_FLOOD_PROP_COLOR, D2D1::Vector4F(1.0f, 1.0f, 1.0f, 1.0f));

ComPtr<ID2D1Effect> affineTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D12DAffineTransform, &affineTransformEffect);

affineTransformEffect->SetInputEffect(0, shadowEffect.Get());

D2D1_MATRIX_3X2_F matrix = D2D1::Matrix3x2F::Translation(20, 20));

affineTransformEffect->SetValue(D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX, matrix);

ComPtr<ID2D1Effect> compositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect);

compositeEffect->SetInputEffect(0, floodEffect.Get());
compositeEffect->SetInputEffect(1, affineTransformEffect.Get());
compositeEffect->SetInput(2, bitmap);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="84c88-122">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="84c88-122">Effect properties</span></span>



| <span data-ttu-id="84c88-123">Nome visualizzato e enumerazione dell'indice</span><span class="sxs-lookup"><span data-stu-id="84c88-123">Display name and index enumeration</span></span>                                                        | <span data-ttu-id="84c88-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84c88-124">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84c88-125">BlurStandardDeviation</span><span class="sxs-lookup"><span data-stu-id="84c88-125">BlurStandardDeviation</span></span><br/> <span data-ttu-id="84c88-126">\_ \_ \_ Deviazione standard della sfocatura d2d1 Shadow Prop \_ \_</span><span class="sxs-lookup"><span data-stu-id="84c88-126">D2D1\_SHADOW\_PROP\_BLUR\_STANDARD\_DEVIATION</span></span><br/> | <span data-ttu-id="84c88-127">Quantità di sfocatura da applicare al canale alfa dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="84c88-127">The amount of blur to be applied to the alpha channel of the image.</span></span> <span data-ttu-id="84c88-128">È possibile calcolare il raggio di sfocatura del kernel moltiplicando la deviazione standard di 3.</span><span class="sxs-lookup"><span data-stu-id="84c88-128">You can compute the blur radius of the kernel by multiplying the standard deviation by 3.</span></span> <span data-ttu-id="84c88-129">Le unità della deviazione standard e del raggio di sfocatura sono dip.</span><span class="sxs-lookup"><span data-stu-id="84c88-129">The units of both the standard deviation and blur radius are DIPs.</span></span><br/> <span data-ttu-id="84c88-130">Questa proprietà corrisponde alla proprietà della deviazione standard [sfocatura gaussiana](gaussian-blur.md) .</span><span class="sxs-lookup"><span data-stu-id="84c88-130">This property is the same as the [Gaussian Blur](gaussian-blur.md) standard deviation property.</span></span> <br/> <span data-ttu-id="84c88-131">Il tipo è FLOAT.</span><span class="sxs-lookup"><span data-stu-id="84c88-131">The type is FLOAT.</span></span><br/> <span data-ttu-id="84c88-132">Il valore predefinito è 3.0 f.</span><span class="sxs-lookup"><span data-stu-id="84c88-132">The default value is 3.0f.</span></span><br/> |
| <span data-ttu-id="84c88-133">Colore</span><span class="sxs-lookup"><span data-stu-id="84c88-133">Color</span></span><br/> <span data-ttu-id="84c88-134">\_Colore della \_ prop \_ shadow d2d1</span><span class="sxs-lookup"><span data-stu-id="84c88-134">D2D1\_SHADOW\_PROP\_COLOR</span></span><br/>                                     | <span data-ttu-id="84c88-135">Colore dell'ombreggiatura.</span><span class="sxs-lookup"><span data-stu-id="84c88-135">The color of the drop shadow.</span></span> <span data-ttu-id="84c88-136">Questa proprietà è un \_ vettore d2d1 \_ 4F definito come: (R, G, B, a).</span><span class="sxs-lookup"><span data-stu-id="84c88-136">This property is a D2D1\_VECTOR\_4F defined as: (R, G, B, A).</span></span> <span data-ttu-id="84c88-137">È necessario specificare questo colore nell'Alpha lineare.</span><span class="sxs-lookup"><span data-stu-id="84c88-137">You must specify this color in straight alpha.</span></span><br/> <span data-ttu-id="84c88-138">Il tipo è D2D1 \_ vector \_ 4F.</span><span class="sxs-lookup"><span data-stu-id="84c88-138">The type is D2D1\_VECTOR\_4F.</span></span><br/> <span data-ttu-id="84c88-139">Il valore predefinito è {0,0 f, 0,0 f, 0,0 f, 1.0 f}.</span><span class="sxs-lookup"><span data-stu-id="84c88-139">The default value is {0.0f, 0.0f, 0.0f, 1.0f}.</span></span><br/>                                                                                                                                                                     |
| <span data-ttu-id="84c88-140">Optimization</span><span class="sxs-lookup"><span data-stu-id="84c88-140">Optimization</span></span><br/> <span data-ttu-id="84c88-141">Ottimizzazione di D2D1 \_ shadow \_ prop \_</span><span class="sxs-lookup"><span data-stu-id="84c88-141">D2D1\_SHADOW\_PROP\_OPTIMIZATION</span></span><br/>                       | <span data-ttu-id="84c88-142">Livello di ottimizzazione delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="84c88-142">The level of performance optimization.</span></span><br/> <span data-ttu-id="84c88-143">Il tipo è l' \_ ottimizzazione dell'ombreggiatura d2d1 \_ .</span><span class="sxs-lookup"><span data-stu-id="84c88-143">The type is D2D1\_SHADOW\_OPTIMIZATION.</span></span><br/> <span data-ttu-id="84c88-144">Il valore predefinito è l' \_ ottimizzazione dell'ombreggiatura d2d1 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="84c88-144">The default value is D2D1\_SHADOW\_OPTIMIZATION\_BALANCED.</span></span><br/>                                                                                                                                                                                                                                                   |



 

## <a name="optimization-modes"></a><span data-ttu-id="84c88-145">Modalità di ottimizzazione</span><span class="sxs-lookup"><span data-stu-id="84c88-145">Optimization modes</span></span>



| <span data-ttu-id="84c88-146">Nome</span><span class="sxs-lookup"><span data-stu-id="84c88-146">Name</span></span>                                          | <span data-ttu-id="84c88-147">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84c88-147">Description</span></span>                                                                                                                           |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84c88-148">\_Velocità di \_ ottimizzazione \_ DIRECTIONALBLUR di d2d1</span><span class="sxs-lookup"><span data-stu-id="84c88-148">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_SPEED</span></span>    | <span data-ttu-id="84c88-149">Applica le ottimizzazioni interne, ad esempio la pre-scalabilità a raggi relativamente piccoli.</span><span class="sxs-lookup"><span data-stu-id="84c88-149">Applies internal optimizations such as pre-scaling at relatively small radii.</span></span> <span data-ttu-id="84c88-150">Usa il filtro lineare.</span><span class="sxs-lookup"><span data-stu-id="84c88-150">Uses linear filtering.</span></span>                                  |
| <span data-ttu-id="84c88-151">\_Ottimizzazione d2d1 \_ DIRECTIONALBLUR \_</span><span class="sxs-lookup"><span data-stu-id="84c88-151">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_BALANCED</span></span> | <span data-ttu-id="84c88-152">Usa le stesse soglie di ottimizzazione della modalità velocità, ma usa il filtro trilineare.</span><span class="sxs-lookup"><span data-stu-id="84c88-152">Uses the same optimization thresholds as Speed mode, but uses trilinear filtering.</span></span>                                                    |
| <span data-ttu-id="84c88-153">\_ \_ Qualità ottimizzazione DIRECTIONALBLUR \_ d2d1</span><span class="sxs-lookup"><span data-stu-id="84c88-153">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_QUALITY</span></span>  | <span data-ttu-id="84c88-154">USA solo le ottimizzazioni interne con raggi di sfocatura grandi, in cui è meno probabile che le approssimazioni siano visibili.</span><span class="sxs-lookup"><span data-stu-id="84c88-154">Only uses internal optimizations with large blur radii, where approximations are less likely to be visible.</span></span> <span data-ttu-id="84c88-155">Usa il filtro trilineare.</span><span class="sxs-lookup"><span data-stu-id="84c88-155">Uses trilinear filtering.</span></span> |



 

## <a name="output-bitmap"></a><span data-ttu-id="84c88-156">Bitmap di output</span><span class="sxs-lookup"><span data-stu-id="84c88-156">Output bitmap</span></span>

<span data-ttu-id="84c88-157">La dimensione della bitmap di output corrisponde alla dimensione dell'output di sfocatura.</span><span class="sxs-lookup"><span data-stu-id="84c88-157">The size of the output bitmap is the size of the blur output.</span></span> <span data-ttu-id="84c88-158">La quantità di dimensioni della bitmap di output rispetto alla bitmap originale può essere calcolata utilizzando l'equazione seguente:</span><span class="sxs-lookup"><span data-stu-id="84c88-158">The amount the output bitmap growth relative to the original bitmap can be calculated using the following equation:</span></span>

<span data-ttu-id="84c88-159">Aumento dimensioni bitmap di output (X e Y) = BlurStandardDeviation (DIP) (device-independent pixel) \* 6 \* (dpi utente)/96</span><span class="sxs-lookup"><span data-stu-id="84c88-159">Output Bitmap Growth (X and Y) = BlurStandardDeviation (device-independent pixels (DIPs))\*6\*(User DPI)/96</span></span>

<span data-ttu-id="84c88-160">L'output aumenta in modo uniforme in tutte le direzioni, quindi, ad esempio, se le dimensioni aumentano di 10 pixel in ogni direzione, l'angolo superiore sinistro della bitmap si trova in corrispondenza di (-5,-5) e il diritto inferiore si trova in (105, 105), come illustrato nel diagramma.</span><span class="sxs-lookup"><span data-stu-id="84c88-160">The output increases equally in all direction, so for example if the size increases by 10 pixels in each direction, the upper left corner of the bitmap is located at (-5, -5) and the lower right will be at (105, 105) as shown in the diagram here.</span></span>

![diagramma di crescita della dimensione dell'output dell'effetto ombreggiatura.](images/drop-shadow-output-growth.png)

## <a name="requirements"></a><span data-ttu-id="84c88-162">Requisiti</span><span class="sxs-lookup"><span data-stu-id="84c88-162">Requirements</span></span>



| <span data-ttu-id="84c88-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="84c88-163">Requirement</span></span> | <span data-ttu-id="84c88-164">Valore</span><span class="sxs-lookup"><span data-stu-id="84c88-164">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="84c88-165">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84c88-165">Minimum supported client</span></span> | <span data-ttu-id="84c88-166">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="84c88-166">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="84c88-167">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84c88-167">Minimum supported server</span></span> | <span data-ttu-id="84c88-168">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="84c88-168">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="84c88-169">Intestazione</span><span class="sxs-lookup"><span data-stu-id="84c88-169">Header</span></span>                   | <span data-ttu-id="84c88-170">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="84c88-170">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="84c88-171">Libreria</span><span class="sxs-lookup"><span data-stu-id="84c88-171">Library</span></span>                  | <span data-ttu-id="84c88-172">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="84c88-172">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="84c88-173">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="84c88-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84c88-174">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="84c88-174">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

