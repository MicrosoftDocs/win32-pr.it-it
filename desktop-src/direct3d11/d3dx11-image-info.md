---
title: Struttura D3DX11_IMAGE_INFO (D3DX11tex. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Fornire facoltativamente informazioni alle API del caricatore di trama per controllare la modalità di caricamento delle trame. | Struttura D3DX11_IMAGE_INFO (D3DX11tex. h)
ms.assetid: 981f4f1d-7609-416a-8f92-c7223d8b2773
keywords:
- Struttura D3DX11_IMAGE_INFO Direct3D 11
- Puntatore alla struttura LPD3DX11_IMAGE_INFO Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_IMAGE_INFO
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 927967f8e76d0147ccc264bcbdd773191a170ae7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982558"
---
# <a name="d3dx11_image_info-structure"></a><span data-ttu-id="4273c-107">Struttura delle informazioni sull' \_ immagine D3DX11 \_</span><span class="sxs-lookup"><span data-stu-id="4273c-107">D3DX11\_IMAGE\_INFO structure</span></span>

> [!Note]  
> <span data-ttu-id="4273c-108">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="4273c-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="4273c-109">Fornire facoltativamente informazioni alle API del caricatore di trama per controllare la modalità di caricamento delle trame.</span><span class="sxs-lookup"><span data-stu-id="4273c-109">Optionally provide information to texture loader APIs to control how textures get loaded.</span></span> <span data-ttu-id="4273c-110">Il valore predefinito D3DX11 \_ per uno di questi parametri provocherà l'uso automatico del valore del file di origine da parte di D3DX.</span><span class="sxs-lookup"><span data-stu-id="4273c-110">A value of D3DX11\_DEFAULT for any of these parameters will cause D3DX to automatically use the value from the source file.</span></span>

## <a name="syntax"></a><span data-ttu-id="4273c-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4273c-111">Syntax</span></span>


```C++
typedef struct D3DX11_IMAGE_INFO {
  UINT                     Width;
  UINT                     Height;
  UINT                     Depth;
  UINT                     ArraySize;
  UINT                     MipLevels;
  UINT                     MiscFlags;
  DXGI_FORMAT              Format;
  D3D11_RESOURCE_DIMENSION ResourceDimension;
  D3DX11_IMAGE_FILE_FORMAT ImageFileFormat;
} D3DX11_IMAGE_INFO, *LPD3DX11_IMAGE_INFO;
```



## <a name="members"></a><span data-ttu-id="4273c-112">Members</span><span class="sxs-lookup"><span data-stu-id="4273c-112">Members</span></span>

<dl> <dt>

<span data-ttu-id="4273c-113">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="4273c-113">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="4273c-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4273c-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4273c-115">Larghezza di destinazione della trama.</span><span class="sxs-lookup"><span data-stu-id="4273c-115">The target width of the texture.</span></span> <span data-ttu-id="4273c-116">Se la larghezza effettiva della trama è maggiore o minore di questo valore, la trama verrà ridimensionata verso l'alto o verso il basso per adattarla a questa larghezza di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4273c-116">If the actual width of the texture is larger or smaller than this value then the texture will be scaled up or down to fit this target width.</span></span>

</dd> <dt>

<span data-ttu-id="4273c-117">**Altezza**</span><span class="sxs-lookup"><span data-stu-id="4273c-117">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="4273c-118">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4273c-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4273c-119">Altezza di destinazione della trama.</span><span class="sxs-lookup"><span data-stu-id="4273c-119">The target height of the texture.</span></span> <span data-ttu-id="4273c-120">Se l'altezza effettiva della trama è maggiore o minore di questo valore, la trama verrà ridimensionata verso l'alto o verso il basso per adattarla a questa altezza di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4273c-120">If the actual height of the texture is larger or smaller than this value then the texture will be scaled up or down to fit this target height.</span></span>

</dd> <dt>

<span data-ttu-id="4273c-121">**Livello nidificazione**</span><span class="sxs-lookup"><span data-stu-id="4273c-121">**Depth**</span></span>
</dt> <dd>

<span data-ttu-id="4273c-122">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4273c-122">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4273c-123">Profondità della trama.</span><span class="sxs-lookup"><span data-stu-id="4273c-123">The depth of the texture.</span></span> <span data-ttu-id="4273c-124">Questo vale solo per le trame del volume.</span><span class="sxs-lookup"><span data-stu-id="4273c-124">This only applies to volume textures.</span></span>

</dd> <dt>

<span data-ttu-id="4273c-125">**ArraySize**</span><span class="sxs-lookup"><span data-stu-id="4273c-125">**ArraySize**</span></span>
</dt> <dd>

<span data-ttu-id="4273c-126">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4273c-126">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4273c-127">Numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="4273c-127">The number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="4273c-128">**MipLevels**</span><span class="sxs-lookup"><span data-stu-id="4273c-128">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="4273c-129">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4273c-129">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4273c-130">Numero massimo di livelli di mipmap nella trama.</span><span class="sxs-lookup"><span data-stu-id="4273c-130">The maximum number of mipmap levels in the texture.</span></span> <span data-ttu-id="4273c-131">Vedere la sezione Osservazioni in [**d3d11 \_ TEX1D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv).</span><span class="sxs-lookup"><span data-stu-id="4273c-131">See the remarks in [**D3D11\_TEX1D\_SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv).</span></span> <span data-ttu-id="4273c-132">Se \_ si usa il valore predefinito 0 o D3DX11, verrà creata una catena mipmap completa.</span><span class="sxs-lookup"><span data-stu-id="4273c-132">Using 0 or D3DX11\_DEFAULT will cause a full mipmap chain to be created.</span></span>

</dd> <dt>

<span data-ttu-id="4273c-133">**MiscFlags**</span><span class="sxs-lookup"><span data-stu-id="4273c-133">**MiscFlags**</span></span>
</dt> <dd>

<span data-ttu-id="4273c-134">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4273c-134">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4273c-135">Proprietà delle risorse varie specificate con un flag di [**\_ \_ \_ flag varie della risorsa d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) .</span><span class="sxs-lookup"><span data-stu-id="4273c-135">Miscellaneous resource properties specified with a [**D3D11\_RESOURCE\_MISC\_FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) flag.</span></span>

</dd> <dt>

<span data-ttu-id="4273c-136">**Formato**</span><span class="sxs-lookup"><span data-stu-id="4273c-136">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="4273c-137">Tipo: **[ **DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="4273c-137">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

</dd> <dd>

<span data-ttu-id="4273c-138">Enumerazione [**del \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) che specifica il formato in cui si troverà la trama dopo il caricamento.</span><span class="sxs-lookup"><span data-stu-id="4273c-138">A [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) enumeration specifying the format the texture will be in after it is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="4273c-139">**ResourceDimension**</span><span class="sxs-lookup"><span data-stu-id="4273c-139">**ResourceDimension**</span></span>
</dt> <dd>

<span data-ttu-id="4273c-140">Tipo: **[ **\_ \_ dimensione della risorsa d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension)**</span><span class="sxs-lookup"><span data-stu-id="4273c-140">Type: **[**D3D11\_RESOURCE\_DIMENSION**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension)**</span></span>

</dd> <dd>

<span data-ttu-id="4273c-141">Valore [**della \_ \_ dimensione della risorsa d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension) , che identifica il tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="4273c-141">A [**D3D11\_RESOURCE\_DIMENSION**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension) value, which identifies the type of resource.</span></span>

</dd> <dt>

<span data-ttu-id="4273c-142">**ImageFileFormat**</span><span class="sxs-lookup"><span data-stu-id="4273c-142">**ImageFileFormat**</span></span>
</dt> <dd>

<span data-ttu-id="4273c-143">Tipo: **[ **D3DX11 \_ Image \_ file \_ Format**](d3dx11-image-file-format.md)**</span><span class="sxs-lookup"><span data-stu-id="4273c-143">Type: **[**D3DX11\_IMAGE\_FILE\_FORMAT**](d3dx11-image-file-format.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4273c-144">Valore [**del \_ \_ \_ formato di file di immagine D3DX11**](d3dx11-image-file-format.md) , che identifica il formato dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="4273c-144">A [**D3DX11\_IMAGE\_FILE\_FORMAT**](d3dx11-image-file-format.md) value, which identifies the image format.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4273c-145">Commenti</span><span class="sxs-lookup"><span data-stu-id="4273c-145">Remarks</span></span>

<span data-ttu-id="4273c-146">Questa struttura viene utilizzata da metodi quali: [**D3DX11GetImageInfoFromFile**](d3dx11getimageinfofromfile.md), [**D3DX11GetImageInfoFromMemory**](d3dx11getimageinfofrommemory.md)o [**D3DX11GetImageInfoFromResource**](d3dx11getimageinfofromresource.md).</span><span class="sxs-lookup"><span data-stu-id="4273c-146">This structure is used by methods such as: [**D3DX11GetImageInfoFromFile**](d3dx11getimageinfofromfile.md), [**D3DX11GetImageInfoFromMemory**](d3dx11getimageinfofrommemory.md), or [**D3DX11GetImageInfoFromResource**](d3dx11getimageinfofromresource.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4273c-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4273c-147">Requirements</span></span>



| <span data-ttu-id="4273c-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="4273c-148">Requirement</span></span> | <span data-ttu-id="4273c-149">Valore</span><span class="sxs-lookup"><span data-stu-id="4273c-149">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4273c-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4273c-150">Header</span></span><br/> | <dl> <span data-ttu-id="4273c-151"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="4273c-151"><dt>D3DX11tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4273c-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4273c-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4273c-153">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="4273c-153">D3DX Structures</span></span>](d3d11-graphics-reference-d3dx11-structures.md)
</dt> </dl>

 

