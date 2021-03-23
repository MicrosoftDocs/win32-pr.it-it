---
title: Sottorisorse (grafica Direct3D 12)
description: Viene descritto come una risorsa è divisa in sottorisorse e viene illustrato come fare riferimento a una singola, più o più sezioni di sottorisorse.
ms.assetid: C4F92F8A-DBF0-412B-8707-CC4C1BF2D88F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e8fa8ea0d48fea7ee8e192d9dcf1fe5e3d22423
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104548840"
---
# <a name="subresources-direct3d-12-graphics"></a><span data-ttu-id="84364-103">Sottorisorse (grafica Direct3D 12)</span><span class="sxs-lookup"><span data-stu-id="84364-103">Subresources (Direct3D 12 Graphics)</span></span>

<span data-ttu-id="84364-104">Viene descritto come una risorsa è divisa in sottorisorse e viene illustrato come fare riferimento a una singola, più o più sezioni di sottorisorse.</span><span class="sxs-lookup"><span data-stu-id="84364-104">Describes how a resource is divided into subresources, and how to reference a single, multiple or slice of subresources.</span></span>

-   [<span data-ttu-id="84364-105">Sottorisorse di esempio</span><span class="sxs-lookup"><span data-stu-id="84364-105">Example subresources</span></span>](#example-subresources)
    -   [<span data-ttu-id="84364-106">Indicizzazione delle risorse</span><span class="sxs-lookup"><span data-stu-id="84364-106">Subresource indexing</span></span>](#subresource-indexing)
    -   [<span data-ttu-id="84364-107">Sezione MIP</span><span class="sxs-lookup"><span data-stu-id="84364-107">Mip slice</span></span>](#mip-slice)
    -   [<span data-ttu-id="84364-108">Sezione matrice</span><span class="sxs-lookup"><span data-stu-id="84364-108">Array slice</span></span>](#array-slice)
    -   [<span data-ttu-id="84364-109">Sezione piano</span><span class="sxs-lookup"><span data-stu-id="84364-109">Plane slice</span></span>](#plane-slice)
    -   [<span data-ttu-id="84364-110">Più sottorisorse</span><span class="sxs-lookup"><span data-stu-id="84364-110">Multiple subresources</span></span>](#multiple-subresources)
-   [<span data-ttu-id="84364-111">API subresource</span><span class="sxs-lookup"><span data-stu-id="84364-111">Subresource APIs</span></span>](#subresource-apis)
-   [<span data-ttu-id="84364-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="84364-112">Related topics</span></span>](#related-topics)

## <a name="example-subresources"></a><span data-ttu-id="84364-113">Sottorisorse di esempio</span><span class="sxs-lookup"><span data-stu-id="84364-113">Example subresources</span></span>

<span data-ttu-id="84364-114">Se una risorsa contiene un buffer, contiene semplicemente una sottorisorsa con un indice pari a 0.</span><span class="sxs-lookup"><span data-stu-id="84364-114">If a resource contains a buffer, then it simply contains one subresource with an index of 0.</span></span> <span data-ttu-id="84364-115">Se la risorsa contiene una trama (o una matrice di trame), fare riferimento alle sottorisorse è più complessa.</span><span class="sxs-lookup"><span data-stu-id="84364-115">If the resource contains a texture (or texture array), then referencing the subresources is more complex.</span></span>

<span data-ttu-id="84364-116">Alcune API accedono a un'intera risorsa, ad esempio il metodo [**ID3D12GraphicsCommandList:: CopyResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource) , mentre altre accedono a una parte di una risorsa, ad esempio il metodo [**ID3D12Resource:: ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) .</span><span class="sxs-lookup"><span data-stu-id="84364-116">Some APIs access an entire resource (such as the [**ID3D12GraphicsCommandList::CopyResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource) method), others access a portion of a resource (for example the [**ID3D12Resource::ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) method).</span></span> <span data-ttu-id="84364-117">I metodi che accedono a una parte di una risorsa utilizzano in genere una descrizione della vista, ad esempio la struttura [**D3D12 \_ TEX2D \_ array \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv) , per specificare le sottorisorse a cui accedere.</span><span class="sxs-lookup"><span data-stu-id="84364-117">The methods that access a portion of a resource generally use a view description (such as the [**D3D12\_TEX2D\_ARRAY\_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv) structure) to specify the subresources to access.</span></span> <span data-ttu-id="84364-118">Per un elenco completo, vedere la sezione [API della sottorisorsa](#subresource-apis) .</span><span class="sxs-lookup"><span data-stu-id="84364-118">Refer to the [Subresource APIs](#subresource-apis) section for a complete list.</span></span>

### <a name="subresource-indexing"></a><span data-ttu-id="84364-119">Indicizzazione delle risorse</span><span class="sxs-lookup"><span data-stu-id="84364-119">Subresource indexing</span></span>

<span data-ttu-id="84364-120">Per indicizzare una determinata sottorisorsa, i livelli MIP vengono indicizzati per primi quando ogni voce della matrice viene indicizzata.</span><span class="sxs-lookup"><span data-stu-id="84364-120">To index a particular subresource, the mip levels are indexed first as each array entry is indexed.</span></span>

![indicizzazione delle risorse](images/subresource-index.png)

### <a name="mip-slice"></a><span data-ttu-id="84364-122">Sezione MIP</span><span class="sxs-lookup"><span data-stu-id="84364-122">Mip slice</span></span>

<span data-ttu-id="84364-123">Una sezione MIP include un livello mipmap per ogni trama in una matrice, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="84364-123">A mip slice includes one mipmap level for every texture in an array, as shown in the following image.</span></span>

![sezioni della sottorisorsa MIP](images/subresource-mip-slice.png)

### <a name="array-slice"></a><span data-ttu-id="84364-125">Sezione matrice</span><span class="sxs-lookup"><span data-stu-id="84364-125">Array slice</span></span>

<span data-ttu-id="84364-126">Data una matrice di trame, ogni trama con mipmap, una sezione della matrice include una trama e tutti i livelli MIP, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="84364-126">Given an array of textures, each texture with mipmaps, an array slice includes one texture and all of its mip levels, as shown in the following image.</span></span>

![sezioni della matrice della sottorisorsa](images/subresource-array-slices.png)

### <a name="plane-slice"></a><span data-ttu-id="84364-128">Sezione piano</span><span class="sxs-lookup"><span data-stu-id="84364-128">Plane slice</span></span>

<span data-ttu-id="84364-129">In genere i formati planari non vengono usati per archiviare i dati di RGBA, ma nei casi in cui sono (probabilmente 24bpp dati RGB), un piano può rappresentare l'immagine rossa, una verde e un'immagine blu.</span><span class="sxs-lookup"><span data-stu-id="84364-129">Typically planar formats are not used to store RGBA data, but in the cases where it is (perhaps 24bpp RGB data), one plane could represent the red image, one the green, and one the blue image.</span></span> <span data-ttu-id="84364-130">Un piano, tuttavia, non è necessariamente un colore, due o più colori possono essere combinati in un piano.</span><span class="sxs-lookup"><span data-stu-id="84364-130">One plane though is not necessarily one color, two or more colors could be combined into one plane.</span></span> <span data-ttu-id="84364-131">Per i dati YCbCr e Depth-Stencil sottocampionati viene usato più di solito dati planari.</span><span class="sxs-lookup"><span data-stu-id="84364-131">More typically planar data is used for sub-sampled YCbCr and Depth-Stencil data.</span></span> <span data-ttu-id="84364-132">Depth-Stencil è l'unico formato che supporta completamente mipmap, matrici e più piani (spesso il piano 0 per la profondità e il piano 1 per stencil).</span><span class="sxs-lookup"><span data-stu-id="84364-132">Depth-Stencil is the only format that fully supports mipmaps, arrays, and multiple planes (often plane 0 for Depth and plane 1 for Stencil).</span></span>

<span data-ttu-id="84364-133">L'indicizzazione delle sottorisorse per una matrice di due immagini Depth-Stencil, ognuna con tre livelli MIP, è illustrata di seguito.</span><span class="sxs-lookup"><span data-stu-id="84364-133">The subresource indexing for an array of two Depth-Stencil images, each with three mip levels, is shown below.</span></span>

![indicizzazione depth stencil](images/depth-stencil-indexing.png)

<span data-ttu-id="84364-135">YCbCr sottocampionato supporta matrici con piani, ma non supporta mipmap.</span><span class="sxs-lookup"><span data-stu-id="84364-135">Sub-sampled YCbCr supports arrays and has planes, but does not support mipmaps.</span></span> <span data-ttu-id="84364-136">Le immagini YCbCr hanno due piani, uno per la luminanza (Y) a cui l'occhio umano è più sensibile e uno per cromatura (CB e CR, con interfoliazione) a cui l'occhio umano è meno sensibile.</span><span class="sxs-lookup"><span data-stu-id="84364-136">YCbCr images have two planes, one for the luminance (Y) that the human eye is most sensitive to, and one for the chrominance (both Cb, and Cr, interleaved) which the human eye is less sensitive to.</span></span> <span data-ttu-id="84364-137">Questo formato consente la compressione dei valori cromatura per comprimere un'immagine senza influire sulla luminanza ed è un formato di compressione video comune per tale motivo, sebbene venga usato per comprimere le immagini ancora.</span><span class="sxs-lookup"><span data-stu-id="84364-137">This format enables compression of the chrominance values in order to compress an image without affecting the luminance, and is a common video compression format for that reason, although it is used to compress still images.</span></span> <span data-ttu-id="84364-138">L'immagine seguente mostra il formato NV12, annotando che cromatura è stato compresso in un trimestre della risoluzione della luminanza, vale a dire che la larghezza di ogni piano è identica e il piano cromatura è metà dell'altezza del piano di luminanza.</span><span class="sxs-lookup"><span data-stu-id="84364-138">The image below shows the NV12 format, noting the chrominance has been compressed to one quarter of the resolution of the luminance, meaning the width of each plane is identical, and the chrominance plane is half the height of the luminance plane.</span></span> <span data-ttu-id="84364-139">I piani verrebbero indicizzati come sottorisorse in modo identico al Depth-Stencil esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="84364-139">The planes would be indexed as subresources in an identical way to the Depth-Stencil example above.</span></span>

![formato NV12](images/ycbcr.png)

<span data-ttu-id="84364-141">In Direct3D 11 sono presenti formati planari, ma non è stato possibile risolvere i singoli piani singolarmente, ad esempio per le operazioni di copia o mapping.</span><span class="sxs-lookup"><span data-stu-id="84364-141">Planar formats existed in Direct3D 11, but individual planes could not be addressed individually, say for copy or mapping operations.</span></span> <span data-ttu-id="84364-142">Questa operazione è stata modificata in Direct3D 12 in modo che ogni piano abbia ricevuto il proprio ID di sottorisorsa.</span><span class="sxs-lookup"><span data-stu-id="84364-142">This was changed in Direct3D 12 so that each plane received its own subresource ID.</span></span> <span data-ttu-id="84364-143">Confrontare i due metodi seguenti per calcolare l'ID della sottorisorsa.</span><span class="sxs-lookup"><span data-stu-id="84364-143">Compare the following two methods for calculating the subresource ID.</span></span>

<span data-ttu-id="84364-144">Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="84364-144">Direct3D 11</span></span>

``` syntax
inline UINT D3D11CalcSubresource( UINT MipSlice, UINT ArraySlice, UINT MipLevels )
{
    return MipSlice + (ArraySlice * MipLevels); 
}
```

<span data-ttu-id="84364-145">Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="84364-145">Direct3D 12</span></span>

``` syntax
inline UINT D3D12CalcSubresource( UINT MipSlice, UINT ArraySlice, UINT PlaneSlice, UINT MipLevels, UINT ArraySize )
{ 
    return MipSlice + (ArraySlice * MipLevels) + (PlaneSlice * MipLevels * ArraySize); 
}
```

<span data-ttu-id="84364-146">La maggior parte dell'hardware presuppone che la memoria per il piano N venga sempre allocata immediatamente dopo il piano N-1.</span><span class="sxs-lookup"><span data-stu-id="84364-146">Most hardware assumes that the memory for plane N is always immediately allocated after plane N-1.</span></span>

<span data-ttu-id="84364-147">Un'alternativa all'uso delle sottorisorse è che un'app potrebbe allocare una risorsa completamente separata per ogni piano.</span><span class="sxs-lookup"><span data-stu-id="84364-147">An alternative to using subresources is that an app could allocate a completely separate resource per plane.</span></span> <span data-ttu-id="84364-148">In questo caso, l'applicazione riconosce che i dati sono planari e usa più risorse per rappresentarlo.</span><span class="sxs-lookup"><span data-stu-id="84364-148">In this case, the application understands the data is planar and uses multiple resources to represent it.</span></span>

### <a name="multiple-subresources"></a><span data-ttu-id="84364-149">Più sottorisorse</span><span class="sxs-lookup"><span data-stu-id="84364-149">Multiple subresources</span></span>

<span data-ttu-id="84364-150">Una visualizzazione risorse shader può selezionare qualsiasi area rettangolare di sottorisorse, usando una delle sezioni descritte in precedenza e l'uso oculato dei campi nelle strutture di visualizzazione (ad esempio, [**D3D12 \_ TEX2D \_ array \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)), come illustrato nell'immagine.</span><span class="sxs-lookup"><span data-stu-id="84364-150">A shader-resource view can select any rectangular region of subresources, using one of the slices described above and judicious use of fields in the view structures (such as [**D3D12\_TEX2D\_ARRAY\_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)), as shown in the image.</span></span>

![selezione di più sottorisorse](images/subresource-multiple.png)

<span data-ttu-id="84364-152">Una visualizzazione di destinazione di rendering può utilizzare una sola sezione subresource o MIP e non può includere sottorisorse da più di una sezione MIP.</span><span class="sxs-lookup"><span data-stu-id="84364-152">A render-target view can only use a single subresource or mip slice and cannot include subresources from more than one mip slice.</span></span> <span data-ttu-id="84364-153">Ovvero ogni trama in una visualizzazione di destinazione di rendering deve avere le stesse dimensioni.</span><span class="sxs-lookup"><span data-stu-id="84364-153">That is, every texture in a render-target view must be the same size.</span></span> <span data-ttu-id="84364-154">Una visualizzazione risorse shader può selezionare qualsiasi area rettangolare di sottorisorse, come illustrato nell'immagine.</span><span class="sxs-lookup"><span data-stu-id="84364-154">A shader-resource view can select any rectangular region of subresources, as shown in the image.</span></span>

## <a name="subresource-apis"></a><span data-ttu-id="84364-155">API subresource</span><span class="sxs-lookup"><span data-stu-id="84364-155">Subresource APIs</span></span>

<span data-ttu-id="84364-156">Le API seguenti fanno riferimento a e funzionano con le sottorisorse:</span><span class="sxs-lookup"><span data-stu-id="84364-156">The following APIs reference and work with subresources:</span></span>

<span data-ttu-id="84364-157">Enumerazioni:</span><span class="sxs-lookup"><span data-stu-id="84364-157">Enumerations:</span></span>

-   [<span data-ttu-id="84364-158">**\_Tipo di \_ Copia \_ trama D3D12**</span><span class="sxs-lookup"><span data-stu-id="84364-158">**D3D12\_TEXTURE\_COPY\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_copy_type)

<span data-ttu-id="84364-159">Le strutture seguenti contengono indici *PlaneSlice* , che contengono la maggior parte degli indici *MipSlice* .</span><span class="sxs-lookup"><span data-stu-id="84364-159">The following structures contain *PlaneSlice* indexes, most contain *MipSlice* indexes.</span></span>

-   [<span data-ttu-id="84364-160">**D3D12 \_ TEX2D \_ RTV**</span><span class="sxs-lookup"><span data-stu-id="84364-160">**D3D12\_TEX2D\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_rtv)
-   [<span data-ttu-id="84364-161">**D3D12 \_ TEX2D \_ array \_ RTV**</span><span class="sxs-lookup"><span data-stu-id="84364-161">**D3D12\_TEX2D\_ARRAY\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv)
-   [<span data-ttu-id="84364-162">**D3D12 \_ TEX2D \_ SRV**</span><span class="sxs-lookup"><span data-stu-id="84364-162">**D3D12\_TEX2D\_SRV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_srv)
-   [<span data-ttu-id="84364-163">**D3D12 \_ TEX2D \_ array \_ SRV**</span><span class="sxs-lookup"><span data-stu-id="84364-163">**D3D12\_TEX2D\_ARRAY\_SRV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)
-   [<span data-ttu-id="84364-164">**D3D12 \_ TEX2D \_ UAV**</span><span class="sxs-lookup"><span data-stu-id="84364-164">**D3D12\_TEX2D\_UAV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_uav)
-   [<span data-ttu-id="84364-165">**D3D12 \_ TEX2D \_ array \_ UAV**</span><span class="sxs-lookup"><span data-stu-id="84364-165">**D3D12\_TEX2D\_ARRAY\_UAV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav)

<span data-ttu-id="84364-166">Le strutture seguenti contengono indici *ArraySlice* , che contengono la maggior parte degli indici *MipSlice* .</span><span class="sxs-lookup"><span data-stu-id="84364-166">The following structures contain *ArraySlice* indexes, most contain *MipSlice* indexes.</span></span>

-   [<span data-ttu-id="84364-167">**Vista \_ \_ origine dati matrice TEX1D D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="84364-167">**D3D12\_TEX1D\_ARRAY\_DSV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_dsv)
-   [<span data-ttu-id="84364-168">**Vista \_ \_ origine dati matrice TEX2D D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="84364-168">**D3D12\_TEX2D\_ARRAY\_DSV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_dsv)
-   [<span data-ttu-id="84364-169">**Vista \_ \_ origine dati matrice TEX2DMS D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="84364-169">**D3D12\_TEX2DMS\_ARRAY\_DSV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_dsv)
-   [<span data-ttu-id="84364-170">**D3D12 \_ TEX1D \_ array \_ RTV**</span><span class="sxs-lookup"><span data-stu-id="84364-170">**D3D12\_TEX1D\_ARRAY\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_rtv)
-   [<span data-ttu-id="84364-171">**D3D12 \_ TEX2D \_ array \_ RTV**</span><span class="sxs-lookup"><span data-stu-id="84364-171">**D3D12\_TEX2D\_ARRAY\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv)
-   [<span data-ttu-id="84364-172">**D3D12 \_ TEX2DMS \_ array \_ RTV**</span><span class="sxs-lookup"><span data-stu-id="84364-172">**D3D12\_TEX2DMS\_ARRAY\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_rtv)
-   [<span data-ttu-id="84364-173">**D3D12 \_ TEX1D \_ array \_ SRV**</span><span class="sxs-lookup"><span data-stu-id="84364-173">**D3D12\_TEX1D\_ARRAY\_SRV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_srv)
-   [<span data-ttu-id="84364-174">**D3D12 \_ TEX2D \_ array \_ SRV**</span><span class="sxs-lookup"><span data-stu-id="84364-174">**D3D12\_TEX2D\_ARRAY\_SRV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)
-   [<span data-ttu-id="84364-175">**D3D12 \_ TEX2DMS \_ array \_ SRV**</span><span class="sxs-lookup"><span data-stu-id="84364-175">**D3D12\_TEX2DMS\_ARRAY\_SRV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_srv)
-   [<span data-ttu-id="84364-176">**D3D12 \_ TEX1D \_ array \_ UAV**</span><span class="sxs-lookup"><span data-stu-id="84364-176">**D3D12\_TEX1D\_ARRAY\_UAV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_uav)
-   [<span data-ttu-id="84364-177">**D3D12 \_ TEX2D \_ array \_ UAV**</span><span class="sxs-lookup"><span data-stu-id="84364-177">**D3D12\_TEX2D\_ARRAY\_UAV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav)

<span data-ttu-id="84364-178">Le strutture seguenti contengono indici *MipSlice* , ma non *ArraySlice* né *PlaneSlice* .</span><span class="sxs-lookup"><span data-stu-id="84364-178">The following structures contain *MipSlice* indexes, but neither *ArraySlice* nor *PlaneSlice* indexes.</span></span>

-   [<span data-ttu-id="84364-179">**Vista \_ origine dati TEX1D D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="84364-179">**D3D12\_TEX1D\_DSV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_dsv)
-   [<span data-ttu-id="84364-180">**Vista \_ origine dati TEX2D D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="84364-180">**D3D12\_TEX2D\_DSV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_dsv)
-   [<span data-ttu-id="84364-181">**D3D12 \_ TEX1D \_ RTV**</span><span class="sxs-lookup"><span data-stu-id="84364-181">**D3D12\_TEX1D\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_rtv)
-   [<span data-ttu-id="84364-182">**D3D12 \_ TEX3D \_ RTV**</span><span class="sxs-lookup"><span data-stu-id="84364-182">**D3D12\_TEX3D\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_rtv)
-   [<span data-ttu-id="84364-183">**D3D12 \_ TEX1D \_ UAV**</span><span class="sxs-lookup"><span data-stu-id="84364-183">**D3D12\_TEX1D\_UAV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_uav)
-   [<span data-ttu-id="84364-184">**D3D12 \_ TEX3D \_ UAV**</span><span class="sxs-lookup"><span data-stu-id="84364-184">**D3D12\_TEX3D\_UAV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_uav)

<span data-ttu-id="84364-185">Anche le strutture seguenti fanno riferimento a sottorisorse:</span><span class="sxs-lookup"><span data-stu-id="84364-185">The following structures also reference subresources:</span></span>

-   <span data-ttu-id="84364-186">[**D3D12 \_ SCARTO \_ Region**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_discard_region) : struttura utilizzata per la rimozione di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="84364-186">[**D3D12\_DISCARD\_REGION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_discard_region) : a structure used in preparation for discarding a resource.</span></span>
-   <span data-ttu-id="84364-187">[**D3D12 \_ \_ \_ Footprint delle sottorisorse inserito**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) : aggiunge un offset in una risorsa al footprint di base.</span><span class="sxs-lookup"><span data-stu-id="84364-187">[**D3D12\_PLACED\_SUBRESOURCE\_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) : adds an offset into a resource to the basic footprint.</span></span>
-   <span data-ttu-id="84364-188">[**D3D12 \_ \_ \_ Barriera di transizione delle risorse**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) : descrive la transizione delle sottorisorse tra diversi utilizzi (risorsa shader, destinazione di rendering e così via).</span><span class="sxs-lookup"><span data-stu-id="84364-188">[**D3D12\_RESOURCE\_TRANSITION\_BARRIER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) : describes the transition of subresources between different usages (shader resource, render target, etc.).</span></span>
-   <span data-ttu-id="84364-189">[**D3D12 \_ \_Dati delle sottorisorse**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) : i dati delle sottorisorse includono i dati stessi e il passo delle righe e delle sezioni.</span><span class="sxs-lookup"><span data-stu-id="84364-189">[**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) : subresource data includes the data itself, and the row and slice pitch.</span></span>
-   <span data-ttu-id="84364-190">[**D3D12 \_ \_Footprint delle sottorisorse**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) : un'impronta include il formato, la larghezza, l'altezza, la profondità e il pitch di riga della sottorisorsa.</span><span class="sxs-lookup"><span data-stu-id="84364-190">[**D3D12\_SUBRESOURCE\_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) : a footprint includes the format, width, height, depth and row-pitch of the subresource.</span></span>
-   <span data-ttu-id="84364-191">[**D3D12 \_ Subresource \_ info**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_info) : contiene l'offset, il pitch di riga e il passo di profondità della sottorisorsa.</span><span class="sxs-lookup"><span data-stu-id="84364-191">[**D3D12\_SUBRESOURCE\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_info) : contains the offset, row pitch and depth pitch of the subresource.</span></span>
-   <span data-ttu-id="84364-192">[**D3D12 \_ \_Affiancamento delle risorse**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) : descrive un volume della sottorisorsa affiancata (fare riferimento a [risorse affiancate dal volume](volume-tiled-resources.md)).</span><span class="sxs-lookup"><span data-stu-id="84364-192">[**D3D12\_SUBRESOURCE\_TILING**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) : describes a tiled subresource volume (refer to [Volume Tiled Resources](volume-tiled-resources.md)).</span></span>
-   <span data-ttu-id="84364-193">[**D3D12 \_ TEXTURE \_ copy \_ location**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) : descrive una parte di una trama per la copia.</span><span class="sxs-lookup"><span data-stu-id="84364-193">[**D3D12\_TEXTURE\_COPY\_LOCATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) : describes a portion of a texture for the purpose of copying.</span></span>
-   <span data-ttu-id="84364-194">[**D3D12 \_ \_ \_ Coordinata della risorsa affiancata**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) : descrive le coordinate di una risorsa affiancata.</span><span class="sxs-lookup"><span data-stu-id="84364-194">[**D3D12\_TILED\_RESOURCE\_COORDINATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) : describes the coordinates of a tiled resource.</span></span>

<span data-ttu-id="84364-195">Metodi:</span><span class="sxs-lookup"><span data-stu-id="84364-195">Methods:</span></span>

-   <span data-ttu-id="84364-196">[**ID3D12Device:: GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints) : ottiene informazioni su una risorsa, per consentire la copia.</span><span class="sxs-lookup"><span data-stu-id="84364-196">[**ID3D12Device::GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints) : gets information on a resource, to enable a copy to be made.</span></span>
-   <span data-ttu-id="84364-197">[**ID3D12Device:: GetResourceTiling**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourcetiling) : ottiene informazioni sul modo in cui una risorsa affiancata viene suddivisa in riquadri.</span><span class="sxs-lookup"><span data-stu-id="84364-197">[**ID3D12Device::GetResourceTiling**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourcetiling) : gets info about how a tiled resource is broken into tiles.</span></span>
-   <span data-ttu-id="84364-198">[**ID3D12GraphicsCommandList:: ResolveSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource) : copia una sottorisorsa multicampionata in una sottorisorsa non multicampionata.</span><span class="sxs-lookup"><span data-stu-id="84364-198">[**ID3D12GraphicsCommandList::ResolveSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource) : copies a multi-sampled subresource into a non-multi-sampled subresource.</span></span>
-   <span data-ttu-id="84364-199">[**ID3D12Resource:: Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) : restituisce un puntatore ai dati specificati nella risorsa e nega l'accesso alla GPU alla sottorisorsa.</span><span class="sxs-lookup"><span data-stu-id="84364-199">[**ID3D12Resource::Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) : returns a pointer to the specified data in the resource, and denies the GPU access to the subresource.</span></span>
-   <span data-ttu-id="84364-200">[**ID3D12Resource:: ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) : copia i dati da una sottorisorsa o da un'area rettangolare di una sottorisorsa.</span><span class="sxs-lookup"><span data-stu-id="84364-200">[**ID3D12Resource::ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) : copies data from a subresource, or a rectangular region of a subresource.</span></span>
-   <span data-ttu-id="84364-201">[**ID3D12Resource:: annullare**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) : Annulla il mapping dell'intervallo di memoria specificato e invalida il puntatore alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="84364-201">[**ID3D12Resource::Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) : unmaps the specified range of memory and invalidates the pointer to the resource.</span></span> <span data-ttu-id="84364-202">Ripristina l'accesso GPU alla sottorisorsa.</span><span class="sxs-lookup"><span data-stu-id="84364-202">Reinstates GPU access to the subresource.</span></span>
-   <span data-ttu-id="84364-203">[**ID3D12Resource:: WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) : copia i dati in una sottorisorsa o in un'area rettangolare di una sottorisorsa.</span><span class="sxs-lookup"><span data-stu-id="84364-203">[**ID3D12Resource::WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) : copies data to a subresource, or a rectangular region of a subresource.</span></span>

<span data-ttu-id="84364-204">Le trame devono trovarsi nello stato [**comune di \_ stato della risorsa \_ \_ D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) per l'accesso alla CPU tramite [**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) e [**ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) come validi, ma non i buffer.</span><span class="sxs-lookup"><span data-stu-id="84364-204">Textures must be in the [**D3D12\_RESOURCE\_STATE\_COMMON**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) state for CPU access through [**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) and [**ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) to be legal; but buffers do not.</span></span> <span data-ttu-id="84364-205">L'accesso alla CPU a una risorsa viene in genere eseguito tramite [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) / [**annullare**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap).</span><span class="sxs-lookup"><span data-stu-id="84364-205">CPU access to a resource is typically done through [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map)/[**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap).</span></span>

## <a name="related-topics"></a><span data-ttu-id="84364-206">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="84364-206">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84364-207">Associazione di risorse</span><span class="sxs-lookup"><span data-stu-id="84364-207">Resource Binding</span></span>](resource-binding.md)
</dt> </dl>

 

 




