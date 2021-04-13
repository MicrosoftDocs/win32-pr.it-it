---
title: Effetto istogramma
description: Usare l'effetto istogramma per generare un istogramma per la bitmap di input in base al numero di contenitori specificato.
ms.assetid: 458E2334-F383-41DE-9479-601AC3007BF3
keywords:
- effetto istogramma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b654ffb2b830914b00a59490ceb429b5de9c51cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400541"
---
# <a name="histogram-effect"></a><span data-ttu-id="aa817-104">Effetto istogramma</span><span class="sxs-lookup"><span data-stu-id="aa817-104">Histogram effect</span></span>

<span data-ttu-id="aa817-105">Usare l'effetto istogramma per generare un istogramma per la bitmap di input in base al numero di contenitori specificato.</span><span class="sxs-lookup"><span data-stu-id="aa817-105">Use the histogram effect to generate a histogram for the input bitmap based on the specified number of bins.</span></span>

<span data-ttu-id="aa817-106">Il CLSID per questo effetto è CLSID \_ D2D1Histogram.</span><span class="sxs-lookup"><span data-stu-id="aa817-106">The CLSID for this effect is CLSID\_D2D1Histogram.</span></span>

-   [<span data-ttu-id="aa817-107">Esempio</span><span class="sxs-lookup"><span data-stu-id="aa817-107">Example</span></span>](#example)
-   [<span data-ttu-id="aa817-108">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="aa817-108">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="aa817-109">Selettori canale</span><span class="sxs-lookup"><span data-stu-id="aa817-109">Channel selectors</span></span>](#channel-selectors)
-   [<span data-ttu-id="aa817-110">Output dei dati</span><span class="sxs-lookup"><span data-stu-id="aa817-110">Data output</span></span>](#data-output)
-   [<span data-ttu-id="aa817-111">Osservazioni:</span><span class="sxs-lookup"><span data-stu-id="aa817-111">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="aa817-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aa817-112">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="aa817-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="aa817-113">Related topics</span></span>](#related-topics)

## <a name="example"></a><span data-ttu-id="aa817-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="aa817-114">Example</span></span>



| <span data-ttu-id="aa817-115">Prima</span><span class="sxs-lookup"><span data-stu-id="aa817-115">Before</span></span>                                                     |
|------------------------------------------------------------|
| ![immagine prima dell'effetto.](images/default-before.jpg) |
| <span data-ttu-id="aa817-117">Grafico dei dati di output dell'istogramma</span><span class="sxs-lookup"><span data-stu-id="aa817-117">Graph of the histogram output data</span></span>                         |
| ![immagine dopo la trasformazione.](images/33-histogram.png) |



 


```C++
ComPtr<ID2D1Effect> histogramEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Histogram, &histogramEffect);

histogramEffect->SetInputEffect(0, m_2DAffineTransformEffectRight.Get());
histogramEffect->SetValue(D2D1_HISTOGRAM_PROP_CHANNEL_SELECT, D2D1_CHANNEL_SELECTOR_G);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(histogramEffect.Get());
m_d2dContext->EndDraw();

// The histogram data is only available once the effect has been 'drawn'.
int histogramBinCount;

HRESULT hr = histogramEffect->GetValue(D2D1_HISTOGRAM_PROP_NUM_BINS, &histogramBinCount);

float *histogramData = new float[histogramBinCount];
hr = histogramEffect->GetValue(D2D1_HISTOGRAM_PROP_HISTOGRAM_OUTPUT, 
                               reinterpret_cast<BYTE*>(histogramData), 
                               histogramBinCount * sizeof(float));
```



## <a name="effect-properties"></a><span data-ttu-id="aa817-119">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="aa817-119">Effect properties</span></span>

<span data-ttu-id="aa817-120">Di seguito è illustrata l'equazione per generare l'output.</span><span class="sxs-lookup"><span data-stu-id="aa817-120">Here's the equation to generate the output.</span></span>

![equazione per generare l'output dell'effetto dell'istogramma.](images/histogram-formula.png)

<span data-ttu-id="aa817-122">*viene valutato* da 0 al numero di contenitori. L'effetto genera un istogramma per i valori dei pixel compresi tra 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="aa817-122">*i* is evaluated from 0 to the number of bins. The effect generates a histogram for pixel values between 0 and 1.</span></span> <span data-ttu-id="aa817-123">I valori al di fuori di questo intervallo vengono fissati all'intervallo.</span><span class="sxs-lookup"><span data-stu-id="aa817-123">Values outside of this range are clamped to the range.</span></span> <span data-ttu-id="aa817-124">L'intervallo di un determinato bucket dipende dal numero di bucket.</span><span class="sxs-lookup"><span data-stu-id="aa817-124">The range of a particular bucket depends on the number of buckets.</span></span> <span data-ttu-id="aa817-125">Questo effetto funziona su pixel bitmap dritti.</span><span class="sxs-lookup"><span data-stu-id="aa817-125">This effect works on straight bitmap pixels.</span></span> <span data-ttu-id="aa817-126">I canali dei colori della bitmap di input sono divisi dal canale alfa per calcolare questo effetto.</span><span class="sxs-lookup"><span data-stu-id="aa817-126">The color channels of the input bitmap are divided by the alpha channel to compute this effect.</span></span>



| <span data-ttu-id="aa817-127">Nome visualizzato e enumerazione dell'indice</span><span class="sxs-lookup"><span data-stu-id="aa817-127">Display name and index enumeration</span></span>                                             | <span data-ttu-id="aa817-128">Tipo e valore predefinito</span><span class="sxs-lookup"><span data-stu-id="aa817-128">Type and default value</span></span>                                                   | <span data-ttu-id="aa817-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aa817-129">Description</span></span>                                                                                                                                                                                   |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa817-130">NumBins</span><span class="sxs-lookup"><span data-stu-id="aa817-130">NumBins</span></span><br/> <span data-ttu-id="aa817-131">D2D1 \_ istogramma \_ prop \_ \_ contenitori</span><span class="sxs-lookup"><span data-stu-id="aa817-131">D2D1\_HISTOGRAM\_PROP\_NUM\_BINS</span></span><br/>                 | <span data-ttu-id="aa817-132">UINT32</span><span class="sxs-lookup"><span data-stu-id="aa817-132">UINT32</span></span><br/> <span data-ttu-id="aa817-133">256</span><span class="sxs-lookup"><span data-stu-id="aa817-133">256</span></span><br/>                                         | <span data-ttu-id="aa817-134">Specifica il numero di bin usati per l'istogramma.</span><span class="sxs-lookup"><span data-stu-id="aa817-134">Specifies the number of bins used for the histogram.</span></span> <span data-ttu-id="aa817-135">L'intervallo di valori di intensità che rientra in un bucket specifico dipende dal numero di bucket specificati.</span><span class="sxs-lookup"><span data-stu-id="aa817-135">The range of intensity values that fall into a particular bucket depend on the number of specified buckets.</span></span>                              |
| <span data-ttu-id="aa817-136">ChannelSelect</span><span class="sxs-lookup"><span data-stu-id="aa817-136">ChannelSelect</span></span><br/> <span data-ttu-id="aa817-137">\_Selezione del \_ \_ canale prop dell'istogramma d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="aa817-137">D2D1\_HISTOGRAM\_PROP\_CHANNEL\_SELECT</span></span><br/>     | <span data-ttu-id="aa817-138">\_Selettore di canale d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="aa817-138">D2D1\_CHANNEL\_SELECTOR</span></span><br/> <span data-ttu-id="aa817-139">\_ \_ R selettore canale d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="aa817-139">D2D1\_CHANNEL\_SELECTOR\_R</span></span><br/> | <span data-ttu-id="aa817-140">Specifica il canale utilizzato per generare l'istogramma.</span><span class="sxs-lookup"><span data-stu-id="aa817-140">Specifies the channel used to generate the histogram.</span></span> <span data-ttu-id="aa817-141">Questo effetto ha un singolo output di dati corrispondente al canale specificato.</span><span class="sxs-lookup"><span data-stu-id="aa817-141">This effect has a single data output corresponding to the specified channel.</span></span> <span data-ttu-id="aa817-142">Per altre informazioni, vedere [selettori di canale](#channel-selectors) .</span><span class="sxs-lookup"><span data-stu-id="aa817-142">See [Channel selectors](#channel-selectors) for more info.</span></span> |
| <span data-ttu-id="aa817-143">HistogramOutput</span><span class="sxs-lookup"><span data-stu-id="aa817-143">HistogramOutput</span></span><br/> <span data-ttu-id="aa817-144">\_ \_ \_ Output istogramma della prop istogramma d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="aa817-144">D2D1\_HISTOGRAM\_PROP\_HISTOGRAM\_OUTPUT</span></span><br/> | <span data-ttu-id="aa817-145">FLOAT\[\]</span><span class="sxs-lookup"><span data-stu-id="aa817-145">FLOAT\[\]</span></span><br/> <span data-ttu-id="aa817-146">Solo proprietà di output.</span><span class="sxs-lookup"><span data-stu-id="aa817-146">Output property only.</span></span><br/>                    | <span data-ttu-id="aa817-147">Matrice di output.</span><span class="sxs-lookup"><span data-stu-id="aa817-147">The output array.</span></span>                                                                                                                                                                             |



 

## <a name="channel-selectors"></a><span data-ttu-id="aa817-148">Selettori canale</span><span class="sxs-lookup"><span data-stu-id="aa817-148">Channel selectors</span></span>



| <span data-ttu-id="aa817-149">Enumerazione</span><span class="sxs-lookup"><span data-stu-id="aa817-149">Enumeration</span></span>                | <span data-ttu-id="aa817-150">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aa817-150">Description</span></span>                                                           |
|----------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="aa817-151">\_ \_ R selettore canale d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="aa817-151">D2D1\_CHANNEL\_SELECTOR\_R</span></span> | <span data-ttu-id="aa817-152">L'effetto genera l'output dell'istogramma in base al canale rosso.</span><span class="sxs-lookup"><span data-stu-id="aa817-152">The effect generates the histogram output based on the red channel.</span></span>   |
| <span data-ttu-id="aa817-153">\_Selettore di canale d2d1 \_ \_ G</span><span class="sxs-lookup"><span data-stu-id="aa817-153">D2D1\_CHANNEL\_SELECTOR\_G</span></span> | <span data-ttu-id="aa817-154">L'effetto genera l'output dell'istogramma in base al canale verde.</span><span class="sxs-lookup"><span data-stu-id="aa817-154">The effect generates the histogram output based on the green channel.</span></span> |
| <span data-ttu-id="aa817-155">\_Selettore di canale d2d1 \_ \_ B</span><span class="sxs-lookup"><span data-stu-id="aa817-155">D2D1\_CHANNEL\_SELECTOR\_B</span></span> | <span data-ttu-id="aa817-156">L'effetto genera l'output dell'istogramma in base al canale blu.</span><span class="sxs-lookup"><span data-stu-id="aa817-156">The effect generates the histogram output based on the blue channel.</span></span>  |
| <span data-ttu-id="aa817-157">\_ \_ Selettore \_ di canale A d2d1</span><span class="sxs-lookup"><span data-stu-id="aa817-157">D2D1\_CHANNEL\_SELECTOR\_A</span></span> | <span data-ttu-id="aa817-158">L'effetto genera l'output dell'istogramma in base al canale alfa.</span><span class="sxs-lookup"><span data-stu-id="aa817-158">The effect generates the histogram output based on the alpha channel.</span></span> |



 

## <a name="data-output"></a><span data-ttu-id="aa817-159">Output dei dati</span><span class="sxs-lookup"><span data-stu-id="aa817-159">Data output</span></span>

<span data-ttu-id="aa817-160">Questo effetto restituisce un valore FLOAT \[ \] con il numero di elementi corrispondenti al numero di contenitori specificati. Ogni elemento del FLOAT \[ \] è un valore float.</span><span class="sxs-lookup"><span data-stu-id="aa817-160">This effect outputs a FLOAT\[\], with the number of elements corresponding to the number of specified bins. Each element in the FLOAT\[\] is a float.</span></span> <span data-ttu-id="aa817-161">Il valore dell'elemento corrisponde al numero di elementi nel contenitore.</span><span class="sxs-lookup"><span data-stu-id="aa817-161">The value of the element corresponds to the number of elements in that bin.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa817-162">Commenti</span><span class="sxs-lookup"><span data-stu-id="aa817-162">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="aa817-163">Il metodo [**CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) ha esito negativo se il dispositivo non supporta DirectCompute e restituisce HRESULT = D2DERR \_ funzionalità del dispositivo insufficienti \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="aa817-163">The [**CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) method fails if the device doesn't support DirectCompute and returns HRESULT = D2DERR\_INSUFFICIENT\_DEVICE\_CAPABILITIES.</span></span> <span data-ttu-id="aa817-164">Tutte le schede DirectX11 e le schede DirectX10 che supportano DirectCompute possono usare l'effetto.</span><span class="sxs-lookup"><span data-stu-id="aa817-164">All DirectX11 cards and DirectX10 cards that support DirectCompute can use the effect.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="aa817-165">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aa817-165">Requirements</span></span>



| <span data-ttu-id="aa817-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa817-166">Requirement</span></span> | <span data-ttu-id="aa817-167">Valore</span><span class="sxs-lookup"><span data-stu-id="aa817-167">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="aa817-168">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aa817-168">Minimum supported client</span></span> | <span data-ttu-id="aa817-169">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="aa817-169">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="aa817-170">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aa817-170">Minimum supported server</span></span> | <span data-ttu-id="aa817-171">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="aa817-171">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="aa817-172">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aa817-172">Header</span></span>                   | <span data-ttu-id="aa817-173">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="aa817-173">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="aa817-174">Libreria</span><span class="sxs-lookup"><span data-stu-id="aa817-174">Library</span></span>                  | <span data-ttu-id="aa817-175">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="aa817-175">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="aa817-176">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="aa817-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa817-177">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="aa817-177">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

