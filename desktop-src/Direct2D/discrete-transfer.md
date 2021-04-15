---
title: Effetto trasferimento discreto
description: Usare l'effetto di trasferimento discreto per eseguire il mapping delle intensità dei colori di un'immagine usando una funzione di trasferimento dei passaggi creata da un elenco di valori forniti.
ms.assetid: 5A612002-2B1D-4FC3-B364-AACD9FD44BEC
keywords:
- effetto trasferimento discreto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c05ef08f9ddf053eaa686cb0f88d4183194d9e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104570432"
---
# <a name="discrete-transfer-effect"></a><span data-ttu-id="76c0d-104">Effetto trasferimento discreto</span><span class="sxs-lookup"><span data-stu-id="76c0d-104">Discrete transfer effect</span></span>

<span data-ttu-id="76c0d-105">Usare l'effetto di trasferimento discreto per eseguire il mapping delle intensità dei colori di un'immagine usando una funzione di trasferimento dei passaggi creata da un elenco di valori forniti.</span><span class="sxs-lookup"><span data-stu-id="76c0d-105">Use the discrete transfer effect to map the color intensities of an image using a step transfer function created from a list of values you provide.</span></span>

<span data-ttu-id="76c0d-106">Il CLSID per questo effetto è CLSID \_ D2D1DiscreteTransfer.</span><span class="sxs-lookup"><span data-stu-id="76c0d-106">The CLSID for this effect is CLSID\_D2D1DiscreteTransfer.</span></span>

-   [<span data-ttu-id="76c0d-107">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="76c0d-107">Example image</span></span>](#example-image)
-   [<span data-ttu-id="76c0d-108">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="76c0d-108">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="76c0d-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76c0d-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="76c0d-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="76c0d-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="76c0d-111">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="76c0d-111">Example image</span></span>

<span data-ttu-id="76c0d-112">L'immagine mostra l'input e l'output dell'effetto di trasferimento discreto.</span><span class="sxs-lookup"><span data-stu-id="76c0d-112">The image here shows the input and output of the discrete transfer effect.</span></span>



| <span data-ttu-id="76c0d-113">Prima</span><span class="sxs-lookup"><span data-stu-id="76c0d-113">Before</span></span>                                                            |
|-------------------------------------------------------------------|
| ![immagine prima dell'effetto.](images/default-before.jpg)        |
| <span data-ttu-id="76c0d-115">After</span><span class="sxs-lookup"><span data-stu-id="76c0d-115">After</span></span>                                                             |
| ![immagine dopo la trasformazione.](images/12-discretetransfer.png) |



 


```C++
ComPtr<ID2D1Effect> discreteTransferEffect;
m_d2dContext->CreateEffect(CLSID_D2D1DiscreteTransfer, &discreteTransferEffect);

discreteTransferEffect->SetInput(0, bitmap);

float table[3] = {0.0f, 0.5f, 1.0f};
discreteTransferEffect->SetValue(D2D1_DISCRETETRANSFER_PROP_RED_TABLE, table);
discreteTransferEffect->SetValue(D2D1_DISCRETETRANSFER_PROP_GREEN_TABLE, table);
discreteTransferEffect->SetValue(D2D1_DISCRETETRANSFER_PROP_BLUE_TABLE, table);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(discreteTransferEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="76c0d-117">La funzione Transfer è basata sull'elenco di input: V = (V0, V1, V2, V3, V?</span><span class="sxs-lookup"><span data-stu-id="76c0d-117">The transfer function is based on the list of inputs: V=(V0,V1,V2,V3,V?</span></span> <span data-ttu-id="76c0d-118">, V<sub>n</sub>), dove N è il numero di elementi-1.</span><span class="sxs-lookup"><span data-stu-id="76c0d-118">,V<sub>N</sub>) where N is the number of elements - 1.</span></span>

<span data-ttu-id="76c0d-119">L'intensità dei pixel di input viene rappresentata come C. L'intensità del pixel di output, C viene calcolata con l'equazione:</span><span class="sxs-lookup"><span data-stu-id="76c0d-119">The input pixel intensity is represented as C. The output pixel intensity, C  is calculated with the equation:</span></span>

<span data-ttu-id="76c0d-120">Per un valore C, scegliere un valore k, in modo che:</span><span class="sxs-lookup"><span data-stu-id="76c0d-120">For a value C, pick a value k, such that:</span></span>

![formula per il processo.](images/discrete-transfer1.png)

<span data-ttu-id="76c0d-122">L'output C può essere calcolato usando l'equazione: C'= V?</span><span class="sxs-lookup"><span data-stu-id="76c0d-122">The output C  can be calculated using the equation: C' = V?</span></span>

<span data-ttu-id="76c0d-123">Questo effetto funziona su immagini alfa diritte e premoltiplicate.</span><span class="sxs-lookup"><span data-stu-id="76c0d-123">This effect works on straight and premultiplied alpha images.</span></span> <span data-ttu-id="76c0d-124">L'effetto restituisce bitmap alfa premoltiplicate.</span><span class="sxs-lookup"><span data-stu-id="76c0d-124">The effect outputs premultiplied alpha bitmaps.</span></span>

<span data-ttu-id="76c0d-125">Di seguito è riportato il grafico della funzione di trasferimento discreto come se gli input fossero `[0.25, 0.5, 0.75, 1.0]` .</span><span class="sxs-lookup"><span data-stu-id="76c0d-125">Here is what the graph of discrete transfer function looks like if the inputs are `[0.25, 0.5, 0.75, 1.0]`.</span></span>

![grafico dell'intensità dei pixel per la funzione di trasferimento discreto.](images/discrete-transfer-graph.png)

## <a name="effect-properties"></a><span data-ttu-id="76c0d-127">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="76c0d-127">Effect properties</span></span>

> [!Note]  
> <span data-ttu-id="76c0d-128">I valori di tutti i canali delle proprietà di trasferimento discreto sono privi di unità e hanno un minimo di 0,0 e un massimo di 1,0.</span><span class="sxs-lookup"><span data-stu-id="76c0d-128">The values of all channels of the discrete transfer properties are unitless and have a minimum of 0.0 and a maximum 1.0.</span></span>

 



| <span data-ttu-id="76c0d-129">Nome visualizzato e enumerazione dell'indice</span><span class="sxs-lookup"><span data-stu-id="76c0d-129">Display name and index enumeration</span></span>                                              | <span data-ttu-id="76c0d-130">Tipo e valore predefinito</span><span class="sxs-lookup"><span data-stu-id="76c0d-130">Type and default value</span></span>                       | <span data-ttu-id="76c0d-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="76c0d-131">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------|----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76c0d-132">RedTable</span><span class="sxs-lookup"><span data-stu-id="76c0d-132">RedTable</span></span><br/> <span data-ttu-id="76c0d-133">D2D1 \_ DISCRETETRANSFER \_ - \_ \_ tabella rossa</span><span class="sxs-lookup"><span data-stu-id="76c0d-133">D2D1\_DISCRETETRANSFER\_PROP\_RED\_TABLE</span></span><br/>         | <span data-ttu-id="76c0d-134">FLOAT\[\]</span><span class="sxs-lookup"><span data-stu-id="76c0d-134">FLOAT\[\]</span></span><br/> <span data-ttu-id="76c0d-135">{0,0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="76c0d-135">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="76c0d-136">Elenco di valori utilizzati per definire la funzione di trasferimento per il canale rosso.</span><span class="sxs-lookup"><span data-stu-id="76c0d-136">The list of values used to define the transfer function for the Red channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="76c0d-137">RedDisable</span><span class="sxs-lookup"><span data-stu-id="76c0d-137">RedDisable</span></span><br/> <span data-ttu-id="76c0d-138">D2D1 \_ DISCRETETRANSFER \_ prop \_ Red \_ Disable</span><span class="sxs-lookup"><span data-stu-id="76c0d-138">D2D1\_DISCRETETRANSFER\_PROP\_RED\_DISABLE</span></span><br/>     | <span data-ttu-id="76c0d-139">BOOL</span><span class="sxs-lookup"><span data-stu-id="76c0d-139">BOOL</span></span><br/> <span data-ttu-id="76c0d-140">FALSE</span><span class="sxs-lookup"><span data-stu-id="76c0d-140">FALSE</span></span><br/>             | <span data-ttu-id="76c0d-141">Se si imposta questo valore su TRUE, l'effetto non applica la funzione di trasferimento al canale rosso.</span><span class="sxs-lookup"><span data-stu-id="76c0d-141">If you set this to TRUE the effect does not apply the transfer function to the Red channel.</span></span> <span data-ttu-id="76c0d-142">Se si imposta questa opzione su FALSE, l'effetto applica la funzione RedDiscreteTransfer al canale rosso.</span><span class="sxs-lookup"><span data-stu-id="76c0d-142">If you set this to FALSE the effect applies the RedDiscreteTransfer function to the Red channel.</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="76c0d-143">GreenTable</span><span class="sxs-lookup"><span data-stu-id="76c0d-143">GreenTable</span></span><br/> <span data-ttu-id="76c0d-144">\_ \_ \_ Tabella verde prop d2d1 \_ DISCRETETRANSFER</span><span class="sxs-lookup"><span data-stu-id="76c0d-144">D2D1\_DISCRETETRANSFER\_PROP\_GREEN\_TABLE</span></span><br/>     | <span data-ttu-id="76c0d-145">FLOAT\[\]</span><span class="sxs-lookup"><span data-stu-id="76c0d-145">FLOAT\[\]</span></span><br/> <span data-ttu-id="76c0d-146">{0,0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="76c0d-146">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="76c0d-147">Elenco di valori che definiscono la funzione di trasferimento per il canale verde.</span><span class="sxs-lookup"><span data-stu-id="76c0d-147">The list of values that define the transfer function for the Green channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="76c0d-148">GreenDisable</span><span class="sxs-lookup"><span data-stu-id="76c0d-148">GreenDisable</span></span><br/> <span data-ttu-id="76c0d-149">D2D1 \_ DISCRETETRANSFER \_ prop \_ Green \_ Disable</span><span class="sxs-lookup"><span data-stu-id="76c0d-149">D2D1\_DISCRETETRANSFER\_PROP\_GREEN\_DISABLE</span></span><br/> | <span data-ttu-id="76c0d-150">BOOL</span><span class="sxs-lookup"><span data-stu-id="76c0d-150">BOOL</span></span><br/> <span data-ttu-id="76c0d-151">FALSE</span><span class="sxs-lookup"><span data-stu-id="76c0d-151">FALSE</span></span><br/>             | <span data-ttu-id="76c0d-152">Se si imposta questo valore su TRUE, l'effetto non applica la funzione di trasferimento al canale verde.</span><span class="sxs-lookup"><span data-stu-id="76c0d-152">If you set this to TRUE the effect does not apply the transfer function to the Green channel.</span></span> <span data-ttu-id="76c0d-153">Se si imposta questa opzione su FALSE, l'effetto applica la funzione GreenDiscreteTransfer al canale verde.</span><span class="sxs-lookup"><span data-stu-id="76c0d-153">If you set this to FALSE the effect applies the GreenDiscreteTransfer function to the Green channel.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="76c0d-154">BlueTable</span><span class="sxs-lookup"><span data-stu-id="76c0d-154">BlueTable</span></span><br/> <span data-ttu-id="76c0d-155">D2D1 \_ DISCRETETRANSFER \_ - \_ tabella blu Prop \_</span><span class="sxs-lookup"><span data-stu-id="76c0d-155">D2D1\_DISCRETETRANSFER\_PROP\_BLUE\_TABLE</span></span><br/>       | <span data-ttu-id="76c0d-156">FLOAT\[\]</span><span class="sxs-lookup"><span data-stu-id="76c0d-156">FLOAT\[\]</span></span><br/> <span data-ttu-id="76c0d-157">{0,0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="76c0d-157">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="76c0d-158">Elenco di valori che definiscono la funzione di trasferimento per il canale blu.</span><span class="sxs-lookup"><span data-stu-id="76c0d-158">The list of values that define the transfer function for the Blue channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="76c0d-159">BlueDisable</span><span class="sxs-lookup"><span data-stu-id="76c0d-159">BlueDisable</span></span><br/> <span data-ttu-id="76c0d-160">D2D1 \_ DISCRETETRANSFER \_ prop \_ Blue \_ Disable</span><span class="sxs-lookup"><span data-stu-id="76c0d-160">D2D1\_DISCRETETRANSFER\_PROP\_BLUE\_DISABLE</span></span><br/>   | <span data-ttu-id="76c0d-161">BOOL</span><span class="sxs-lookup"><span data-stu-id="76c0d-161">BOOL</span></span><br/> <span data-ttu-id="76c0d-162">FALSE</span><span class="sxs-lookup"><span data-stu-id="76c0d-162">FALSE</span></span><br/>             | <span data-ttu-id="76c0d-163">Se si imposta questo valore su TRUE, l'effetto non applica la funzione di trasferimento al canale blu.</span><span class="sxs-lookup"><span data-stu-id="76c0d-163">If you set this to TRUE the effect does not apply the transfer function to the Blue channel.</span></span> <span data-ttu-id="76c0d-164">Se si imposta questa opzione su FALSE, l'effetto applica la funzione BlueDiscreteTransfer al canale blu.</span><span class="sxs-lookup"><span data-stu-id="76c0d-164">If you set this to FALSE the effect applies the BlueDiscreteTransfer function to the Blue channel.</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="76c0d-165">AlphaTable</span><span class="sxs-lookup"><span data-stu-id="76c0d-165">AlphaTable</span></span><br/> <span data-ttu-id="76c0d-166">\_Tabella d2d1 DISCRETETRANSFER \_ prop \_ Alpha \_</span><span class="sxs-lookup"><span data-stu-id="76c0d-166">D2D1\_DISCRETETRANSFER\_PROP\_ALPHA\_TABLE</span></span><br/>     | <span data-ttu-id="76c0d-167">FLOAT\[\]</span><span class="sxs-lookup"><span data-stu-id="76c0d-167">FLOAT\[\]</span></span><br/> <span data-ttu-id="76c0d-168">{0,0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="76c0d-168">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="76c0d-169">Elenco di valori che definiscono la funzione di trasferimento per il canale alfa.</span><span class="sxs-lookup"><span data-stu-id="76c0d-169">The list of values that define the transfer function for the Alpha channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="76c0d-170">AlphaDisable</span><span class="sxs-lookup"><span data-stu-id="76c0d-170">AlphaDisable</span></span><br/> <span data-ttu-id="76c0d-171">D2D1 \_ DISCRETETRANSFER \_ prop \_ Alpha \_ Disable</span><span class="sxs-lookup"><span data-stu-id="76c0d-171">D2D1\_DISCRETETRANSFER\_PROP\_ALPHA\_DISABLE</span></span><br/> | <span data-ttu-id="76c0d-172">BOOL</span><span class="sxs-lookup"><span data-stu-id="76c0d-172">BOOL</span></span><br/> <span data-ttu-id="76c0d-173">FALSE</span><span class="sxs-lookup"><span data-stu-id="76c0d-173">FALSE</span></span><br/>             | <span data-ttu-id="76c0d-174">Se si imposta questo valore su TRUE, l'effetto non applica la funzione di trasferimento al canale alfa.</span><span class="sxs-lookup"><span data-stu-id="76c0d-174">If you set this to TRUE the effect does not apply the transfer function to the Alpha channel.</span></span> <span data-ttu-id="76c0d-175">Se si imposta questa opzione su FALSE, l'effetto applica la funzione AlphaDiscreteTransfer al canale alfa.</span><span class="sxs-lookup"><span data-stu-id="76c0d-175">If you set this to FALSE the effect applies the AlphaDiscreteTransfer function to the Alpha channel.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="76c0d-176">ClampOutput</span><span class="sxs-lookup"><span data-stu-id="76c0d-176">ClampOutput</span></span><br/> <span data-ttu-id="76c0d-177">D2D1 \_ DISCRETETRANSFER \_ prop \_ \_ output Clamp</span><span class="sxs-lookup"><span data-stu-id="76c0d-177">D2D1\_DISCRETETRANSFER\_PROP\_CLAMP\_OUTPUT</span></span><br/>   | <span data-ttu-id="76c0d-178">BOOL</span><span class="sxs-lookup"><span data-stu-id="76c0d-178">BOOL</span></span><br/> <span data-ttu-id="76c0d-179">FALSE</span><span class="sxs-lookup"><span data-stu-id="76c0d-179">FALSE</span></span><br/>             | <span data-ttu-id="76c0d-180">Indica se l'effetto fissa i valori dei colori a un valore compreso tra 0 e 1 prima che l'effetto passi i valori all'effetto successivo nel grafico.</span><span class="sxs-lookup"><span data-stu-id="76c0d-180">Whether the effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph.</span></span> <span data-ttu-id="76c0d-181">L'effetto blocca i valori prima di premoltiplicare l'alfa.</span><span class="sxs-lookup"><span data-stu-id="76c0d-181">The effect clamps the values before it premultiplies the alpha.</span></span><br/> <span data-ttu-id="76c0d-182">Se si imposta questa impostazione su TRUE, i valori vengono bloccati dall'effetto.</span><span class="sxs-lookup"><span data-stu-id="76c0d-182">If you set this to TRUE the effect will clamp the values.</span></span> <span data-ttu-id="76c0d-183">Se si imposta questa proprietà su FALSE, l'effetto non blocca i valori dei colori, mentre altri effetti e la superficie di output possono bloccare i valori se non hanno una precisione sufficientemente elevata.</span><span class="sxs-lookup"><span data-stu-id="76c0d-183">If you set this to FALSE, the effect will not clamp the color values, but other effects and the output surface may clamp the values if they are not of high enough precision.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="76c0d-184">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76c0d-184">Requirements</span></span>



| <span data-ttu-id="76c0d-185">Requisito</span><span class="sxs-lookup"><span data-stu-id="76c0d-185">Requirement</span></span> | <span data-ttu-id="76c0d-186">Valore</span><span class="sxs-lookup"><span data-stu-id="76c0d-186">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="76c0d-187">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76c0d-187">Minimum supported client</span></span> | <span data-ttu-id="76c0d-188">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="76c0d-188">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="76c0d-189">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76c0d-189">Minimum supported server</span></span> | <span data-ttu-id="76c0d-190">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="76c0d-190">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="76c0d-191">Intestazione</span><span class="sxs-lookup"><span data-stu-id="76c0d-191">Header</span></span>                   | <span data-ttu-id="76c0d-192">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="76c0d-192">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="76c0d-193">Libreria</span><span class="sxs-lookup"><span data-stu-id="76c0d-193">Library</span></span>                  | <span data-ttu-id="76c0d-194">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="76c0d-194">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="76c0d-195">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="76c0d-195">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76c0d-196">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="76c0d-196">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

