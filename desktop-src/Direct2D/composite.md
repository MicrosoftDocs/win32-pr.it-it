---
title: Effetto composito
description: Usare l'effetto composito per combinare due o più immagini. Questo effetto ha 13 diverse modalità composite.
ms.assetid: 60b878e9-1bc6-40d4-ade3-4bbd5c822c55
keywords:
- effetto composito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9872a66d031e8307f911ec7270af81397a80276
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964368"
---
# <a name="composite-effect"></a><span data-ttu-id="11d2e-105">Effetto composito</span><span class="sxs-lookup"><span data-stu-id="11d2e-105">Composite effect</span></span>

<span data-ttu-id="11d2e-106">Usare l'effetto composito per combinare due o più immagini.</span><span class="sxs-lookup"><span data-stu-id="11d2e-106">Use the composite effect to combine 2 or more images.</span></span> <span data-ttu-id="11d2e-107">Questo effetto ha 13 diverse modalità composite.</span><span class="sxs-lookup"><span data-stu-id="11d2e-107">This effect has 13 different composite modes.</span></span> <span data-ttu-id="11d2e-108">T</span><span class="sxs-lookup"><span data-stu-id="11d2e-108">T</span></span>

<span data-ttu-id="11d2e-109">L'effetto composito accetta due o più input.</span><span class="sxs-lookup"><span data-stu-id="11d2e-109">The composite effect accepts 2 or more inputs.</span></span> <span data-ttu-id="11d2e-110">Quando si specificano 2 immagini, la destinazione è il primo input (indice 0) e l'origine è il secondo input (indice 1).</span><span class="sxs-lookup"><span data-stu-id="11d2e-110">When you specify 2 images, destination is the first input (index 0) and the source is the second input (index 1).</span></span> <span data-ttu-id="11d2e-111">Se si specificano più di 2 input, le immagini vengono composte a partire dal primo input e dal secondo e così via.</span><span class="sxs-lookup"><span data-stu-id="11d2e-111">If you specify more than 2 inputs the images are composited starting with the first input and the second and so on.</span></span>

<span data-ttu-id="11d2e-112">Questo effetto implementa tutte le modalità usando l'unità di fusione dell'unità di elaborazione grafica (GPU).</span><span class="sxs-lookup"><span data-stu-id="11d2e-112">This effect implements all of the modes using the blending unit of the graphics processing unit (GPU).</span></span>

<span data-ttu-id="11d2e-113">Il CLSID per questo effetto è CLSID \_ D2D1Composite.</span><span class="sxs-lookup"><span data-stu-id="11d2e-113">The CLSID for this effect is CLSID\_D2D1Composite.</span></span>

-   [<span data-ttu-id="11d2e-114">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="11d2e-114">Example image</span></span>](#example-image)
-   [<span data-ttu-id="11d2e-115">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="11d2e-115">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="11d2e-116">Tipi di modalità</span><span class="sxs-lookup"><span data-stu-id="11d2e-116">Mode types</span></span>](#mode-types)
-   [<span data-ttu-id="11d2e-117">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="11d2e-117">Sample code</span></span>](#sample-code)
-   [<span data-ttu-id="11d2e-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="11d2e-118">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="11d2e-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="11d2e-119">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="11d2e-120">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="11d2e-120">Example image</span></span>

<span data-ttu-id="11d2e-121">L'immagine mostra due rettangoli arrotondati delle stesse dimensioni sovrapposti.</span><span class="sxs-lookup"><span data-stu-id="11d2e-121">The image here shows 2 rounded rectangles of the same size that overlap.</span></span> <span data-ttu-id="11d2e-122">Il rettangolo blu è l'origine e il rettangolo rosso è la destinazione.</span><span class="sxs-lookup"><span data-stu-id="11d2e-122">The blue rectangle is the source and the red rectangle is the destination.</span></span> <span data-ttu-id="11d2e-123">Le immagini sono state composte con l'origine in modalità.</span><span class="sxs-lookup"><span data-stu-id="11d2e-123">The images were composited with the Source Over mode.</span></span>

![immagine di esempio che mostra 2 rettangoli arrotondati delle stesse dimensioni che si sovrappongono usando la modalità di origine.](images/composite-over.png)

<span data-ttu-id="11d2e-125">Ecco un altro esempio che usa la modalità predefinita.</span><span class="sxs-lookup"><span data-stu-id="11d2e-125">Here's another example using the default mode.</span></span>



| <span data-ttu-id="11d2e-126">Prima dell'immagine 1</span><span class="sxs-lookup"><span data-stu-id="11d2e-126">Before image 1</span></span>                                                          |
|-------------------------------------------------------------------------|
| ![prima immagine di origine prima dell'effetto.](images/default-before.jpg) |
| <span data-ttu-id="11d2e-128">Prima dell'immagine 2</span><span class="sxs-lookup"><span data-stu-id="11d2e-128">Before image 2</span></span>                                                          |
| ![seconda immagine prima dell'effetto.](images/3-composite(2of2).png)    |
| <span data-ttu-id="11d2e-130">After</span><span class="sxs-lookup"><span data-stu-id="11d2e-130">After</span></span>                                                                   |
| ![immagine dopo la trasformazione.](images/3-composite.png)               |



 


```C++
ComPtr<ID2D1Effect> compositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect);

compositeEffect->SetInput(0, bitmap);
compositeEffect->SetInput(1, bitmapTwo);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="11d2e-132">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="11d2e-132">Effect properties</span></span>



| <span data-ttu-id="11d2e-133">Nome visualizzato e enumerazione dell'indice</span><span class="sxs-lookup"><span data-stu-id="11d2e-133">Display name and index enumeration</span></span>                     | <span data-ttu-id="11d2e-134">Tipo e valore predefinito</span><span class="sxs-lookup"><span data-stu-id="11d2e-134">Type and default value</span></span>                                                          | <span data-ttu-id="11d2e-135">Descrizione</span><span class="sxs-lookup"><span data-stu-id="11d2e-135">Description</span></span>                   |
|--------------------------------------------------------|---------------------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="11d2e-136">Mode</span><span class="sxs-lookup"><span data-stu-id="11d2e-136">Mode</span></span><br/> <span data-ttu-id="11d2e-137">\_Modalità prop composito d2d1 \_ \_</span><span class="sxs-lookup"><span data-stu-id="11d2e-137">D2D1\_COMPOSITE\_PROP\_MODE</span></span><br/> | <span data-ttu-id="11d2e-138">\_Modalità composita d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="11d2e-138">D2D1\_COMPOSITE\_MODE</span></span><br/> <span data-ttu-id="11d2e-139">\_ \_ Origine modalità COMPOSIta d2d1 \_ \_</span><span class="sxs-lookup"><span data-stu-id="11d2e-139">D2D1\_COMPOSITE\_MODE\_SOURCE\_OVER</span></span><br/> | <span data-ttu-id="11d2e-140">Modalità utilizzata per l'effetto.</span><span class="sxs-lookup"><span data-stu-id="11d2e-140">The mode used for the effect.</span></span> |



 

## <a name="mode-types"></a><span data-ttu-id="11d2e-141">Tipi di modalità</span><span class="sxs-lookup"><span data-stu-id="11d2e-141">Mode types</span></span>

<span data-ttu-id="11d2e-142">La tabella seguente mostra le modalità di questo effetto.</span><span class="sxs-lookup"><span data-stu-id="11d2e-142">The table here shows the modes of this effect.</span></span> <span data-ttu-id="11d2e-143">Le equazioni elencate nella tabella utilizzano questi elementi:</span><span class="sxs-lookup"><span data-stu-id="11d2e-143">The equations listed in the table use these elements:</span></span>

-   <span data-ttu-id="11d2e-144">O = output</span><span class="sxs-lookup"><span data-stu-id="11d2e-144">O = Output</span></span>
-   <span data-ttu-id="11d2e-145">S = origine</span><span class="sxs-lookup"><span data-stu-id="11d2e-145">S = Source</span></span>
-   <span data-ttu-id="11d2e-146">SA = Alpha di origine</span><span class="sxs-lookup"><span data-stu-id="11d2e-146">SA = Source Alpha</span></span>
-   <span data-ttu-id="11d2e-147">D = destinazione</span><span class="sxs-lookup"><span data-stu-id="11d2e-147">D = Destination</span></span>
-   <span data-ttu-id="11d2e-148">DA = Alpha di destinazione</span><span class="sxs-lookup"><span data-stu-id="11d2e-148">DA = Destination Alpha</span></span>



| <span data-ttu-id="11d2e-149">Enumerazione</span><span class="sxs-lookup"><span data-stu-id="11d2e-149">Enumeration</span></span>                                  | <span data-ttu-id="11d2e-150">Equazione</span><span class="sxs-lookup"><span data-stu-id="11d2e-150">Equation</span></span>                          | <span data-ttu-id="11d2e-151">Dimensioni bitmap di output</span><span class="sxs-lookup"><span data-stu-id="11d2e-151">Output Bitmap Size</span></span>                                                                                      |
|----------------------------------------------|-----------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11d2e-152">\_ \_ Origine modalità COMPOSIta d2d1 \_ \_</span><span class="sxs-lookup"><span data-stu-id="11d2e-152">D2D1\_COMPOSITE\_MODE\_SOURCE\_OVER</span></span>          | <span data-ttu-id="11d2e-153">O = S + (1 SA) \* D</span><span class="sxs-lookup"><span data-stu-id="11d2e-153">O = S + (1   SA) \* D</span></span>             | <span data-ttu-id="11d2e-154">Unione delle bitmap di origine e di destinazione</span><span class="sxs-lookup"><span data-stu-id="11d2e-154">Union of source and destination bitmaps</span></span>                                                                 |
| <span data-ttu-id="11d2e-155">\_ \_ Destinazione modalità COMPOSIta d2d1 \_ \_</span><span class="sxs-lookup"><span data-stu-id="11d2e-155">D2D1\_COMPOSITE\_MODE\_DESTINATION\_OVER</span></span>     | <span data-ttu-id="11d2e-156">O = (1 DA) \* S + D</span><span class="sxs-lookup"><span data-stu-id="11d2e-156">O = (1   DA) \* S + D</span></span>             | <span data-ttu-id="11d2e-157">Unione delle bitmap di origine e di destinazione</span><span class="sxs-lookup"><span data-stu-id="11d2e-157">Union of source and destination bitmaps</span></span>                                                                 |
| <span data-ttu-id="11d2e-158">\_Origine modalità composita d2d1 \_ \_ \_ in</span><span class="sxs-lookup"><span data-stu-id="11d2e-158">D2D1\_COMPOSITE\_MODE\_SOURCE\_IN</span></span>            | <span data-ttu-id="11d2e-159">O = DA \* S</span><span class="sxs-lookup"><span data-stu-id="11d2e-159">O = DA \* S</span></span>                       | <span data-ttu-id="11d2e-160">Intersezione delle bitmap di origine e di destinazione</span><span class="sxs-lookup"><span data-stu-id="11d2e-160">Intersection of source and destination bitmaps</span></span>                                                          |
| <span data-ttu-id="11d2e-161">\_Destinazione modalità composita d2d1 \_ \_ \_ in</span><span class="sxs-lookup"><span data-stu-id="11d2e-161">D2D1\_COMPOSITE\_MODE\_DESTINATION\_IN</span></span>       | <span data-ttu-id="11d2e-162">O = SA \* D</span><span class="sxs-lookup"><span data-stu-id="11d2e-162">O = SA \* D</span></span>                       | <span data-ttu-id="11d2e-163">Intersezione delle bitmap di origine e di destinazione</span><span class="sxs-lookup"><span data-stu-id="11d2e-163">Intersection of source and destination bitmaps</span></span>                                                          |
| <span data-ttu-id="11d2e-164">\_ \_ Origine modalità COMPOSIta d2d1 \_ \_</span><span class="sxs-lookup"><span data-stu-id="11d2e-164">D2D1\_COMPOSITE\_MODE\_SOURCE\_OUT</span></span>           | <span data-ttu-id="11d2e-165">O = (1-DA) \* S</span><span class="sxs-lookup"><span data-stu-id="11d2e-165">O = (1 - DA) \* S</span></span>                 | <span data-ttu-id="11d2e-166">Area della bitmap di origine</span><span class="sxs-lookup"><span data-stu-id="11d2e-166">Region of the source bitmap</span></span>                                                                             |
| <span data-ttu-id="11d2e-167">\_ \_ \_ Uscita dalla destinazione della modalità composita d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="11d2e-167">D2D1\_COMPOSITE\_MODE\_DESTINATION\_OUT</span></span>      | <span data-ttu-id="11d2e-168">O = (1-SA) \* D</span><span class="sxs-lookup"><span data-stu-id="11d2e-168">O = (1 - SA) \* D</span></span>                 | <span data-ttu-id="11d2e-169">Area della bitmap di destinazione</span><span class="sxs-lookup"><span data-stu-id="11d2e-169">Region of the destination bitmap</span></span>                                                                        |
| <span data-ttu-id="11d2e-170">\_Origine modalità composita d2d1 in \_ \_ \_ cima</span><span class="sxs-lookup"><span data-stu-id="11d2e-170">D2D1\_COMPOSITE\_MODE\_SOURCE\_ATOP</span></span>          | <span data-ttu-id="11d2e-171">O = DA \* S + (1-SA) \* D</span><span class="sxs-lookup"><span data-stu-id="11d2e-171">O = DA \* S + (1 - SA) \* D</span></span>       | <span data-ttu-id="11d2e-172">Area della bitmap di destinazione</span><span class="sxs-lookup"><span data-stu-id="11d2e-172">Region of the destination bitmap</span></span>                                                                        |
| <span data-ttu-id="11d2e-173">\_Destinazione modalità composita d2d1 in \_ \_ \_ cima</span><span class="sxs-lookup"><span data-stu-id="11d2e-173">D2D1\_COMPOSITE\_MODE\_DESTINATION\_ATOP</span></span>     | <span data-ttu-id="11d2e-174">O = (1-DA) \* S + SA \* D</span><span class="sxs-lookup"><span data-stu-id="11d2e-174">O = (1 - DA) \* S + SA \* D</span></span>       | <span data-ttu-id="11d2e-175">Area della bitmap di origine</span><span class="sxs-lookup"><span data-stu-id="11d2e-175">Region of the source bitmap</span></span>                                                                             |
| <span data-ttu-id="11d2e-176">\_Xor in \_ modalità COMPOSIta d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="11d2e-176">D2D1\_COMPOSITE\_MODE\_XOR</span></span>                   | <span data-ttu-id="11d2e-177">O = (1-DA) \* S + (1-SA) \* D</span><span class="sxs-lookup"><span data-stu-id="11d2e-177">O = (1 - DA) \* S + (1 - SA) \* D</span></span> | <span data-ttu-id="11d2e-178">Unione delle bitmap di origine e di destinazione</span><span class="sxs-lookup"><span data-stu-id="11d2e-178">Union of source and destination bitmaps</span></span>                                                                 |
| <span data-ttu-id="11d2e-179">\_Modalità composita d2d1 \_ \_ Plus</span><span class="sxs-lookup"><span data-stu-id="11d2e-179">D2D1\_COMPOSITE\_MODE\_PLUS</span></span>                  | <span data-ttu-id="11d2e-180">O = S + D</span><span class="sxs-lookup"><span data-stu-id="11d2e-180">O = S + D</span></span>                         | <span data-ttu-id="11d2e-181">Unione delle bitmap di origine e di destinazione</span><span class="sxs-lookup"><span data-stu-id="11d2e-181">Union of source and destination bitmaps</span></span>                                                                 |
| <span data-ttu-id="11d2e-182">\_Copia di \_ origine in modalità COMPOSIta d2d1 \_ \_</span><span class="sxs-lookup"><span data-stu-id="11d2e-182">D2D1\_COMPOSITE\_MODE\_SOURCE\_COPY</span></span>          | <span data-ttu-id="11d2e-183">O = S</span><span class="sxs-lookup"><span data-stu-id="11d2e-183">O = S</span></span>                             | <span data-ttu-id="11d2e-184">Area della bitmap di origine</span><span class="sxs-lookup"><span data-stu-id="11d2e-184">Region of the source bitmap</span></span>                                                                             |
| <span data-ttu-id="11d2e-185">\_Copia di \_ \_ origine vincolata in modalità composita \_ d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="11d2e-185">D2D1\_COMPOSITE\_MODE\_BOUNDED\_SOURCE\_COPY</span></span> | <span data-ttu-id="11d2e-186">O = S (solo dove esiste l'origine)</span><span class="sxs-lookup"><span data-stu-id="11d2e-186">O = S (only where source exists)</span></span>  | <span data-ttu-id="11d2e-187">Unione delle bitmap di origine e di destinazione.</span><span class="sxs-lookup"><span data-stu-id="11d2e-187">Union of source and destination bitmaps.</span></span> <span data-ttu-id="11d2e-188">La destinazione non viene sovrascritta dove l'origine non esiste.</span><span class="sxs-lookup"><span data-stu-id="11d2e-188">Destination is not overwritten where the source doesn't exist.</span></span> |
| <span data-ttu-id="11d2e-189">\_Maschera della modalità composita d2d1 \_ \_ \_ invertita</span><span class="sxs-lookup"><span data-stu-id="11d2e-189">D2D1\_COMPOSITE\_MODE\_MASK\_INVERT</span></span>          | <span data-ttu-id="11d2e-190">O = (1 D) \* S + (1 SA) \* D</span><span class="sxs-lookup"><span data-stu-id="11d2e-190">O = (1   D) \* S + (1   SA) \* D</span></span>  | <span data-ttu-id="11d2e-191">Unione delle bitmap di origine e di destinazione. I valori alfa sono invariati.</span><span class="sxs-lookup"><span data-stu-id="11d2e-191">Union of source and destination bitmaps.The alpha values are unchanged.</span></span>                                 |



 

<span data-ttu-id="11d2e-192">Nella figura seguente viene illustrato un esempio di ogni modalità con immagini con un'opacità di 1,0 o 0,5.</span><span class="sxs-lookup"><span data-stu-id="11d2e-192">The figure here shows an example of each of the modes with images that have an opacity of 1.0 or 0.5.</span></span>

![immagine di esempio di ciascuna modalità con opacità impostata su 1,0 o 0,5.](images/composite-types.png)

## <a name="sample-code"></a><span data-ttu-id="11d2e-194">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="11d2e-194">Sample code</span></span>

<span data-ttu-id="11d2e-195">Per un esempio di questo effetto, scaricare l' [esempio Direct2D composite Effect modes](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample).</span><span class="sxs-lookup"><span data-stu-id="11d2e-195">For an example of this effect, download the [Direct2D composite effect modes sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample).</span></span>

## <a name="requirements"></a><span data-ttu-id="11d2e-196">Requisiti</span><span class="sxs-lookup"><span data-stu-id="11d2e-196">Requirements</span></span>



| <span data-ttu-id="11d2e-197">Requisito</span><span class="sxs-lookup"><span data-stu-id="11d2e-197">Requirement</span></span> | <span data-ttu-id="11d2e-198">Valore</span><span class="sxs-lookup"><span data-stu-id="11d2e-198">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="11d2e-199">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="11d2e-199">Minimum supported client</span></span> | <span data-ttu-id="11d2e-200">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="11d2e-200">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="11d2e-201">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="11d2e-201">Minimum supported server</span></span> | <span data-ttu-id="11d2e-202">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="11d2e-202">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="11d2e-203">Intestazione</span><span class="sxs-lookup"><span data-stu-id="11d2e-203">Header</span></span>                   | <span data-ttu-id="11d2e-204">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="11d2e-204">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="11d2e-205">Libreria</span><span class="sxs-lookup"><span data-stu-id="11d2e-205">Library</span></span>                  | <span data-ttu-id="11d2e-206">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="11d2e-206">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="11d2e-207">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="11d2e-207">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11d2e-208">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="11d2e-208">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

