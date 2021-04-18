---
title: Struttura DDS_HEADER_DXT10 (DDS. h)
description: Estensione dell'intestazione DDS per gestire matrici di risorse, formati pixel DXGI che non vengono mappati alle strutture legacy di formato pixel di Microsoft DirectDraw e metadati aggiuntivi.
ms.assetid: 502d6943-8f25-446c-b990-8276f862c195
keywords:
- Struttura DDS_HEADER_DXT10 DDS
topic_type:
- apiref
api_name:
- DDS_HEADER_DXT10
api_location:
- Dds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a2f5dd4a6948d38b86b49584db81937ce5148b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322293"
---
# <a name="dds_header_dxt10-structure"></a><span data-ttu-id="0c9a4-104">\_Struttura DXT10 dell'intestazione DDS \_</span><span class="sxs-lookup"><span data-stu-id="0c9a4-104">DDS\_HEADER\_DXT10 structure</span></span>

<span data-ttu-id="0c9a4-105">Estensione dell'intestazione DDS per gestire matrici di risorse, formati pixel DXGI che non vengono mappati alle strutture legacy di formato pixel di Microsoft DirectDraw e metadati aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="0c9a4-105">DDS header extension to handle resource arrays, DXGI pixel formats that don't map to the legacy Microsoft DirectDraw pixel format structures, and additional metadata.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c9a4-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0c9a4-106">Syntax</span></span>


```C++
typedef struct {
  DXGI_FORMAT              dxgiFormat;
  D3D10_RESOURCE_DIMENSION resourceDimension;
  UINT                     miscFlag;
  UINT                     arraySize;
  UINT                     miscFlags2;
} DDS_HEADER_DXT10;
```



## <a name="members"></a><span data-ttu-id="0c9a4-107">Members</span><span class="sxs-lookup"><span data-stu-id="0c9a4-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="0c9a4-108">**dxgiFormat**</span><span class="sxs-lookup"><span data-stu-id="0c9a4-108">**dxgiFormat**</span></span>
</dt> <dd>

<span data-ttu-id="0c9a4-109">Tipo: **[ **DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="0c9a4-109">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

</dd> <dd>

<span data-ttu-id="0c9a4-110">Formato pixel della superficie (vedere [**il \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).</span><span class="sxs-lookup"><span data-stu-id="0c9a4-110">The surface pixel format (see [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).</span></span>

</dd> <dt>

<span data-ttu-id="0c9a4-111">**resourceDimension**</span><span class="sxs-lookup"><span data-stu-id="0c9a4-111">**resourceDimension**</span></span>
</dt> <dd>

<span data-ttu-id="0c9a4-112">Tipo: **[ **\_ \_ dimensione della risorsa D3D10**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_dimension)**</span><span class="sxs-lookup"><span data-stu-id="0c9a4-112">Type: **[**D3D10\_RESOURCE\_DIMENSION**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_dimension)**</span></span>

</dd> <dd>

<span data-ttu-id="0c9a4-113">Identifica il tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="0c9a4-113">Identifies the type of resource.</span></span> <span data-ttu-id="0c9a4-114">I valori seguenti per questo membro sono un subset dei valori nell'enumerazione della dimensione della [**\_ risorsa D3D10 \_**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_dimension) o della [**\_ \_ dimensione della risorsa d3d11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_dimension) :</span><span class="sxs-lookup"><span data-stu-id="0c9a4-114">The following values for this member are a subset of the values in the [**D3D10\_RESOURCE\_DIMENSION**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_dimension) or [**D3D11\_RESOURCE\_DIMENSION**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_dimension) enumeration:</span></span>



| <span data-ttu-id="0c9a4-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="0c9a4-115">Type</span></span>                                                              | <span data-ttu-id="0c9a4-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c9a4-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="0c9a4-117">Valore</span><span class="sxs-lookup"><span data-stu-id="0c9a4-117">Value</span></span> |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="0c9a4-118">\_Dimensione DDS \_ TEXTURE1D ( \_ dimensione risorsa \_ D3D10 \_ TEXTURE1D)</span><span class="sxs-lookup"><span data-stu-id="0c9a4-118">DDS\_DIMENSION\_TEXTURE1D (D3D10\_RESOURCE\_DIMENSION\_TEXTURE1D)</span></span> | <span data-ttu-id="0c9a4-119">La risorsa è una [trama 1D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types).</span><span class="sxs-lookup"><span data-stu-id="0c9a4-119">Resource is a [1D texture](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types).</span></span> <span data-ttu-id="0c9a4-120">Il membro **dwWidth** dell' [**\_ intestazione DDS**](dds-header.md) specifica le dimensioni della trama.</span><span class="sxs-lookup"><span data-stu-id="0c9a4-120">The **dwWidth** member of [**DDS\_HEADER**](dds-header.md) specifies the size of the texture.</span></span> <span data-ttu-id="0c9a4-121">In genere, il membro **dwHeight** dell' **\_ intestazione DDS** viene impostato su 1. è necessario impostare anche il \_ flag di altezza DDSD  nel membro dwFlags **dell' \_ intestazione DDS**.</span><span class="sxs-lookup"><span data-stu-id="0c9a4-121">Typically, you set the **dwHeight** member of **DDS\_HEADER** to 1; you also must set the DDSD\_HEIGHT flag in the **dwFlags** member of **DDS\_HEADER**.</span></span>                      | <span data-ttu-id="0c9a4-122">2</span><span class="sxs-lookup"><span data-stu-id="0c9a4-122">2</span></span>     |
| <span data-ttu-id="0c9a4-123">\_Dimensione DDS \_ TEXTURE2D ( \_ dimensione risorsa \_ D3D10 \_ TEXTURE2D)</span><span class="sxs-lookup"><span data-stu-id="0c9a4-123">DDS\_DIMENSION\_TEXTURE2D (D3D10\_RESOURCE\_DIMENSION\_TEXTURE2D)</span></span> | <span data-ttu-id="0c9a4-124">Resource è una [trama 2D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) con un'area specificata dai membri **dwWidth** e **dwHeight** dell' [**\_ intestazione DDS**](dds-header.md).</span><span class="sxs-lookup"><span data-stu-id="0c9a4-124">Resource is a [2D texture](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) with an area specified by the **dwWidth** and **dwHeight** members of [**DDS\_HEADER**](dds-header.md).</span></span> <span data-ttu-id="0c9a4-125">È anche possibile usare questo tipo per identificare una trama del mapping del cubo.</span><span class="sxs-lookup"><span data-stu-id="0c9a4-125">You can also use this type to identify a cube-map texture.</span></span> <span data-ttu-id="0c9a4-126">Per ulteriori informazioni sull'identificazione di una trama con mappa cubo, vedere **miscFlag** e **arraySize** members.</span><span class="sxs-lookup"><span data-stu-id="0c9a4-126">For more information about how to identify a cube-map texture, see **miscFlag** and **arraySize** members.</span></span> | <span data-ttu-id="0c9a4-127">3</span><span class="sxs-lookup"><span data-stu-id="0c9a4-127">3</span></span>     |
| <span data-ttu-id="0c9a4-128">\_Dimensione DDS \_ TEXTURE3D ( \_ dimensione risorsa \_ D3D10 \_ TEXTURE3D)</span><span class="sxs-lookup"><span data-stu-id="0c9a4-128">DDS\_DIMENSION\_TEXTURE3D (D3D10\_RESOURCE\_DIMENSION\_TEXTURE3D)</span></span> | <span data-ttu-id="0c9a4-129">Resource è una [trama 3D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) con un volume specificato dai membri **dwWidth**, **DwHeight** e **dwDepth** dell' [**\_ intestazione DDS**](dds-header.md).</span><span class="sxs-lookup"><span data-stu-id="0c9a4-129">Resource is a [3D texture](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) with a volume specified by the **dwWidth**, **dwHeight**, and **dwDepth** members of [**DDS\_HEADER**](dds-header.md).</span></span> <span data-ttu-id="0c9a4-130">È anche necessario impostare il \_ flag di profondità DDSD nel membro **dwFlags** dell' **\_ intestazione DDS**.</span><span class="sxs-lookup"><span data-stu-id="0c9a4-130">You also must set the DDSD\_DEPTH flag in the **dwFlags** member of **DDS\_HEADER**.</span></span>                                                                   | <span data-ttu-id="0c9a4-131">4</span><span class="sxs-lookup"><span data-stu-id="0c9a4-131">4</span></span>     |



 

</dd> <dt>

<span data-ttu-id="0c9a4-132">**miscFlag**</span><span class="sxs-lookup"><span data-stu-id="0c9a4-132">**miscFlag**</span></span>
</dt> <dd>

<span data-ttu-id="0c9a4-133">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0c9a4-133">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0c9a4-134">Identifica altre opzioni meno comuni per le risorse.</span><span class="sxs-lookup"><span data-stu-id="0c9a4-134">Identifies other, less common options for resources.</span></span> <span data-ttu-id="0c9a4-135">Il valore seguente per questo membro è un subset dei valori nel [**\_ \_ \_ flag misc della risorsa D3D10**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_misc_flag) o nell'enumerazione del [**\_ \_ \_ flag varie della risorsa d3d11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_misc_flag) :</span><span class="sxs-lookup"><span data-stu-id="0c9a4-135">The following value for this member is a subset of the values in the [**D3D10\_RESOURCE\_MISC\_FLAG**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_misc_flag) or [**D3D11\_RESOURCE\_MISC\_FLAG**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_misc_flag) enumeration:</span></span>



| <span data-ttu-id="0c9a4-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="0c9a4-136">Type</span></span>                             | <span data-ttu-id="0c9a4-137">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c9a4-137">Description</span></span>                                                                                                  | <span data-ttu-id="0c9a4-138">Valore</span><span class="sxs-lookup"><span data-stu-id="0c9a4-138">Value</span></span> |
|----------------------------------|--------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="0c9a4-139">\_risorsa DDS \_ \_ TEXTURECUBE varie</span><span class="sxs-lookup"><span data-stu-id="0c9a4-139">DDS\_RESOURCE\_MISC\_TEXTURECUBE</span></span> | <span data-ttu-id="0c9a4-140">Indica che una [trama 2D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) è una trama con mappa cubo.</span><span class="sxs-lookup"><span data-stu-id="0c9a4-140">Indicates a [2D texture](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) is a cube-map texture.</span></span> | <span data-ttu-id="0c9a4-141">0x4</span><span class="sxs-lookup"><span data-stu-id="0c9a4-141">0x4</span></span>   |



 

</dd> <dt>

<span data-ttu-id="0c9a4-142">**arraySize**</span><span class="sxs-lookup"><span data-stu-id="0c9a4-142">**arraySize**</span></span>
</dt> <dd>

<span data-ttu-id="0c9a4-143">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0c9a4-143">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0c9a4-144">Numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="0c9a4-144">The number of elements in the array.</span></span>

<span data-ttu-id="0c9a4-145">Per una [trama 2D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) che è anche una trama con mappa cubo, questo numero rappresenta il numero di cubi.</span><span class="sxs-lookup"><span data-stu-id="0c9a4-145">For a [2D texture](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) that is also a cube-map texture, this number represents the number of cubes.</span></span> <span data-ttu-id="0c9a4-146">Questo numero corrisponde al numero nel membro **NumCubes** di [**D3D10 \_ TEXCUBE \_ array \_ srv1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_texcube_array_srv1) o [**d3d11 \_ TEXCUBE \_ array \_ SRV**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_texcube_array_srv)).</span><span class="sxs-lookup"><span data-stu-id="0c9a4-146">This number is the same as the number in the **NumCubes** member of [**D3D10\_TEXCUBE\_ARRAY\_SRV1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_texcube_array_srv1) or [**D3D11\_TEXCUBE\_ARRAY\_SRV**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_texcube_array_srv)).</span></span> <span data-ttu-id="0c9a4-147">In questo caso, il file DDS contiene **arraySize** \* 6 trame 2D.</span><span class="sxs-lookup"><span data-stu-id="0c9a4-147">In this case, the DDS file contains **arraySize**\*6 2D textures.</span></span> <span data-ttu-id="0c9a4-148">Per ulteriori informazioni su questo caso, vedere la descrizione di **miscFlag** .</span><span class="sxs-lookup"><span data-stu-id="0c9a4-148">For more information about this case, see the **miscFlag** description.</span></span>

<span data-ttu-id="0c9a4-149">Per una [trama 3D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types), è necessario impostare questo numero su 1.</span><span class="sxs-lookup"><span data-stu-id="0c9a4-149">For a [3D texture](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types), you must set this number to 1.</span></span>

</dd> <dt>

<span data-ttu-id="0c9a4-150">**miscFlags2**</span><span class="sxs-lookup"><span data-stu-id="0c9a4-150">**miscFlags2**</span></span>
</dt> <dd>

<span data-ttu-id="0c9a4-151">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0c9a4-151">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0c9a4-152">Contiene metadati aggiuntivi (in precedenza è stato riservato).</span><span class="sxs-lookup"><span data-stu-id="0c9a4-152">Contains additional metadata (formerly was reserved).</span></span> <span data-ttu-id="0c9a4-153">I 3 bit inferiori indicano la modalità Alpha della risorsa associata.</span><span class="sxs-lookup"><span data-stu-id="0c9a4-153">The lower 3 bits indicate the alpha mode of the associated resource.</span></span> <span data-ttu-id="0c9a4-154">I 29 bit superiori sono riservati e sono in genere 0.</span><span class="sxs-lookup"><span data-stu-id="0c9a4-154">The upper 29 bits are reserved and are typically 0.</span></span>



| <span data-ttu-id="0c9a4-155">Tipo</span><span class="sxs-lookup"><span data-stu-id="0c9a4-155">Type</span></span>                            | <span data-ttu-id="0c9a4-156">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c9a4-156">Description</span></span>                                                                                                                              | <span data-ttu-id="0c9a4-157">Valore</span><span class="sxs-lookup"><span data-stu-id="0c9a4-157">Value</span></span> |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="0c9a4-158">\_modalità Alpha \_ DDS \_ sconosciuta</span><span class="sxs-lookup"><span data-stu-id="0c9a4-158">DDS\_ALPHA\_MODE\_UNKNOWN</span></span>       | <span data-ttu-id="0c9a4-159">Il contenuto del canale alfa è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="0c9a4-159">Alpha channel content is unknown.</span></span> <span data-ttu-id="0c9a4-160">Si tratta del valore per i file legacy, che in genere si presuppone essere "Alpha".</span><span class="sxs-lookup"><span data-stu-id="0c9a4-160">This is the value for legacy files, which typically is assumed to be 'straight' alpha.</span></span>                 | <span data-ttu-id="0c9a4-161">0x0</span><span class="sxs-lookup"><span data-stu-id="0c9a4-161">0x0</span></span>   |
| <span data-ttu-id="0c9a4-162">\_modalità Alpha \_ DDS \_ diritta</span><span class="sxs-lookup"><span data-stu-id="0c9a4-162">DDS\_ALPHA\_MODE\_STRAIGHT</span></span>      | <span data-ttu-id="0c9a4-163">Si presume che il contenuto del canale alfa usi un Alpha diretto.</span><span class="sxs-lookup"><span data-stu-id="0c9a4-163">Any alpha channel content is presumed to use straight alpha.</span></span>                                                                             | <span data-ttu-id="0c9a4-164">0x1</span><span class="sxs-lookup"><span data-stu-id="0c9a4-164">0x1</span></span>   |
| <span data-ttu-id="0c9a4-165">\_modalità alfa \_ DDS \_ premoltiplicata</span><span class="sxs-lookup"><span data-stu-id="0c9a4-165">DDS\_ALPHA\_MODE\_PREMULTIPLIED</span></span> | <span data-ttu-id="0c9a4-166">Qualsiasi contenuto del canale alfa utilizza un alfa premoltiplicato.</span><span class="sxs-lookup"><span data-stu-id="0c9a4-166">Any alpha channel content is using premultiplied alpha.</span></span> <span data-ttu-id="0c9a4-167">Gli unici formati di file legacy che indicano queste informazioni sono ' DX2' è DX4'.</span><span class="sxs-lookup"><span data-stu-id="0c9a4-167">The only legacy file formats that indicate this information are 'DX2' and 'DX4'.</span></span> | <span data-ttu-id="0c9a4-168">0x2</span><span class="sxs-lookup"><span data-stu-id="0c9a4-168">0x2</span></span>   |
| <span data-ttu-id="0c9a4-169">\_opaco in \_ modalità \_ Alpha DDS</span><span class="sxs-lookup"><span data-stu-id="0c9a4-169">DDS\_ALPHA\_MODE\_OPAQUE</span></span>        | <span data-ttu-id="0c9a4-170">Tutti i contenuti del canale alfa sono tutti impostati su completamente opachi.</span><span class="sxs-lookup"><span data-stu-id="0c9a4-170">Any alpha channel content is all set to fully opaque.</span></span>                                                                                    | <span data-ttu-id="0c9a4-171">0x3</span><span class="sxs-lookup"><span data-stu-id="0c9a4-171">0x3</span></span>   |
| <span data-ttu-id="0c9a4-172">\_personalizzazione della \_ modalità \_ Alpha DDS</span><span class="sxs-lookup"><span data-stu-id="0c9a4-172">DDS\_ALPHA\_MODE\_CUSTOM</span></span>        | <span data-ttu-id="0c9a4-173">Qualsiasi contenuto del canale alfa viene usato come quarto canale e non è destinato a rappresentare la trasparenza (diritta o premoltiplicata).</span><span class="sxs-lookup"><span data-stu-id="0c9a4-173">Any alpha channel content is being used as a 4th channel and is not intended to represent transparency (straight or premultiplied).</span></span>      | <span data-ttu-id="0c9a4-174">0x4</span><span class="sxs-lookup"><span data-stu-id="0c9a4-174">0x4</span></span>   |



 

> [!Note]  
> <span data-ttu-id="0c9a4-175">Le librerie di utilità legacy D3DX 10 e [D3DX 11](/windows/desktop/direct3d11/d3d11-graphics-reference-d3dx11) non verranno caricate. Il file DDS con **miscFlags2** non è uguale a zero.</span><span class="sxs-lookup"><span data-stu-id="0c9a4-175">The legacy D3DX 10 and [D3DX 11](/windows/desktop/direct3d11/d3d11-graphics-reference-d3dx11) utility libraries will fail to load any .DDS file with **miscFlags2** not equal to zero.</span></span>

 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0c9a4-176">Commenti</span><span class="sxs-lookup"><span data-stu-id="0c9a4-176">Remarks</span></span>

<span data-ttu-id="0c9a4-177">Usare questa struttura insieme a un' [**\_ intestazione DDS**](dds-header.md) per archiviare una matrice di risorse in un file DDS.</span><span class="sxs-lookup"><span data-stu-id="0c9a4-177">Use this structure together with a [**DDS\_HEADER**](dds-header.md) to store a resource array in a DDS file.</span></span> <span data-ttu-id="0c9a4-178">Per altre informazioni, vedere [matrici di trame](dx-graphics-dds-pguide.md).</span><span class="sxs-lookup"><span data-stu-id="0c9a4-178">For more info, see [texture arrays](dx-graphics-dds-pguide.md).</span></span>

<span data-ttu-id="0c9a4-179">Questa intestazione è presente se il membro **dwFourCC** della struttura del gruppo di test di [**DDS \_**](dds-pixelformat.md) è impostato su' DX10'.</span><span class="sxs-lookup"><span data-stu-id="0c9a4-179">This header is present if the **dwFourCC** member of the [**DDS\_PIXELFORMAT**](dds-pixelformat.md) structure is set to 'DX10'.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c9a4-180">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0c9a4-180">Requirements</span></span>



| <span data-ttu-id="0c9a4-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c9a4-181">Requirement</span></span> | <span data-ttu-id="0c9a4-182">Valore</span><span class="sxs-lookup"><span data-stu-id="0c9a4-182">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0c9a4-183">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0c9a4-183">Header</span></span><br/> | <dl> <span data-ttu-id="0c9a4-184"><dt>DDS. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c9a4-184"><dt>Dds.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c9a4-185">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0c9a4-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c9a4-186">Informazioni di riferimento per DDS</span><span class="sxs-lookup"><span data-stu-id="0c9a4-186">Reference for DDS</span></span>](dx-graphics-dds-reference.md)
</dt> </dl>

 

