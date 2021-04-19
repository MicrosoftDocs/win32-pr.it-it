---
description: Descrive i parametri usati per caricare una trama da un'altra trama.
ms.assetid: dee693ce-afa7-479b-a76a-00816e30d5cf
title: Struttura D3DX10_TEXTURE_LOAD_INFO (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_TEXTURE_LOAD_INFO
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: d3a689bb2104ee4cb419eb1483619d1fcf71d7e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322952"
---
# <a name="d3dx10_texture_load_info-structure"></a><span data-ttu-id="eb534-103">\_Struttura delle \_ informazioni di caricamento della trama d3dx10 \_</span><span class="sxs-lookup"><span data-stu-id="eb534-103">D3DX10\_TEXTURE\_LOAD\_INFO structure</span></span>

<span data-ttu-id="eb534-104">Descrive i parametri usati per caricare una trama da un'altra trama.</span><span class="sxs-lookup"><span data-stu-id="eb534-104">Describes parameters used to load a texture from another texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb534-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eb534-105">Syntax</span></span>


```C++
typedef struct _D3DX10_TEXTURE_LOAD_INFO {
  D3D10_BOX *pSrcBox;
  D3D10_BOX *pDstBox;
  UINT      SrcFirstMip;
  UINT      DstFirstMip;
  UINT      NumMips;
  UINT      SrcFirstElement;
  UINT      DstFirstElement;
  UINT      NumElements;
  UINT      Filter;
  UINT      MipFilter;
} D3DX10_TEXTURE_LOAD_INFO;
```



## <a name="members"></a><span data-ttu-id="eb534-106">Members</span><span class="sxs-lookup"><span data-stu-id="eb534-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="eb534-107">**pSrcBox**</span><span class="sxs-lookup"><span data-stu-id="eb534-107">**pSrcBox**</span></span>
</dt> <dd>

<span data-ttu-id="eb534-108">Tipo: **[ **D3D10 \_ Box**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)\***</span><span class="sxs-lookup"><span data-stu-id="eb534-108">Type: **[**D3D10\_BOX**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)\***</span></span>

</dd> <dd>

<span data-ttu-id="eb534-109">Casella trama di origine (vedere [**D3D10 \_ Box**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)).</span><span class="sxs-lookup"><span data-stu-id="eb534-109">Source texture box (see [**D3D10\_BOX**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)).</span></span>

</dd> <dt>

<span data-ttu-id="eb534-110">**pDstBox**</span><span class="sxs-lookup"><span data-stu-id="eb534-110">**pDstBox**</span></span>
</dt> <dd>

<span data-ttu-id="eb534-111">Tipo: **[ **D3D10 \_ Box**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)\***</span><span class="sxs-lookup"><span data-stu-id="eb534-111">Type: **[**D3D10\_BOX**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)\***</span></span>

</dd> <dd>

<span data-ttu-id="eb534-112">Casella trama di destinazione (vedere [**D3D10 \_ Box**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)).</span><span class="sxs-lookup"><span data-stu-id="eb534-112">Destination texture box (see [**D3D10\_BOX**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)).</span></span>

</dd> <dt>

<span data-ttu-id="eb534-113">**SrcFirstMip**</span><span class="sxs-lookup"><span data-stu-id="eb534-113">**SrcFirstMip**</span></span>
</dt> <dd>

<span data-ttu-id="eb534-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eb534-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="eb534-115">Livello di mipmap trama di origine. per altre informazioni, vedere [**D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource) .</span><span class="sxs-lookup"><span data-stu-id="eb534-115">Source texture mipmap level, see [**D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource) for more detail.</span></span>

</dd> <dt>

<span data-ttu-id="eb534-116">**DstFirstMip**</span><span class="sxs-lookup"><span data-stu-id="eb534-116">**DstFirstMip**</span></span>
</dt> <dd>

<span data-ttu-id="eb534-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eb534-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="eb534-118">Livello di mipmap della trama di destinazione. per altre informazioni, vedere [**D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource) .</span><span class="sxs-lookup"><span data-stu-id="eb534-118">Destination texture mipmap level, see [**D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource) for more detail.</span></span>

</dd> <dt>

<span data-ttu-id="eb534-119">**NumMips**</span><span class="sxs-lookup"><span data-stu-id="eb534-119">**NumMips**</span></span>
</dt> <dd>

<span data-ttu-id="eb534-120">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eb534-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="eb534-121">Numero di livelli di mipmap nella trama di origine.</span><span class="sxs-lookup"><span data-stu-id="eb534-121">Number of mipmap levels in the source texture.</span></span>

</dd> <dt>

<span data-ttu-id="eb534-122">**SrcFirstElement**</span><span class="sxs-lookup"><span data-stu-id="eb534-122">**SrcFirstElement**</span></span>
</dt> <dd>

<span data-ttu-id="eb534-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eb534-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="eb534-124">Primo elemento della trama di origine.</span><span class="sxs-lookup"><span data-stu-id="eb534-124">First element of the source texture.</span></span>

</dd> <dt>

<span data-ttu-id="eb534-125">**DstFirstElement**</span><span class="sxs-lookup"><span data-stu-id="eb534-125">**DstFirstElement**</span></span>
</dt> <dd>

<span data-ttu-id="eb534-126">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eb534-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="eb534-127">Primo elemento della trama di destinazione.</span><span class="sxs-lookup"><span data-stu-id="eb534-127">First element of the destination texture.</span></span>

</dd> <dt>

<span data-ttu-id="eb534-128">**NumElements**</span><span class="sxs-lookup"><span data-stu-id="eb534-128">**NumElements**</span></span>
</dt> <dd>

<span data-ttu-id="eb534-129">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eb534-129">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="eb534-130">Numero di elementi da caricare.</span><span class="sxs-lookup"><span data-stu-id="eb534-130">Number of elements to load.</span></span>

</dd> <dt>

<span data-ttu-id="eb534-131">**Filter**</span><span class="sxs-lookup"><span data-stu-id="eb534-131">**Filter**</span></span>
</dt> <dd>

<span data-ttu-id="eb534-132">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eb534-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="eb534-133">Opzioni di filtro durante il ricampionamento (vedere [**\_ \_ flag di filtro d3dx10**](d3dx10-filter-flag.md)).</span><span class="sxs-lookup"><span data-stu-id="eb534-133">Filtering options during resampling (see [**D3DX10\_FILTER\_FLAG**](d3dx10-filter-flag.md)).</span></span>

</dd> <dt>

<span data-ttu-id="eb534-134">**MipFilter**</span><span class="sxs-lookup"><span data-stu-id="eb534-134">**MipFilter**</span></span>
</dt> <dd>

<span data-ttu-id="eb534-135">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eb534-135">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="eb534-136">Opzioni di filtro durante la generazione di livelli MIP (vedere [**\_ \_ flag di filtro d3dx10**](d3dx10-filter-flag.md)).</span><span class="sxs-lookup"><span data-stu-id="eb534-136">Filtering options when generating mip levels (see [**D3DX10\_FILTER\_FLAG**](d3dx10-filter-flag.md)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eb534-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="eb534-137">Remarks</span></span>

<span data-ttu-id="eb534-138">Questa struttura viene utilizzata in una chiamata a [**D3DX10LoadTextureFromTexture**](d3dx10loadtexturefromtexture.md).</span><span class="sxs-lookup"><span data-stu-id="eb534-138">This structure is used in a call to [**D3DX10LoadTextureFromTexture**](d3dx10loadtexturefromtexture.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eb534-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eb534-139">Requirements</span></span>



| <span data-ttu-id="eb534-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb534-140">Requirement</span></span> | <span data-ttu-id="eb534-141">Valore</span><span class="sxs-lookup"><span data-stu-id="eb534-141">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb534-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eb534-142">Header</span></span><br/> | <dl> <span data-ttu-id="eb534-143"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb534-143"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb534-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eb534-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb534-145">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="eb534-145">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
