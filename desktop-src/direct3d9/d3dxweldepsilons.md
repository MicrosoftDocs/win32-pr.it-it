---
description: Specifica i valori di tolleranza per ogni componente vertex quando si confrontano i vertici per determinare se sono abbastanza simili per essere saldati insieme.
ms.assetid: 534903da-ff65-4629-9be9-66c9daed6ef5
title: Struttura D3DXWELDEPSILONS (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXWELDEPSILONS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 6b6673e16b153f53baf17967b7f33c4bcb40d518
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322853"
---
# <a name="d3dxweldepsilons-structure"></a><span data-ttu-id="6efd2-103">Struttura D3DXWELDEPSILONS</span><span class="sxs-lookup"><span data-stu-id="6efd2-103">D3DXWELDEPSILONS structure</span></span>

<span data-ttu-id="6efd2-104">Specifica i valori di tolleranza per ogni componente vertex quando si confrontano i vertici per determinare se sono abbastanza simili per essere saldati insieme.</span><span class="sxs-lookup"><span data-stu-id="6efd2-104">Specifies tolerance values for each vertex component when comparing vertices to determine if they are similar enough to be welded together.</span></span>

## <a name="syntax"></a><span data-ttu-id="6efd2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6efd2-105">Syntax</span></span>


```C++
typedef struct _D3DXWELDEPSILONS {
  FLOAT Position;
  FLOAT BlendWeights;
  FLOAT Normal;
  FLOAT PSize;
  FLOAT Specular;
  FLOAT Diffuse;
  FLOAT Texcoord[8];
  FLOAT Tangent;
  FLOAT Binormal;
  FLOAT TessFactor;
} D3DXWELDEPSILONS, *LPD3DXWELDEPSILONS;
```



## <a name="members"></a><span data-ttu-id="6efd2-106">Members</span><span class="sxs-lookup"><span data-stu-id="6efd2-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="6efd2-107">**Position**</span><span class="sxs-lookup"><span data-stu-id="6efd2-107">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="6efd2-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6efd2-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6efd2-109">Posizione</span><span class="sxs-lookup"><span data-stu-id="6efd2-109">Position</span></span>

</dd> <dt>

<span data-ttu-id="6efd2-110">**BlendWeights**</span><span class="sxs-lookup"><span data-stu-id="6efd2-110">**BlendWeights**</span></span>
</dt> <dd>

<span data-ttu-id="6efd2-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6efd2-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6efd2-112">Spessore di Blend</span><span class="sxs-lookup"><span data-stu-id="6efd2-112">Blend weight</span></span>

</dd> <dt>

<span data-ttu-id="6efd2-113">**Normal**</span><span class="sxs-lookup"><span data-stu-id="6efd2-113">**Normal**</span></span>
</dt> <dd>

<span data-ttu-id="6efd2-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6efd2-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6efd2-115">Normale</span><span class="sxs-lookup"><span data-stu-id="6efd2-115">Normal</span></span>

</dd> <dt>

<span data-ttu-id="6efd2-116">**PSize**</span><span class="sxs-lookup"><span data-stu-id="6efd2-116">**PSize**</span></span>
</dt> <dd>

<span data-ttu-id="6efd2-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6efd2-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6efd2-118">Valore dimensioni punto</span><span class="sxs-lookup"><span data-stu-id="6efd2-118">Point size value</span></span>

</dd> <dt>

<span data-ttu-id="6efd2-119">**Speculare**</span><span class="sxs-lookup"><span data-stu-id="6efd2-119">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="6efd2-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6efd2-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6efd2-121">Valore di illuminazione speculare</span><span class="sxs-lookup"><span data-stu-id="6efd2-121">Specular lighting value</span></span>

</dd> <dt>

<span data-ttu-id="6efd2-122">**Diffusa**</span><span class="sxs-lookup"><span data-stu-id="6efd2-122">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="6efd2-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6efd2-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6efd2-124">Valore di illuminazione diffusa</span><span class="sxs-lookup"><span data-stu-id="6efd2-124">Diffuse lighting value</span></span>

</dd> <dt>

<span data-ttu-id="6efd2-125">**Texcoord**</span><span class="sxs-lookup"><span data-stu-id="6efd2-125">**Texcoord**</span></span>
</dt> <dd>

<span data-ttu-id="6efd2-126">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6efd2-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6efd2-127">Otto coordinate di trama</span><span class="sxs-lookup"><span data-stu-id="6efd2-127">Eight texture coordinates</span></span>

</dd> <dt>

<span data-ttu-id="6efd2-128">**Tangente**</span><span class="sxs-lookup"><span data-stu-id="6efd2-128">**Tangent**</span></span>
</dt> <dd>

<span data-ttu-id="6efd2-129">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6efd2-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6efd2-130">Tangente</span><span class="sxs-lookup"><span data-stu-id="6efd2-130">Tangent</span></span>

</dd> <dt>

<span data-ttu-id="6efd2-131">**Binormale**</span><span class="sxs-lookup"><span data-stu-id="6efd2-131">**Binormal**</span></span>
</dt> <dd>

<span data-ttu-id="6efd2-132">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6efd2-132">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6efd2-133">Binormale</span><span class="sxs-lookup"><span data-stu-id="6efd2-133">Binormal</span></span>

</dd> <dt>

<span data-ttu-id="6efd2-134">**TessFactor**</span><span class="sxs-lookup"><span data-stu-id="6efd2-134">**TessFactor**</span></span>
</dt> <dd>

<span data-ttu-id="6efd2-135">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6efd2-135">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6efd2-136">Fattore a mosaico</span><span class="sxs-lookup"><span data-stu-id="6efd2-136">Tessellation factor</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6efd2-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="6efd2-137">Remarks</span></span>

<span data-ttu-id="6efd2-138">Il tipo LPD3DXWELDEPSILONS è definito come un puntatore alla struttura **D3DXWELDEPSILONS** .</span><span class="sxs-lookup"><span data-stu-id="6efd2-138">The LPD3DXWELDEPSILONS type is defined as a pointer to the **D3DXWELDEPSILONS** structure.</span></span>


```
typedef D3DXWELDEPSILONS *LPD3DXWELDEPSILONS;
```



## <a name="requirements"></a><span data-ttu-id="6efd2-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6efd2-139">Requirements</span></span>



| <span data-ttu-id="6efd2-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="6efd2-140">Requirement</span></span> | <span data-ttu-id="6efd2-141">Valore</span><span class="sxs-lookup"><span data-stu-id="6efd2-141">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6efd2-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6efd2-142">Header</span></span><br/> | <dl> <span data-ttu-id="6efd2-143"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="6efd2-143"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6efd2-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6efd2-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6efd2-145">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="6efd2-145">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="6efd2-146">**D3DXWeldVertices**</span><span class="sxs-lookup"><span data-stu-id="6efd2-146">**D3DXWeldVertices**</span></span>](d3dxweldvertices.md)
</dt> </dl>

 

 
