---
title: Effetto trasferimento tabella
description: Utilizzare l'effetto di trasferimento tabella per eseguire il mapping delle intensità di colore di un'immagine utilizzando una funzione di trasferimento creata dall'interpolazione di un elenco di valori forniti.
ms.assetid: FB426909-3C91-4709-9E3A-E45C7AE345A3
keywords:
- effetto trasferimento tabella
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d590e7f232ac3d4cecd434786353dfc5b8ea80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476751"
---
# <a name="table-transfer-effect"></a><span data-ttu-id="10cd6-104">Effetto trasferimento tabella</span><span class="sxs-lookup"><span data-stu-id="10cd6-104">Table transfer effect</span></span>

<span data-ttu-id="10cd6-105">Utilizzare l'effetto di trasferimento tabella per eseguire il mapping delle intensità di colore di un'immagine utilizzando una funzione di trasferimento creata dall'interpolazione di un elenco di valori forniti.</span><span class="sxs-lookup"><span data-stu-id="10cd6-105">Use the table transfer effect to map the color intensities of an image using a transfer function created from interpolating a list of values you provide.</span></span>

<span data-ttu-id="10cd6-106">Il CLSID per questo effetto è CLSID \_ D2D1TableTransfer.</span><span class="sxs-lookup"><span data-stu-id="10cd6-106">The CLSID for this effect is CLSID\_D2D1TableTransfer.</span></span>

-   [<span data-ttu-id="10cd6-107">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="10cd6-107">Example image</span></span>](#example-image)
-   [<span data-ttu-id="10cd6-108">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="10cd6-108">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="10cd6-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="10cd6-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="10cd6-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="10cd6-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="10cd6-111">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="10cd6-111">Example image</span></span>

<span data-ttu-id="10cd6-112">L'immagine mostra l'input e l'output dell'effetto di trasferimento tabella.</span><span class="sxs-lookup"><span data-stu-id="10cd6-112">The image here shows the input and output of the table transfer effect.</span></span>



| <span data-ttu-id="10cd6-113">Prima</span><span class="sxs-lookup"><span data-stu-id="10cd6-113">Before</span></span>                                                         |
|----------------------------------------------------------------|
| ![immagine prima dell'effetto.](images/default-before.jpg)     |
| <span data-ttu-id="10cd6-115">After</span><span class="sxs-lookup"><span data-stu-id="10cd6-115">After</span></span>                                                          |
| ![immagine dopo la trasformazione.](images/11-tabletransfer.png) |



 


```C++
ComPtr<ID2D1Effect> tableTransferEffect;
m_d2dContext->CreateEffect(CLSID_D2D1TableTransfer, &tableTransferEffect);

tableTransferEffect->SetInput(0, bitmap);

float table[2] = {0.75f, 1.0f};
tableTransferEffect->SetValue(D2D1_TABLETRANSFER_PROP_BLUE_TABLE, table);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(tableTransferEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="10cd6-117">La funzione di trasferimento si basa su un elenco di input V = (V0, V1, V2, V3, V?</span><span class="sxs-lookup"><span data-stu-id="10cd6-117">The transfer function is based on a list of inputs V=(V0,V1,V2,V3, V?</span></span> <span data-ttu-id="10cd6-118">, V<sub>n</sub>), dove N è il numero di elementi-1.</span><span class="sxs-lookup"><span data-stu-id="10cd6-118">,V<sub>N</sub>) where N is the number of elements - 1.</span></span>

<span data-ttu-id="10cd6-119">L'intensità dei pixel di input viene rappresentata come C. L'intensità del pixel di output, C può essere calcolata con l'equazione.</span><span class="sxs-lookup"><span data-stu-id="10cd6-119">The input pixel intensity is represented as C. The output pixel intensity, C  can be calculated with the equation.</span></span>

<span data-ttu-id="10cd6-120">Per un valore C, scegliere un valore k, in modo che: k/N = C < (k + 1)/N</span><span class="sxs-lookup"><span data-stu-id="10cd6-120">For a value C, pick a value k, such that: k/N = C < (k+1)/N</span></span>

<span data-ttu-id="10cd6-121">L'output C viene calcolato utilizzando l'equazione seguente: C'= V?</span><span class="sxs-lookup"><span data-stu-id="10cd6-121">The output C  is calculated using the following equation: C' = V?</span></span> <span data-ttu-id="10cd6-122">+ (C-k/N) \* n \* (V??? 1?</span><span class="sxs-lookup"><span data-stu-id="10cd6-122">+ (C -  k/N) \* N \* (V???1?</span></span> <span data-ttu-id="10cd6-123">-V?</span><span class="sxs-lookup"><span data-stu-id="10cd6-123">- V?)</span></span>

<span data-ttu-id="10cd6-124">Questo effetto funziona su immagini alfa diritte e premoltiplicate.</span><span class="sxs-lookup"><span data-stu-id="10cd6-124">This effect works on straight and premultiplied alpha images.</span></span> <span data-ttu-id="10cd6-125">L'effetto restituisce bitmap alfa premoltiplicate.</span><span class="sxs-lookup"><span data-stu-id="10cd6-125">The effect outputs premultiplied alpha bitmaps.</span></span>

<span data-ttu-id="10cd6-126">Di seguito è riportato il grafico della funzione di trasferimento della tabella se la proprietà Table è impostata su `[0.0, 0.25, 1.0]` .</span><span class="sxs-lookup"><span data-stu-id="10cd6-126">Here is what the graph of table transfer function looks like if the table property is set to `[0.0, 0.25, 1.0]`.</span></span>

![grafico dell'intensità dei pixel per la funzione di trasferimento della tabella.](images/table-transfer-graph.png)

## <a name="effect-properties"></a><span data-ttu-id="10cd6-128">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="10cd6-128">Effect properties</span></span>

> [!Note]  
> <span data-ttu-id="10cd6-129">I valori di tutti i canali delle proprietà di trasferimento della tabella sono privi di unità e hanno un minimo di 0,0 e un massimo di 1,0.</span><span class="sxs-lookup"><span data-stu-id="10cd6-129">The values of all channels of the table transfer properties are unitless and have a minimum of 0.0 and a maximum 1.0.</span></span>

 



| <span data-ttu-id="10cd6-130">Nome visualizzato e enumerazione dell'indice</span><span class="sxs-lookup"><span data-stu-id="10cd6-130">Display name and index enumeration</span></span>                                           | <span data-ttu-id="10cd6-131">Tipo e valore predefinito</span><span class="sxs-lookup"><span data-stu-id="10cd6-131">Type and default value</span></span>                       | <span data-ttu-id="10cd6-132">Descrizione</span><span class="sxs-lookup"><span data-stu-id="10cd6-132">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10cd6-133">RedTable</span><span class="sxs-lookup"><span data-stu-id="10cd6-133">RedTable</span></span><br/> <span data-ttu-id="10cd6-134">D2D1 \_ TABLETRANSFER \_ - \_ \_ tabella rossa</span><span class="sxs-lookup"><span data-stu-id="10cd6-134">D2D1\_TABLETRANSFER\_PROP\_RED\_TABLE</span></span><br/>         | <span data-ttu-id="10cd6-135">FLOAT\[\]</span><span class="sxs-lookup"><span data-stu-id="10cd6-135">FLOAT\[\]</span></span><br/> <span data-ttu-id="10cd6-136">{0,0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="10cd6-136">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="10cd6-137">Elenco di valori utilizzati per definire la funzione di trasferimento per il canale rosso.</span><span class="sxs-lookup"><span data-stu-id="10cd6-137">The list of values used to define the transfer function for the Red channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="10cd6-138">RedDisable</span><span class="sxs-lookup"><span data-stu-id="10cd6-138">RedDisable</span></span><br/> <span data-ttu-id="10cd6-139">D2D1 \_ TABLETRANSFER \_ prop \_ Red \_ Disable</span><span class="sxs-lookup"><span data-stu-id="10cd6-139">D2D1\_TABLETRANSFER\_PROP\_RED\_DISABLE</span></span><br/>     | <span data-ttu-id="10cd6-140">BOOL</span><span class="sxs-lookup"><span data-stu-id="10cd6-140">BOOL</span></span><br/> <span data-ttu-id="10cd6-141">FALSE</span><span class="sxs-lookup"><span data-stu-id="10cd6-141">FALSE</span></span><br/>             | <span data-ttu-id="10cd6-142">Se si imposta questo valore su TRUE, l'effetto non applica la funzione di trasferimento al canale rosso.</span><span class="sxs-lookup"><span data-stu-id="10cd6-142">If you set this to TRUE the effect does not apply the transfer function to the Red channel.</span></span> <span data-ttu-id="10cd6-143">Se si imposta questa opzione su FALSE, viene applicata la funzione RedTableTransfer al canale rosso.</span><span class="sxs-lookup"><span data-stu-id="10cd6-143">If you set this to FALSE it applies the RedTableTransfer function to the Red channel.</span></span>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="10cd6-144">GreenTable</span><span class="sxs-lookup"><span data-stu-id="10cd6-144">GreenTable</span></span><br/> <span data-ttu-id="10cd6-145">\_ \_ \_ Tabella verde prop d2d1 \_ TABLETRANSFER</span><span class="sxs-lookup"><span data-stu-id="10cd6-145">D2D1\_TABLETRANSFER\_PROP\_GREEN\_TABLE</span></span><br/>     | <span data-ttu-id="10cd6-146">FLOAT\[\]</span><span class="sxs-lookup"><span data-stu-id="10cd6-146">FLOAT\[\]</span></span><br/> <span data-ttu-id="10cd6-147">{0,0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="10cd6-147">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="10cd6-148">Elenco di valori utilizzati per definire la funzione di trasferimento per il canale verde.</span><span class="sxs-lookup"><span data-stu-id="10cd6-148">The list of values used to define the transfer function for the Green channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="10cd6-149">GreenDisable</span><span class="sxs-lookup"><span data-stu-id="10cd6-149">GreenDisable</span></span><br/> <span data-ttu-id="10cd6-150">D2D1 \_ TABLETRANSFER \_ prop \_ Green \_ Disable</span><span class="sxs-lookup"><span data-stu-id="10cd6-150">D2D1\_TABLETRANSFER\_PROP\_GREEN\_DISABLE</span></span><br/> | <span data-ttu-id="10cd6-151">BOOL</span><span class="sxs-lookup"><span data-stu-id="10cd6-151">BOOL</span></span><br/> <span data-ttu-id="10cd6-152">FALSE</span><span class="sxs-lookup"><span data-stu-id="10cd6-152">FALSE</span></span><br/>             | <span data-ttu-id="10cd6-153">Se si imposta questo valore su TRUE, l'effetto non applica la funzione di trasferimento al canale verde.</span><span class="sxs-lookup"><span data-stu-id="10cd6-153">If you set this to TRUE the effect does not apply the transfer function to the Green channel.</span></span> <span data-ttu-id="10cd6-154">Se si imposta questa opzione su FALSE, viene applicata la funzione GreenTableTransfer al canale verde.</span><span class="sxs-lookup"><span data-stu-id="10cd6-154">If you set this to FALSE it applies the GreenTableTransfer function to the Green channel.</span></span>                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="10cd6-155">BlueTable</span><span class="sxs-lookup"><span data-stu-id="10cd6-155">BlueTable</span></span><br/> <span data-ttu-id="10cd6-156">D2D1 \_ TABLETRANSFER \_ - \_ tabella blu Prop \_</span><span class="sxs-lookup"><span data-stu-id="10cd6-156">D2D1\_TABLETRANSFER\_PROP\_BLUE\_TABLE</span></span><br/>       | <span data-ttu-id="10cd6-157">FLOAT\[\]</span><span class="sxs-lookup"><span data-stu-id="10cd6-157">FLOAT\[\]</span></span><br/> <span data-ttu-id="10cd6-158">{0,0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="10cd6-158">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="10cd6-159">Elenco di valori utilizzati per definire la funzione di trasferimento per il canale blu.</span><span class="sxs-lookup"><span data-stu-id="10cd6-159">The list of values used to define the transfer function for the Blue channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="10cd6-160">BlueDisable</span><span class="sxs-lookup"><span data-stu-id="10cd6-160">BlueDisable</span></span><br/> <span data-ttu-id="10cd6-161">D2D1 \_ TABLETRANSFER \_ prop \_ Blue \_ Disable</span><span class="sxs-lookup"><span data-stu-id="10cd6-161">D2D1\_TABLETRANSFER\_PROP\_BLUE\_DISABLE</span></span><br/>   | <span data-ttu-id="10cd6-162">BOOL</span><span class="sxs-lookup"><span data-stu-id="10cd6-162">BOOL</span></span><br/> <span data-ttu-id="10cd6-163">FALSE</span><span class="sxs-lookup"><span data-stu-id="10cd6-163">FALSE</span></span><br/>             | <span data-ttu-id="10cd6-164">Se si imposta questo valore su TRUE, l'effetto non applica la funzione di trasferimento al canale blu.</span><span class="sxs-lookup"><span data-stu-id="10cd6-164">If you set this to TRUE the effect does not apply the transfer function to the Blue channel.</span></span> <span data-ttu-id="10cd6-165">Se si imposta questa opzione su FALSE, viene applicata la funzione BlueTableTransfer al canale blu.</span><span class="sxs-lookup"><span data-stu-id="10cd6-165">If you set this to FALSE it applies the BlueTableTransfer function to the Blue channel.</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="10cd6-166">AlphaTable</span><span class="sxs-lookup"><span data-stu-id="10cd6-166">AlphaTable</span></span><br/> <span data-ttu-id="10cd6-167">Tabella D2D1 per il \_ trasferimento della tabella \_ \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="10cd6-167">D2D1\_TABLE\_TRANSFER\_PROP\_ALPHA\_TABLE</span></span><br/>   | <span data-ttu-id="10cd6-168">FLOAT\[\]</span><span class="sxs-lookup"><span data-stu-id="10cd6-168">FLOAT\[\]</span></span><br/> <span data-ttu-id="10cd6-169">{0,0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="10cd6-169">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="10cd6-170">Elenco di valori utilizzati per definire la funzione di trasferimento per il canale alfa.</span><span class="sxs-lookup"><span data-stu-id="10cd6-170">The list of values used to define the transfer function for the Alpha channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="10cd6-171">AlphaDisable</span><span class="sxs-lookup"><span data-stu-id="10cd6-171">AlphaDisable</span></span><br/> <span data-ttu-id="10cd6-172">D2D1 \_ TABLETRANSFER \_ prop \_ Alpha \_ Disable</span><span class="sxs-lookup"><span data-stu-id="10cd6-172">D2D1\_TABLETRANSFER\_PROP\_ALPHA\_DISABLE</span></span><br/> | <span data-ttu-id="10cd6-173">BOOL</span><span class="sxs-lookup"><span data-stu-id="10cd6-173">BOOL</span></span><br/> <span data-ttu-id="10cd6-174">FALSE</span><span class="sxs-lookup"><span data-stu-id="10cd6-174">FALSE</span></span><br/>             | <span data-ttu-id="10cd6-175">Se si imposta questo valore su TRUE, l'effetto non applica la funzione di trasferimento al canale alfa.</span><span class="sxs-lookup"><span data-stu-id="10cd6-175">If you set this to TRUE the effect does not apply the transfer function to the Alpha channel.</span></span> <span data-ttu-id="10cd6-176">Se si imposta questa opzione su FALSE, viene applicata la funzione AlphaTableTransfer al canale alfa.</span><span class="sxs-lookup"><span data-stu-id="10cd6-176">If you set this to FALSE it applies the AlphaTableTransfer function to the Alpha channel.</span></span>                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="10cd6-177">ClampOutput</span><span class="sxs-lookup"><span data-stu-id="10cd6-177">ClampOutput</span></span><br/> <span data-ttu-id="10cd6-178">D2D1 \_ TABLETRANSFER \_ prop \_ \_ output Clamp</span><span class="sxs-lookup"><span data-stu-id="10cd6-178">D2D1\_TABLETRANSFER\_PROP\_CLAMP\_OUTPUT</span></span><br/>   | <span data-ttu-id="10cd6-179">BOOL</span><span class="sxs-lookup"><span data-stu-id="10cd6-179">BOOL</span></span><br/> <span data-ttu-id="10cd6-180">FALSE</span><span class="sxs-lookup"><span data-stu-id="10cd6-180">FALSE</span></span><br/>             | <span data-ttu-id="10cd6-181">Indica se l'effetto fissa i valori dei colori a un valore compreso tra 0 e 1 prima che l'effetto passi i valori all'effetto successivo nel grafico.</span><span class="sxs-lookup"><span data-stu-id="10cd6-181">Whether the effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph.</span></span> <span data-ttu-id="10cd6-182">L'effetto blocca i valori prima di premoltiplicare l'alfa.</span><span class="sxs-lookup"><span data-stu-id="10cd6-182">The effect clamps the values before it premultiplies the alpha .</span></span><br/> <span data-ttu-id="10cd6-183">Se si imposta questa impostazione su TRUE, i valori vengono bloccati dall'effetto.</span><span class="sxs-lookup"><span data-stu-id="10cd6-183">If you set this to TRUE the effect will clamp the values.</span></span> <span data-ttu-id="10cd6-184">Se si imposta questa proprietà su FALSE, l'effetto non blocca i valori dei colori, mentre altri effetti e la superficie di output possono bloccare i valori se non hanno una precisione sufficientemente elevata.</span><span class="sxs-lookup"><span data-stu-id="10cd6-184">If you set this to FALSE, the effect will not clamp the color values, but other effects and the output surface may clamp the values if they are not of high enough precision.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="10cd6-185">Requisiti</span><span class="sxs-lookup"><span data-stu-id="10cd6-185">Requirements</span></span>



| <span data-ttu-id="10cd6-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="10cd6-186">Requirement</span></span> | <span data-ttu-id="10cd6-187">Valore</span><span class="sxs-lookup"><span data-stu-id="10cd6-187">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="10cd6-188">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="10cd6-188">Minimum supported client</span></span> | <span data-ttu-id="10cd6-189">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="10cd6-189">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="10cd6-190">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="10cd6-190">Minimum supported server</span></span> | <span data-ttu-id="10cd6-191">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="10cd6-191">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="10cd6-192">Intestazione</span><span class="sxs-lookup"><span data-stu-id="10cd6-192">Header</span></span>                   | <span data-ttu-id="10cd6-193">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="10cd6-193">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="10cd6-194">Libreria</span><span class="sxs-lookup"><span data-stu-id="10cd6-194">Library</span></span>                  | <span data-ttu-id="10cd6-195">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="10cd6-195">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="10cd6-196">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="10cd6-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10cd6-197">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="10cd6-197">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

