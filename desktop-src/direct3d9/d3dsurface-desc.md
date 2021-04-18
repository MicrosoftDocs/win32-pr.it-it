---
description: Descrive una superficie.
ms.assetid: fad8ffdb-36e5-4695-b343-e1315357c31a
title: Struttura D3DSURFACE_DESC (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSURFACE_DESC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 6424bbe9b78532657670bc5cd9ad0705de89a3b0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322438"
---
# <a name="d3dsurface_desc-structure"></a><span data-ttu-id="2359f-103">\_Struttura D3DSURFACE DESC</span><span class="sxs-lookup"><span data-stu-id="2359f-103">D3DSURFACE\_DESC structure</span></span>

<span data-ttu-id="2359f-104">Descrive una superficie.</span><span class="sxs-lookup"><span data-stu-id="2359f-104">Describes a surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="2359f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2359f-105">Syntax</span></span>


```C++
typedef struct D3DSURFACE_DESC {
  D3DFORMAT           Format;
  D3DRESOURCETYPE     Type;
  DWORD               Usage;
  D3DPOOL             Pool;
  D3DMULTISAMPLE_TYPE MultiSampleType;
  DWORD               MultiSampleQuality;
  UINT                Width;
  UINT                Height;
} D3DSURFACE_DESC, *LPD3DSURFACE_DESC;
```



## <a name="members"></a><span data-ttu-id="2359f-106">Members</span><span class="sxs-lookup"><span data-stu-id="2359f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2359f-107">**Formato**</span><span class="sxs-lookup"><span data-stu-id="2359f-107">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="2359f-108">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="2359f-108">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2359f-109">Membro del tipo enumerato [D3DFORMAT](d3dformat.md) , che descrive il formato della superficie.</span><span class="sxs-lookup"><span data-stu-id="2359f-109">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the surface format.</span></span>

</dd> <dt>

<span data-ttu-id="2359f-110">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2359f-110">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="2359f-111">Tipo: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**</span><span class="sxs-lookup"><span data-stu-id="2359f-111">Type: **[**D3DRESOURCETYPE**](./d3dresourcetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2359f-112">Membro del tipo enumerato [**D3DRESOURCETYPE**](./d3dresourcetype.md) , che identifica questa risorsa come superficie.</span><span class="sxs-lookup"><span data-stu-id="2359f-112">Member of the [**D3DRESOURCETYPE**](./d3dresourcetype.md) enumerated type, identifying this resource as a surface.</span></span>

</dd> <dt>

<span data-ttu-id="2359f-113">**Utilizzo**</span><span class="sxs-lookup"><span data-stu-id="2359f-113">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="2359f-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2359f-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2359f-115">\_Valori D3DUSAGE DEPTHSTENCIL o D3DUSAGE \_ RENDERTARGET.</span><span class="sxs-lookup"><span data-stu-id="2359f-115">Either the D3DUSAGE\_DEPTHSTENCIL or D3DUSAGE\_RENDERTARGET values.</span></span> <span data-ttu-id="2359f-116">Per ulteriori informazioni, vedere [**D3DUSAGE**](d3dusage.md).</span><span class="sxs-lookup"><span data-stu-id="2359f-116">For more information, see [**D3DUSAGE**](d3dusage.md).</span></span>

</dd> <dt>

<span data-ttu-id="2359f-117">**Pool**</span><span class="sxs-lookup"><span data-stu-id="2359f-117">**Pool**</span></span>
</dt> <dd>

<span data-ttu-id="2359f-118">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="2359f-118">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2359f-119">Membro del tipo enumerato [**D3DPOOL**](./d3dpool.md) , che specifica la classe di memoria allocata per questa superficie.</span><span class="sxs-lookup"><span data-stu-id="2359f-119">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, specifying the class of memory allocated for this surface.</span></span>

</dd> <dt>

<span data-ttu-id="2359f-120">**MultiSampleType**</span><span class="sxs-lookup"><span data-stu-id="2359f-120">**MultiSampleType**</span></span>
</dt> <dd>

<span data-ttu-id="2359f-121">Tipo: **[ **D3DMULTISAMPLE \_**](./d3dmultisample-type.md)**</span><span class="sxs-lookup"><span data-stu-id="2359f-121">Type: **[**D3DMULTISAMPLE\_TYPE**](./d3dmultisample-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2359f-122">Membro del tipo enumerato di [**\_ tipo D3DMULTISAMPLE**](./d3dmultisample-type.md) , che specifica i livelli di multicampionamento a scena completa supportati dalla superficie.</span><span class="sxs-lookup"><span data-stu-id="2359f-122">Member of the [**D3DMULTISAMPLE\_TYPE**](./d3dmultisample-type.md) enumerated type, specifying the levels of full-scene multisampling supported by the surface.</span></span>

</dd> <dt>

<span data-ttu-id="2359f-123">**MultiSampleQuality**</span><span class="sxs-lookup"><span data-stu-id="2359f-123">**MultiSampleQuality**</span></span>
</dt> <dd>

<span data-ttu-id="2359f-124">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2359f-124">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2359f-125">Livello di qualità.</span><span class="sxs-lookup"><span data-stu-id="2359f-125">Quality level.</span></span> <span data-ttu-id="2359f-126">L'intervallo valido è compreso tra zero e uno minore del livello restituito da pQualityLevels usato da [**CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype).</span><span class="sxs-lookup"><span data-stu-id="2359f-126">The valid range is between zero and one less than the level returned by pQualityLevels used by [**CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype).</span></span> <span data-ttu-id="2359f-127">Se si passa un valore maggiore, viene restituito l'errore D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="2359f-127">Passing a larger value returns the error, D3DERR\_INVALIDCALL.</span></span> <span data-ttu-id="2359f-128">I valori MultisampleQuality delle destinazioni di rendering associate, depth stencil superfici e il tipo multisample devono corrispondere.</span><span class="sxs-lookup"><span data-stu-id="2359f-128">The MultisampleQuality values of paired render targets, depth stencil surfaces and the MultiSample type must all match.</span></span>

</dd> <dt>

<span data-ttu-id="2359f-129">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="2359f-129">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="2359f-130">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2359f-130">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2359f-131">Larghezza, in pixel, della superficie.</span><span class="sxs-lookup"><span data-stu-id="2359f-131">Width of the surface, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="2359f-132">**Altezza**</span><span class="sxs-lookup"><span data-stu-id="2359f-132">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="2359f-133">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2359f-133">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2359f-134">Altezza, in pixel, della superficie.</span><span class="sxs-lookup"><span data-stu-id="2359f-134">Height of the surface, in pixels.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2359f-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2359f-135">Requirements</span></span>



| <span data-ttu-id="2359f-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="2359f-136">Requirement</span></span> | <span data-ttu-id="2359f-137">Valore</span><span class="sxs-lookup"><span data-stu-id="2359f-137">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2359f-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2359f-138">Header</span></span><br/> | <dl> <span data-ttu-id="2359f-139"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="2359f-139"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2359f-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2359f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2359f-141">Strutture Direct3D</span><span class="sxs-lookup"><span data-stu-id="2359f-141">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="2359f-142">**GetLevelDesc**</span><span class="sxs-lookup"><span data-stu-id="2359f-142">**GetLevelDesc**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getleveldesc)
</dt> <dt>

[<span data-ttu-id="2359f-143">**Getdesc**</span><span class="sxs-lookup"><span data-stu-id="2359f-143">**GetDesc**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getdesc)
</dt> <dt>

[<span data-ttu-id="2359f-144">**GetLevelDesc**</span><span class="sxs-lookup"><span data-stu-id="2359f-144">**GetLevelDesc**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getleveldesc)
</dt> </dl>

 

 
