---
title: Effetto composito aritmetico
description: Usare l'effetto composito aritmetico per combinare 2 immagini usando una somma ponderata dei pixel dalle immagini di input.
ms.assetid: 6EC8CD61-5B51-4A8E-8A61-B291ABB5C5E0
keywords:
- effetto composito aritmetico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04c235ecb024c6b9e7adbce31c9f0cd65bc36cdf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964690"
---
# <a name="arithmetic-composite-effect"></a><span data-ttu-id="e73a5-104">Effetto composito aritmetico</span><span class="sxs-lookup"><span data-stu-id="e73a5-104">Arithmetic composite effect</span></span>

<span data-ttu-id="e73a5-105">Usare l'effetto composito aritmetico per combinare 2 immagini usando una somma ponderata dei pixel dalle immagini di input.</span><span class="sxs-lookup"><span data-stu-id="e73a5-105">Use the arithmetic composite effect to combine 2 images using a weighted sum of pixels from the input images.</span></span>

<span data-ttu-id="e73a5-106">Il CLSID per questo effetto è CLSID \_ D2D1ArithmeticComposite.</span><span class="sxs-lookup"><span data-stu-id="e73a5-106">The CLSID for this effect is CLSID\_D2D1ArithmeticComposite.</span></span>

-   [<span data-ttu-id="e73a5-107">Formula</span><span class="sxs-lookup"><span data-stu-id="e73a5-107">Formula</span></span>](#formula)
-   [<span data-ttu-id="e73a5-108">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="e73a5-108">Example image</span></span>](#example-image)
-   [<span data-ttu-id="e73a5-109">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="e73a5-109">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="e73a5-110">Bitmap di output</span><span class="sxs-lookup"><span data-stu-id="e73a5-110">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="e73a5-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e73a5-111">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="e73a5-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e73a5-112">Related topics</span></span>](#related-topics)

## <a name="formula"></a><span data-ttu-id="e73a5-113">Formula</span><span class="sxs-lookup"><span data-stu-id="e73a5-113">Formula</span></span>

<span data-ttu-id="e73a5-114">Questa formula viene usata per calcolare questo effetto.</span><span class="sxs-lookup"><span data-stu-id="e73a5-114">The formula here is used to compute this effect.</span></span>

<span data-ttu-id="e73a5-115">Output<sub>RGBA</sub> = C1 \* source<sub>RGBA</sub> \* Destination<sub>RGBA</sub> + C2 \* source<sub>RGBA</sub> + C3 \* Destination<sub>RGBA</sub> + C4</span><span class="sxs-lookup"><span data-stu-id="e73a5-115">Output<sub>rgba</sub> = C1 \* Source<sub>rgba</sub> \* Destination<sub>rgba</sub> + C2 \* Source<sub>rgba</sub> + C3 \* Destination<sub>rgba</sub> + C4</span></span>

<span data-ttu-id="e73a5-116">Dove C1, C2, C3, C4 sono coefficienti impostati.</span><span class="sxs-lookup"><span data-stu-id="e73a5-116">Where C1, C2, C3, C4 are coefficients that you set.</span></span>

<span data-ttu-id="e73a5-117">Il mapping dei coefficienti ai valori in un \_ vettore d2d1 \_ 4F (x, y, z, w):</span><span class="sxs-lookup"><span data-stu-id="e73a5-117">The coefficients map to the values in a D2D1\_VECTOR\_4F (x, y, z, w):</span></span>

-   <span data-ttu-id="e73a5-118">x = C1</span><span class="sxs-lookup"><span data-stu-id="e73a5-118">x = C1</span></span>
-   <span data-ttu-id="e73a5-119">y = C2</span><span class="sxs-lookup"><span data-stu-id="e73a5-119">y = C2</span></span>
-   <span data-ttu-id="e73a5-120">z = C3</span><span class="sxs-lookup"><span data-stu-id="e73a5-120">z = C3</span></span>
-   <span data-ttu-id="e73a5-121">w = C4</span><span class="sxs-lookup"><span data-stu-id="e73a5-121">w = C4</span></span>

## <a name="example-image"></a><span data-ttu-id="e73a5-122">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="e73a5-122">Example image</span></span>

<span data-ttu-id="e73a5-123">Un esempio semplice consiste nell'aggiungere i pixel di origine e di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e73a5-123">A simple example is to add the source and destination pixels.</span></span> <span data-ttu-id="e73a5-124">Nell'esempio, 2 rettangoli arrotondati vengono composti insieme.</span><span class="sxs-lookup"><span data-stu-id="e73a5-124">In the example, 2 rounded rectangles are composited together.</span></span> <span data-ttu-id="e73a5-125">Il rettangolo di origine è blu e la destinazione è rossa.</span><span class="sxs-lookup"><span data-stu-id="e73a5-125">The source rectangle is blue and the destination is red.</span></span>

<span data-ttu-id="e73a5-126">L'immagine è l'output dell'effetto composito aritmetico con i coefficienti dell'equazione impostati sui valori qui.</span><span class="sxs-lookup"><span data-stu-id="e73a5-126">The image here is the output of the Arithmetic Composite effect with the coefficients of the equation set to the values here.</span></span>

-   <span data-ttu-id="e73a5-127">C1 = 0</span><span class="sxs-lookup"><span data-stu-id="e73a5-127">C1 = 0</span></span>
-   <span data-ttu-id="e73a5-128">C2 = 1</span><span class="sxs-lookup"><span data-stu-id="e73a5-128">C2 = 1</span></span>
-   <span data-ttu-id="e73a5-129">C3 = 1</span><span class="sxs-lookup"><span data-stu-id="e73a5-129">C3 = 1</span></span>
-   <span data-ttu-id="e73a5-130">C4 = 0</span><span class="sxs-lookup"><span data-stu-id="e73a5-130">C4 = 0</span></span>

![immagine di esempio che mostra 2 rettangoli arrotondati delle stesse dimensioni che si sovrappongono utilizzando l'effetto composito aritmetico.](images/arithmetic-50-percent.png)

<span data-ttu-id="e73a5-132">Il risultato è che vengono aggiunti i valori dei pixel per l'origine e la destinazione.</span><span class="sxs-lookup"><span data-stu-id="e73a5-132">The result is that the pixel values for the source and destination are added.</span></span> <span data-ttu-id="e73a5-133">Le aree in cui i rettangoli non si sovrappongono i valori RGBA sono tutti 0.</span><span class="sxs-lookup"><span data-stu-id="e73a5-133">The regions where the rectangles don't overlap the RGBA values are all 0.</span></span> <span data-ttu-id="e73a5-134">Laddove i rettangoli si sovrappongono, il colore è Magenta perché i valori R e B sono entrambi al massimo.</span><span class="sxs-lookup"><span data-stu-id="e73a5-134">Where the rectangles overlap the color is magenta because the R and B values are both at maximum.</span></span>

<span data-ttu-id="e73a5-135">Ecco un'altra immagine di esempio con il codice.</span><span class="sxs-lookup"><span data-stu-id="e73a5-135">Here's another example image with code.</span></span>



| <span data-ttu-id="e73a5-136">Prima dell'immagine 1</span><span class="sxs-lookup"><span data-stu-id="e73a5-136">Before image 1</span></span>                                                             |
|----------------------------------------------------------------------------|
| ![prima immagine di origine prima dell'effetto.](images/default-before.jpg)    |
| <span data-ttu-id="e73a5-138">Prima dell'immagine 2</span><span class="sxs-lookup"><span data-stu-id="e73a5-138">Before image 2</span></span>                                                             |
| ![seconda immagine prima dell'effetto.](images/4-arthimetic-composite2.jpg) |
| <span data-ttu-id="e73a5-140">After</span><span class="sxs-lookup"><span data-stu-id="e73a5-140">After</span></span>                                                                      |
| ![immagine dopo la trasformazione.](images/4-arithmeticcomposite.png)        |



 


```C++
ComPtr<ID2D1Effect> arithmeticCompositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1ArithmeticComposite, &arithmeticCompositeEffect);

arithmeticCompositeEffect->SetInput(0, bitmap);
arithmeticCompositeEffect->SetInput(1, bitmapTwo);
arithmeticCompositeEffect->SetValue(D2D1_ARITHMETICCOMPOSITE_PROP_COEFFICIENTS, D2D1::Vector4F(0.0f, 0.5f, 0.5f, 0.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(arithmeticCompositeEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="e73a5-142">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="e73a5-142">Effect properties</span></span>



| <span data-ttu-id="e73a5-143">Nome visualizzato e enumerazione dell'indice</span><span class="sxs-lookup"><span data-stu-id="e73a5-143">Display name and index enumeration</span></span>                                               | <span data-ttu-id="e73a5-144">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e73a5-144">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e73a5-145">Coefficienti</span><span class="sxs-lookup"><span data-stu-id="e73a5-145">Coefficients</span></span><br/> <span data-ttu-id="e73a5-146">\_COefficienti della prop ARITHMETICCOMPOSITE d2d1 \_ \_</span><span class="sxs-lookup"><span data-stu-id="e73a5-146">D2D1\_ARITHMETICCOMPOSITE\_PROP\_COEFFICIENTS</span></span><br/> | <span data-ttu-id="e73a5-147">Coefficienti per l'equazione utilizzata per comporre le due immagini di input.</span><span class="sxs-lookup"><span data-stu-id="e73a5-147">The coefficients for the equation used to composite the two input images.</span></span> <span data-ttu-id="e73a5-148">I coefficienti sono senza unità e senza limiti.</span><span class="sxs-lookup"><span data-stu-id="e73a5-148">The coefficients are unitless and unbounded.</span></span> <span data-ttu-id="e73a5-149">Il tipo è D2D1 \_ vector \_ 4F.</span><span class="sxs-lookup"><span data-stu-id="e73a5-149">Type is D2D1\_VECTOR\_4F.</span></span><br/> <span data-ttu-id="e73a5-150">Il valore predefinito è {1.0 f, 0,0 f, 0,0 f, 0,0 f}.</span><span class="sxs-lookup"><span data-stu-id="e73a5-150">Default value is {1.0f, 0.0f, 0.0f, 0.0f}.</span></span><br/>                                                                                                                                                                                                                                 |
| <span data-ttu-id="e73a5-151">ClampOutput</span><span class="sxs-lookup"><span data-stu-id="e73a5-151">ClampOutput</span></span><br/> <span data-ttu-id="e73a5-152">D2D1 \_ ARITHMETICCOMPOSITE \_ prop \_ \_ output Clamp</span><span class="sxs-lookup"><span data-stu-id="e73a5-152">D2D1\_ARITHMETICCOMPOSITE\_PROP\_CLAMP\_OUTPUT</span></span><br/> | <span data-ttu-id="e73a5-153">L'effetto fissa i valori dei colori a un valore compreso tra 0 e 1 prima che l'effetto passi i valori all'effetto successivo nel grafico.</span><span class="sxs-lookup"><span data-stu-id="e73a5-153">The effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph.</span></span> <br/> <span data-ttu-id="e73a5-154">Se si imposta questa impostazione su TRUE, i valori vengono bloccati dall'effetto.</span><span class="sxs-lookup"><span data-stu-id="e73a5-154">If you set this to TRUE the effect will clamp the values.</span></span> <span data-ttu-id="e73a5-155">Se si imposta questa proprietà su FALSE, l'effetto non blocca i valori dei colori, mentre altri effetti e la superficie di output possono bloccare i valori se non hanno una precisione sufficientemente elevata.</span><span class="sxs-lookup"><span data-stu-id="e73a5-155">If you set this to FALSE, the effect will not clamp the color values, but other effects and the output surface may clamp the values if they are not of high enough precision.</span></span><br/> <span data-ttu-id="e73a5-156">Il tipo è BOOL.</span><span class="sxs-lookup"><span data-stu-id="e73a5-156">Type is BOOL.</span></span><br/> <span data-ttu-id="e73a5-157">Il valore predefinito è FALSE.</span><span class="sxs-lookup"><span data-stu-id="e73a5-157">Default value is FALSE.</span></span><br/> |



 

## <a name="output-bitmap"></a><span data-ttu-id="e73a5-158">Bitmap di output</span><span class="sxs-lookup"><span data-stu-id="e73a5-158">Output bitmap</span></span>

<span data-ttu-id="e73a5-159">La bitmap di output dipende dai valori coefficienti.</span><span class="sxs-lookup"><span data-stu-id="e73a5-159">The output bitmap depends on the coefficient values.</span></span> <span data-ttu-id="e73a5-160">Queste sono le possibili dimensioni della bitmap di output.</span><span class="sxs-lookup"><span data-stu-id="e73a5-160">These are the possible output bitmap sizes.</span></span>

-   <span data-ttu-id="e73a5-161">Se C1 è l'unico coefficiente diverso da zero, la dimensione di output è l'intersezione dei rettangoli di input.</span><span class="sxs-lookup"><span data-stu-id="e73a5-161">If C1 is the only non-zero coefficient, the output size is the intersection of the input rectangles.</span></span>
-   <span data-ttu-id="e73a5-162">Se C2 è l'unico coefficiente diverso da zero, la dimensione di output corrisponde alla dimensione del rettangolo di origine.</span><span class="sxs-lookup"><span data-stu-id="e73a5-162">If C2 is the only non-zero coefficient, the output size is the size of the Source rectangle.</span></span>
-   <span data-ttu-id="e73a5-163">Se C3 è l'unico coefficiente diverso da zero, la dimensione di output corrisponde alla dimensione del rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e73a5-163">If C3 is the only non-zero coefficient, the output size is the size of the Destination rectangle..</span></span>
-   <span data-ttu-id="e73a5-164">Se tutti i coefficienti sono pari a zero, la dimensione di output è un rettangolo vuoto.</span><span class="sxs-lookup"><span data-stu-id="e73a5-164">If all coefficients are zero, the output size is an empty rectangle.</span></span>
-   <span data-ttu-id="e73a5-165">Per tutti gli altri valori coefficienti, le dimensioni di output sono l'Unione dei rettangoli di input.</span><span class="sxs-lookup"><span data-stu-id="e73a5-165">For all other coefficient values, the output size is the union of the input rectangles.</span></span>

## <a name="requirements"></a><span data-ttu-id="e73a5-166">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e73a5-166">Requirements</span></span>



| <span data-ttu-id="e73a5-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="e73a5-167">Requirement</span></span> | <span data-ttu-id="e73a5-168">Valore</span><span class="sxs-lookup"><span data-stu-id="e73a5-168">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e73a5-169">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e73a5-169">Minimum supported client</span></span> | <span data-ttu-id="e73a5-170">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="e73a5-170">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="e73a5-171">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e73a5-171">Minimum supported server</span></span> | <span data-ttu-id="e73a5-172">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="e73a5-172">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="e73a5-173">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e73a5-173">Header</span></span>                   | <span data-ttu-id="e73a5-174">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="e73a5-174">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="e73a5-175">Libreria</span><span class="sxs-lookup"><span data-stu-id="e73a5-175">Library</span></span>                  | <span data-ttu-id="e73a5-176">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="e73a5-176">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="e73a5-177">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e73a5-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e73a5-178">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="e73a5-178">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

