---
description: Fornire facoltativamente informazioni alle API del caricatore di trama per controllare la modalità di caricamento delle trame. Il valore predefinito D3DX10 \_ per uno di questi parametri provocherà l'uso automatico del valore del file di origine da parte di D3DX.
ms.assetid: 8325d50e-a8a9-4ee2-87e2-e60fb3699af6
title: Struttura D3DX10_IMAGE_LOAD_INFO (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_IMAGE_LOAD_INFO
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: 89e819e81c11842feaa6996e047f3cac3587792c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323323"
---
# <a name="d3dx10_image_load_info-structure"></a><span data-ttu-id="19937-104">\_Struttura delle \_ informazioni sul caricamento dell'immagine d3dx10 \_</span><span class="sxs-lookup"><span data-stu-id="19937-104">D3DX10\_IMAGE\_LOAD\_INFO structure</span></span>

<span data-ttu-id="19937-105">Fornire facoltativamente informazioni alle API del caricatore di trama per controllare la modalità di caricamento delle trame.</span><span class="sxs-lookup"><span data-stu-id="19937-105">Optionally provide information to texture loader APIs to control how textures get loaded.</span></span> <span data-ttu-id="19937-106">Il valore predefinito D3DX10 \_ per uno di questi parametri provocherà l'uso automatico del valore del file di origine da parte di D3DX.</span><span class="sxs-lookup"><span data-stu-id="19937-106">A value of D3DX10\_DEFAULT for any of these parameters will cause D3DX to automatically use the value from the source file.</span></span>

## <a name="syntax"></a><span data-ttu-id="19937-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="19937-107">Syntax</span></span>


```C++
typedef struct D3DX10_IMAGE_LOAD_INFO {
  UINT              Width;
  UINT              Height;
  UINT              Depth;
  UINT              FirstMipLevel;
  UINT              MipLevels;
  D3D10_USAGE       Usage;
  UINT              BindFlags;
  UINT              CpuAccessFlags;
  UINT              MiscFlags;
  DXGI_FORMAT       Format;
  UINT              Filter;
  UINT              MipFilter;
  D3DX10_IMAGE_INFO *pSrcInfo;
} D3DX10_IMAGE_LOAD_INFO, *LPD3DX10_IMAGE_LOAD_INFO;
```



## <a name="members"></a><span data-ttu-id="19937-108">Members</span><span class="sxs-lookup"><span data-stu-id="19937-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="19937-109">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="19937-109">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="19937-110">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="19937-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="19937-111">Larghezza di destinazione della trama.</span><span class="sxs-lookup"><span data-stu-id="19937-111">The target width of the texture.</span></span> <span data-ttu-id="19937-112">Se la larghezza effettiva della trama è maggiore o minore di questo valore, la trama verrà ridimensionata verso l'alto o verso il basso per adattarla a questa larghezza di destinazione.</span><span class="sxs-lookup"><span data-stu-id="19937-112">If the actual width of the texture is larger or smaller than this value then the texture will be scaled up or down to fit this target width.</span></span>

</dd> <dt>

<span data-ttu-id="19937-113">**Altezza**</span><span class="sxs-lookup"><span data-stu-id="19937-113">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="19937-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="19937-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="19937-115">Altezza di destinazione della trama.</span><span class="sxs-lookup"><span data-stu-id="19937-115">The target height of the texture.</span></span> <span data-ttu-id="19937-116">Se l'altezza effettiva della trama è maggiore o minore di questo valore, la trama verrà ridimensionata verso l'alto o verso il basso per adattarla a questa altezza di destinazione.</span><span class="sxs-lookup"><span data-stu-id="19937-116">If the actual height of the texture is larger or smaller than this value then the texture will be scaled up or down to fit this target height.</span></span>

</dd> <dt>

<span data-ttu-id="19937-117">**Livello nidificazione**</span><span class="sxs-lookup"><span data-stu-id="19937-117">**Depth**</span></span>
</dt> <dd>

<span data-ttu-id="19937-118">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="19937-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="19937-119">Profondità della trama.</span><span class="sxs-lookup"><span data-stu-id="19937-119">The depth of the texture.</span></span> <span data-ttu-id="19937-120">Questo vale solo per le trame del volume.</span><span class="sxs-lookup"><span data-stu-id="19937-120">This only applies to volume textures.</span></span>

</dd> <dt>

<span data-ttu-id="19937-121">**FirstMipLevel**</span><span class="sxs-lookup"><span data-stu-id="19937-121">**FirstMipLevel**</span></span>
</dt> <dd>

<span data-ttu-id="19937-122">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="19937-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="19937-123">Livello di mipmap di risoluzione più alto della trama.</span><span class="sxs-lookup"><span data-stu-id="19937-123">The highest resolution mipmap level of the texture.</span></span> <span data-ttu-id="19937-124">Se è maggiore di 0, dopo il caricamento della trama FirstMipLevel verrà eseguito il mapping a mipmap livello 0.</span><span class="sxs-lookup"><span data-stu-id="19937-124">If this is greater than 0, then after the texture is loaded FirstMipLevel will be mapped to mipmap level 0.</span></span>

</dd> <dt>

<span data-ttu-id="19937-125">**MipLevels**</span><span class="sxs-lookup"><span data-stu-id="19937-125">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="19937-126">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="19937-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="19937-127">Numero massimo di livelli di mipmap che avrà la trama.</span><span class="sxs-lookup"><span data-stu-id="19937-127">The maximum number of mipmap levels that the texture will have.</span></span> <span data-ttu-id="19937-128">Se \_ si usa il valore predefinito 0 o d3dx10, verrà creata una catena mipmap completa.</span><span class="sxs-lookup"><span data-stu-id="19937-128">Using 0 or D3DX10\_DEFAULT will cause a full mipmap chain to be created.</span></span>

</dd> <dt>

<span data-ttu-id="19937-129">**Utilizzo**</span><span class="sxs-lookup"><span data-stu-id="19937-129">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="19937-130">Tipo: **[ **\_ utilizzo di D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)**</span><span class="sxs-lookup"><span data-stu-id="19937-130">Type: **[**D3D10\_USAGE**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)**</span></span>

</dd> <dd>

<span data-ttu-id="19937-131">Il modo in cui la risorsa di trama deve essere utilizzata.</span><span class="sxs-lookup"><span data-stu-id="19937-131">The way the texture resource is intended to be used.</span></span> <span data-ttu-id="19937-132">Vedere [**\_ utilizzo di D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage).</span><span class="sxs-lookup"><span data-stu-id="19937-132">See [**D3D10\_USAGE**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage).</span></span>

</dd> <dt>

<span data-ttu-id="19937-133">**BindFlags**</span><span class="sxs-lookup"><span data-stu-id="19937-133">**BindFlags**</span></span>
</dt> <dd>

<span data-ttu-id="19937-134">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="19937-134">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="19937-135">Fasi della pipeline a cui sarà consentita l'associazione della trama.</span><span class="sxs-lookup"><span data-stu-id="19937-135">The pipeline stages that the texture will be allowed to bind to.</span></span> <span data-ttu-id="19937-136">Vedere [**\_ \_ flag di binding D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag).</span><span class="sxs-lookup"><span data-stu-id="19937-136">See [**D3D10\_BIND\_FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag).</span></span>

</dd> <dt>

<span data-ttu-id="19937-137">**CpuAccessFlags**</span><span class="sxs-lookup"><span data-stu-id="19937-137">**CpuAccessFlags**</span></span>
</dt> <dd>

<span data-ttu-id="19937-138">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="19937-138">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="19937-139">Autorizzazioni di accesso che la CPU avrà per la risorsa di trama.</span><span class="sxs-lookup"><span data-stu-id="19937-139">The access permissions the cpu will have for the texture resource.</span></span> <span data-ttu-id="19937-140">Vedere [**\_ flag di \_ accesso \_ alla CPU D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag).</span><span class="sxs-lookup"><span data-stu-id="19937-140">See [**D3D10\_CPU\_ACCESS\_FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag).</span></span>

</dd> <dt>

<span data-ttu-id="19937-141">**MiscFlags**</span><span class="sxs-lookup"><span data-stu-id="19937-141">**MiscFlags**</span></span>
</dt> <dd>

<span data-ttu-id="19937-142">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="19937-142">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="19937-143">Proprietà delle risorse varie ( [**vedere \_ \_ \_ flag varie della risorsa D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag)).</span><span class="sxs-lookup"><span data-stu-id="19937-143">Miscellaneous resource properties (see [**D3D10\_RESOURCE\_MISC\_FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag)).</span></span>

</dd> <dt>

<span data-ttu-id="19937-144">**Formato**</span><span class="sxs-lookup"><span data-stu-id="19937-144">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="19937-145">Tipo: **[ **DXGI \_ Format**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="19937-145">Type: **[**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

</dd> <dd>

<span data-ttu-id="19937-146">Formato in cui si troverà la trama dopo il caricamento.</span><span class="sxs-lookup"><span data-stu-id="19937-146">The format the texture will be in after it is loaded.</span></span> <span data-ttu-id="19937-147">Vedere [**il \_ formato DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="19937-147">See [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

</dd> <dt>

<span data-ttu-id="19937-148">**Filter**</span><span class="sxs-lookup"><span data-stu-id="19937-148">**Filter**</span></span>
</dt> <dd>

<span data-ttu-id="19937-149">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="19937-149">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="19937-150">Filtrare la trama usando il filtro specificato (solo quando si esegue il ricampionamento).</span><span class="sxs-lookup"><span data-stu-id="19937-150">Filter the texture using the specified filter (only when resampling).</span></span> <span data-ttu-id="19937-151">Vedere [**\_ \_ flag di filtro d3dx10**](d3dx10-filter-flag.md).</span><span class="sxs-lookup"><span data-stu-id="19937-151">See [**D3DX10\_FILTER\_FLAG**](d3dx10-filter-flag.md).</span></span>

</dd> <dt>

<span data-ttu-id="19937-152">**MipFilter**</span><span class="sxs-lookup"><span data-stu-id="19937-152">**MipFilter**</span></span>
</dt> <dd>

<span data-ttu-id="19937-153">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="19937-153">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="19937-154">Filtrare i livelli MIP della trama usando il filtro specificato (solo se si sta generando mipmap).</span><span class="sxs-lookup"><span data-stu-id="19937-154">Filter the texture mip levels using the specified filter (only if generating mipmaps).</span></span> <span data-ttu-id="19937-155">I valori validi sono D3DX10 \_ Filter \_ None, d3dx10 Filter \_ \_ Point, D3DX10 \_ Filter \_ Linear o d3dx10 \_ Filter \_ Triangle.</span><span class="sxs-lookup"><span data-stu-id="19937-155">Valid values are D3DX10\_FILTER\_NONE, D3DX10\_FILTER\_POINT, D3DX10\_FILTER\_LINEAR, or D3DX10\_FILTER\_TRIANGLE.</span></span> <span data-ttu-id="19937-156">Vedere [**\_ \_ flag di filtro d3dx10**](d3dx10-filter-flag.md).</span><span class="sxs-lookup"><span data-stu-id="19937-156">See [**D3DX10\_FILTER\_FLAG**](d3dx10-filter-flag.md).</span></span>

</dd> <dt>

<span data-ttu-id="19937-157">**pSrcInfo**</span><span class="sxs-lookup"><span data-stu-id="19937-157">**pSrcInfo**</span></span>
</dt> <dd>

<span data-ttu-id="19937-158">Tipo: **[ **d3dx10 \_ Image \_ info**](d3dx10-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="19937-158">Type: **[**D3DX10\_IMAGE\_INFO**](d3dx10-image-info.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="19937-159">Informazioni sull'immagine originale.</span><span class="sxs-lookup"><span data-stu-id="19937-159">Information about the original image.</span></span> <span data-ttu-id="19937-160">Vedere [**d3dx10 \_ Image \_ info**](d3dx10-image-info.md).</span><span class="sxs-lookup"><span data-stu-id="19937-160">See [**D3DX10\_IMAGE\_INFO**](d3dx10-image-info.md).</span></span> <span data-ttu-id="19937-161">Può essere ottenuto con [**D3DX10GetImageInfoFromFile**](d3dx10getimageinfofromfile.md), [**D3DX10GetImageInfoFromMemory**](d3dx10getimageinfofrommemory.md)o [**D3DX10GetImageInfoFromResource**](d3dx10getimageinfofromresource.md).</span><span class="sxs-lookup"><span data-stu-id="19937-161">Can be obtained with [**D3DX10GetImageInfoFromFile**](d3dx10getimageinfofromfile.md), [**D3DX10GetImageInfoFromMemory**](d3dx10getimageinfofrommemory.md), or [**D3DX10GetImageInfoFromResource**](d3dx10getimageinfofromresource.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="19937-162">Commenti</span><span class="sxs-lookup"><span data-stu-id="19937-162">Remarks</span></span>

<span data-ttu-id="19937-163">Quando si inizializza la struttura, è possibile impostare qualsiasi membro su D3DX10 \_ default e D3DX lo inizializza con un valore predefinito dalla trama di origine quando viene caricata la trama.</span><span class="sxs-lookup"><span data-stu-id="19937-163">When initializing the structure, you may set any member to D3DX10\_DEFAULT and D3DX will initialize it with a default value from the source texture when the texture is loaded.</span></span>

<span data-ttu-id="19937-164">Questa struttura può essere usata dalle API che:</span><span class="sxs-lookup"><span data-stu-id="19937-164">This structure can be used by APIs that:</span></span>

-   <span data-ttu-id="19937-165">Creare risorse, ad esempio [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) e [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md).</span><span class="sxs-lookup"><span data-stu-id="19937-165">Create resources, such as [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) and [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md).</span></span>
-   <span data-ttu-id="19937-166">Creare processori di dati, ad esempio [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md) o [**D3DX10CreateAsyncShaderResourceViewProcessor**](d3dx10createasyncshaderresourceviewprocessor.md).</span><span class="sxs-lookup"><span data-stu-id="19937-166">Create data processors, such as [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md) or [**D3DX10CreateAsyncShaderResourceViewProcessor**](d3dx10createasyncshaderresourceviewprocessor.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="19937-167">Requisiti</span><span class="sxs-lookup"><span data-stu-id="19937-167">Requirements</span></span>



| <span data-ttu-id="19937-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="19937-168">Requirement</span></span> | <span data-ttu-id="19937-169">Valore</span><span class="sxs-lookup"><span data-stu-id="19937-169">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="19937-170">Intestazione</span><span class="sxs-lookup"><span data-stu-id="19937-170">Header</span></span><br/> | <dl> <span data-ttu-id="19937-171"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="19937-171"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19937-172">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="19937-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19937-173">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="19937-173">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
