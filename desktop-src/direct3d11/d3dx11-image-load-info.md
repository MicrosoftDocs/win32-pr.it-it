---
title: Struttura D3DX11_IMAGE_LOAD_INFO (D3DX11tex. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Fornire facoltativamente informazioni alle API del caricatore di trama per controllare la modalità di caricamento delle trame. | Struttura D3DX11_IMAGE_LOAD_INFO (D3DX11tex. h)
ms.assetid: 6cd2f590-4e15-41e6-9f04-cd91eeb082db
keywords:
- Struttura D3DX11_IMAGE_LOAD_INFO Direct3D 11
- Puntatore alla struttura LPD3DX11_IMAGE_LOAD_INFO Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_IMAGE_LOAD_INFO
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2905d135a515f4ef90557ac74c35665623462439
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982555"
---
# <a name="d3dx11_image_load_info-structure"></a><span data-ttu-id="d0157-107">\_Struttura delle \_ informazioni sul caricamento dell'immagine D3DX11 \_</span><span class="sxs-lookup"><span data-stu-id="d0157-107">D3DX11\_IMAGE\_LOAD\_INFO structure</span></span>

> [!Note]  
> <span data-ttu-id="d0157-108">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="d0157-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="d0157-109">Fornire facoltativamente informazioni alle API del caricatore di trama per controllare la modalità di caricamento delle trame.</span><span class="sxs-lookup"><span data-stu-id="d0157-109">Optionally provide information to texture loader APIs to control how textures get loaded.</span></span> <span data-ttu-id="d0157-110">Il valore predefinito D3DX11 \_ per uno di questi parametri provocherà l'uso automatico del valore del file di origine da parte di D3DX.</span><span class="sxs-lookup"><span data-stu-id="d0157-110">A value of D3DX11\_DEFAULT for any of these parameters will cause D3DX to automatically use the value from the source file.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0157-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d0157-111">Syntax</span></span>


```C++
typedef struct D3DX11_IMAGE_LOAD_INFO {
  UINT              Width;
  UINT              Height;
  UINT              Depth;
  UINT              FirstMipLevel;
  UINT              MipLevels;
  D3D11_USAGE       Usage;
  UINT              BindFlags;
  UINT              CpuAccessFlags;
  UINT              MiscFlags;
  DXGI_FORMAT       Format;
  UINT              Filter;
  UINT              MipFilter;
  D3DX11_IMAGE_INFO *pSrcInfo;
} D3DX11_IMAGE_LOAD_INFO, *LPD3DX11_IMAGE_LOAD_INFO;
```



## <a name="members"></a><span data-ttu-id="d0157-112">Members</span><span class="sxs-lookup"><span data-stu-id="d0157-112">Members</span></span>

<dl> <dt>

<span data-ttu-id="d0157-113">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="d0157-113">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="d0157-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d0157-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d0157-115">Larghezza di destinazione della trama.</span><span class="sxs-lookup"><span data-stu-id="d0157-115">The target width of the texture.</span></span> <span data-ttu-id="d0157-116">Se la larghezza effettiva della trama è maggiore o minore di questo valore, la trama verrà ridimensionata verso l'alto o verso il basso per adattarla a questa larghezza di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d0157-116">If the actual width of the texture is larger or smaller than this value then the texture will be scaled up or down to fit this target width.</span></span>

</dd> <dt>

<span data-ttu-id="d0157-117">**Altezza**</span><span class="sxs-lookup"><span data-stu-id="d0157-117">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="d0157-118">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d0157-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d0157-119">Altezza di destinazione della trama.</span><span class="sxs-lookup"><span data-stu-id="d0157-119">The target height of the texture.</span></span> <span data-ttu-id="d0157-120">Se l'altezza effettiva della trama è maggiore o minore di questo valore, la trama verrà ridimensionata verso l'alto o verso il basso per adattarla a questa altezza di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d0157-120">If the actual height of the texture is larger or smaller than this value then the texture will be scaled up or down to fit this target height.</span></span>

</dd> <dt>

<span data-ttu-id="d0157-121">**Livello nidificazione**</span><span class="sxs-lookup"><span data-stu-id="d0157-121">**Depth**</span></span>
</dt> <dd>

<span data-ttu-id="d0157-122">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d0157-122">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d0157-123">Profondità della trama.</span><span class="sxs-lookup"><span data-stu-id="d0157-123">The depth of the texture.</span></span> <span data-ttu-id="d0157-124">Questo vale solo per le trame del volume.</span><span class="sxs-lookup"><span data-stu-id="d0157-124">This only applies to volume textures.</span></span>

</dd> <dt>

<span data-ttu-id="d0157-125">**FirstMipLevel**</span><span class="sxs-lookup"><span data-stu-id="d0157-125">**FirstMipLevel**</span></span>
</dt> <dd>

<span data-ttu-id="d0157-126">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d0157-126">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d0157-127">Livello di mipmap di risoluzione più alto della trama.</span><span class="sxs-lookup"><span data-stu-id="d0157-127">The highest resolution mipmap level of the texture.</span></span> <span data-ttu-id="d0157-128">Se è maggiore di 0, dopo il caricamento della trama FirstMipLevel verrà eseguito il mapping a mipmap livello 0.</span><span class="sxs-lookup"><span data-stu-id="d0157-128">If this is greater than 0, then after the texture is loaded FirstMipLevel will be mapped to mipmap level 0.</span></span>

</dd> <dt>

<span data-ttu-id="d0157-129">**MipLevels**</span><span class="sxs-lookup"><span data-stu-id="d0157-129">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="d0157-130">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d0157-130">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d0157-131">Numero massimo di livelli di mipmap nella trama.</span><span class="sxs-lookup"><span data-stu-id="d0157-131">The maximum number of mipmap levels in the texture.</span></span> <span data-ttu-id="d0157-132">Vedere la sezione Osservazioni in [**d3d11 \_ TEX1D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv).</span><span class="sxs-lookup"><span data-stu-id="d0157-132">See the remarks in [**D3D11\_TEX1D\_SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv).</span></span> <span data-ttu-id="d0157-133">Se \_ si usa il valore predefinito 0 o D3DX11, verrà creata una catena mipmap completa.</span><span class="sxs-lookup"><span data-stu-id="d0157-133">Using 0 or D3DX11\_DEFAULT will cause a full mipmap chain to be created.</span></span>

</dd> <dt>

<span data-ttu-id="d0157-134">**Utilizzo**</span><span class="sxs-lookup"><span data-stu-id="d0157-134">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="d0157-135">Tipo: **[ **\_ utilizzo di d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)**</span><span class="sxs-lookup"><span data-stu-id="d0157-135">Type: **[**D3D11\_USAGE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)**</span></span>

</dd> <dd>

<span data-ttu-id="d0157-136">Il modo in cui la risorsa di trama deve essere utilizzata.</span><span class="sxs-lookup"><span data-stu-id="d0157-136">The way the texture resource is intended to be used.</span></span> <span data-ttu-id="d0157-137">Vedere [**\_ utilizzo di d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage).</span><span class="sxs-lookup"><span data-stu-id="d0157-137">See [**D3D11\_USAGE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage).</span></span>

</dd> <dt>

<span data-ttu-id="d0157-138">**BindFlags**</span><span class="sxs-lookup"><span data-stu-id="d0157-138">**BindFlags**</span></span>
</dt> <dd>

<span data-ttu-id="d0157-139">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d0157-139">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d0157-140">Fasi della pipeline a cui sarà consentita l'associazione della trama.</span><span class="sxs-lookup"><span data-stu-id="d0157-140">The pipeline stages that the texture will be allowed to bind to.</span></span> <span data-ttu-id="d0157-141">Vedere [**\_ \_ flag di binding d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag).</span><span class="sxs-lookup"><span data-stu-id="d0157-141">See [**D3D11\_BIND\_FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag).</span></span>

</dd> <dt>

<span data-ttu-id="d0157-142">**CpuAccessFlags**</span><span class="sxs-lookup"><span data-stu-id="d0157-142">**CpuAccessFlags**</span></span>
</dt> <dd>

<span data-ttu-id="d0157-143">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d0157-143">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d0157-144">Autorizzazioni di accesso che la CPU avrà per la risorsa di trama.</span><span class="sxs-lookup"><span data-stu-id="d0157-144">The access permissions the cpu will have for the texture resource.</span></span> <span data-ttu-id="d0157-145">Vedere [**\_ flag di \_ accesso \_ alla CPU d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag).</span><span class="sxs-lookup"><span data-stu-id="d0157-145">See [**D3D11\_CPU\_ACCESS\_FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag).</span></span>

</dd> <dt>

<span data-ttu-id="d0157-146">**MiscFlags**</span><span class="sxs-lookup"><span data-stu-id="d0157-146">**MiscFlags**</span></span>
</dt> <dd>

<span data-ttu-id="d0157-147">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d0157-147">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d0157-148">Proprietà delle risorse varie ( [**vedere \_ \_ \_ flag varie della risorsa d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)).</span><span class="sxs-lookup"><span data-stu-id="d0157-148">Miscellaneous resource properties (see [**D3D11\_RESOURCE\_MISC\_FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)).</span></span>

</dd> <dt>

<span data-ttu-id="d0157-149">**Formato**</span><span class="sxs-lookup"><span data-stu-id="d0157-149">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="d0157-150">Tipo: **[ **DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="d0157-150">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

</dd> <dd>

<span data-ttu-id="d0157-151">Enumerazione [**del \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) che indica il formato in cui si troverà la trama dopo il caricamento.</span><span class="sxs-lookup"><span data-stu-id="d0157-151">A [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) enumeration indicating the format the texture will be in after it is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="d0157-152">**Filter**</span><span class="sxs-lookup"><span data-stu-id="d0157-152">**Filter**</span></span>
</dt> <dd>

<span data-ttu-id="d0157-153">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d0157-153">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d0157-154">Filtrare la trama usando il filtro specificato (solo quando si esegue il ricampionamento).</span><span class="sxs-lookup"><span data-stu-id="d0157-154">Filter the texture using the specified filter (only when resampling).</span></span> <span data-ttu-id="d0157-155">Vedere [**\_ \_ flag di filtro D3DX11**](d3dx11-filter-flag.md).</span><span class="sxs-lookup"><span data-stu-id="d0157-155">See [**D3DX11\_FILTER\_FLAG**](d3dx11-filter-flag.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0157-156">**MipFilter**</span><span class="sxs-lookup"><span data-stu-id="d0157-156">**MipFilter**</span></span>
</dt> <dd>

<span data-ttu-id="d0157-157">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d0157-157">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d0157-158">Filtrare i livelli MIP della trama usando il filtro specificato (solo se si sta generando mipmap).</span><span class="sxs-lookup"><span data-stu-id="d0157-158">Filter the texture mip levels using the specified filter (only if generating mipmaps).</span></span> <span data-ttu-id="d0157-159">I valori validi sono D3DX11 \_ Filter \_ None, D3DX11 Filter \_ \_ Point, D3DX11 \_ Filter \_ Linear o D3DX11 \_ Filter \_ Triangle.</span><span class="sxs-lookup"><span data-stu-id="d0157-159">Valid values are D3DX11\_FILTER\_NONE, D3DX11\_FILTER\_POINT, D3DX11\_FILTER\_LINEAR, or D3DX11\_FILTER\_TRIANGLE.</span></span> <span data-ttu-id="d0157-160">Vedere [**\_ \_ flag di filtro D3DX11**](d3dx11-filter-flag.md).</span><span class="sxs-lookup"><span data-stu-id="d0157-160">See [**D3DX11\_FILTER\_FLAG**](d3dx11-filter-flag.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0157-161">**pSrcInfo**</span><span class="sxs-lookup"><span data-stu-id="d0157-161">**pSrcInfo**</span></span>
</dt> <dd>

<span data-ttu-id="d0157-162">Tipo: **[ **D3DX11 \_ Image \_ info**](d3dx11-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="d0157-162">Type: **[**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="d0157-163">Informazioni sull'immagine originale.</span><span class="sxs-lookup"><span data-stu-id="d0157-163">Information about the original image.</span></span> <span data-ttu-id="d0157-164">Vedere [**D3DX11 \_ Image \_ info**](d3dx11-image-info.md).</span><span class="sxs-lookup"><span data-stu-id="d0157-164">See [**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md).</span></span> <span data-ttu-id="d0157-165">Può essere ottenuto con [**D3DX11GetImageInfoFromFile**](d3dx11getimageinfofromfile.md), [**D3DX11GetImageInfoFromMemory**](d3dx11getimageinfofrommemory.md)o [**D3DX11GetImageInfoFromResource**](d3dx11getimageinfofromresource.md).</span><span class="sxs-lookup"><span data-stu-id="d0157-165">Can be obtained with [**D3DX11GetImageInfoFromFile**](d3dx11getimageinfofromfile.md), [**D3DX11GetImageInfoFromMemory**](d3dx11getimageinfofrommemory.md), or [**D3DX11GetImageInfoFromResource**](d3dx11getimageinfofromresource.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d0157-166">Commenti</span><span class="sxs-lookup"><span data-stu-id="d0157-166">Remarks</span></span>

<span data-ttu-id="d0157-167">Quando si inizializza la struttura, è possibile impostare qualsiasi membro su D3DX11 \_ default e D3DX lo inizializza con un valore predefinito dalla trama di origine quando viene caricata la trama.</span><span class="sxs-lookup"><span data-stu-id="d0157-167">When initializing the structure, you may set any member to D3DX11\_DEFAULT and D3DX will initialize it with a default value from the source texture when the texture is loaded.</span></span>

<span data-ttu-id="d0157-168">Questa struttura può essere usata dalle API che:</span><span class="sxs-lookup"><span data-stu-id="d0157-168">This structure can be used by APIs that:</span></span>

-   <span data-ttu-id="d0157-169">Creare risorse, ad esempio [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) e [**D3DX11CreateShaderResourceViewFromFile**](d3dx11createshaderresourceviewfromfile.md).</span><span class="sxs-lookup"><span data-stu-id="d0157-169">Create resources, such as [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) and [**D3DX11CreateShaderResourceViewFromFile**](d3dx11createshaderresourceviewfromfile.md).</span></span>
-   <span data-ttu-id="d0157-170">Creare processori di dati, ad esempio [**D3DX11CreateAsyncTextureInfoProcessor**](d3dx11createasynctextureinfoprocessor.md) o [**D3DX11CreateAsyncShaderResourceViewProcessor**](d3dx11createasyncshaderresourceviewprocessor.md).</span><span class="sxs-lookup"><span data-stu-id="d0157-170">Create data processors, such as [**D3DX11CreateAsyncTextureInfoProcessor**](d3dx11createasynctextureinfoprocessor.md) or [**D3DX11CreateAsyncShaderResourceViewProcessor**](d3dx11createasyncshaderresourceviewprocessor.md).</span></span>

<span data-ttu-id="d0157-171">I valori predefiniti sono:</span><span class="sxs-lookup"><span data-stu-id="d0157-171">The default values are:</span></span>


```
    Width = D3DX11_DEFAULT;
    Height = D3DX11_DEFAULT;
    Depth = D3DX11_DEFAULT;
    FirstMipLevel = D3DX11_DEFAULT;
    MipLevels = D3DX11_DEFAULT;
    Usage = (D3D11_USAGE) D3DX11_DEFAULT;
    BindFlags = D3DX11_DEFAULT;
    CpuAccessFlags = D3DX11_DEFAULT;
    MiscFlags = D3DX11_DEFAULT;
    Format = DXGI_FORMAT_FROM_FILE;
    Filter = D3DX11_DEFAULT;
    MipFilter = D3DX11_DEFAULT;
    pSrcInfo = NULL;
```



<span data-ttu-id="d0157-172">Ecco un breve esempio che usa questa struttura per fornire il formato pixel durante il caricamento di una trama.</span><span class="sxs-lookup"><span data-stu-id="d0157-172">Here is a brief example that uses this structure to supply the pixel format when loading a texture.</span></span> <span data-ttu-id="d0157-173">Per il codice completo, vedere l'esempio HDRFormats10. cpp in [HDRToneMappingCS11](https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="d0157-173">For the complete code, see HDRFormats10.cpp in [HDRToneMappingCS11 Sample](https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx).</span></span>


```
ID3D11ShaderResourceView* pCubeRV = NULL;
WCHAR strPath[MAX_PATH];
D3DX11_IMAGE_LOAD_INFO LoadInfo;

    DXUTFindDXSDKMediaFileCch( strPath, MAX_PATH, 
        L"Light Probes\\uffizi_cross.dds" );

    LoadInfo.Format = DXGI_FORMAT_R16G16B16A16_FLOAT;

    hr = D3DX11CreateShaderResourceViewFromFile( pd3dDevice, strPath, 
        &LoadInfo, NULL, &pCubeRV, NULL );
```



## <a name="requirements"></a><span data-ttu-id="d0157-174">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d0157-174">Requirements</span></span>



| <span data-ttu-id="d0157-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0157-175">Requirement</span></span> | <span data-ttu-id="d0157-176">Valore</span><span class="sxs-lookup"><span data-stu-id="d0157-176">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0157-177">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d0157-177">Header</span></span><br/> | <dl> <span data-ttu-id="d0157-178"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0157-178"><dt>D3DX11tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0157-179">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d0157-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0157-180">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="d0157-180">D3DX Structures</span></span>](d3d11-graphics-reference-d3dx11-structures.md)
</dt> </dl>

 

