---
title: Struttura D3DX11_TEXTURE_LOAD_INFO (D3DX11tex. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Descrive i parametri usati per caricare una trama da un'altra trama.
ms.assetid: 2fe24752-d1bc-4666-bf0f-cc397394da56
keywords:
- Struttura D3DX11_TEXTURE_LOAD_INFO Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_TEXTURE_LOAD_INFO
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ca893908f854b6b127d783af25cc2fb9bc5df6a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996059"
---
# <a name="d3dx11_texture_load_info-structure"></a><span data-ttu-id="8a166-105">\_Struttura delle \_ informazioni di caricamento della trama D3DX11 \_</span><span class="sxs-lookup"><span data-stu-id="8a166-105">D3DX11\_TEXTURE\_LOAD\_INFO structure</span></span>

> [!Note]  
> <span data-ttu-id="8a166-106">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="8a166-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="8a166-107">Descrive i parametri usati per caricare una trama da un'altra trama.</span><span class="sxs-lookup"><span data-stu-id="8a166-107">Describes parameters used to load a texture from another texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a166-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8a166-108">Syntax</span></span>


```C++
typedef struct _D3DX11_TEXTURE_LOAD_INFO {
  D3D11_BOX *pSrcBox;
  D3D11_BOX *pDstBox;
  UINT      SrcFirstMip;
  UINT      DstFirstMip;
  UINT      NumMips;
  UINT      SrcFirstElement;
  UINT      DstFirstElement;
  UINT      NumElements;
  UINT      Filter;
  UINT      MipFilter;
} D3DX11_TEXTURE_LOAD_INFO;
```



## <a name="members"></a><span data-ttu-id="8a166-109">Members</span><span class="sxs-lookup"><span data-stu-id="8a166-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="8a166-110">**pSrcBox**</span><span class="sxs-lookup"><span data-stu-id="8a166-110">**pSrcBox**</span></span>
</dt> <dd>

<span data-ttu-id="8a166-111">Tipo: **[ **d3d11 \_ Box**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)\***</span><span class="sxs-lookup"><span data-stu-id="8a166-111">Type: **[**D3D11\_BOX**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)\***</span></span>

</dd> <dd>

<span data-ttu-id="8a166-112">Casella trama di origine (vedere [**d3d11 \_ Box**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)).</span><span class="sxs-lookup"><span data-stu-id="8a166-112">Source texture box (see [**D3D11\_BOX**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)).</span></span>

</dd> <dt>

<span data-ttu-id="8a166-113">**pDstBox**</span><span class="sxs-lookup"><span data-stu-id="8a166-113">**pDstBox**</span></span>
</dt> <dd>

<span data-ttu-id="8a166-114">Tipo: **[ **d3d11 \_ Box**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)\***</span><span class="sxs-lookup"><span data-stu-id="8a166-114">Type: **[**D3D11\_BOX**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)\***</span></span>

</dd> <dd>

<span data-ttu-id="8a166-115">Casella trama di destinazione (vedere [**d3d11 \_ Box**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)).</span><span class="sxs-lookup"><span data-stu-id="8a166-115">Destination texture box (see [**D3D11\_BOX**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)).</span></span>

</dd> <dt>

<span data-ttu-id="8a166-116">**SrcFirstMip**</span><span class="sxs-lookup"><span data-stu-id="8a166-116">**SrcFirstMip**</span></span>
</dt> <dd>

<span data-ttu-id="8a166-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8a166-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="8a166-118">Livello di mipmap trama di origine. per altre informazioni, vedere [**D3D11CalcSubresource**](/windows/desktop/api/D3D11/nf-d3d11-d3d11calcsubresource) .</span><span class="sxs-lookup"><span data-stu-id="8a166-118">Source texture mipmap level, see [**D3D11CalcSubresource**](/windows/desktop/api/D3D11/nf-d3d11-d3d11calcsubresource) for more detail.</span></span>

</dd> <dt>

<span data-ttu-id="8a166-119">**DstFirstMip**</span><span class="sxs-lookup"><span data-stu-id="8a166-119">**DstFirstMip**</span></span>
</dt> <dd>

<span data-ttu-id="8a166-120">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8a166-120">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="8a166-121">Livello di mipmap della trama di destinazione. per altre informazioni, vedere [**D3D11CalcSubresource**](/windows/desktop/api/D3D11/nf-d3d11-d3d11calcsubresource) .</span><span class="sxs-lookup"><span data-stu-id="8a166-121">Destination texture mipmap level, see [**D3D11CalcSubresource**](/windows/desktop/api/D3D11/nf-d3d11-d3d11calcsubresource) for more detail.</span></span>

</dd> <dt>

<span data-ttu-id="8a166-122">**NumMips**</span><span class="sxs-lookup"><span data-stu-id="8a166-122">**NumMips**</span></span>
</dt> <dd>

<span data-ttu-id="8a166-123">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8a166-123">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="8a166-124">Numero di livelli di mipmap nella trama di origine.</span><span class="sxs-lookup"><span data-stu-id="8a166-124">Number of mipmap levels in the source texture.</span></span>

</dd> <dt>

<span data-ttu-id="8a166-125">**SrcFirstElement**</span><span class="sxs-lookup"><span data-stu-id="8a166-125">**SrcFirstElement**</span></span>
</dt> <dd>

<span data-ttu-id="8a166-126">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8a166-126">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="8a166-127">Primo elemento della trama di origine.</span><span class="sxs-lookup"><span data-stu-id="8a166-127">First element of the source texture.</span></span>

</dd> <dt>

<span data-ttu-id="8a166-128">**DstFirstElement**</span><span class="sxs-lookup"><span data-stu-id="8a166-128">**DstFirstElement**</span></span>
</dt> <dd>

<span data-ttu-id="8a166-129">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8a166-129">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="8a166-130">Primo elemento della trama di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8a166-130">First element of the destination texture.</span></span>

</dd> <dt>

<span data-ttu-id="8a166-131">**NumElements**</span><span class="sxs-lookup"><span data-stu-id="8a166-131">**NumElements**</span></span>
</dt> <dd>

<span data-ttu-id="8a166-132">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8a166-132">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="8a166-133">Numero di elementi da caricare.</span><span class="sxs-lookup"><span data-stu-id="8a166-133">Number of elements to load.</span></span>

</dd> <dt>

<span data-ttu-id="8a166-134">**Filter**</span><span class="sxs-lookup"><span data-stu-id="8a166-134">**Filter**</span></span>
</dt> <dd>

<span data-ttu-id="8a166-135">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8a166-135">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="8a166-136">Opzioni di filtro durante il ricampionamento (vedere [**\_ \_ flag di filtro D3DX11**](d3dx11-filter-flag.md)).</span><span class="sxs-lookup"><span data-stu-id="8a166-136">Filtering options during resampling (see [**D3DX11\_FILTER\_FLAG**](d3dx11-filter-flag.md)).</span></span>

</dd> <dt>

<span data-ttu-id="8a166-137">**MipFilter**</span><span class="sxs-lookup"><span data-stu-id="8a166-137">**MipFilter**</span></span>
</dt> <dd>

<span data-ttu-id="8a166-138">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8a166-138">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="8a166-139">Opzioni di filtro durante la generazione di livelli MIP (vedere [**\_ \_ flag di filtro D3DX11**](d3dx11-filter-flag.md)).</span><span class="sxs-lookup"><span data-stu-id="8a166-139">Filtering options when generating mip levels (see [**D3DX11\_FILTER\_FLAG**](d3dx11-filter-flag.md)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8a166-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="8a166-140">Remarks</span></span>

<span data-ttu-id="8a166-141">Questa struttura viene utilizzata in una chiamata a [**D3DX11LoadTextureFromTexture**](d3dx11loadtexturefromtexture.md).</span><span class="sxs-lookup"><span data-stu-id="8a166-141">This structure is used in a call to [**D3DX11LoadTextureFromTexture**](d3dx11loadtexturefromtexture.md).</span></span>

<span data-ttu-id="8a166-142">I valori predefiniti sono:</span><span class="sxs-lookup"><span data-stu-id="8a166-142">The default values are:</span></span>


```
    pSrcBox = NULL;
    pDstBox = NULL;
    SrcFirstMip = 0;
    DstFirstMip = 0;
    NumMips = D3DX11_DEFAULT;
    SrcFirstElement = 0;
    DstFirstElement = 0;
    NumElements = D3DX11_DEFAULT;
    Filter = D3DX11_DEFAULT;
    MipFilter = D3DX11_DEFAULT;
```



## <a name="requirements"></a><span data-ttu-id="8a166-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8a166-143">Requirements</span></span>



| <span data-ttu-id="8a166-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a166-144">Requirement</span></span> | <span data-ttu-id="8a166-145">Valore</span><span class="sxs-lookup"><span data-stu-id="8a166-145">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a166-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8a166-146">Header</span></span><br/> | <dl> <span data-ttu-id="8a166-147"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a166-147"><dt>D3DX11tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a166-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8a166-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a166-149">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="8a166-149">D3DX Structures</span></span>](d3d11-graphics-reference-d3dx11-structures.md)
</dt> </dl>

 

